# Integrations

**Integrations** section of [.](./ "mention") has **Slack** and **Jira** integrations available.

<figure><img src="../../.gitbook/assets/settings-integration-1.png" alt=""><figcaption></figcaption></figure>

## Slack Integration

In order to setup **Slack** for [alerts.md](../notifications/alerts.md "mention") and [reports.md](../notifications/reports.md "mention") you need to navigate to **Settings** menu item at the bottom part of the menu to the left, choose **Integrations** section and click Slack button.

After that you will be redirected to the Slack setup page.

![Slack setup screen](<../../.gitbook/assets/image (11).png>)

Once you have Slack setup, you will have your workspace channels available in [setting-up-alerts-and-reports.md](../../guides/monitoring-cloud-costs/setting-up-alerts-and-reports.md "mention").

## Jira Integration

In order to use [savings-threads.md](../cost-savings/key-concepts/savings-threads.md "mention") workflow functionality, you need to set up Jira **integration.**

{% hint style="success" %}
Cloudthread currently supports only [Jira project management](https://www.atlassian.com/software/jira) integration. Both **Cloud** and **Server** versions are supported.
{% endhint %}

### Jira Cloud

### Jira Server

<div align="left">

<figure><img src="../../.gitbook/assets/settings-integrations-2-jira-server.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

#### Detailed instructions&#x20;

1. Go to Jira Administration > Applications > Application Links
2. Click `Create Link` and select `External application` + `Direction Incoming`
3. For Name - set to whatever they want (`Cloudthread` is fine)
4. For Redirect URL  - set to [`https://app.cloudthread.io/settings/third-party-integrations?provider=jira_server`](https://app.cloudthread.io/settings/third-party-integrations?provider=jira\_server)
5. For Application permissions - set to `Write`
6. Click `Save`
7. Go to Cloudthread and Settings >Integrations and click `JIRA Server`
8. Enter:
9. Client ID from step 6
10. Client Secret from step 6
11. Jira server url including https:// and no trailing slash (e.g. [`https://mycompany.atlassian.server.com`](https://mycompany.atlassian.server.com/))
12. Follow through integration flow
