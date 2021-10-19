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

You can also use the [Azure cli version of this tutorial](/README.md).

## 1. Set up your initial environment

1. Have an Azure account with an active subscription. [Create an account for free](https://azure.microsoft.com/free/?ref=microsoft.com&utm_source=microsoft.com&utm_medium=docs&utm_campaign=visualstudio).

Having issues? [Let us know](https://aka.ms/DjangoCLITutorialHelp).

## 2. Create Azure App Service

Please follow the doc [Quickstart: Deploy an ASP.NET web app](https://docs.microsoft.com/en-us/azure/app-service/quickstart-dotnetcore?tabs=netcore31&pivots=development-environment-vs) to create an ASP.Net web application

## 3. Create Azure Storage:
Please follow the doc [Create a storage account](https://docs.microsoft.com/en-us/azure/storage/common/storage-account-create?tabs=azure-portal) to create a storage account.

## 4. Build Connection 
Go to web app resource select Service Connector (Preview) toc:
![Select Service Connector Tab](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/toctab.jpg?raw=true)

Create connector:
![Create Step 1](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/createsc1.jpg?raw=true)

![Create Step 2](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/createsc2.jpg?raw=true)

![Create Step 3](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/createsc3.jpg?raw=true)

![Creating](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/creating.jpg?raw=true)

![Created](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/created.jpg?raw=true)

![Created Show](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/created2.jpg?raw=true)

## 5. Clone or download the sample app

Clone the sample repository:
```terminal
git clone https://github.com/LianwMS/WebAppStorageMISample.git
```
Publish the sample project
![Publish](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/publish.jpg?raw=true)

## 6. Validation
https://webappstoragemisampleportal.azurewebsites.net/
You will see "Hello Resource Connector! Current is {UTC Time Now}."
![Validate](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/validate.jpg?raw=true)

