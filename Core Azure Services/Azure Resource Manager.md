# Azure Resource manager

# What is Azure Resource Manager?
Azure Resource Manager is the deployment and management service for Azure. It provides a management layer that enables you to create, update, and delete resources in your Azure account. You use management features, like access control, locks, and tags, to secure and organize your resources after deployment.

# Consistent Management Layer
When a user sends a request from any of the Azure tools, APIs, or SDKs, Resource Manager receives the request. It authenticates and authorizes the request. Resource Manager sends the request to the Azure service, which takes the requested action. Because all requests are handled through the same API, you see consistent results and capabilities in all the different tools.

# Resource Manager template 
A JavaScript Object Notation (JSON) file that defines one or more resources to deploy to a resource group, subscription, management group, or tenant. The template can be used to deploy the resources consistently and repeatedly. See Template deployment overview.

# Advantages
The benefits of using Resource Manager
With Resource Manager, you can:

- Manage your infrastructure through declarative templates rather than scripts.

- Deploy, manage, and monitor all the resources for your solution as a group, rather than handling these resources individually.

- Redeploy your solution throughout the development lifecycle and have confidence your resources are deployed in a consistent state.

- Define the dependencies between resources so they're deployed in the correct order.

- Apply access control to all services because Azure role-based access control (Azure RBAC) is natively integrated into the management platform.

- Apply tags to resources to logically organize all the resources in your subscription.

- Clarify your organization's billing by viewing costs for a group of resources sharing the same tag.

# Resiliency of Azure Resource Manager
The Azure Resource Manager service is designed for resiliency and continuous availability. Resource Manager and control plane operations (requests sent to management.azure.com) in the REST API are:

Distributed across regions. Some services are regional.

Distributed across Availability Zones (as well as regions) in locations that have multiple Availability Zones.

Not dependent on a single logical data center.

Never taken down for maintenance activities.