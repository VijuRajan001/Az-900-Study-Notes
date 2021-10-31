# Management Groups

An Azure Management group is logical containers that allow Azure Administrators to manage access, policy, and compliance across multiple Azure Subscriptions en masse. Management groups allow you to build an Azure Subscription tree that can be used with several other Azure service, including Azure Policy and Azure Role Based Access Control. Azure Management Groups provide flexibility for organizing policy, access control, and compliance across multiple subscriptions. We can nest Azure Management Groups up to six levels deep for efficient management of resources.

# Effective use of management groups
Among the multiple ways management groups can be utilized, Azure Management Groups can mirror your billing hierarchy. Often enterprises begin utilizing management groups in this method. However, the power of management groups is when you use them to model your organization. Azure Subscriptions can be grouped based on a need for common roles assigned along with Azure Policies and initiatives.

# Properties
All subscription objects within a management group receives a copy of the role-based access control and policy settings applied to the management group. 

# Azure Active Directory and Management Groups
Each Azure Active Directory (AD) tenant includes a top level or “root” management group. By default, only an Azure AD Global Administrator can access this root level group, and only after elevating access. The root management group has several important facts to be aware of:
Root management group is named Tenant root group, though the name can be changed.
The root management group cannot be moved or deleted
All management groups in the Azure AD are under the root management group.
All Azure users can see the root management group
You can only have one root management group
New subscriptions are automatically placed in the root management group when created.