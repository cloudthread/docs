# Connecting AWS Account

Connecting AWS account is an **essential** part of Cloudthread onboarding process and the most fundamental part of the setup. You cannot skip this step – your organization's AWS billing and usage data is essential for the platform to deliver value, i.e. help you to increase efficiency of your cloud spend.

## Cloudthread AWS access

{% hint style="success" %}
We are very careful with the access to your AWS environment, you can always see and adjust the policy templates we use in your accounts. Our policies are **read-only**, except for the billing S3 bucket we setup for you with your permission.

[Cloudthread Policy](../policy\_cfn\_cldthrd.yaml)
{% endhint %}

Cloudthread is using a delegated access role to read data from your account into the application This role has read access only to the resources necessary for generating the insights – AWS cost and usage data. This includes but not limited to:

* [AWS Cost and Usage Report](https://aws.amazon.com/aws-cost-management/aws-cost-and-usage-reporting/) (CUR)
* [AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/) API
* [CloudWatch](https://aws.amazon.com/cloudwatch/) metrics
* [AWS Simple Storage](https://aws.amazon.com/s3) (S3)
  * To read saved CUR files

{% hint style="info" %}
In more detail, Cloudthread needs roughly **5 sets** of permissions / actions:

1. **CUR bucket creation**, with complete access to this bucket (and only this bucket). This allows us to maintain the bucket policy overtime for any AWS changes that are required to maintain the CUR connection, and read CUR data.
2. **Listing organization root ids** to power StackSet functionality so that's it's easy to integrate many sub accounts to power unit metics
3. **CloudWatch read access** to list metrics and collect CloudWatch data
4. **Cost Explorer complete access** to power the first 24 hours of the tool and trusted advisor maintenance
5. **CUR report complete access** to create a cur report and help maintain existing ones
{% endhint %}

{% hint style="warning" %}
Before connecting your account to Cloudthread we recommend you make sure [AWS Organizations with consolidated billing](https://aws.amazon.com/organizations/) are **enabled** in your AWS environment.
{% endhint %}

{% hint style="success" %}
Cloudthread is using the most granular version of [AWS Cost and Usage Report](https://aws.amazon.com/aws-cost-management/aws-cost-and-usage-reporting/) **(CUR)** to deliver cost insights. Unlike with most other cloud cost management solutions, with Cloudthread you do not need to set it up yourself, our onboarding process takes care of it.

_If you have a version of CUR already enabled in your account, Cloudthread can work with it as well._
{% endhint %}

## Connecting Cloudthread via CF Stack

{% hint style="info" %}
Cloudthread is using [**AWS CloudFormation**](https://aws.amazon.com/cloudformation/) **(CF)** **service** to enable fast and reliable integration. You control every part of this setup process and have full visibility into actions CF is performing with your AWS environment. At any point in time you can disconnect your account from Settings page in Cloudthread app.
{% endhint %}

### 1. Create and confirm Cloudthread account

After your account is [created](https://app.core.cloudthread.io/sign-up/) and confirmed via email, you'll be prompted to "_Connect Cloudthread via CF Stack_".

![Connect Cloudthread via CF Stack](../.gitbook/assets/connecting-aws-account\_\_1\_cf\_stack\_page.png)

### 2. Redirect to AWS

Pressing "_Connect Cloudthread via CF Stack_" will automatically **redirect** you to your AWS console, and **pre-populate** a CF Stack with Cloudthread's required access permissions.

{% hint style="warning" %}
* Make sure you are in the right AWS account.
* We recommend to start with AWS management account.
{% endhint %}

### 3. Review CF stack and confirm creation

![CF stack setup AWS screen](https://archbee-image-uploads.s3.amazonaws.com/c7\_e5ZVbCODT0rr09z9Gx/cpr-c6EyGtNIdzG6Pzk9E\_image.png)

{% hint style="warning" %}
Make sure to check mark **"I acknowledge that AWS CloudFormation might create IAM resources."**
{% endhint %}

{% hint style="danger" %}
**Note:** In order for Cloudthread to work, [Cost and Usage Report](https://docs.aws.amazon.com/cur/latest/userguide/what-is-cur.html) (CUR) file needs to be set up in **us-east-1** region. CloudFormation stack has it preset, but if you change the region the stack won't work.
{% endhint %}

Once you initiate CF stack creation, it will take up to an hour to setup the required resources and policies for Cloudthread to generate initial insights. Your AWS console will show something like this:

![AWS console after CF stack launch](https://archbee-image-uploads.s3.amazonaws.com/c7\_e5ZVbCODT0rr09z9Gx/9ZyRUNWNOupFwOa5b55Ey\_image.png)

### 4. Come back to Cloudthread App

Once the initial setup is complete, you will be able to see first cost insights in the app.

![Cloudthread App](../.gitbook/assets/connecting-aws-account\_\_default\_cost\_view.png)

{% hint style="info" %}
**"Initial" cost insights**

Cloudthread is using [AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/) API service to supply cost insights while more detailed AWS Cost and Usage Report (CUR) is being created (which can take up to 48 hours).

_This means that you'll have high level cost analytics available through the Cost Explorer API immediately when you login and that more granular resource level data will only be available when CUR data is ready._
{% endhint %}

{% hint style="warning" %}
Once the CUR file is ready Cloudthread will notify you, and you will be able to see deeper insights on the platform.

_Often, when CUR file is created it does not have all the historical data – your AWS support must be contacted to backfill it._
{% endhint %}
