## Install an AKS Cluster
**Create a resource group:**
```bash
az group create --name gowebrg --location eastus
```
This command creates a resource group named "gowebrg" in the "eastus" region.

## Create an AKS cluster:

```bash
az aks create --resource-group gowebrg --name gowebcluster --node-count 1 --enable-addons monitoring --generate-ssh-keys
```
This command creates an AKS cluster named `gowebcluster` in the `gowebrg` resource group with one node and enables monitoring. 
The `--generate-ssh-keys` option generates SSH keys if you don't already have them.