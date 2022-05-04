# Unit Metrics Overview

**Unit Metrics Overview** is the section of the app where you can see insights and adjust [unit-metric.md](unit-metric.md "mention").

### Key Features

#### Unit Metrics Control Pane

This is top pane of the page that includes:

* [unit-metrics-library.md](unit-metrics-library.md "mention")
* [#date-picker](unit-metrics-lab.md#date-picker "mention") and [#undefined](unit-metrics-lab.md#undefined "mention")

![Unit Metrics Control Pane](<../../.gitbook/assets/image (6).png>)

#### Date Picker

This is functionality for setting the dates for the cost efficiency insights.

![Date Picker](<../../.gitbook/assets/image (10).png>)

#### New Metric Constructor

Constructor allows for [creating-custom-unit-metrics.md](../../guides/creating-custom-unit-metrics.md "mention") by defining Numerator and Denominator.

![](<../../.gitbook/assets/image (5).png>)

#### Unit Metric Chart

Unit Metric cost chart with **current** and **previous** period spend vs. time lines.

{% hint style="info" %}
**Previous period** is defined as period of equal length directly proceeding the current period:

* If current period is May 1, 2022 - May 7, 2022, previous period is April 24, 2022 - April 30, 2022
{% endhint %}

Unit metrics chart also allows for [#alerts](../../guides/setting-up-alerts-and-reports.md#alerts "mention") setup.

![](<../../.gitbook/assets/image (8).png>)

#### Unit Metric Numerator Chart

Absolute cost chart for the Numerator part of Unit Metric with **current** and **previous** period spend vs. time lines ($).

#### Unit Metric Denominator Chart

Absolute cost chart for the Denominator part of Unit Metric with **current** and **previous** period spend vs. time lines (usage units).
