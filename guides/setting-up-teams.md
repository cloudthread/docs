# Setting up Teams

Cloudthread platform allows to assign users to [teams.md](../fundamentals/settings/teams.md "mention") that have **global filters** enabled, i.e. every user belonging to the Team can see all the data filtered without an ability to remove the filtering.

This feature allows to restrict the access to the sensitive data across the complex organizational structure.

{% hint style="warning" %}
You have be an **Admin** in order to set up Teams. See [teams.md](../fundamentals/settings/teams.md "mention") for more details on the functionality.
{% endhint %}

## What do I need it for? <a href="#what-do-i-need-it-for" id="what-do-i-need-it-for"></a>

{% hint style="info" %}
Setting up teams allows to:

* **Restrict** the access of the certain group of users to the data that is relevant only to them
* **Manage** alerting and reporting at Team level, with dedicated Slack channel
* Assign Custom [cost-columns.md](../fundamentals/settings/cost-columns.md "mention") to the Team
{% endhint %}

## Detailed instructions <a href="#detailed-instructions" id="detailed-instructions"></a>

1. Go to [settings](../fundamentals/settings/ "mention") section from the left menu pane
2. Choose [teams.md](../fundamentals/settings/teams.md "mention") tab
3. Fill in Team Name, Slack Channel and Cost Columns (if present)
4. Set up the **global team filter**
   * This filter will appear in [cost-view-library.md](../fundamentals/cost-transparency/cost-view-library.md "mention") under Team Global Filters section, it can be edited in the same as [cost-view.md](../fundamentals/cost-transparency/cost-view.md "mention") are
5. Click "Save Team"
6. See the team appear in the table in Settings and in the Admin Team Assumption drop-down at the left menu pane
7. Add [cost-view.md](../fundamentals/cost-transparency/cost-view.md "mention") to the newly created team from the table in the Settings as necessary
   * These Cost Views will be available for the team with the global filter applied on top (in addition to any existing filters)
   * By default, the Team members have no previously created custom Cost Views available to them
8. Assume the created team through the drop-down at the left menu pane to check if everything was set up correctly

<figure><img src="../.gitbook/assets/managing-team-access_demo.gif" alt=""><figcaption><p>Setting up Team Access</p></figcaption></figure>
