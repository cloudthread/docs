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

1. Choose Unit Metrics section in the menu to the right, then choose Unit Metrics Overview item
   * You will see a page with charts for a default metric prebuilt for you by Cloudthread
2. Adjust Date filter at the top-right of the window as needed
   * By default the dates are shown for the last 7 days
3. Click "Create New Metric" button at the top-right of the window and add necessary filters for Numerator (cost) and Denominator (CloudWatch units) in the constructor section
   * This is where you introduce all necessary conditions for custom unit metric dimensions
4. Input constructor conditions for Numerator and Denominator
5. Put a descriptive name and click save
6. See your saved Unit Metric in the Library

![](<../.gitbook/assets/Screen Cast 2022-05-01 at 11.05.47 PM.gif>)

