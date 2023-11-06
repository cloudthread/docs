# Integrations

**Integrations** section of [.](./ "mention") has **Slack** and **Jira** integrations available.

<div align="left">

<figure><img src="../../.gitbook/assets/settings-integration-1.png" alt="" width="563"><figcaption></figcaption></figure>

</div>

## Slack Integration

In order to setup **Slack** for [alerts.md](../notifications/alerts.md "mention") and [reports.md](../notifications/reports.md "mention") you need to navigate to **Settings** menu item at the bottom part of the menu to the left, choose **Integrations** section and click Slack button.

After that you will be redirected to the Slack setup page.

<div align="left">

<img src="../../.gitbook/assets/image (11).png" alt="Slack setup screen" width="375">

</div>

Once you have Slack setup, you will have your workspace channels available in [setting-up-alerts-and-reports.md](../../guides/monitoring-cloud-costs/setting-up-alerts-and-reports.md "mention").

## Jira Integration

In order to use [savings-threads.md](../cost-savings/key-concepts/savings-threads.md "mention") workflow functionality, you need to set up Jira **integration.**

{% hint style="success" %}
Cloudthread currently supports only [Jira project management](https://www.atlassian.com/software/jira) integration. Both **Cloud** and **Server** versions are supported.
{% endhint %}

### Jira Cloud

![](../../.gitbook/assets/settings-integrations-1-jira-cloud.png)

#### Detailed instructions&#x20;

1. Once you click `Integrate` in Integrations section of Settings, you will be redirected to Atlassian sign-in
2. Sign in or create an account for JIRA cloud
3.  Accept access request

    <div align="left">

    <figure><img src="../../.gitbook/assets/settings-integrations-1-jira-cloud-2.png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
4. Come back to Cloudthread app to verify that integration is successful

<div align="left">

<figure><img src="../../.gitbook/assets/settings-integrations-1-jira-cloud-3.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

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

### Jira Webhook

{% hint style="info" %}
Some helpful information about adding a new webhook you can find in official [Jira documentation](https://developer.atlassian.com/cloud/jira/platform/webhooks/).
{% endhint %}

#### Detailed Instructions for Jira Cloud

1.  In Jira go into Settings → System

    <div align="left">

    <figure><img src="../../.gitbook/assets/settings-integrations-4-jira-webhook.png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
2.  In Jira go into Advanced → Webhooks



    <div align="left">

    <figure><img src="../../.gitbook/assets/settings-integrations-5-jira-webhook.png" alt="" width="240"><figcaption></figcaption></figure>

    </div>
3.  Click on Create a `WebHooks` button



    <div align="left">

    <figure><img src="../../.gitbook/assets/settings-integrations-8-jira-webhook.png" alt="" width="229"><figcaption></figcaption></figure>

    </div>
4.  Copy webhook URL from Cloudthread → Settings → Integrations → JIRA Webhook URL



    <div align="left">

    <figure><img src="../../.gitbook/assets/settings-integrations-6-jira-webhook.png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
5.  Put Cloudthread WebHook URL into URL field in `Create a WebHook` UI in Jira cloud



    <div align="left">

    <figure><img src="../../.gitbook/assets/settings-integrations-9-jira-webhook.png" alt="" width="375"><figcaption></figcaption></figure>

    </div>
6.  Select ‘updated’ and ‘deleted’ events for Jira issues. You are allowed to write a specific JQL query for the related project to reduce the amount of events that are sent to Cloudthread



    <div align="left">

    <figure><img src="../../.gitbook/assets/settings-integrations-7-jira-webhook.png" alt="" width="129"><figcaption></figcaption></figure>

    </div>
