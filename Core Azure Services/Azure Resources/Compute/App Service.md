# Azure App Service

Azure App Service enables you to build and host web apps, mobile back ends, and RESTful APIs in the programming language of your choice without managing infrastructure. It offers auto-scaling and high availability, supports both Windows and Linux, and enables automated deployments from GitHub, Azure DevOps, or any Git repo.

This platform as a service (PaaS) environment allows you to focus on the website and API logic while Azure handles the infrastructure to run and scale your web applications.

# App Service on Linux
App Service can also host web apps natively on Linux for supported application stacks. It can also run custom Linux containers (also known as Web App for Containers). App Service on Linux supports a number of language specific built-in images. Just deploy your code. Supported languages include: Node.js, Java (JRE 8 & JRE 11), PHP, Python, .NET Core, and Ruby. If the runtime your application requires is not supported in the built-in images, you can deploy it with a custom container.

# Types of app services
With App Service, you can host most common app service styles like:

Web apps
API apps
WebJobs
Mobile apps

# Advantages of app service plan
Multiple languages and frameworks
Managed production environment 
Containerization and Docker 
DevOps optimization
Global scale with high availability
Connections to SaaS platforms and on-premises data
Security and compliance
Application templates
Visual Studio and Visual Studio Code integration
API and mobile features 
Serverless code


# Limitations
App Service on Linux does have some limitations:

App Service on Linux is not supported on Shared pricing tier.
You can't mix Windows and Linux apps in the same App Service plan.
Historically, you could not mix Windows and Linux apps in the same resource group. However, all resource groups created on or after January 21, 2021 do support this scenario. Support for resource groups created before January 21, 2021 will be rolled out across Azure regions (including National cloud regions) soon.
The Azure portal shows only features that currently work for Linux apps. As features are enabled, they're activated on the portal.

# Azure App Service plans
In App Service, an app (Web Apps, API Apps, or Mobile Apps) always runs in an App Service plan. An App Service plan defines a set of compute resources for a web app to run. One or more apps can be configured to run on the same computing resources (or in the same App Service plan). 

When you create an App Service plan in a certain region (for example, West Europe), a set of compute resources is created for that plan in that region. Whatever apps you put into this App Service plan run on these compute resources as defined by your App Service plan. Each App Service plan defines:

Region (West US, East US, etc.)
Number of VM instances
Size of VM instances (Small, Medium, Large)
Pricing tier (Free, Shared, Basic, Standard, Premium, PremiumV2, PremiumV3, Isolated)

# Pricing Tier app service
The pricing tier of an App Service plan determines what App Service features you get and how much you pay for the plan. There are a few categories of pricing tiers:

Shared compute: Both Free and Shared share the resource pools of your apps with the apps of other customers. These tiers allocate CPU quotas to each app that runs on the shared resources, and the resources can't scale out.
Dedicated compute: The Basic, Standard, Premium, PremiumV2, and PremiumV3 tiers run apps on dedicated Azure VMs. Only apps in the same App Service plan share the same compute resources. The higher the tier, the more VM instances are available to you for scale-out.
Isolated: This tier runs dedicated Azure VMs on dedicated Azure Virtual Networks. It provides network isolation on top of compute isolation to your apps. It provides the maximum scale-out capabilities.
Consumption: This tier is only available to function apps. It scales the functions dynamically depending on workload.

Isolate your app into a new App Service plan when:

The app is resource-intensive.
You want to scale the app independently from the other apps the existing plan.
The app needs resource in a different geographical region.

# Use deployment slots
Whenever possible, use deployment slots when deploying a new production build. When using a Standard App Service Plan tier or better, you can deploy your app to a staging environment and then swap your staging and production slots. The swap operation warms up the necessary worker instances to match your production scale, thus eliminating downtime.

# Am I charged for apps while they are in stopped state?
Yes. Rates listed apply to apps in stopped state. Please delete apps that are not in use or update tier to Free to avoid charges.

# Which pricing tier should i use for dev\test workloads
The Shared service plan is designed for running production workloads.

# Which pricing tier should i use for production workloads
The Standard service plan is designed for running production workloads.

# How to add scalability to app service
1. You can scale up (increase RAM and Disk) (Choosing F1=>D1=>B1 pricing tier to increase or declrease scale)
2. You can scale out (Increase VM instances) (Increase\Decrease instance counts )

An Azure App Service Plan (opens new window)is pinned to a specific Azure Region. Any App Service Apps (opens new window)created in the App Service Plan will be provisioned in that same region. If your app needs additional redundancies in other regions or geographies, you'll have to:

Provision them yourself (you'll need to create new App Service Plans in those regions, if they don't already exist).
Use Azure Traffic Manager to route traffic to all available redundancies (you can only specify one App Service endpoint per region in a Traffic Manager profile). More details here (opens new window).

SLA for App Service - 99.95%