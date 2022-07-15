# Creating custom Unit Metrics

[unit-metrics](../fundamentals/unit-metrics/ "mention") is the major feature of Cloudthread aimed at helping you to figure out how much value you are getting from your cloud. It is fully available once the full data setup is done, which can take up to **48 hours** from the AWS account connection.

## What do I need it for?

{% hint style="info" %}
Creating custom [unit-metric.md](../fundamentals/unit-metrics/unit-metric.md "mention") can help you to:

* Find out answers to the questions like "How much does my **team** really pays AWS for **every** Lambda **invocation** in **us-east-1** region?"
* See the **trends** for your unit metric
* Set up reports and alerts for the Unit Metric, so that you can be notified on important changes in your cloud cost efficiency
  * Check out [setting-up-alerts-and-reports.md](setting-up-alerts-and-reports.md "mention") guide to learn more
{% endhint %}

## Detailed instructions

1. Choose [unit-metrics-library.md](../fundamentals/unit-metrics/unit-metrics-library.md "mention") menu item under [unit-metrics](../fundamentals/unit-metrics/ "mention") section in the menu to the left
   * You will see a table with a list of predefined unit metrics ("base",created by Cloudthread out of the box) as well as custom ones (created by your team)
2.  Click "Create New Metric" button at the top-right corner of the screen, you will see the form to create a basis for your future custom unit metric

    ![](<../.gitbook/assets/creating-custom-unit-metrics-1-new-metric-form (1).png>)****
3. Choose **base metric** from the list – this is the the source of denominator for the Unit Metric
4. Set up **custom dimensions** – filters for the metric numerator (cost): account, region and tag&#x20;
5. Choose **numerator cost** type
   * **Service** – **** numerator will include only the cost of the service numerator as part of the unit metric. This is valuable when you want to isolate that specific service's cost efficiency (e.g. lambda $ / lambda invocation)numerator to the service relevant to the denominator specified in the base metric (e.g. lambda $ / lambda invocation)
   * **Total** – numerator include all costs associated with filters you've selected, not just the cost of the service. This is valuable when you want to use the unit metric as a proxy for the team's overall efficiency (e.g. tag-teamX $ / ELB request)
6. Input the unit metric name
7. Click "Save Metric"
8. See your saved Unit Metric in the Library
   * You will be able to edit the metric further with the filter functionality in [unit-metrics-lab.md](../fundamentals/unit-metrics/unit-metrics-lab.md "mention")&#x20;

![Creating a custom Unit Metric](../.gitbook/assets/creating-custom-unit-metrics-1-demo.gif)
