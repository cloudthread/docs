# Setting up Alerts and Reports

Once you get familiar with [creating-custom-cost-views.md](creating-custom-cost-views.md "mention") and [creating-custom-unit-metrics.md](creating-custom-unit-metrics.md "mention"), you might want to setup [notifications](../fundamentals/notifications/ "mention") for the metrics so that important insights are not missed by you and your team.

Cloudthread has two types of notifications:

* [alerts.md](../fundamentals/notifications/alerts.md "mention") – short notifications sent on certain event (like threshold break)
* [reports.md](../fundamentals/notifications/reports.md "mention") – detailed notifications sent on schedule

{% hint style="success" %}
All  notifications can be delivered through **e-mail** and **Slack** (see [slack-integration.md](../fundamentals/notifications/slack-integration.md "mention") for Slack App setup instructions).
{% endhint %}

## What do I need it for? <a href="#what-do-i-need-it-for" id="what-do-i-need-it-for"></a>

{% hint style="info" %}
Using [alerts.md](../fundamentals/notifications/alerts.md "mention") and [reports.md](../fundamentals/notifications/reports.md "mention") will help you to:

* Get **notified** when your [cost-view.md](../fundamentals/cost-transparency/cost-view.md "mention") or [unit-metric.md](../fundamentals/unit-metrics/unit-metric.md "mention") break absolute or relative threshold you defined.
* Receive **detailed** insights on cloud spend relevant to you every week/month/quarter.
* **Subscribe** team members to important notifications so that they receive important information on their cloud costs in time.
{% endhint %}

## Detailed instructions <a href="#detailed-instructions" id="detailed-instructions"></a>

### Alerts

{% hint style="warning" %}
Currently alerts are available for [unit-metric.md](../fundamentals/unit-metrics/unit-metric.md "mention") only.
{% endhint %}

1. To set up [alerts.md](../fundamentals/notifications/alerts.md "mention") you should navigate to Unit Metrics Overview in the right menu pane
2. Once you are in Unit Metrics, choose the saved metric that you want to set alert on
3. Push "Set Alert" button at the bottom part of the first chart (Unit Metric) in Threshold Alerts section
   * ![](<../.gitbook/assets/Screen Cast 2022-05-03 at 5.37.54 PM.gif>)
4. Push "Add Alert" and fill in the form with the alert name, threshold type (absolute $ or relative %) and the value
5. Fill in the delivery channel details
   1. For e-mails you can add as many addresses as you want separated by a comma
   2. For Slack you need to supply webhooks data for channels you want the alerts be delivered to – see [slack-integration.md](../fundamentals/notifications/slack-integration.md "mention") for more details on how to obtain webhook IDs
6. Save the alert one form is filled
7. You should now be receiving a notification whenever the threshold for your unit metric is broken

![Setting up an Alert](<../.gitbook/assets/setting-up-alerts-and-reports__alerts_demo.gif>)

### Reports

{% hint style="warning" %}
Currently only one report type is available: **General Cost Report** is delivered **weekly**. You can learn more about it in [reports.md](../fundamentals/notifications/reports.md "mention") section.
{% endhint %}

1. To set up [reports.md](../fundamentals/notifications/reports.md "mention") you should navigate to Reports section at the bottom part of the right menu
2. There you will be able to see the list of the reports that already exist (created by any user of the platform) as well as the form to create a new report
3. Fill the form in with report name and report type (for now only one value is available - General Report)
4. Choose saved Cost View that the report will be based on
   * See [cost-view.md](../fundamentals/cost-transparency/cost-view.md "mention") for more details
   * You can choose only one Cost View for your report
   * If nothing is selected, default Cost View (Total Cost) will be used
5. Choose saved Unit Metrics to be added to report
   1. See [unit-metric.md](../fundamentals/unit-metrics/unit-metric.md "mention") for more details
   2. You can choose multiple unit metrics to be added to your report
   3. If nothing is selected, no unit metric section will be present in report
6. Add threshold data for the report section flagging biggest spend changes
   * Absolute Spend Threshold: report will not highlight items that have absolute spend less than the threshold
   * Absolute Change Threshold: report will not highlight items that have absolute spend change less than the threshold
   * Relative Change Threshold: report will not highlight items that have % spend change less than the threshold
7. Fill in the delivery channel details
   * For e-mails you can add as many addresses as you want separated by a comma
   * For Slack you need to supply webhooks data for channels you want the alerts be delivered to – see [slack-integration.md](../fundamentals/notifications/slack-integration.md "mention") for more details on how to obtain webhook IDs
8. Save the report – it should appear in the list above the form, and you will be getting the report on schedule specified in report description (see [reports.md](../fundamentals/notifications/reports.md "mention") for more details)

{% hint style="success" %}
By default a report for **Total Cost** view is created as part of **onboarding** process. After you set up an account, you will be receiving a weekly report to your inbox, no action needed.
{% endhint %}

![Setting up a Report](<../.gitbook/assets/setting-up-alerts-and-reports__reports_demo.gif>)
