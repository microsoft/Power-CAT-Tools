# Get started

The Power CAT Tools app is built using Power Platform and requires adequate licensing and capacity.

## Prerequisites

### Mandatory requirements

- A [**Power Platform environment with Dataverse as a data store**](https://learn.microsoft.com/power-platform/admin/create-environment). <br>
  Microsoft Dataverse is used to store the Power CAT Tools app configuration and test tables data. <br>
  The user performing the installation of the Power CAT Tools app must have the **system administrator** security role on the environment.
- Ensure AI Builder prompts are enabled in the admin center. [Enable AI Builder in Dataverse](https://learn.microsoft.com/en-us/ai-builder/administer).
- Adequate licensing to run a **Power Apps model-driven application**.
- Adequate licensing to run **Power Automate cloud flows** using **Premium** connectors.
  **AI Builder credits**.<br>
  This integration is useful to use AI Builder prompts to analyze an AI-generated answer and compare it with a sample answer or validation instructions. Learn more about AI Builder prompts licensing [here](https://learn.microsoft.com/ai-builder/credit-management#ai-prompt-licensing).

### Dependencies

- Power CAT Tools app is using advanced components from the Creator Kit. If you install Power CAT Tools solution manually, please make sure to deploy it before deploying Power CAT Tools app - [Creator Kit installation instructions](https://learn.microsoft.com/power-platform/guidance/creator-kit/setup)

### Connector requirements

- [Microsoft Dataverse](https://learn.microsoft.com/connectors/commondataserviceforapps/)

## Installation instructions

You can choose **either of the following options** to install **PowerCAT Tools**, based on your preference or environment setup.

### From AppSource

Refer to the [Detailed Installation Guide](INSTALLATION_GUIDE.md) for step-by-step instructions to install **PowerCAT Tools** via AppSource.

### Manual installation 

1. First install the [latest version of Creator Kit](https://github.com/microsoft/powercat-creator-kit/releases/latest) (core solution)
2. Download and install the managed solution from the desired release. We recommend installing the managed solution from the [latest release](https://github.com/microsoft/Power-CAT-Tools/releases/latest).

## Troubleshooting guide (TSG)

If you run into issues installing in an environment with the Dataverse Accelerator already installed, you can [uninstall the Dataverse Accelerator solution](https://learn.microsoft.com/power-apps/maker/data-platform/dataverse-accelerator/dataverse-accelerator#uninstall-the-dataverse-accelerator) as an immediate workaround. Please note data stored using the API playground (API Request Cache, API Request Folder) will be lost, you may export before you delete the solution if desired.
