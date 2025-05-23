---
title: Upgrade data for Dynamics GP cloud migration
description: This article explains the process for running the data upgrade as part of Dynamics GP cloud migration. 
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: upgrade-and-migration-article
ms.date: 02/29/2024
ms.custom: bap-template 
---
# Upgrade data for Dynamics GP cloud migration

This article explains the process for running the data upgrade as part of cloud migration. Data upgrade transforms Dynamics GP tables into Business Central tables.

[!INCLUDE [migrate-e2e-process](../developer/includes/migrate-e2e-process-gp.md)]

## Prerequisites

You ran data replication on the company or companies that you're migrating to the online environment. For more information, go to [Run data replication](migrate-data-replication-run.md).

[!INCLUDE [cloud-migration-telemetry](../includes/bc-cloud-migrate-replicate-all-before-upgrade.md)]

## Prepare

Once you start the data upgrade on an environment, all client connections are terminated. You can't reconnect until the upgrade process has completed. Also, hotfixes can't be applied and scheduled tasks can't be run. This behavior means data upgrade is the only process running on the environment, which helps prevent potentials database locks and errors.

Inform any active Business Central online users to finish what they're doing and sign out.

## Run data upgrade

1. Search for and open the **Cloud Migration Management** page.
2. Select **Run data upgrade** > **Yes** > **OK** to schedule the data upgrade.

   The data upgrade process starts. To check whether the migration succeeded or failed. go to the **Cloud Migration Management** page. If the upgrade fails, go to **Migration Errors** FactBox where you can drill down to view the errors.

> [!TIP]
> [!INCLUDE [cloud-migration-telemetry](../developer/includes/cloud-migration-telemetry.md)]. You can also track the status of the data upgrade on the **Operations** page in the admin center (see [Operations log](tenant-admin-center-environments.md#opslog)).

## Next steps

[Complete cloud migration](migration-finish-gp.md).  

## Related information

[Dynamics GP migration to Business Central online: End-to-end overview](migrate-gp-overview.md)  
[Compare Work in Dynamics GP to Business Central](migrate-dynamics-gp-videos.md)  
[FAQ about migrating to Business Central online from on-premises solutions](faq-migrate-data.md)  
