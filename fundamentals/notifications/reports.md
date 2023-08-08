# Reports

**Reports** are detailed notifications sent on schedule.

{% hint style="info" %}
Cloudthread supports the delivery of reports through **e-mail** and **Slack**. See [setting-up-alerts-and-reports.md](../../guides/monitoring-cloud-costs/setting-up-alerts-and-reports.md "mention") for setup instructions.
{% endhint %}

{% hint style="success" %}
Cloudthread supports 3 types of Reports:

* **Daily Cost Update**
* **Weekly Cost Report**
  * **Movers & Shakers Section**
    * This report is a type of anomaly detection implemented on Cloudthread platform: it is being sent only in case there are significant changes in cost detected within the whole AWS environment
* **Weekly Savings Report**
  * Report on [optimization-opportunities.md](../cost-savings/key-concepts/optimization-opportunities.md "mention")
{% endhint %}

{% hint style="info" %}
Movers & Shakers is the version of **anomaly detection** Cloudthread platform supports.
{% endhint %}

## **Cost** Reports

### Email

<figure><img src="../../.gitbook/assets/Screen Cast 2022-08-24 at 9.35.33 PM.gif" alt=""><figcaption><p>Cloudthread Email Weekly Cost Report</p></figcaption></figure>

### Slack

<figure><img src="../../.gitbook/assets/Screen Cast 2022-08-24 at 9.33.40 PM.gif" alt=""><figcaption><p>Cloudthread Slack Weekly Cost Report</p></figcaption></figure>

## Savings Report

Savings report is part of [cost-savings](../cost-savings/ "mention") functionality. It is generated on a weekly basis and brings up the [optimization-opportunities.md](../cost-savings/key-concepts/optimization-opportunities.md "mention") discovered during the week.

The report has 3 parts:

* Total savings statistics
* Workflows summary: [savings-threads.md](../cost-savings/key-concepts/savings-threads.md "mention")
* Top 5 opportunities

<figure><img src="../../.gitbook/assets/savings-report-1.gif" alt=""><figcaption><p>Cloudthread Savings Report</p></figcaption></figure>
