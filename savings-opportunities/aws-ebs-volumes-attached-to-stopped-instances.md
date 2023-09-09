# AWS EBS Volumes Attached to Stopped Instances

## Key Features

### Source

AWS

### Service

Amazon EC2

### Difficulty

Easy

{% hint style="info" %}
**Easy**, **Medium** or **Hard**
{% endhint %}

### Type

Usage

{% hint style="info" %}
**Usage** or **Rate**
{% endhint %}

### Description

Cloudthread scans EC2 for instances older than 1 days that are in the \`stopped\` state, and gathers attached volumes.

{% hint style="info" %}
Intro blurb of what Savings Opportunity is trying to do.
{% endhint %}

## Details

### How Opportunity is Detected

Cloudthread scans EC2 for instances older than 1 days that are in the \`stopped\` state, and gathers attached volumes.

{% hint style="info" %}
Human readable description of how the Savings Opportunity is detected.
{% endhint %}

### Opportunity Threshold Metrics

* VolumeReadOps
  * Default value: 0
* VolumeWriteOps
  * Default value: 0

{% hint style="info" %}
What metrics the Savings Opportunity is referencing.
{% endhint %}

### How Estimated Monthly Savings is Calculated

The daily cost impact for this opportunity is the average daily cost of the volume ($5.029869) between 2023-08-09 and 2023-09-06 minus the cost of archiving a snapshot of the same volume size for one day ($0.894783). Note that this is an upper bound for snapshot cost - snapshots are typically smaller than the full volume size.

{% hint style="info" %}
Describe how savings is calculated. Include source or reference links.
{% endhint %}

### Example

\<aside> ℹ️ Numerical example of savings calculated.

\</aside>

XYZ

### Record ID Explanation

\<aside> ℹ️ Record ID Explanation

\</aside>

XYZ

### Actions You Can Take

Generate a snapshot of the volume, archive the generated snapshot, then delete the volume.

#### CLI code

```jsx
XYZ
```

### Other Notes

XYZ

