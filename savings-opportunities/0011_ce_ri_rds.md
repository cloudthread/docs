# Cost Explorer RDS Rerserved Instance

{% hint style="success" %}
See [optimization-opportunities.md](../fundamentals/cost-savings/key-concepts/optimization-opportunities.md "mention") for more details on the concept.
{% endhint %}

## Key Metadata

### Source: `Cost Explorer`

### Service: `Amazon Relational Database Service`

### Difficulty: `Easy`

{% hint style="info" %}
**Easy:** Zero downtime, zero performance risks

**Medium:** Zero downtime, potential performance trade-offs

**Hard:** Downtime required, potential performance trade-offs
{% endhint %}

### Type: `Rate`

{% hint style="info" %}
**Usage:** Actions altering actual cloud resources (e.g. changing VM specs, storage retention policies, removing unused resources)

**Rate:** Actions targeting financial concepts, mainly commitment-based discounts (e.g. [Reserved Instances](https://aws.amazon.com/ec2/pricing/reserved-instances/) and [Savings Plans](https://aws.amazon.com/savingsplans/) for AWS, [Committed Use Discounts](https://cloud.google.com/compute/docs/instances/signing-up-committed-use-discounts) for GCP)

**Custom:** Ad-hoc opportunities for custom tracking needs. See [creating-custom-optimization-opportunities.md](../guides/optimizing-cloud-costs/creating-custom-optimization-opportunities.md "mention") for more details.
{% endhint %}

## Details

### How Opportunity is Detected

Cloudthread uses the AWS Cost Explorer API to get suggestions for purchasing reserved instances.

### How Estimated Monthly Savings is Calculated

The cost impact for this opportunity is estimated by Cost Explorer. Please be aware this is amortized over the life of the reservation.

### Example

The daily cost impact for this opportunity if you purchase the recommended reservation ($7.801429), divided by 30. Please be aware this is amortized over the life of the reservation.

### Record ID Explanation

Composed of the following fields (separated by colon symbol `:`):
 - opportunity type, fixed value: `0011_ce_ri_rds`
 - account ID, e.g. `123456789012`
 - region, e.g. `us-east-1`
 - database engine, e.g. `PostgreSQL`
 - database edition, e.g. ``
 - deployment option, e.g. `Single-AZ`
 - database instance type, e.g. `db.m4.large`
 - license model, e.g. `No license required`
 - is current generation, e.g. `True` 
 - is size flexible, e.g. `False`
that are followed by a slash symbol `/` and the reservation options that you can choose in the Cloudthread Savings Hub UI (separated by colon symbol `:`):
 - payment option, e.g. `ALL_UPFRONT`
 - term, e.g. `THREE_YEARS`

The example record id would then be as follows:
`0011_ce_ri_rds/123456789012:us-east-1:PostgreSQL::Single-AZ:db.m4.large:No license required:False:True/ALL_UPFRONT:THREE_YEARS`

### Actions You Can Take

Purchase the recommended reservation.
