# Tag Catalogs

**Tag Catalogs** is a section of an app that covers **tagging automation** functionality Cloudthread provides.

It represents the setup interface for **Tag Catalog** creation and maintenance.

{% hint style="warning" %}
Tag Automation currently is supporting on **GitHub** and **Terraform** based Infrastructure as a Code (IaaC) environments.
{% endhint %}

Connected to GitHub repository through [GitHub Actions](https://docs.github.com/en/actions), Tag Catalog allows to make sure all the Terraform builds in the repository get the tags outlined in the catalog. This allows to maintain consistent tagging and control it from a single place.

GitHub Actions should be set up for the repo with a Cloudthread  **API Key** and **Actions Variable** matching the **Tag Catalog Key.** Based on the connection between GitHub and Cloudthread established this way, the tags from the catalog are getting propagated to the `.tf` build files in the repository: every time the action is run a PR adding new tags is created.

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

### Key Features

* #### [#tag-catalogs-control-pane](tag-catalogs.md#tag-catalogs-control-pane "mention")
* #### [#tag-catalogs-table](tag-catalogs.md#tag-catalogs-table "mention")

#### Tag Catalogs Control Pane

The pane at the top of the page that includes major Tag Catalog actions:

* Adding new Tag Catalog
  * This creates a new tag catalog
  * The idea is that one tag catalog covers one repository, so that different repositories can be getting different tags
* Adding new API key
  * This is needed for connecting Cloudthread to GitHub repository
* Synchronizing tags
  * This grabs your current active cost allocation tags from Cost Explorer and retrieves values from the last 7 days. 
  * These keys and values are available for tag catalog entries.
  * **If you want to add a new key to a tag catalog, you must first add it as a cost allocation tag in AWS.**

#### Tag Catalogs Table

This is the table containing tag Catalogs. It allows to set the tag key-value pairs within the Tag Catalog, saving the catalog state and resetting the Catalog.
