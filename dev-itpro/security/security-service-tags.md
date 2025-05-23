---
title: Use Azure security service tags
description: "List of Azure service tags for Dynamics 365 Business Central"
author: SusanneWindfeldPedersen
ms.author: solsen
ms.topic: article
ms.date: 01/30/2025
ms.reviewer: solsen
---

# Use Azure security service tags to restrict network access from/to Business Central

An Azure service tag represents a group of IP addresses from/to which traffic from a specific service may come, which allows you to set up firewalls for a specific service to allow only traffic from certain services. The **Dynamics365BusinessCentral** service tag enables administrators to restrict access from/to [!INCLUDE [prod_short](../developer/includes/prod_short.md)] using firewall and network security group rules. The **Dynamics365BusinessCentral** service tag is automatically updated as this group of IP addresses changes over time, so administrators can avoid frequent updates to network security rules to keep up with those changes.

> [!IMPORTANT]  
> The scenario of customers explicitly allowlisting IP addresses on the network that their employees use to interact with [!INCLUDE [prod_short](../developer/includes/prod_short.md)] isn't yet fully supported:  
>  - Teams and Excel clients will be using IP addresses not included in service tags for the foreseeable future
>  - If you write data from your environment directly to a storage account in the same or a paired Azure region, requests on the storage account will originate from an internal IP address and not be affected by service tags applied to the storage account. Learn more [here](/azure/storage/common/storage-network-security?tabs=azure-portal#grant-access-from-an-internet-ip-range).

> [!NOTE]  
> The IP addresses included in the service tag are used by all [!INCLUDE [prod_short](../developer/includes/prod_short.md)] environments. It's not possible to control traffic on a more granular scale, for example, using a dedicated IP address for a single environment or by filtering them to a specific region.

The group of IP addresses making up the service tag are available through the [Azure Management API](/rest/api/virtualnetwork/service-tags/list?tabs=HTTP) and as [downloadable JSON files](/azure/virtual-network/service-tags-overview#discover-service-tags-by-using-downloadable-json-files) to use for any systems that don't support service tags.

## Traffic to Business Central requirements

- A Network Security Group that allows 443 to the `AzureFrontDoor.Frontend` service tag
- A Network Security Group that allows 443 (and all other ports such as ODATA etc.) to the `Dynamics365BusinessCentral` service tag

## Traffic from Business Central requirements

- A Network Security Group that allows traffic from the `Dynamics365BusinessCentral` service tag

Learn more about service tags [Virtual network service tags](/azure/virtual-network/service-tags-overview).

## Related information

[Security and protection](Security-and-Protection.md)  
