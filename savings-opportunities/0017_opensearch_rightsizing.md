# OpenSearch Righsizing

{% hint style="success" %}
See [optimization-opportunities.md](../fundamentals/cost-savings/key-concepts/optimization-opportunities.md "mention") for more details on the concept.
{% endhint %}

## Key Metadata

### Source: `AWS`

### Service: `Amazon OpenSearch`

### Difficulty: `Easy`

{% hint style="info" %}
**Easy:** Zero downtime, zero performance risks

**Medium:** Zero downtime, potential performance trade-offs

**Hard:** Downtime required, potential performance trade-offs
{% endhint %}

### Type: `Usage`

{% hint style="info" %}
**Usage:** Actions altering actual cloud resources (e.g. changing VM specs, storage retention policies, removing unused resources)

**Rate:** Actions targeting financial concepts, mainly commitment-based discounts (e.g. [Reserved Instances](https://aws.amazon.com/ec2/pricing/reserved-instances/) and [Savings Plans](https://aws.amazon.com/savingsplans/) for AWS, [Committed Use Discounts](https://cloud.google.com/compute/docs/instances/signing-up-committed-use-discounts) for GCP)

**Custom:** Ad-hoc opportunities for custom tracking needs. See [creating-custom-optimization-opportunities.md](../guides/optimizing-cloud-costs/creating-custom-optimization-opportunities.md "mention") for more details.
{% endhint %}

## Details

### How Opportunity is Detected

Cloudthread scans OpenSearch for domains eligible for downsizing based on CPU and memory utilization maximum being below adjustable thresholds.

### Opportunity Threshold Metrics

* CPUUtilization
  * **Default value:** `40%`
* SysMemoryUtilization
  * **Default value:** `40%`

{% hint style="info" %}
What metrics the Savings Opportunity is referencing.
{% endhint %}

### How Estimated Monthly Savings is Calculated

Cost impact for this opportunity is the average daily ESInstance cost of the domain multiplied by the discount of downsizing the instance. The discount is ratio of the recommended instance size cost to the current instance size cost.

{% hint style="warning" %}
Note that this is an **upper bound** for snapshot cost - snapshots are typically smaller than the full volume size.
{% endhint %}

### Example

The daily cost impact for this opportunity is the average daily ESInstance cost of the instance ($8.123818) between 2023-08-09 and 2023-09-06 multiplied by the discount of downsizing the instance from m6g.4xlarge.search to m6g.2xlarge.search.'

### Record ID Explanation

ARN of OpenSearch domain, followed by a slash character and the current instance size e.g. 'arn:aws:es:eu-central-1:341922118221:domain/costopt/m6g.4xlarge.search'

### Actions You Can Take

Resize the Domain to recommended size.
