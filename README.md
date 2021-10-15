---
title: 'Tutorial: Deploy a Web Application Connected to Azure Storage Blob with Service Connector'
description: .
ms.devlang: .Net
author: shizn
ms.author: xshi
ms.service: service-connector
ms.topic: tutorial
ms.date: 10/28/2021
zone_pivot_groups: 
---
# Tutorial: Deploy a Web Application Connected to Azure Storage Blob with Service Connector

::: zone pivot=""

This tutorial shows .

In this tutorial, you use the Azure CLI to complete the following tasks:

> [!div class="checklist"]
> * Set up


You can also use the [Azure portal version of this tutorial](/azure/developer/python/tutorial-python-postgresql-app-portal?pivots=postgres-single-server).

:::zone-end

## 1. Set up your initial environment

1. Have an Azure account with an active subscription. [Create an account for free](https://azure.microsoft.com/free/?ref=microsoft.com&utm_source=microsoft.com&utm_medium=docs&utm_campaign=visualstudio).
2. Install the <a href="/cli/azure/install-azure-cli" target="_blank">Azure CLI</a> 2.18.0 or higher, with which you run commands in any shell to provision and configure Azure resources.

---

Check that your Azure CLI version is 2.18.0 or higher:

```azurecli
az --version
```

If you need to upgrade, try the `az upgrade` command (requires version 2.11+) or see <a href="/cli/azure/install-azure-cli" target="_blank">Install the Azure CLI</a>.

Then sign in to Azure through the CLI:

```azurecli
az login
```

This command opens a browser to gather your credentials. When the command finishes, it shows JSON output containing information about your subscriptions.

Once signed in, you can run Azure commands with the Azure CLI to work with resources in your subscription.

Having issues? [Let us know](https://aka.ms/DjangoCLITutorialHelp).

## 2. Clone or download the sample app

# [Git clone](#tab/clone)

Clone the sample repository:
```terminal
git clone https://github.com/LianwMS/WebAppStorageMISample.git
```

## 3. Create App Service 
Go to the root folder of repository:
```terminal
cd WebAppStorageMISample
```

Create the webapp use webapp up:
```terminal
az webapp up --name WebAPPStorageMISample --sku B1 --location eastus
```

## 4. Create Azure Storage
```terminal
az storage account create --name storageforwebappsample --resource-group {rg_name} --sku Standard_RAGRS --https-only
```

## 5. Build Connection
```terminal
az webapp connection create storage-blob -g {rg_name} -n WebAPPStorageMISample --tg {rg_name} --account storageforwebappsample --system-identity
```

## 6. Validation
https://webappstoragemisample.azurewebsites.net/
You will see "Hello Resource Connector! Current is {UTC Time Now}."

