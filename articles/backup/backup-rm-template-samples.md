---
title: Azure Resource Manager and Bicep templates
description: Azure Resource Manager and Bicep templates for use with Recovery Services vaults and Azure Backup features
ms.topic: sample
ms.date: 06/10/2022
ms.custom: mvc
author: v-amallick
ms.service: backup
ms.author: v-amallick
---
# Azure Resource Manager and Bicep templates for Azure Backup

The following table includes a link to a repository of Azure Resource Manager and Bicep templates for use with Recovery Services vaults and Azure Backup features. To learn about the JSON or Bicep syntax and properties, see [Microsoft.RecoveryServices resource types](/azure/templates/microsoft.recoveryservices/allversions).

| Template | Description |
|---|---|
|**Recovery Services vault** | |
| [Create a Recovery Services vault](https://github.com/Azure/azure-quickstart-templates/tree/master/quickstarts/microsoft.recoveryservices/recovery-services-vault-create)| Create a Recovery Services vault. The vault can be used for Azure Backup and Azure Site Recovery. |
|**Back up virtual machines**| |
| [Back up Resource Manager VMs](https://github.com/Azure/azure-quickstart-templates/tree/master/quickstarts/microsoft.recoveryservices/recovery-services-backup-vms) | Use the existing Recovery Services vault and Backup policy to back up Resource Manager-virtual machines in the same resource group.|
| [Back up IaaS VMs to Recovery Services vault](https://github.com/Azure/azure-quickstart-templates/tree/master/quickstarts/microsoft.recoveryservices/recovery-services-backup-classic-resource-manager-vms) | Template to back up classic and Resource Manager-virtual machines. |
| [Create Weekly Backup policy for IaaS VMs](https://github.com/Azure/azure-quickstart-templates/tree/master/quickstarts/microsoft.recoveryservices/recovery-services-weekly-backup-policy-create) | Template creates Recovery Services vault and a weekly backup policy, which is used to back up classic and Resource Manager-virtual machines.|
| [Create Daily Backup policy for IaaS VMs](https://github.com/Azure/azure-quickstart-templates/tree/master/quickstarts/microsoft.recoveryservices/recovery-services-daily-backup-policy-create) | Template creates Recovery Services vault and a daily backup policy, which is used to back up classic and Resource Manager-virtual machines.|
| [Deploy Windows Server VM with backup enabled](https://github.com/Azure/azure-quickstart-templates/tree/master/quickstarts/microsoft.recoveryservices/recovery-services-create-vm-and-configure-backup) | Template creates a Windows Server VM and Recovery Services vault with the default backup policy enabled.|
|**Monitor Backup jobs** |  |
| [Use Azure Monitor logs with Azure Backup](https://github.com/Azure/azure-quickstart-templates/tree/master/demos/backup-oms-monitoring) | Template deploys Azure Monitor logs with Azure Backup, which allows you to monitor backup and restore jobs, backup alerts, and the Cloud storage used in your Recovery Services vaults.|
|**Back up SQL Server in Azure VM** |  |
| [Back up SQL Server in Azure VM](https://github.com/Azure/azure-quickstart-templates/tree/master/quickstarts/microsoft.recoveryservices/recovery-services-vm-workload-backup) | Template creates a Recovery Services vault and Workload specific Backup Policy. It Registers the VM with Azure Backup service and Configures Protection on that VM. Currently, it only works for SQL Gallery images. |
|**Back up Azure file shares** |  |
| [Back up Azure file shares](https://github.com/Azure/azure-quickstart-templates/tree/master/quickstarts/microsoft.recoveryservices/recovery-services-backup-file-share) | This template configures protection for an existing Azure file share by specifying appropriate details for the Recovery Services vault and backup policy. It optionally creates a new Recovery Services vault and backup policy, and registers the storage account containing the file share to the Recovery Services vault. |
|   |   |
