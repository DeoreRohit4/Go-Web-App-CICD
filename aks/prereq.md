## Prerequisites

### kubectl
**Description:** A command-line tool for working with Kubernetes clusters.  
**More Information:** For installation or updating instructions, see [Installing or updating kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/).

### Azure CLI
**Description:** A command-line tool for managing Azure resources, including AKS clusters.  
**More Information:** For installation, updating, and configuration instructions, see [Install the Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli).

**Configuration:** After installing the Azure CLI, log in and configure it with the following commands:

```bash
az login
az account set --subscription "your-subscription-id"
```

## Azure AKS CLI
**Description:** A command-line tool extension for managing AKS clusters specifically, part of the Azure CLI.
**More Information:** The Azure AKS CLI is included in the Azure CLI by default. 
You can update it with:

```bash
az extension add --name aks-preview
az extension update --name aks-preview
```