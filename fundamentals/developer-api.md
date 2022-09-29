# Developer API

Cloudthread provides a powerful and flexible REST Developer API to help get the most out of your data.

Below describes how to use the API, and what features are currently available.

## Basic setup

Cloudthread's Developer API lives at: `api.cloudthread.io`

Cloudthread requires an API Token to process incoming developer API requests. Admin's have the ability to generate API Tokens on the Cloudthread platform within the **Settings* tab.

This API Token will need to be included as part of a header to all Developer API requests as follows:

`x-api-key: {API_TOKEN}`

## Data Ingestion

Cloudthread requires a Data Stream Token in order to send data to our systems -- this applies to all ingestion endpoints. This token helps organize and control the flow of data. This token will be included in the body of incoming ingestion requests.

Admin's have the ability to generate a Data Stream Token on the Cloudthread platform within the **Settings* tab.

Endpoint: `api.cloudthread.io/streams/ingest`

## Custom Data Ingestion

Cloudthread can process custom data to help customers understand their non-cost data as it relates to their cost data.

To send custom data to Cloudthread, use the **Data Ingeation** endpoint with the following payload:

{
  data_stream_token: {DATA_STREAM_TOKEN},
  metric_agg_func: 'Sum' | 'Average' | 'Maximum' | 'Minimum',
  data: [
    {
      timestamp: datetime,
      metric_name: string,
      metric_value: float,
      custom_dimensions: {
        string: string,
        ...
      },
      ...
    }
  ]
}

`metric_agg_func`: aggregation function across the dataset. *Do not* include data with different aggregation methods into the same request.
`timestamp`: datetime with **hourly* granularity -- any timestamp with minutes, seconds, etc. will be rejected -- e.g. `'2022-10-01 00:00:00'`. To send daily data, send data with the timepart = `00:00:00`.
`metric_name`: name of the metric -- all metrics that share a name and aggregation function will be grouped together by date given the prescribed aggregation function.
`mertic_value`: float convertiable value of the metric.
`custom_dimensions` is an array of **up to 10** key value pairs that you will be able to segment the data by on the Cloudthread platform.

Cloudthread creates a record ID for each data point by hashing the metric name, metric aggreation function, and the custom dimensions into a single key. To update a data point that's already been sent, the incoming data point must match along these fields -- otherwise a new data point will be generated. You can then update a given timestamp and metric value pair by sending in the matching timestamp with a new value.

Data sent via this API will appear in the **Unit Metrics Lab** on Cloudthread's platform.

## Event Overlay Ingestion

COMING SOON! Contact support@cloudthread.io if you wish to see this feature faster.
