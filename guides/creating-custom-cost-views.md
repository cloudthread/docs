# Creating custom Cost Views

Once your AWS account is connected, Cloudthread is ready to serve you cost insights. You might want to start with exploring the absolute spend your environment has generated, and create custom [cost-view.md](../fundamentals/cost-transparency/cost-view.md "mention") using our [cost-transparency](../fundamentals/cost-transparency/ "mention") feature.

## What do I need it for?

{% hint style="info" %}
Creating custom [cost-view.md](../fundamentals/cost-transparency/cost-view.md "mention") can help you to:

* Find out answers to the questions like "How much did my **team** spend in total on **EC2** (S3, RDS, etc.) last **week** (month, quarter, etc.), and how is this spend distributed across AWS **regions** (accounts, operations, etc.)?"
* See the **trends** for your absolute cloud spend
* See the spend by **Kubernetes** namespaces, clusters, pods, labels
  * Check out [performing-k8s-cost-analysis.md](performing-k8s-cost-analysis.md "mention") guide to learn more
* See the breakdown of your costs by various dimensions to understand top spending categories
* [drill-down.md](../fundamentals/cost-transparency/drill-down.md "mention") from the Cost View into cloud spend to identify root cause of the spike in costs you see
  * Check out [performing-root-cause-analysis.md](performing-root-cause-analysis.md "mention") guide to learn more
* Set up reports and alerts for the Cost View, so that you can be notified on important changes in your cloud spend
  * Check out [setting-up-alerts-and-reports.md](setting-up-alerts-and-reports.md "mention") guide to learn more
{% endhint %}

## Detailed instructions

1. Choose [costs-overview.md](../fundamentals/cost-transparency/costs-overview.md "mention") menu item under [cost-transparency](../fundamentals/cost-transparency/ "mention") section in the menu to the left
   * You will see a page with Default View – a default Cost View representing **total spend** from added accounts, with **no** filters applied
2. Adjust **Date** filter at the top-right of the window as needed
   * By default the dates are shown for the last 7 days
3. Open **Filter** pane at the top-right of the window and add necessary filters
   * This is where you introduce all necessary conditions for absolute cloud spend filtering
   * The filter allows for 10 dimensions:
     * 6 for **AWS**: Account, Region, Service and Tag, Usage Type, Operation
     * 4 for **Kubernetes**: Cluster, Namespace, Pod, Label
       * Choosing K8s dimensions automatically applies EC2 Service filter
       * See more in [performing-k8s-cost-analysis.md](performing-k8s-cost-analysis.md "mention") guide
   * You can add filter conditions in buckets, where each bucket represents AND condition for lines of different dimensions inside, and separate buckets are connected by OR condition
   * Click "Apply" button to apply the filters
4. Check the **charts** if they represent the data you were looking for
   * Top chart shows total filtered spend for chosen period and the period of same size right before
   * Bottom chart is a "breakdown", it shows same spend by one of the six dimensions: Account, Region, Service, Usage Type, Operation and Resource
5. Click "Save as New" at top pane right near the default Cost View name
6. Put a descriptive name and click save
7. See your saved Cost View in the [cost-view-library.md](../fundamentals/cost-transparency/cost-view-library.md "mention")

<figure><img src="../.gitbook/assets/Screen Cast 2022-08-24 at 8.12.52 PM.gif" alt=""><figcaption><p>Creating a custom Cost View</p></figcaption></figure>
