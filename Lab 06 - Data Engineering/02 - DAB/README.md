## Getting started

1. Install the Databricks CLI from https://docs.databricks.com/dev-tools/cli/databricks-cli.html

2. Authenticate to your Databricks workspace, if you have not done so already:
    ```
    $ databricks auth login https://<workspace-url>
    ```

3. To deploy a development copy of this project, type:
    ```
    $ databricks bundle deploy --target dev --profile <profile> --var target_prefix=<user_name>
    ```
    (Note that "dev" is the default target, so the `--target` parameter
    is optional here.)

    This deploys everything that's defined for this project.
    For example, the default template would deploy a job called
    `[dev yourname] apjuice_worshop_job` to your workspace.
    You can find that job by opening your workspace and clicking on **Workflows**.

4. To run a job or pipeline, use the "run" command:
   ```
   $ databricks bundle run --profile <profile> --var target_prefix=<user_name> apjuice_pipeline
   ```

5. Optionally, install developer tools such as the Databricks extension for Visual Studio Code from
   https://docs.databricks.com/dev-tools/vscode-ext.html.

6. For documentation on the Databricks asset bundles format used
   for this project, and for CI/CD configuration, see
   https://docs.databricks.com/dev-tools/bundles/index.html.
