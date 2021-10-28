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
# Tutorial: Deploy an ASP.Net Web Application Connected to Azure Storage Blob with Service Connector

In this tutorial, you use the Azure portal to complete the following tasks:
* Create an ASP.Net App application.
* Create a storage account and an Azure Blob Storage container.
* Deploy code to Azure App Service and connect to storage with managed identity using Service Connector in Azure Portal.

You can also use the [Azure CLI version of this tutorial](/README.md).

## 1. Set up your initial environment

1. Have an Azure account with an active subscription. [Create an account for free](https://azure.microsoft.com/free/?ref=microsoft.com&utm_source=microsoft.com&utm_medium=docs&utm_campaign=visualstudio).

Having issues? [Let us know](https://aka.ms/DjangoCLITutorialHelp).

## 2. Create Azure App Service

Please follow the doc [Quickstart: Deploy an ASP.NET web app](https://docs.microsoft.com/en-us/azure/app-service/quickstart-dotnetcore?tabs=netcore31&pivots=development-environment-vs) to create an ASP.Net web application

## 3. Create Azure Storage:
Please follow the doc [Create a storage account](https://docs.microsoft.com/en-us/azure/storage/common/storage-account-create?tabs=azure-portal) to create a storage account.

## 4. Build Connection 
Go to web app resource select "Service Connector (Preview)" tab, and Click "Create" button.
![Select Service Connector Tab](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/toctab.jpg?raw=true)

Select the target resource details including storage subscription, resource type, storage account and client type as following. Click "Next: Authentication"
![Create Step 1](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/createsc1.jpg?raw=true)

In Authentication tab select "System assigned managed identity" and click "Next: Review + Create"
![Create Step 2](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/createsc2.jpg?raw=true)

After review the configure, click "Create"
![Create Step 3](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/createsc3.jpg?raw=true)

In Notifications tab, it will show that the creation start.
![Creating](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/creating.jpg?raw=true)

After creation started, we can find the connection descriptions "Service Connector (Preview)" tab.
![Created](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/created.jpg?raw=true)

## 5. Clone or download the sample app and publish

Clone the sample repository:
```terminal
git clone https://github.com/LianwMS/WebAppStorageMISample.git
```
Open WebStorageSample.csproj with Visual Studio 2019 and Publish the sample project by visual studio [Publish your web app](https://docs.microsoft.com/en-us/azure/app-service/quickstart-dotnetcore?tabs=netcore31&pivots=development-environment-vs#publish-your-web-app)
![Publish](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/publish.jpg?raw=true)

## 6. Validation
Click the URL in Overview tab from the Web App portal.
![WebApp](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/webapp.jpg?raw=true)
You will see "Hello Service Connector! UTC Now: {UTC Time Now}."
![Validate](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/validate.jpg?raw=true)

