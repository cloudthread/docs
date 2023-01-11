# Tag Overview

**Tag Overview** is a section of an app containing analytics around tagging compliance.

{% hint style="info" %}
**Tagging** is one of the foundations of cloud cost management supporting all the major phases of [FinOps cycle](https://www.finops.org/framework/phases/) (inform -> optimize -> operate).

You can learn about tagging in AWS in our [blog](https://www.cloudthread.io/blog/a-complete-introductory-guide-to-aws-cost-allocation-tags).
{% endhint %}

### Key Features

* #### [#tag-overview-control-pane](tag-overview.md#tag-overview-control-pane "mention")
* #### [#tag-key-selection-field](tag-overview.md#tag-key-selection-field "mention")
* #### [#tag-coverage-overview-chart](tag-overview.md#tag-coverage-overview-chart "mention")
* #### [#tag-coverage-breakdown-chart](tag-overview.md#tag-coverage-breakdown-chart "mention")

#### Tag Overview Control Pane

The pane at the top of the page that includes [#date-picker](../cost-transparency/costs-overview.md#date-picker "mention") and [#filter-pane](../cost-transparency/costs-overview.md#filter-pane "mention") similar to the ones at other sections of the app ([unit-metrics-lab.md](../unit-metrics/unit-metrics-lab.md "mention") and [costs-overview.md](../cost-transparency/costs-overview.md "mention")).

#### Tag Key Selection Field

This is the field for a quick pre-filtering for the tag key to analyze.

![](<../../.gitbook/assets/image (6).png>)

#### Tag Coverage Overview Chart

This is the chart displaying **tag coverage metric** (percentage of resources covered with tags vs all the resources) by time dimension. This excludes default tags AWS resources get by default.

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

#### Tag Coverage Breakdown Chart

This is the chart with added breakdown functionality. It allows to breakdown the tag coverage metric with the following dimensions:

* Account
* Regions
* Services
* Usage Types
* Operations
* Resources

<figure><img src="../../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>
