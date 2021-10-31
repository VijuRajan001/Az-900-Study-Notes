# Resource Group
A logical groups of resources—such as VMs, storage volumes, IP addresses, network interfaces, etc.You decide how you want to allocate resources to Azure resource groups based on what makes the most sense for your organization, but as a best practice, we suggest assigning resources with a similar lifecycle to the same Azure resource group, so you can easily deploy, update, and delete them as a group.

The resource group collects metadata from each individual resource to facilitate more granular management than at the subscription level. 

To Create a resource group below details are required

Subscription: Choose your subscription
Resource group: Enter a valid name for the Resource group
Region: Choose a region for the Resource group


## Advantages 
- easier to apply access controls
- monitor activity
- track the costs related to specific workloads

## How Azure resource groups benefit administration and cost management
Using Azure resource groups enables users to deploy resources using declarative templates (using Azure Resource Manager templates), rather than scripts.  Azure Resource Manager orchestrates the deployment of interdependent resources so they are created in the correct order.

 It's possible to assign a cost allocation tag to the resource group, and the costs of running the resources within the whole group will be accounted for together for cost management purposes.

 ## Applying role-based access controls to a resource group in Azure

 Applying role-based access controls (RBACs) to a resource group in Azure enables organizations to manage who has access to Azure resources, what they can do with those resources, and what areas they have access to.

In regards to cloud security and governance, RBACs help businesses adhere to the principle of least privilege. Users, processes, applications, and devices can be given the minimum permissions required at the resource group level, rather than at the management group or subscription levels.

# Do Azure resource groups cost money?
The answer to this question is absolute No, There is no price for the Resource Group. You need to pay for the resources as per the pricing model. So you need to pay for the resources, not for the Resource Groups.

# How many Resource Groups can a resource be added?
Each resource can only exist in one resource group. If one resource needs to exist on a different deployment cycle it should be in another resource group.

# How do I restore a resource group in Azure?
Remember that, there is no direct way to restore a deleted resource group. Deleting a resource group is an irreversible action. Two workarounds you can try, in order to get back

You can try raising a ticket to Microsoft to restore it back.
We can also try to find the deployment template for the resources that we created earlier in our deleted resource group and then we can use the same template while creating a new one.

# Properties

In most cases, a child resource can't be moved independently from its parent resource. Child resources have a resource type in the format of <resource-provider-namespace>/<parent-resource>/<child-resource>. For example, Microsoft.ServiceBus/namespaces/queues is a child resource of Microsoft.ServiceBus/namespaces. When you move the parent resource, the child resource is automatically moved with it. 

Not all resources can be moved to different resource groups. refer [Move Operation support](https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/move-support-resources)

The resources you include in a resource group can be located in different Azure regions, even in different regions than the group itself. However, sometimes, it is a best practice to keep all resources in a resource group in the same region to reduce latency or cross-region data transfer. Regardless, the group needs a location to specify where the metadata will be stored, which is necessary for some compliance policies. 

When a resource group is deleted, all resources in the group are deleted 

Group limits: you can deploy up to 800 instances of a resource type in each resource group – with [some exceptions](https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/resources-without-resource-group-limit).


