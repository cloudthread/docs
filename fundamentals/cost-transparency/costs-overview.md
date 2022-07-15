# Costs Overview

**Costs Overview** is the section of the app where you can see insights and adjust [cost-view.md](cost-view.md "mention").

### Key Features

#### Cost View Control Pane

This is the top pane of the page that includes:

* Cost View name
* Filter indicator
* **Delete**, **save as new** and **save changes** buttons
* [#date-picker](costs-overview.md#date-picker "mention") and [#filter-pane](costs-overview.md#filter-pane "mention")
* [#absolute-cost-chart](costs-overview.md#absolute-cost-chart "mention")
* [#absolute-cost-breakdown-chart](costs-overview.md#absolute-cost-breakdown-chart "mention")
* [#undefined](costs-overview.md#undefined "mention")

![Cost View Control Pane](../../.gitbook/assets/image.png)

#### Date Picker

![](../../.gitbook/assets/date-picker.png)



#### Filter Pane

Filter pane is designed for a convenient filtering of AWS cost data and [creating-custom-cost-views.md](../../guides/creating-custom-cost-views.md "mention").

{% hint style="success" %}
Cloudthread allows for complex filtering of AWS cost data across **Account**, **Region**, **Service** and **Tag** dimensions. Both **AND** and **OR** filter conditions are supported as well as **IS** and **IS NOT** clauses.
{% endhint %}

![Filter Pane](<../../.gitbook/assets/Screen Cast 2022-05-03 at 8.13.50 PM.gif>)

#### Absolute Cost Chart

Absolute cost chart with **current** and **previous** period spend vs. time lines.

{% hint style="info" %}
**Previous period** is defined as period of equal length directly proceeding the current period:

* If current period is May 1, 2022 - May 7, 2022, previous period is April 24, 2022 - April 30, 2022
{% endhint %}

![Absolute Cost Chart](<../../.gitbook/assets/image (9).png>)

#### Absolute Cost Breakdown Chart

Absolute cost chart with the **additional** data dimension, but no previous period displayed.

This chart also has a data table attached to see the breakdown in more convenient way and control [drill-down.md](../drill-down.md "mention").

![Absolute cost breakdown chart](<../../.gitbook/assets/Screen Cast 2022-05-03 at 8.03.32 PM.gif>)

#### Tag Analyzer

Table with spend distributed by tag. See [tag-analyzer.md](tag-analyzer.md "mention") for more details.
