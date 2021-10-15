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


You can also use the [Azure cli version of this tutorial](/README.md).

:::zone-end

## 1. Set up your initial environment

1. Have an Azure account with an active subscription. [Create an account for free](https://azure.microsoft.com/free/?ref=microsoft.com&utm_source=microsoft.com&utm_medium=docs&utm_campaign=visualstudio).

Having issues? [Let us know](https://aka.ms/DjangoCLITutorialHelp).

## 2. Create a Resource Group

[/img/createrg.jpg]

## 3. Create Azure App Service

Create App Service Plan:
Go to resource group and +Create->App Service Plan
[/img/createwebappplan.jpg]

Create App Service:
Go to resource group and +Create->Web App
[/img/createwebapp.jpg]

## 4. Create Azure Storage:
Go to resource group and +Create->Storage account
[/img/createsa.jpg]

## 5. Build Connection 
Go to web app resource select Service Connector (Preview) toc:
[/img/toctab.jpg]

Create connector:
[/img/create1.jpg]

[/img/create2.jpg]

[/img/create3.jpg]

[/img/creating.jpg]

[/img/created.jpg]

[/img/created2.jpg]

## 6. Clone or download the sample app

Clone the sample repository:
```terminal
git clone https://github.com/LianwMS/WebAppStorageMISample.git
```
Publish the sample project
[/img/publish.jpg]

## 7. Validation
https://webappstoragemisampleportal.azurewebsites.net/
You will see "Hello Resource Connector! Current is {UTC Time Now}."
[/img/validate.jpg]

