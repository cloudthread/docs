# AWS EBS Volumes Attached to Stopped Instances

{% hint style="success" %}
See [optimization-opportunities.md](../fundamentals/cost-savings/key-concepts/optimization-opportunities.md "mention") for more details on the concept.
{% endhint %}

## Key Metadata

### Source: `AWS`

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

Cloudthread scans EC2 for instances older than 1 days that are in the \`stopped\` state, and gathers attached volumes.

### Opportunity Threshold Metrics

* VolumeReadOps
  * **Default value:** `0`
* VolumeWriteOps
  * **Default value:** `0`

{% hint style="info" %}
What metrics the Savings Opportunity is referencing.
{% endhint %}

### How Estimated Monthly Savings is Calculated

The daily cost impact for this opportunity is the `average daily cost of the volume` ($) between `period start date` and `period end date` minus the `cost of archiving a snapshot` of the same volume size for one day ($).&#x20;

{% hint style="warning" %}
Note that this is an **upper bound** for snapshot cost - snapshots are typically smaller than the full volume size.
{% endhint %}

### Example

The daily cost impact for this opportunity is the average daily cost of the volume ($5.029869) between 2023-08-09 and 2023-09-06 minus the cost of archiving a snapshot of the same volume size for one day ($0.894783). Note that this is an upper bound for snapshot cost - snapshots are typically smaller than the full volume size.

### Record ID Explanation

An ID of EBS volume, e.g. `vol-0c2aecd978c03dd7a`

### Actions You Can Take

Generate a snapshot of the volume, archive the generated snapshot, then delete the volume.

#### CLI code

```jsx
XYZ
```

### Other Notes

XYZ

