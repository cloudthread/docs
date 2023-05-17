# Creating Unit Metrics

[unit-metrics](../../fundamentals/unit-metrics/ "mention") is the major feature of Cloudthread aimed at helping you to figure out how much value you are getting from your cloud. It allows to construct unit metrics based on various sources of data, so that your teams can track them and focus on cost efficiency.

{% hint style="warning" %}
Unit metrics flow is available once the full data setup is done, which can take up to **48 hours** from the AWS account connection.
{% endhint %}

## What do I need it for?

{% hint style="info" %}
Creating custom [unit-metric.md](../../fundamentals/unit-metrics/key-concepts/unit-metric.md "mention") can help you to:

* Find out answers to the questions like "How much does my **team** really pays AWS for **every** Lambda **invocation** in **us-east-1** region?"
* See the **trends** for your unit metric
* Set up reports and alerts for the Unit Metric, so that you can be notified on important changes in your cloud cost efficiency
  * Check out [setting-up-alerts-and-reports.md](setting-up-alerts-and-reports.md "mention") guide to learn more
{% endhint %}

## Detailed instructions

1. Navigate to [unit-metrics-lab.md](../../fundamentals/unit-metrics/unit-metrics-lab.md "mention") section in [unit-metrics](../../fundamentals/unit-metrics/ "mention") space in the menu to the left:
   * You can get there via several different paths:
     * From the menu pane at the left
     * From the [summary-dashboard.md](../../fundamentals/dashboards/summary-dashboard.md "mention") by clicking "Create New Unit Metric"
     * From the [unit-metrics-library.md](../../fundamentals/unit-metrics/unit-metrics-library.md "mention") by clicking "Create New Metric"
       * A good practice is to explore the Library if the metric you want to create already exists
   * You will see a page with empty chart placeholders (Cost per Unit, Numerator, Denominator) as well as the settings pane to the right
     * Find more about the settings pane: [#settings-pane](../../fundamentals/unit-metrics/unit-metrics-lab.md#settings-pane "mention")
2. Set the **Numerator** Source and Filters:
   * CUR source – billing data from Cost Usage Report ($), default option
     * Service, Usage Type and Operation filters available
   * CloudWatch source – monitoring data, requires [Broken link](broken-reference "mention")
     * Namespace, Account, Region and Tag filters available
   * Custom Data source – any data pushed to Cloudthread through [custom-data-api.md](../../fundamentals/custom-data-api.md "mention")
     * Stream Token and Dimension filters available
   * **Note:** Leaving filters blank sets numerator to the default value (e.g.: Total Spend for CUR option)
3. Set the **Denominator** Source and Filters:
   * This is a **required** step – denominator data is essential for the charts to show data
   * The sources and dimensions available are similar to the ones in Numerator
4. Check the charts to see the trend and accuracy
5. Click "Save as..." at the left top corner of the screen
6. See your saved Unit Metric in the [unit-metrics-library.md](../../fundamentals/unit-metrics/unit-metrics-library.md "mention")

<figure><img src="../../.gitbook/assets/creating-custom-unit-metrics-1_demo.gif" alt=""><figcaption><p>Creating custom Unit Metric</p></figcaption></figure>
