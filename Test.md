---
title: Tutorial - App Containerization and Migration with Azure Migrate
description: In this tutorial, you learn how to containerize and migrate ASP.Net and Java web apps to Azure Kubernetes Service and Azure App Service.
author: rahugup
manager: bsiva
ms.topic: tutorial
ms.date: 08/04/2021
---

# Tutorial: App Containerization using Azure Migrate

In this article, you'll learn how to containerize ASP.Net and Java web applications (running on Apache Tomcat) and migrate them to [Azure Kubernetes Service (AKS)](https://azure.microsoft.com/services/kubernetes-service/) and [Azure App Service](https://azure.microsoft.com/services/app-service/) using the Azure Migrate: App Containerization tool.

The Azure Migrate: App Containerization tool helps you to -

- **Discover your application**: The tool remotely connects to the application servers running your Java web application (running on Apache Tomcat) and discovers the application components. The tool creates a Dockerfile that can be used to create a container image for the application.
- **Build the container image**: You can inspect and further customize the Dockerfile as per your application requirements and use that to build your application container image. The application container image is pushed to an Azure Container Registry you specify.
- **Deploy to Azure Kubernetes Service**:  The tool generates the Kubernetes resource definition YAML files needed to deploy the containerized application to your Azure Kubernetes Service cluster. You can customize the YAML files and use them to deploy the application on AKS.
- **Deploy to Azure App Service**:  The tool generates the deployment files needed to deploy the containerized application to Azure App Service.

> [!NOTE]
>  The Azure Migrate: App Containerization tool helps you discover specific application types (ASP.NET and Java web apps on Apache Tomcat) and their components on an application server. To discover servers and the inventory of apps, roles, and features running on on-premises machines, use Azure Migrate: Discovery and assessment capability. [Learn more](./tutorial-discover-vmware.md)

While all applications won't benefit from a straight shift to containers without significant rearchitecting, some of the benefits of moving existing apps to containers without rewriting include:

- **Improved infrastructure utilization:** With containers, multiple applications can share resources and be hosted on the same infrastructure. This can help you consolidate infrastructure and improve utilization.
- **Simplified management:** By hosting your applications on a modern managed platform like AKS and App Service, you can simplify your management practices. You can achieve this by retiring or reducing the infrastructure maintenance and management processes that you'd traditionally perform with owned infrastructure.
- **Application portability:** With increased adoption and standardization of container specification formats and platforms, application portability is no longer a concern.
- **Adopt modern management with DevOps:** Helps you adopt and standardize on modern practices for management and security and transition to DevOps.

The Azure Migrate: App Containerization tool currently supports -

- Containerizing ASP.NET apps and Java web apps deploying them on Windows containers on Azure Kubernetes Service. [Learn more](./tutorial-app-containerization-aspnet-kubernetes.md)
- Containerizing ASP.NET apps and Java web apps deploying them on Windows containers on Azure App Service. [Learn more](./tutorial-app-containerization-aspnet-app-service.md)
