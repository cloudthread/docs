# Data Collection

Cloudthread provides easy integrations for data sets across your environment. The information below explains different inegrations options to have Cloudthread pull data from your environment.

## AWS

Cloudthread's AWS integrations are all Cloudformation Stack based.

There are four types of integration stacks Cloudthread provides:
1. Master Account templates with a New Cost and Usage Report
2. Master Account templates with a Existing Cost and Usage Report
2. StackSet template
3. Sub Account templates

You can generate these templates in the Settings > Data Collection part of the platform. Please note that you must have already integrated a Master Account template in your organization root acccount to be able to use a StackSet template. StackSet templates require a Root ID 

## Master Account templates with a New Cost and Usage Report

This stack template is for companies who do not already have a Cost and Usage report that matches Cloudthread's requirements. This template should be run in your main account if you're mono-account, or in your payer account / organization root account if you're multi-account.

## Master Account templates with a Existing Cost and Usage Report (Onboarding flow only)

This stack template is for companies who have an existing Cost and Usage repor that matches Cloudthread's requirements. You will be required to submit your report name, report prefix, and report bucket in the creation form. This template should be run in your main account if you're mono-account, or in your payer account / organization root account if you're multi-account.

## StackSet

This stack template is for companies with many sub-accounts that would like to integrate all sub-accounts with a single stack. This template requires an Organization Root ID from a previously run Master Account stack.

## Sub Account

This stack template is for companies that would like to integrate only a few sub-accounts from their environment.
