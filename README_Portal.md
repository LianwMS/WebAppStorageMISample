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

![Create Resource Group](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/createrg.jpg?raw=true)

## 3. Create Azure App Service

Create App Service Plan:
Go to resource group and +Create->App Service Plan
![Create Web App Plan](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/createwebappplan.jpg?raw=true)

Create App Service:
Go to resource group and +Create->Web App
![Create Web App](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/createwebapp.jpg?raw=true)


## 4. Create Azure Storage:
Go to resource group and +Create->Storage account
![Create Storage Account](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/createsa.jpg?raw=true)

## 5. Build Connection 
Go to web app resource select Service Connector (Preview) toc:
![Select Service Connector Tab](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/toctab.jpg?raw=true)

Create connector:
![Create Step 1](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/createsc1.jpg?raw=true)

![Create Step 2](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/createsc2.jpg?raw=true)

![Create Step 3](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/createsc3.jpg?raw=true)

![Creating](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/creating.jpg?raw=true)

![Created](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/created.jpg?raw=true)

![Created Show](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/created2.jpg?raw=true)

## 6. Clone or download the sample app

Clone the sample repository:
```terminal
git clone https://github.com/LianwMS/WebAppStorageMISample.git
```
Publish the sample project
![Publish](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/publish.jpg?raw=true)

## 7. Validation
https://webappstoragemisampleportal.azurewebsites.net/
You will see "Hello Resource Connector! Current is {UTC Time Now}."
![Validate](https://github.com/LianwMS/WebAppStorageMISample/blob/main/img/validate.jpg?raw=true)

