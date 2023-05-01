---
description: App Section
---

# Opportunities Explorer

**Opportunities Explorer** is the section of the app where you can manage [optimization-opportunities.md](key-concepts/optimization-opportunities.md "mention").

<figure><img src="../../.gitbook/assets/opportunity-explorer-1.png" alt=""><figcaption><p>Cloudthread Opportunities Explorer</p></figcaption></figure>

## Key Features

### Create New Opportunity Button

Cloudthread allows for creation of custom optimization opportunities. This button starts the creation flow. Refer to [creating-custom-optimization-opportunities.md](../../guides/optimizing-cloud-costs/creating-custom-optimization-opportunities.md "mention") for more details.

### Unassigned Opportunities Table

List of all discovered and custom opportunities that were not assigned to any thread:

* Opportunity ID
* Record ID
  * Resource ID or Discount code
* [Estimated Monthly Savings](key-concepts/optimization-opportunities.md#estimated-savings)
* [Difficulty](key-concepts/optimization-opportunities.md#difficulty)
* [Type](key-concepts/optimization-opportunities.md#optimization-type)
* [Category](key-concepts/optimization-opportunities.md#recommendation-context)
* [Status](key-concepts/optimization-opportunities.md#workflow-context)
* [Resource context](key-concepts/optimization-opportunities.md#resource-context)
  * Account
  * Region
  * Service
  * Tags
* First Detected
* Last Detected

{% hint style="success" %}
Each row in the table can be **extended** to see the raw JSON details on opportunity.
{% endhint %}

The rows of the table are **selectable.** For the selected rows 3 actions are available (buttons at the top of the table):

* Create New Thread
* Assign To Thread
* Archive Selected

#### Create New Thread

Redirects to a form for creating a new Thread (see [savings-threads.md](key-concepts/savings-threads.md "mention")) with selected opportunities.

#### Assign To Thread Button

Redirects to a form for adding opportunities to an existing Thread (see [savings-threads.md](key-concepts/savings-threads.md "mention")).

#### Archive Selected Button

Moves selected opportunities to [#archived-opportunities-table](opportunities-explorer.md#archived-opportunities-table "mention"). This functionality allows to **ignore** the opportunities that are **irrelevant** and will not be implemented.

{% hint style="info" %}
Opportunities can be **archived** by clicking trash bin button in Actions column at the end of the table.
{% endhint %}

### Archived Opportunities Table

The table with matching structure tot he above containing archived opportunities.

{% hint style="info" %}
Archived opportunities can be **restored** by clicking restore button in Actions column at the end of the table.
{% endhint %}

### Opportunity Details Page

By clicking on the **Opportunity ID** in the tables above, you will be redirected to **Opportunity Details Page** containing detailed context on the optimization opportunity. See [optimization-opportunities.md](key-concepts/optimization-opportunities.md "mention") for description of the context types.

