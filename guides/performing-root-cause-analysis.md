# Performing Root Cause Analysis

Root Cause Analysis (RCA)​ is an important part of dealing with cloud costs: identifying the reason of cost spikes efficiently is essential. Cloudthread's [drill-down.md](../fundamentals/drill-down.md "mention") feature empowers you to do it with the depth of AWS resource level.

## What do I need it for? <a href="#what-do-i-need-it-for" id="what-do-i-need-it-for"></a>

{% hint style="info" %}
Using [drill-down.md](../fundamentals/drill-down.md "mention") feature for RCA can help you to:

* Find out answers to the questions like "Which AWS **resource** is behind the increase in cost of my **team's** cloud infrastructure?"
* See the **breakdown** of specific parts of you spend by Account, Region, Service,, Usage Type, Operation and Resource.
{% endhint %}

## Detailed instructions <a href="#detailed-instructions" id="detailed-instructions"></a>

1. Choose Costs Transparency section in the menu to the right, then choose Cost Overview item
   * You will see a page with Total Cost View – a default Cost View representing all the spend from added accounts, will no filters applied
2. Choose the saved Cost View from the list or create a new one (see[creating-custom-cost-views.md](creating-custom-cost-views.md "mention") for guidance)
3. Move to the second chart on page – **Breakdown Chart** and navigate to table below the chart
   * The table shows the items visualized on breakdown chart
4. Hover over the table row you want to drill-down into and click the drill-down button (arrow down)
   * You will see table and chart change to show the items on the next level of drill-down contributing to the item you chose
   * The drill-down level sequence we currently support: Account -> Region -> Service -> Usage Type -> Operation -> Resource
   * Usage Type -> Operation -> Resource levels are available starting from Service )i.e. you cannot drill down to resource right from Account level)
5. Once you are in drill-down mode, you can see the level you are at on the control line above the table
   * You can change levels from the control line as you go
   * Going level back is also done through control line by deleting the latest level

![](<../.gitbook/assets/Screen Cast 2022-05-03 at 2.25.34 PM (1).gif>)
