# Setting up Tag Catalog

Cloudthread allows to automate tagging of Terraform-created resources through the use of [tag-catalogs.md](../../fundamentals/tag-assistant/tag-catalogs.md "mention").

## What do I need it for? <a href="#what-do-i-need-it-for" id="what-do-i-need-it-for"></a>

{% hint style="info" %}
Adding a Tag Catalog entry allows to:

* **Make** **sure** no AWS resources without proper tags from a centrally maintained tag repository are brought up by Terraform builds
* **Change** existing tags for a new AWS resources globally
* **Track** the changes to the tag catalog
{% endhint %}

## Detailed instructions <a href="#detailed-instructions" id="detailed-instructions"></a>

1.  Proceed to the [tag-catalogs.md](../../fundamentals/tag-assistant/tag-catalogs.md "mention") tab under [tag-assistant](../../fundamentals/tag-assistant/ "mention") section in the main menu (left pane)

    ![](<../../.gitbook/assets/image (1).png>)
2.  Click 'Create New Catalog' and fill in the form

    ![](<../../.gitbook/assets/image (27).png>)
3. Click 'Create API Key for Tag Assistant' and create an API key. **Only admins can generate API keys**
4.  Add the following GitHub action yaml file `.github/workflows/tag-assistant.yml` to your repository

    ```
    name: Tag Assistant

    on:
    pull_request

    jobs:
    tag-assistant-job:
        runs-on: ubuntu-latest
        steps:
        - uses: actions/checkout@v3
        - name: Run CloudThread Tag Assistant
            uses: cloudthread/tag-assistant-action@v2
            with:
            terraform-path: TBD (optional)
            catalog-key: ${{ secrets.CLOUDTHREAD_CATALOG_KEY }}
            cloudthread-token: ${{ secrets.CLOUDTHREAD_TOKEN }}
    ```

    * `terraform-path` should be the file path for where your Terraform project lives within the repository.
5. Add the required `CLOUDTHREAD_CATALOG_KEY` and `CLOUDTHREAD_TOKEN` variables to your repository **Action Secrets** in the repository Settings page. `CLOUDTHREAD_CATALOG_KEY` should be set to the catalog key from **Step 2**, and `CLOUDTHREAD_TOKEN` set to the API Key generated in **Step 3.**
6. Ensure **Action Workflow permissions** is set to `Read and write permission` and that you enable `Allow GitHub Actions to create and approve pull requests` in the repository Settings page.
