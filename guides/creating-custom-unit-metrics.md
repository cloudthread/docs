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
2. Click "Create New Metric" button at the top-right corner of the screen
3. Fill in the form to create a basis for your future custom unit metric
4. Input constructor conditions for Numerator and Denominator
5. Put a descriptive name and click save
6. See your saved Unit Metric in the Library

![Creating a custom Unit Metric](../.gitbook/assets/creating-custom-unit-metrics-1-demo.gif)
