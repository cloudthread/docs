# Setting Up Cost Allocation Rules

Cloudthread allows to create [cost-allocation-rules.md](../../fundamentals/cost-transparency/key-concepts/cost-allocation-rules.md "mention"): custom **tags** used to split costs based on certain dimensions.  based on them. This is needed for slicing the cost data and allocating the spend to the dimensions that are not provided by cloud data.

## What do I need it for? <a href="#what-do-i-need-it-for" id="what-do-i-need-it-for"></a>

{% hint style="info" %}
Adding a Tag Catalog entry allows to:

* **Slicing** the cost data
* **Allocating** the spend to [teams.md](../../fundamentals/settings/teams.md "mention")
{% endhint %}

## Detailed instructions

1. Navigate to [rule-editor.md](../../fundamentals/cost-transparency/rule-editor.md "mention") section in the menu to the left
2. Choose costs source from [#costs-source-dropdown](../../fundamentals/cost-transparency/rule-editor.md#costs-source-dropdown "mention")
3. Select the first Split Dimension from [#split-dimension-dropdown](../../fundamentals/cost-transparency/rule-editor.md#split-dimension-dropdown "mention")
4. Set the first value for the split dimension
   * By default the two-way split is created: the dimension with the value you choose (e.g. Region = us-east-1) and Other
5. Add another value for the split dimension by clicking "Add child" and choosing the value
   * Other split value stays
6. Add Rule Tags by clicking "Add rule tags" and defining new tag key and tag value
   * This is used for Custom Rule Tags definition – these tags can be used in filters across [cost-transparency](../../fundamentals/cost-transparency/ "mention") features
7. Add another split to any of the values of the split dimension, repeat 4-6
