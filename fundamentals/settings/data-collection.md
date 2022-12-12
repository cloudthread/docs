# Data Collection

Cloudthread provides easy integrations for data sets across your environment. The information below explains different inegrations options to have Cloudthread pull or push data from your environment.

## AWS

Cloudthread's AWS integrations are all Cloudformation Stack based.

There are four types of integration stacks Cloudthread provides:
1. Master Account template with a New Cost and Usage Report
2. Master Account template for an Existing Cost and Usage Report
2. StackSet template
3. Sub Account template

You can generate these templates in the Settings > Data Collection part of the platform. Please note that you must have already integrated a **Master Account** template in an organization root account to be able to use a **StackSet** template. **StackSet** templates require your organization root ID - which will be pre-filled based on the organization root account you decide to integrate.

**Cloudthreat existing Cost and Usage report requirements**:
1. Hourly time granularity
2. Parquet file type
3. Overwrite Report file versioning
4. Resource ID level report content

### Master Account templates with a New Cost and Usage Report

This stack template is for companies who do not already have a Cost and Usage report that matches Cloudthread's requirements. This template should be run in your main account if you're not using AWS Organizations, or in your organization root account if you are using AWS Organizations.

### Master Account templates with an Existing Cost and Usage Report

This stack template is for companies who have an existing Cost and Usage report that matches Cloudthread's requirements. You will be required to submit your report name, report prefix, and report bucket in the creation form. This template should be run in your main account if you're not using AWS Organizations, or in your organization root account if you are using AWS Organizations.

### StackSet

This stack template is for companies with many sub-accounts that would like to integrate all sub-accounts with a single stack. This template requires an organization root ID collected from a previously run master account template.

### Sub Account

This stack template is for companies that would like to integrate only a few sub-accounts from their environment.

## Kubernetes

Cloudthread's K8s integration is Helm Chart based.

Cloudthread requires a **Data Stream Token** to process incoming Data Ingestion API requests. This token helps organize and control the flow of data. Data Stream Tokens are generated with a **Data Stream Type** that determines how the incoming data is validated. Admin's have the ability to generate a Data Stream Token on the Cloudthread platform within the **Settings** tab.

Our K8s require a data stream token to be generated with **Data Stream Type** `kubernetes` - generating this token will also generated an AWS Key and Secret to be used for this integration in particular that are required for **Step 1** below.


1. Generate a **Data Stream Token** with **Data Stream Type** `kubernetes` from the **Settings** tab
2. Copy the data stream token, AWS credentials (Role Arn and External ID) tied to the data stream, and Organiztion ID
2. Add cloudhtread helm charts with: `helm repo add cloudthread  https://cloudthread.github.io/helm-charts/`
3. Create a kubernetes namespace to run the exporter `kubectl create namespace cloudthread`
4. Install kubernetes exporter with a command like this one:
```
helm install kubex cloudthread/cloudtread-kubex  \
    --namespace cloudthread \
    --set cloudthread.role_arn= YOUR ROLE ARN HERE \
    --set cloudthread.role_external_id=  YOUR ROLE_EXTERNAL_ID HERE \
    --set cloudthread.stream_token= YOUR STREAM_TOKEN  \
    --set cloudthread.org_id= YOUR ORG_ID  \
    --set cloudthread.dst_bucket=cloudthread-push \
    --set cloudthread.cluster_id= OPTIONAL HUMAN READABLE CLUSTER ID \
    --set cloudthread.region= CLOSEST AWS REGION
```
