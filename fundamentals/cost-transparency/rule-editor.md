---
description: App Section
---

# Rule Lab

**Rule Lab** is the section of the app where you can define [cost-allocation-rules.md](key-concepts/cost-allocation-rules.md "mention").

<figure><img src="../../.gitbook/assets/rules-lab-1.png" alt=""><figcaption><p>Cloudthread Rule Lab</p></figcaption></figure>

## Key Features

### Rule Lab Control Pane

<figure><img src="../../.gitbook/assets/rule-ditor-1-control-pane.png" alt=""><figcaption></figcaption></figure>

This is the top pane of the page that includes:

* Rule name
  * This is editable
* **Delete**, **Save** and **Save As** buttons
* [#cost-type-selector](rule-editor.md#cost-type-selector "mention")
* [#month-picker](rule-editor.md#month-picker "mention")

#### Cost Type Selector

Allows for choosing the cost type and adding/removing cost components such as Taxes, Credits, Refunds, Discounts, Fees as well as Amortization.

<div align="left">

<figure><img src="../../.gitbook/assets/rule-editor-2-cost-type.png" alt="" width="225"><figcaption></figcaption></figure>

</div>

#### Month Picker

Needed for showing the total cost per rule.

<div align="left">

<figure><img src="../../.gitbook/assets/rule-editor-3-month-picker.png" alt="" width="284"><figcaption></figcaption></figure>

</div>

### Tags Summary Pane

This pane summarizes all Custom Tags you have created in Rule Lab.

<div align="left">

<figure><img src="../../.gitbook/assets/rule-editor-4-tags-summary.png" alt="" width="374"><figcaption></figcaption></figure>

</div>

#### Export Costs Button

The button saves the costs distributed by tags (by cost allocation rules) in CSV format.

### Rule Lab Interface

This is the interface for creating and editing the [cost-allocation-rules.md](key-concepts/cost-allocation-rules.md "mention").

<div align="left">

<figure><img src="../../.gitbook/assets/rule-editor-5-rule-editor.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

The interface has **2 major steps**:

1. Costs source dropdown
2. Split Dimension dropdown

#### Costs Source Dropdown

Currently 2 options are available:

* AWS Costs
* Custom Data from [custom-data-api.md](../custom-data-api.md "mention")

#### Split Dimension Dropdown

The data dimensions for the split, based on the [#costs-source-dropdown](rule-editor.md#costs-source-dropdown "mention")

* For AWS:
  * Accounts
  * Payer Accounts
  * Regions
  * Tags
  * Services
  * Invoice IDs
  * Charge Categories
  * Purchase Options
  * RI / SP ARNs

{% hint style="success" %}
You can see the instructions on how to create the rule in [setting-up-cost-allocation-rules.md](../../guides/monitoring-cloud-costs/setting-up-cost-allocation-rules.md "mention") guide.
{% endhint %}
