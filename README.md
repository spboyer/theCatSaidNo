# GitHub to Cloud in Minutes with the Azure Developer CLI

Building applications that use multiple cloud services, connecting them all together in a secure way, and setting up a CI/CI pipeline can be a confusing and daunting task. Not to mention a time consuming one with many options. Learn how you can use the Microsoft Azure Developer CLI and the associated code templates to quickly get these types of applications up and running in cloud in minutes; build upon them and templatize your own ideas to do the same.

## Prerequisites

1. Azure Account
    - Sign up for [FREE](https://azure.microsoft.com/free/?WT.mc_id=A261C142F). You also need [contributor role assigned](https://learn.microsoft.com/en-us/azure/role-based-access-control/role-assignments-portal) to your Azure subscription.
2. Install [azd](https://aka.ms/azd-install)

### Resources

- Documentation: <https://aka.ms/azure-dev/devhub>
- Source Repo: <https://github.com/azure/azure-dev>

## Quickstart

Create a new directory.

`mkdir gh-universe`.

Next, change directories,

`cd gh-universe` and run the following command:

 ```bash
 azd up -t spboyer/thecatsaidno
 ```

 The command clones the template, creates the infrastructure and publishes the application code to Azure.

 You will be promted for:

- The name to use for this environment. This should be descriptive enough to identify the project and stage i.e. **thecatsaidno-dev** or **workshop-catpaw** etc.
- Azure subscription to use
- Location (eastus, westus, etc) to deploy the application to.

The output provides the url to browse to for the published application.

## Step by Step

Create a new directory.

`mkdir gh-universe`.

Next, change directories,

`cd gh-universe` and run the following command:

 ```bash
 azd init -t spboyer/thecatsaidno
 ```

 The sample template code is cloned to the current directory.

 Next, provision the infrastructure for the application in Azure using the `provision` command.

 ```bash
 azd provision
 ```

 *** Answer prompts for environment name, subscription, and geographical location.

 Once complete, use the `deploy` command to publish the application code to Azure.

 ```bash
azd deploy
 ```

 The output provides the url to browse to for the published application.
