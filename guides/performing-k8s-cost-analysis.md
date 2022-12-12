# Performing K8s Cost Analysis

If you are using Kubernetes (K8s) on top of your AWS compute resources, Cloudthread's [kubernetes-dimensions.md](../fundamentals/cost-transparency/kubernetes-dimensions.md "mention") feature can help you with the container cost allocation that is essential for accurate cloud spend monitoring.

## What do I need it for? <a href="#what-do-i-need-it-for" id="what-do-i-need-it-for"></a>

{% hint style="info" %}
Using [kubernetes-dimensions.md](../fundamentals/cost-transparency/kubernetes-dimensions.md "mention") feature can help you to:

* Find out answers to the questions like "How much my team's **container** workloads cost?"
* Filter absolute AWS costs by Kubernetes **Cluster, Namespace, Pod and Label**
{% endhint %}

## Detailed instructions

1. Choose [costs-overview.md](../fundamentals/cost-transparency/costs-overview.md "mention") menu item under [cost-transparency](../fundamentals/cost-transparency/ "mention") section in the menu to the left
   * You will see a page with Default View – a default Cost View representing **total spend** from added accounts, with **no** filters applied
   * If you want to work with a a custom filtered view that was saved earlier or with the base view (predefined cost category), choose [cost-view-library.md](../fundamentals/cost-transparency/cost-view-library.md "mention") or see[creating-custom-cost-views.md](creating-custom-cost-views.md "mention") for guidance
2. Open **Filter** pane at the top-right of the window and add necessary K8s filters
   * The filter allows for 4 **Kubernetes dimensions**: Cluster, Namespace, Pod, Label
     * Choosing K8s dimensions automatically applies EC2 Service filter
     * ![](<../.gitbook/assets/Screen Shot 2022-08-24 at 8.41.28 PM.png>)
   * You can add filter conditions in buckets, where each bucket represents AND condition for lines of different dimensions inside, and separate buckets are connected by OR condition
   * Click "Apply" button to apply the filters
3. Check the **charts** if they represent the data you were looking for
   * Top chart shows total filtered spend for chosen period and the period of same size right before
   * Bottom chart is a "breakdown", it shows same spend by one of the six dimensions: Account, Region, Service, Usage Type, Operation and Resource
