# RDS Righsizing

{% hint style="success" %}
See [optimization-opportunities.md](../fundamentals/cost-savings/key-concepts/optimization-opportunities.md "mention") for more details on the concept.
{% endhint %}

## Key Metadata

### Source: `AWS`

### Service: `Amazon RDS`

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

Cloudthread scans RDS for instances eligible for downsizing based on CPU utilization maximum days below adjustable threshold and freeable memory minimum being above respective adjustable threshold.'

### Opportunity Threshold Metrics

* CPUUtilization
  * **Default value:** `40%`
* FreeableMemory
  * **Default value:** `60%`

{% hint style="info" %}
What metrics the Savings Opportunity is referencing.
{% endhint %}

### How Estimated Monthly Savings is Calculated

Cost impact for this opportunity is the average daily InstanceUsage cost of the instance multiplied by the discount of downsizing the instance. The discount is ratio of the recommended instance size cost to the current instance size cost.

### Example

The daily cost impact for this opportunity is the average daily InstanceUsage cost of the instance ($12.313171) between 2023-08-18 and 2023-09-15 multiplied by the discount of downsizing the instance from db.t3.2xlarge to db.t3.xlarge.

### Record ID Explanation

An ARN of RDS database followed by a slash characer and the current database instance type, e.g. `arn:aws:rds:us-west-2:101311352144:db:lama-dev/db.t3.2xlarge`

### Actions You Can Take

Downsize the instance to recommended size.
