---
description: App Section
---

# Savings Threads \[App Section]

**Savings Threads** is the section of the app where you can manage [savings-threads.md](key-concepts/savings-threads.md "mention").

<figure><img src="../../.gitbook/assets/savings-threads-section-1.png" alt=""><figcaption><p>Cloudthread Savings Threads Section</p></figcaption></figure>

## Key Features

### Create New Thread Button

Creating a new thread functionality.

### Threads Summary Card

Summary of the [savings-threads.md](key-concepts/savings-threads.md "mention") created:

* Number of threads and estimated savings by thread status (see [#optimization-context](key-concepts/savings-threads.md#optimization-context "mention"))

### Savings Threads Table

List of all the threads with the following columns:

* Thread ID
* Thread Name
* Estimated Monthly Savings
* Number of Opportunities assigned
* Status

{% hint style="info" %}
Each row in the table can be **extended** to see the list of **assigned** **opportunities**.
{% endhint %}

### Assigned Opportunities Table

List of all opportunities assigned to threads. Filtered view of the [opportunities-explorer.md](opportunities-explorer.md "mention") main table.

### Savings Thread Details Page

<figure><img src="../../.gitbook/assets/savings-threads-section-2-thread-details.png" alt=""><figcaption><p>Savings Thread Details Page</p></figcaption></figure>

By clicking on the **Thread ID** in the tables above, you will be redirected to **Savings Thread Details Page** containing detailed context on the thread. See [savings-threads.md](key-concepts/savings-threads.md "mention") for description of the context types.

#### Start Workflow Button

The button for creating a **JIRA ticket** based on the Thread. It starts the implementation workflow and changes the thread status to **Active.**

<div align="left">

<figure><img src="../../.gitbook/assets/savings-threads-section-3-thread-details-workflow.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

{% hint style="warning" %}
**JIRA integration** is required. See [#jira-integration](../settings/slack-integration.md#jira-integration "mention") for details.
{% endhint %}

#### Reject Thread Button

Rejects thread and sets its status to **Rejected**.

{% hint style="warning" %}
All the opportunities of rejected thread are getting **archived**.
{% endhint %}

#### Savings Potential Card

Total savings potential of the thread.

#### JIRA Issues Card

List of all JIRA issues associated with he thread.

#### Description Card

Details of the thread (entered at the time of thread creation).

#### Opportunities Table

List of [optimization-opportunities.md](key-concepts/optimization-opportunities.md "mention") assigned to the Thread.

#### GitHub PRs Table

List of GitHub PRs associated with the Thread.



