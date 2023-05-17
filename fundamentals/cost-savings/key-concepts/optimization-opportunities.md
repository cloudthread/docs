# Optimization Opportunities

**Optimization Opportunity** is a concrete **recommendation** on the **cost optimization action** for a **specific** cloud **resource** (or group of resources for Rate Optimization).

It is a key concept of [..](../ "mention") functionality Cloudthread platform provides, and is a building block for [savings-threads.md](savings-threads.md "mention").

Cloudthread **automatically** discovers and surfaces Optimization Opportunities in [opportunities-explorer.md](../opportunities-explorer.md "mention") app section by scanning your cloud environments. In order to setup the discovery engine, you need to go through [onboarding](../../../guides/onboarding/ "mention") stage.

Cloudthread also support creation of **custom** opportunities for ad-hoc optimization needs. Refer to [creating-custom-optimization-opportunities.md](../../../guides/optimizing-cloud-costs/creating-custom-optimization-opportunities.md "mention") for more details.

{% hint style="success" %}
See [#supported-opportunities](optimization-opportunities.md#supported-opportunities "mention") for the list of recommendations Cloudthread currently supports.
{% endhint %}

## Key Features

Optimization Opportunity represents a **collection of datapoints** aimed at **analysis** and **implementation** support of **cost optimization action** targeted at **specific** cloud **resource** or **group or resources**.&#x20;

Below are the major types of insights Optimization Opportunity contains.

### **Optimization context**

Baseline features of optimization.

#### Optimization type

Optimization **type** defines the nature of the cost savings recommendation. Different recommendation types have different representation on Cloudthread platform and are targeted at different use cases and stakeholders.&#x20;

{% hint style="info" %}
Cloudthread currently supports **3 major types** of Optimization Opportunities:

**Usage** Opportunities

* Actions altering actual cloud resources (e.g. changing VM specs, storage retention policies, removing unused resources)

**Rate** Opportunities

* Actions targeting financial concepts, mainly commitment-based discounts (e.g. [Reserved Instances](https://aws.amazon.com/ec2/pricing/reserved-instances/) and [Savings Plans](https://aws.amazon.com/savingsplans/) for AWS, [Committed Use Discounts](https://cloud.google.com/compute/docs/instances/signing-up-committed-use-discounts) for GCP)

**Custom** Opportunities

* Ad-hoc opportunities for custom tracking needs. See [creating-custom-optimization-opportunities.md](../../../guides/optimizing-cloud-costs/creating-custom-optimization-opportunities.md "mention") for more details.
{% endhint %}

#### Estimated savings

An estimated financial impact of acting on opportunity recommendation. Can be Daily, Monthly, Quarterly and Yearly.

#### Difficulty

Estimated difficulty of opportunity recommendation implementation. Considers potential **downtime** and **performance** risks.

{% hint style="info" %}
Cloudthread Optimization Opportunities have **3 levels** of difficulty:

* **Easy**
  * Zero downtime, zero performance risks
* **Medium**
  * Zero downtime, potential performance trade-offs
* **Hard**
  * Potential downtime, potential performance trade-offs
{% endhint %}

### **Resource context**

Key dimensions if the cloud resource covered by the recommendation.

* ResourceID
* Cloud provider
* Account (Project)
* Region
* Service

{% hint style="warning" %}
For opportunities of **Rate** [#optimization-type](optimization-opportunities.md#optimization-type "mention") ResourceID is not available as the concept of usage-based discount is not tied to a specific VM, but rather to the type of resource.
{% endhint %}

### **Workflow context**

Data on the state of opportunity in the implementation process.

* **Opportunity status**
  * Open
  * Archived
  * Done
* Existing [savings-threads.md](savings-threads.md "mention") containing the opportunity
* **Open JIRA tickets** addressing the opportunity

### **Visual context**

Charts with metrics for recommendation analysis.

* **Resource utilization**
  * Max CPU
  * Memory
  * Network
  * Throughput
  * DB connections
  * Etc. – depends on the type of opportunity
* **Resource cost**
  * Cost of resource over time (incl. cumulative)

### **Recommendation context**

Detailed description of the recommended actions.

* **Text description with concrete steps**
* **Links to guides/materials**

### **Risk context**

Description of risks connected with oportunity implementation.

* **Risk description**
* **Mitigation recommendations**&#x20;
  * E.g. backup

### **Implementation support context**

Code snippets or automation setup.

* **Code snippets for Terraform**
* **Code snippets for CLI**
* **Opt-in automation if applicable**

## Supported Opportunities

{% hint style="success" %}
The list below is **live** and updates dynamically as we are implementing new opportunities.

If you are not seeing something that is **important** for you, please let us know [here](https://www.cloudthread.io/contact-us).
{% endhint %}

{% embed url="https://docs.google.com/spreadsheets/d/1idSzjpVyMLdWQDtbhFkgkZyTdHvXyJ4m4dIPpRTSu6I/edit?usp=sharing" fullWidth="true" %}
Cloudthread Optimization Opportunities
{% endembed %}

{% hint style="info" %}
The spreadsheet above can be accessed [here](https://docs.google.com/spreadsheets/d/1idSzjpVyMLdWQDtbhFkgkZyTdHvXyJ4m4dIPpRTSu6I/edit?usp=sharing).
{% endhint %}
