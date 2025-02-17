## Azure terminology

It's helpful to know the following definitions as you begin your Azure cloud adoption journey:

- **Resource:** An entity that's managed by Azure. Examples include Azure Virtual Machines, virtual networks, and storage accounts.
- **Subscription:** A logical container for your resources. Each Azure resource is associated with only one subscription. Creating a subscription is the first step in adopting Azure.
- **Azure account:** The email address that you provide when you create an Azure subscription is the Azure account for the subscription. The party that's associated with the email account is responsible for the monthly costs incurred by the resources in the subscription. When you create an Azure account, you provide contact information and billing details, like a credit card. You can use the same Azure account for multiple subscriptions. Each subscription is associated with only one Azure account.
- **Account administrator:** The party associated with the email address that's used to create an Azure subscription. The account administrator is responsible for paying for all costs that incur by the subscription's resources.
- **Microsoft Entra ID:** The Microsoft cloud-based identity and access management service. Microsoft Entra ID lets your employees sign in and access resources.
- **Microsoft Entra tenant:** A dedicated and trusted instance of Microsoft Entra ID. When your organization signs up for a Microsoft cloud service subscription, it automatically creates a Microsoft Entra tenant. For example, Microsoft Azure, Intune, or Microsoft 365. An Azure tenant represents a single organization.
- **Microsoft Entra directory:** Each Microsoft Entra tenant has a single, dedicated, and trusted directory. The directory includes the tenant's users, groups, and applications. Use the directory to manage identity and access management functions for tenant resources. You can associate a directory with multiple subscriptions but each subscription is associated with only one directory.
- **Resource groups:** Logical containers that you use to group related resources in a subscription. Each resource can exist in only one resource group. Resource groups allow for more granular grouping within a subscription. They're commonly used to represent a collection of assets that are required to support a workload, application, or specific function within a subscription.
- **Management groups:** Logical containers that you use for one or more subscriptions. You can define a hierarchy of management groups, subscriptions, resource groups, and resources to efficiently manage access, policies, and compliance through inheritance.
- **Region:** A set of Azure datacenters that deploy inside a latency-defined perimeter. The datacenters connect through a dedicated, regional, low-latency network. Most Azure resources run in a specific Azure region.

[](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/considerations/fundamental-concepts?toc=%2Fazure%2Fvirtual-network%2Ftoc.json#azure-subscription-purposes)

## Azure subscription purposes

An Azure subscription serves several purposes, such as:

- **A legal agreement.** Each subscription is associated with an [Azure offer](https://azure.microsoft.com/support/legal/offer-details), like a free trial or pay-as-you-go. Each offer provides a specific rate plan, benefits, and associated terms and conditions. Choose an Azure offer when you create a subscription.
- **A payment agreement.** When you create a subscription, you provide payment information for that subscription, such as a credit card number. Each month, the costs that incur by the resources deployed to the subscription are calculated and billed to that payment method.
- **A boundary of scale.** Scale limits you define for a subscription. The subscription's resources can't exceed the set scale limits. For example, there's a limit on the number of virtual machines that you can create in a single subscription.
- **An administrative boundary.** A subscription can act as a boundary for administration, security, and policy. Azure also provides other mechanisms to meet these needs, such as management groups, resource groups, and Azure role-based access control.

[](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/considerations/fundamental-concepts?toc=%2Fazure%2Fvirtual-network%2Ftoc.json#azure-subscription-considerations)

## Azure subscription considerations

When you create an Azure subscription, you make several key choices about the subscription:

- **Who is responsible for paying for the subscription?** By default, the account administrator is the person associated with the email address that you provide when you create a subscription. This person is responsible for paying for all costs incurred by the subscription's resources.
- **Which Azure offer am I interested in?** Each subscription is associated with a specific [Azure offer](https://azure.microsoft.com/support/legal/offer-details). You can choose the Azure offer that best meets your needs. For example, if you intend to use a subscription to run non-production workloads, you might choose the Pay-As-You-Go Dev/Test offer, or the Enterprise Dev/Test offer.

 Note

When you sign up for Azure, you might see the phrase _Create an Azure account_. You create an Azure account when you create an Azure subscription. You can associate the subscription with an email account.

[](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/considerations/fundamental-concepts?toc=%2Fazure%2Fvirtual-network%2Ftoc.json#azure-administrative-roles)

## Azure administrative roles

Azure defines three types of roles for administering subscriptions, identities, and resources:

- Classic subscription administrator roles
- Azure roles
- Microsoft Entra roles

The account administrator role is assigned to the email account that's used to create the Azure subscription. The account administrator is the billing owner of the subscription. The account administrator can [manage subscription administrators](https://learn.microsoft.com/en-us/azure/cost-management-billing/manage/add-change-subscription-administrator) in the Azure portal.

By default, the service administrator role for a subscription is also assigned to the email account that's used to create the Azure subscription. The service administrator has permissions to the subscription equivalent to the Azure role-based access control Owner role. The service administrator also has full access to the Azure portal. The account administrator can change the service administrator to a different email account.

When you create an Azure subscription, you can associate it with an existing Microsoft Entra tenant. You provide an email account and can associate that email account with multiple Azure subscriptions. An account administrator can transfer a subscription to another account. For more information, see [Classic subscription administrator roles, Azure roles, and Microsoft Entra roles](https://learn.microsoft.com/en-us/azure/role-based-access-control/rbac-and-directory-admin-roles).

[](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/considerations/fundamental-concepts?toc=%2Fazure%2Fvirtual-network%2Ftoc.json#subscriptions-and-regions)

## Subscriptions and regions

Every Azure resource is logically associated with one subscription. When you create a resource, you choose which Azure subscription to deploy that resource to. You can move a resource to another subscription later.

Subscriptions aren't tied to a specific Azure region, but each Azure resource deploys to only one region. You can have resources in multiple regions that are associated with the same subscription.

 Note

Most Azure resources deploy to a specific region. Certain resource types are considered global resources, such as policies that you set by using the Azure Policy services.