# Data Collection

Cloudthread provides easy integrations for data sets across your environment. The information below explains different inegrations options to have Cloudthread pull data from your environment.

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

### Master Account templates with an Existing Cost and Usage Report (Onboarding flow only)

This stack template is for companies who have an existing Cost and Usage report that matches Cloudthread's requirements. You will be required to submit your report name, report prefix, and report bucket in the creation form. This template should be run in your main account if you're not using AWS Organizations, or in your organization root account if you are using AWS Organizations.

### StackSet

This stack template is for companies with many sub-accounts that would like to integrate all sub-accounts with a single stack. This template requires an organization root ID collected from a previously run master account template.

### Sub Account

This stack template is for companies that would like to integrate only a few sub-accounts from their environment.
