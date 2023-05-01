---
description: App Section
---

# Tags Catalog

**Tag Catalogs** is a section of an app that covers **tagging automation** functionality Cloudthread provides.

It represents the setup interface for **Tag Catalog** creation and maintenance.

{% hint style="warning" %}
Tag Automation currently is supported on **GitHub** and **Terraform** based Infrastructure as a Code (IaaC) environments.
{% endhint %}

{% hint style="warning" %}
You can also use our `/api/tag-catalog` endpoint directly [here](https://docs.cloudthread.io/v/api-docs/reference/api-reference/tag\_catalog) via the developer API to create your own automation.
{% endhint %}

Connected to a GitHub repository through [GitHub Actions](https://docs.github.com/en/actions), Tag Catalog allows to make sure all the Terraform builds in the repository get the tags outlined in the catalog. This allows to maintain consistent tagging and control it from a single place.

GitHub Actions should be set up for the repo with a Cloudthread **API Key** and **Tag Catalog Key** in Action Secrets. Based on the connection between GitHub and Cloudthread established this way, the tags from the catalog are getting propagated to the `.tf` build files in the repository: every time the action is run a PR adding new tags is created.

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

### Key Features

* [#tag-catalogs-control-pane](tag-catalogs.md#tag-catalogs-control-pane "mention")
* [#tag-catalogs-table](tag-catalogs.md#tag-catalogs-table "mention")

#### Tag Catalogs Control Pane

The pane at the top of the page that includes major Tag Catalog actions:

* Adding new Tag Catalog
  * This creates a new tag catalog
  * The idea is that one tag catalog covers one repository, so that different repositories can be tagged differently
* Adding new API key
  * This is needed for fetching tag catalog from the GitHub repository
* Synchronizing tags
  * This syncs your current active AWS Cost Allocation tags from Cost Explorer and retrieves values from the last 7 days over all integrated **AWS Master Accounts**
  * These keys and values are then available for tag catalog tag key value pairs
  * **If you want to add a new key to a tag catalog, you must first add it as a Cost Allocation tag in AWS**
  * **Only AWS Master Accounts have access to cost allocation tags - you must integrate at least one payer AWS account to use Tag Catalogs**

#### Tag Catalogs Table

This is the table containing tag Catalogs. It allows to set the tag key-value pairs within the Tag Catalog, saving the catalog state and resetting the Catalog.
