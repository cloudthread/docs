# Compute Optimizer EC2 Rightsizing

{% hint style="success" %}
See [optimization-opportunities.md](../fundamentals/cost-savings/key-concepts/optimization-opportunities.md "mention") for more details on the concept.
{% endhint %}

## Key Metadata

### Source: `AWS Compute Optimizer`

### Service: `Amazon EC2`

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

Cloudthread uses the AWS Compute Optimizer API to find instances that are overprovisioned.

### How Estimated Monthly Savings is Calculated

The cost impact for this opportunity is the Compute Optimizer estimated monthly savings for downsizing the instance.

### Example

Compute Opmimizer estimated monthly savings for downsizing this instance is $100.00.

### Record ID Explanation

An ID of EC2 instance, e.g. `i-04223c86f3f149f21`

### Actions You Can Take

Resize the instance to recommended size.
