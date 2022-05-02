# Creating custom Unit Metrics

[unit-metrics](../fundamentals/unit-metrics/ "mention") is the major feature of Cloudthread aimed at helping you to figure out how much value you are getting from your cloud. It is fully available once the full data setup is done, which can take up to **48 hours** from the AWS account connection.

## What do I need it for?

{% hint style="info" %}
Creating custom [unit-metric.md](../fundamentals/unit-metrics/unit-metric.md "mention") can help you to:

* Find out answers to the questions like "?"
* See the **trends** for your absolute cloud spend
* See the breakdown of your costs by various dimensions to understand top spending categories
* [drill-down.md](../fundamentals/drill-down.md "mention") from the Cost View into cloud spend to identify root cause of the spike in costs you see
  * Check out [performing-root-cause-analysis.md](performing-root-cause-analysis.md "mention") guide to learn more
* Set up reports and alerts for the Cost View, so that you can be notified on important changes in your cloud spend
  * Check out [setting-up-alerts-and-reports.md](setting-up-alerts-and-reports.md "mention") guide to learn more
{% endhint %}

## Detailed instructions

1. Choose Costs Transparency section in the menu to the right, then choose Cost Overview item
   * You will see a page with Total Cost View – a default Cost View representing all the spend from added accounts, will no filters applied
2. Adjust Date filter at the top-right of the window as needed
   * By default the dates are shown for the last 7 days
3. Open Filter pane at the top-right of the window and add necessary filters
   * This is where you introduce all necessary conditions for absolute cloud spend filtering
   * The filter allows for 4 dimensions: Account, Region, Service and Tag
   * You can add filter conditions in buckets, where each bucket represents AND condition for lines of different dimensions inside, and separate buckets are connected by OR condition
   * Click "Apply" button to apply the filters
4. Check the charts if they represent the data you were looking for
   * Top chart shows total filtered spend for chosen period and the period of same size right before
   * Bottom chart is a "breakdown", it shows same spend by one of the four dimensions: Account, Region, Service and Operation
5. Click "Save as New" at top pane right near the default Cost View name
6. Put a descriptive name and click save
7. See your saved Cost View in the Library

