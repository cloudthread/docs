# Connecting AWS Account

Connecting AWS account is an **essential** part of Cloudthread onboarding process and the most fundamental part of the setup. You cannot skip this step – your organization's AWS billing and usage data is essential for the platform to deliver value, i.e. help you to increase efficiency of your cloud spend.

## Cloudthread AWS access

{% hint style="success" %}
We are very careful with the access to your AWS environment, you can always see and adjust the policy templates we use in your accounts. Our policies are **read-only**, except for the billing S3 bucket we setup for you with your permission.



[Cloudthread Policy](http://s3.us-west-2.amazonaws.com/cloudthread-cfn-resources/stacks/VLiZS1awYio9Hlp2afzh1QKEG4HOV4nAPEEzC5ckHDQ.yaml)
{% endhint %}

Cloudthread is using a delegated access role to read data from your account into the application This role has read access only to the resources necessary for generating the insights – AWS cost and usage data. This includes but not limited to:[](https://aws.amazon.com/aws-cost-management/aws-cost-and-usage-reporting/)&#x20;

*   [AWS Cost and Usage Report](https://aws.amazon.com/aws-cost-management/aws-cost-and-usage-reporting/) (CUR)

*   [AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/) API

*   [CloudWatch](https://aws.amazon.com/cloudwatch/) metrics

*   [AWS Simple Storage](https://aws.amazon.com/s3) (S3)

    *   To read saved CUR files

{% hint style="info" %}
### Cloudthread AWS access policy in detail



**\[Thomas to fill in]**



Example from CloudZero:



*CloudZero is a different type of Cloud Cost Management solution and requires permissions beyond the typical cost and usage data. By using metadata on how your AWS environment is operating, the services that you are using, and how they are being used CloudZero can boost tag coverage, identify more complex anomalies and highlight the specific resources and changes that are responsible for cost changes in your environment.*

***All of CloudZero's permissions are Read-Only****
We have no access to data except where explicitly authorized (for example the S3 bucket where your cost and usage report is stored)*

***Summary of Permissions:***

*   *Management Account*

    *   *Our access is required to function*

    *   *Access to the Cost and Usage, Billing and Organizations API*

    *   *Access to the Cost and Usage S3 bucket where reports are stored*

    *   *Access to CloudWatch Metrics, and list/read-only metadata service API's*

*   *Resource (member) Accounts*

    *   *Our access is optional, required for waste and root cause analysis*

    *   *Access to CloudWatch Metrics, and list/read-only metadata service API's*

*Note: If you have resources (in your AWS cloud) in any regions for which STS is not active by default (e.g. ap-east-1 or eu-south-1), make sure you activate those regions following the *[*Managing AWS STS in an AWS Region*](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_temp_enable-regions.html)* guide.*
{% endhint %}

{% hint style="success" %}
Before connecting your account to Cloudthread we recommend you make sure [AWS Organisations with consolidated billing](https://aws.amazon.com/organizations/) are** enabled in your AWS environment**[****](https://aws.amazon.com/organizations/)**.**
{% endhint %}

{% hint style="warning" %}
Cloudthread is using the most granular version of [AWS Cost and Usage Report](https://aws.amazon.com/aws-cost-management/aws-cost-and-usage-reporting/) **(CUR)** to deliver cost insights. Unlike with most other cloud cost management solutions, with Cloudthread you do not need to set it up yourself, our onboarding process takes care of it.



*If you have a version of CUR enabled in your account Cloudthread can work with it as well.*
{% endhint %}

# Connecting Cloudthread via CF Stack

{% hint style="info" %}
Cloudthread is using [**AWS CloudFormation**](https://aws.amazon.com/cloudformation/)** (CF) **service** **to enable fast and reliable integration. You control every part of this setup process and have full visibility into actions CF is performing with your AWS environment. At any point in time you can disconnect your account from Settings page in Cloudthread app.
{% endhint %}

## 1. Create and confirm Cloudthread account

After your account is [created](app.cloudthread.io/sign-up) and confirmed via email, you'll be prompted to "*Connect Cloudthread via CF Stack*".

![Connect Cloudthread via CF Stack](https://archbee-image-uploads.s3.amazonaws.com/c7_e5ZVbCODT0rr09z9Gx/51jIaOM0EwsLP__rD08MG_image.png)

## 2. Redirect to AWS

Pressing "*Connect Cloudthread via CF Stack*" will automatically **redirect** you to your AWS console, and **pre-populate** a CF Stack with Cloudthread's required access permissions.&#x20;

{% hint style="warning" %}
*   Make sure you are in the right AWS account.

*   We recommend to start with AWS management account.
{% endhint %}

## 3. Review CF stack and confirm creation

![CF stack setup AWS screen](https://archbee-image-uploads.s3.amazonaws.com/c7_e5ZVbCODT0rr09z9Gx/cpr-c6EyGtNIdzG6Pzk9E_image.png)

{% hint style="warning" %}
Make sure to check mark *"Acknowlegde that CloudFormation might create IAM resources"*
{% endhint %}

{% hint style="danger" %}
**Note:** In order for Cloudthread to work, [Cost and Usage Report](https://docs.aws.amazon.com/cur/latest/userguide/what-is-cur.html) (CUR) file needs to be set up in **us-east-1**. Our CloudFormation stack has it preset, but if you change the region the stack won't work.
{% endhint %}

Once you initiate CF stack creation, it will take up to an hour to setup the required resources and policies for Cloudthred to generate initial insights. Your AWS console will show something like this:

![AWS console after CF stack launch](https://archbee-image-uploads.s3.amazonaws.com/c7_e5ZVbCODT0rr09z9Gx/9ZyRUNWNOupFwOa5b55Ey_image.png)

## 4. Come back to Cloudthread App

Once the initial setup is complete, you will be able to see first cost insights in the app.

![Cloudthread App](https://archbee-image-uploads.s3.amazonaws.com/c7_e5ZVbCODT0rr09z9Gx/D20Bh-wmsnI_x-x4ASjtQ_image.png)

{% hint style="info" %}
### **"Initial" cost insights**



Cloudthread is using  [AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/) API service to supply cost insights while more detailed AWS Cost and Usage Report (CUR) is being created (which can take up to 48 hours).



*This means that you'll have high level cost analytics available through the Cost Explorer API immediately when you login and that more granular resource level data will only be available when CUR data is ready. *
{% endhint %}

{% hint style="warning" %}
Once the CUR file is ready Cloudthread will notify you, and you will be able to see deeper insights on the platform.



*Often, when CUR file is created it does not have all the historical data – your AWS support must be contacted to backfill it.*
{% endhint %}

\[We need to explicitly outline what Cost Explorer data does not provide – Thomas]

