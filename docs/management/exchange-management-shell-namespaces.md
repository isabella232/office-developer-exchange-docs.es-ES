---
title: Espacios de nombres de Shell de administración de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ff849238-06b7-4891-884b-c51ce0f1ebbc
description: Obtenga información acerca de los espacios de nombres de la consola de administración de Exchange en Exchange.
ms.openlocfilehash: d1683f99fbd233c1b878eb86d529b58ea1ebd8c9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763307"
---
# <a name="exchange-management-shell-namespaces"></a><span data-ttu-id="17d3f-103">Espacios de nombres de Shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="17d3f-103">Exchange Management Shell namespaces</span></span>

<span data-ttu-id="17d3f-104">Obtenga información acerca de los espacios de nombres de la consola de administración de Exchange en Exchange.</span><span class="sxs-lookup"><span data-stu-id="17d3f-104">Find information about the namespaces for the Exchange Management Shell in Exchange.</span></span>
  
<span data-ttu-id="17d3f-105">**Se aplica a:** Exchange Online | Exchange Server 2013 | Office 365</span><span class="sxs-lookup"><span data-stu-id="17d3f-105">**Applies to:** Exchange Online | Exchange Server 2013 | Office 365</span></span>
  
<span data-ttu-id="17d3f-106">Aplicaciones de consola de administración de Exchange para Exchange Online, Exchange Online como parte de Office 365 o una versión de Exchange a partir de Exchange 2013 interactúan con el entorno de Windows PowerShell a través de los tipos expuestos por el ** System.Management.Automation** espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="17d3f-106">Exchange Management Shell applications for Exchange Online, Exchange Online as part of Office 365, or a version of Exchange starting with Exchange 2013 interact with the Windows PowerShell environment through the types that are exposed by the **System.Management.Automation** namespace.</span></span> <span data-ttu-id="17d3f-107">Los cmdlets del Shell de administración de Exchange usar tipos de un número de bibliotecas de Exchange.</span><span class="sxs-lookup"><span data-stu-id="17d3f-107">The Exchange Management Shell cmdlets use types from a number of Exchange libraries.</span></span> <span data-ttu-id="17d3f-108">En esta sección se proporciona información de referencia acerca de los tipos y las interfaces de las bibliotecas de Exchange que se usan por los cmdlets del Shell de administración de Exchange.</span><span class="sxs-lookup"><span data-stu-id="17d3f-108">This section provides reference information about the types and interfaces from the Exchange libraries that are used by Exchange Management Shell cmdlets.</span></span> 
  
<span data-ttu-id="17d3f-109">El Shell de administración de Exchange contiene los siguientes espacios de nombres:</span><span class="sxs-lookup"><span data-stu-id="17d3f-109">The Exchange Management Shell contains the following namespaces:</span></span>
  
- [<span data-ttu-id="17d3f-110">Microsoft.Exchange.Configuration.Tasks</span><span class="sxs-lookup"><span data-stu-id="17d3f-110">Microsoft.Exchange.Configuration.Tasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Configuration.Tasks.aspx)
    
- [<span data-ttu-id="17d3f-111">Microsoft.Exchange.Data</span><span class="sxs-lookup"><span data-stu-id="17d3f-111">Microsoft.Exchange.Data</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.aspx)
    
- [<span data-ttu-id="17d3f-112">Microsoft.Exchange.Data.Directory</span><span class="sxs-lookup"><span data-stu-id="17d3f-112">Microsoft.Exchange.Data.Directory</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.aspx)
    
- [<span data-ttu-id="17d3f-113">Microsoft.Exchange.Data.Directory.Management</span><span class="sxs-lookup"><span data-stu-id="17d3f-113">Microsoft.Exchange.Data.Directory.Management</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.Management.aspx)
    
- [<span data-ttu-id="17d3f-114">Microsoft.Exchange.Data.Directory.Permission</span><span class="sxs-lookup"><span data-stu-id="17d3f-114">Microsoft.Exchange.Data.Directory.Permission</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.Permission.aspx)
    
- [<span data-ttu-id="17d3f-115">Microsoft.Exchange.Data.Directory.Recipient</span><span class="sxs-lookup"><span data-stu-id="17d3f-115">Microsoft.Exchange.Data.Directory.Recipient</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.Recipient.aspx)
    
- [<span data-ttu-id="17d3f-116">Microsoft.Exchange.Data.Directory.SystemConfiguration</span><span class="sxs-lookup"><span data-stu-id="17d3f-116">Microsoft.Exchange.Data.Directory.SystemConfiguration</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.aspx)
    
- [<span data-ttu-id="17d3f-117">Microsoft.Exchange.Data.Mapi</span><span class="sxs-lookup"><span data-stu-id="17d3f-117">Microsoft.Exchange.Data.Mapi</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mapi.aspx)
    
- [<span data-ttu-id="17d3f-118">Microsoft.Exchange.Data.QueueDigest</span><span class="sxs-lookup"><span data-stu-id="17d3f-118">Microsoft.Exchange.Data.QueueDigest</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.QueueDigest.aspx)
    
- [<span data-ttu-id="17d3f-119">Microsoft.Exchange.Data.QueueViewer</span><span class="sxs-lookup"><span data-stu-id="17d3f-119">Microsoft.Exchange.Data.QueueViewer</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.QueueViewer.aspx)
    
- [<span data-ttu-id="17d3f-120">Microsoft.Exchange.Data.RightsManagement</span><span class="sxs-lookup"><span data-stu-id="17d3f-120">Microsoft.Exchange.Data.RightsManagement</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.RightsManagement.aspx)
    
- [<span data-ttu-id="17d3f-121">Microsoft.Exchange.Data.Storage</span><span class="sxs-lookup"><span data-stu-id="17d3f-121">Microsoft.Exchange.Data.Storage</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Storage.aspx)
    
- [<span data-ttu-id="17d3f-122">Microsoft.Exchange.Data.Storage.ActiveMonitoring</span><span class="sxs-lookup"><span data-stu-id="17d3f-122">Microsoft.Exchange.Data.Storage.ActiveMonitoring</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Storage.ActiveMonitoring.aspx)
    
- [<span data-ttu-id="17d3f-123">Microsoft.Exchange.Data.Storage.Management</span><span class="sxs-lookup"><span data-stu-id="17d3f-123">Microsoft.Exchange.Data.Storage.Management</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Storage.Management.aspx)
    
- [<span data-ttu-id="17d3f-124">Microsoft.Exchange.Data.Storage.Management.Migration</span><span class="sxs-lookup"><span data-stu-id="17d3f-124">Microsoft.Exchange.Data.Storage.Management.Migration</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Storage.Management.Migration.aspx)
    
- [<span data-ttu-id="17d3f-125">Microsoft.Exchange.Data.Storage.StoreConfigurableType</span><span class="sxs-lookup"><span data-stu-id="17d3f-125">Microsoft.Exchange.Data.Storage.StoreConfigurableType</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Storage.StoreConfigurableType.aspx)
    
- [<span data-ttu-id="17d3f-126">Microsoft.Exchange.EdgeSync.Validation</span><span class="sxs-lookup"><span data-stu-id="17d3f-126">Microsoft.Exchange.EdgeSync.Validation</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.EdgeSync.Validation.aspx)
    
- [<span data-ttu-id="17d3f-127">Microsoft.Exchange.MailboxReplicationService</span><span class="sxs-lookup"><span data-stu-id="17d3f-127">Microsoft.Exchange.MailboxReplicationService</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.MailboxReplicationService.aspx)
    
- [<span data-ttu-id="17d3f-128">Microsoft.Exchange.Management.AgentTasks</span><span class="sxs-lookup"><span data-stu-id="17d3f-128">Microsoft.Exchange.Management.AgentTasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.AgentTasks.aspx)
    
- [<span data-ttu-id="17d3f-129">Microsoft.Exchange.Management.ClassificationDefinitions</span><span class="sxs-lookup"><span data-stu-id="17d3f-129">Microsoft.Exchange.Management.ClassificationDefinitions</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.ClassificationDefinitions.aspx)
    
- [<span data-ttu-id="17d3f-130">Microsoft.Exchange.Management.Extension</span><span class="sxs-lookup"><span data-stu-id="17d3f-130">Microsoft.Exchange.Management.Extension</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.Extension.aspx)
    
- [<span data-ttu-id="17d3f-131">Microsoft.Exchange.Management.FfoReporting</span><span class="sxs-lookup"><span data-stu-id="17d3f-131">Microsoft.Exchange.Management.FfoReporting</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.FfoReporting.aspx)
    
- [<span data-ttu-id="17d3f-132">Microsoft.Exchange.Management.FfoReporting.Common</span><span class="sxs-lookup"><span data-stu-id="17d3f-132">Microsoft.Exchange.Management.FfoReporting.Common</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.FfoReporting.Common.aspx)
    
- [<span data-ttu-id="17d3f-133">Microsoft.Exchange.Management.MessagingPolicies.AddressRewrite</span><span class="sxs-lookup"><span data-stu-id="17d3f-133">Microsoft.Exchange.Management.MessagingPolicies.AddressRewrite</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.MessagingPolicies.AddressRewrite.aspx)
    
- [<span data-ttu-id="17d3f-134">Microsoft.Exchange.Management.Migration</span><span class="sxs-lookup"><span data-stu-id="17d3f-134">Microsoft.Exchange.Management.Migration</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.Migration.aspx)
    
- [<span data-ttu-id="17d3f-135">Microsoft.Exchange.Management.OutlookProtectionRules</span><span class="sxs-lookup"><span data-stu-id="17d3f-135">Microsoft.Exchange.Management.OutlookProtectionRules</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.OutlookProtectionRules.aspx)
    
- [<span data-ttu-id="17d3f-136">Microsoft.Exchange.Management.PolicyNudges</span><span class="sxs-lookup"><span data-stu-id="17d3f-136">Microsoft.Exchange.Management.PolicyNudges</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.PolicyNudges.aspx)
    
- [<span data-ttu-id="17d3f-137">Microsoft.Exchange.Management.ProvisioningTasks</span><span class="sxs-lookup"><span data-stu-id="17d3f-137">Microsoft.Exchange.Management.ProvisioningTasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.ProvisioningTasks.aspx)
    
- [<span data-ttu-id="17d3f-138">Microsoft.Exchange.Management.RecipientTasks</span><span class="sxs-lookup"><span data-stu-id="17d3f-138">Microsoft.Exchange.Management.RecipientTasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.RecipientTasks.aspx)
    
- [<span data-ttu-id="17d3f-139">Microsoft.Exchange.Management.ReportingTask.Common</span><span class="sxs-lookup"><span data-stu-id="17d3f-139">Microsoft.Exchange.Management.ReportingTask.Common</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.ReportingTask.Common.aspx)
    
- [<span data-ttu-id="17d3f-140">Microsoft.Exchange.Management.ReportingTask.Query</span><span class="sxs-lookup"><span data-stu-id="17d3f-140">Microsoft.Exchange.Management.ReportingTask.Query</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.ReportingTask.Query.aspx)
    
- [<span data-ttu-id="17d3f-141">Microsoft.Exchange.Management.ReportingTask.TenantReport</span><span class="sxs-lookup"><span data-stu-id="17d3f-141">Microsoft.Exchange.Management.ReportingTask.TenantReport</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.ReportingTask.TenantReport.aspx)
    
- [<span data-ttu-id="17d3f-142">Microsoft.Exchange.Management.RightsManagement</span><span class="sxs-lookup"><span data-stu-id="17d3f-142">Microsoft.Exchange.Management.RightsManagement</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.RightsManagement.aspx)
    
- [<span data-ttu-id="17d3f-143">Microsoft.Exchange.Management.Sharing</span><span class="sxs-lookup"><span data-stu-id="17d3f-143">Microsoft.Exchange.Management.Sharing</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.Sharing.aspx)
    
- [<span data-ttu-id="17d3f-144">Microsoft.Exchange.Management.StoreTasks</span><span class="sxs-lookup"><span data-stu-id="17d3f-144">Microsoft.Exchange.Management.StoreTasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.StoreTasks.aspx)
    
- [<span data-ttu-id="17d3f-145">Microsoft.Exchange.Management.Supervision</span><span class="sxs-lookup"><span data-stu-id="17d3f-145">Microsoft.Exchange.Management.Supervision</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.Supervision.aspx)
    
- [<span data-ttu-id="17d3f-146">Microsoft.Exchange.Management.SystemConfigurationTasks</span><span class="sxs-lookup"><span data-stu-id="17d3f-146">Microsoft.Exchange.Management.SystemConfigurationTasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.SystemConfigurationTasks.aspx)
    
- [<span data-ttu-id="17d3f-147">Microsoft.Exchange.Management.Tasks</span><span class="sxs-lookup"><span data-stu-id="17d3f-147">Microsoft.Exchange.Management.Tasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.Tasks.aspx)
    
- [<span data-ttu-id="17d3f-148">Microsoft.Exchange.Management.Tools</span><span class="sxs-lookup"><span data-stu-id="17d3f-148">Microsoft.Exchange.Management.Tools</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.Tools.aspx)
    
- [<span data-ttu-id="17d3f-149">Microsoft.Exchange.Management.Tracking</span><span class="sxs-lookup"><span data-stu-id="17d3f-149">Microsoft.Exchange.Management.Tracking</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.Tracking.aspx)
    
- [<span data-ttu-id="17d3f-150">Microsoft.Exchange.Management.TransportLogSearchTasks</span><span class="sxs-lookup"><span data-stu-id="17d3f-150">Microsoft.Exchange.Management.TransportLogSearchTasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.TransportLogSearchTasks.aspx)
    
- [<span data-ttu-id="17d3f-151">Microsoft.Exchange.MessagingPolicies.CompliancePrograms.Tasks</span><span class="sxs-lookup"><span data-stu-id="17d3f-151">Microsoft.Exchange.MessagingPolicies.CompliancePrograms.Tasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.MessagingPolicies.CompliancePrograms.Tasks.aspx)
    
- [<span data-ttu-id="17d3f-152">Microsoft.Exchange.MessagingPolicies.Journaling</span><span class="sxs-lookup"><span data-stu-id="17d3f-152">Microsoft.Exchange.MessagingPolicies.Journaling</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.MessagingPolicies.Journaling.aspx)
    
- [<span data-ttu-id="17d3f-153">Microsoft.Exchange.MessagingPolicies.Rules.Tasks</span><span class="sxs-lookup"><span data-stu-id="17d3f-153">Microsoft.Exchange.MessagingPolicies.Rules.Tasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.MessagingPolicies.Rules.Tasks.aspx)
    
- [<span data-ttu-id="17d3f-154">Microsoft.Exchange.Migration</span><span class="sxs-lookup"><span data-stu-id="17d3f-154">Microsoft.Exchange.Migration</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Migration.aspx)
    
- [<span data-ttu-id="17d3f-155">Microsoft.Exchange.Monitoring</span><span class="sxs-lookup"><span data-stu-id="17d3f-155">Microsoft.Exchange.Monitoring</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Monitoring.aspx)
    
- [<span data-ttu-id="17d3f-156">Microsoft.Exchange.Monitoring.ActiveMonitoring</span><span class="sxs-lookup"><span data-stu-id="17d3f-156">Microsoft.Exchange.Monitoring.ActiveMonitoring</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Monitoring.ActiveMonitoring.aspx)
    
- [<span data-ttu-id="17d3f-157">Microsoft.Exchange.Transport.Sync.Common.Subscription</span><span class="sxs-lookup"><span data-stu-id="17d3f-157">Microsoft.Exchange.Transport.Sync.Common.Subscription</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Transport.Sync.Common.Subscription.aspx)
    
- [<span data-ttu-id="17d3f-158">Microsoft.Exchange.Transport.Sync.Common.Subscription.Connect</span><span class="sxs-lookup"><span data-stu-id="17d3f-158">Microsoft.Exchange.Transport.Sync.Common.Subscription.Connect</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Transport.Sync.Common.Subscription.Connect.aspx)
    
- [<span data-ttu-id="17d3f-159">Microsoft.Exchange.Transport.Sync.Common.Subscription.DeltaSync</span><span class="sxs-lookup"><span data-stu-id="17d3f-159">Microsoft.Exchange.Transport.Sync.Common.Subscription.DeltaSync</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Transport.Sync.Common.Subscription.DeltaSync.aspx)
    
- [<span data-ttu-id="17d3f-160">Microsoft.Exchange.Transport.Sync.Common.Subscription.Imap</span><span class="sxs-lookup"><span data-stu-id="17d3f-160">Microsoft.Exchange.Transport.Sync.Common.Subscription.Imap</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Transport.Sync.Common.Subscription.Imap.aspx)
    
- [<span data-ttu-id="17d3f-161">Microsoft.Exchange.Transport.Sync.Common.Subscription.Pim</span><span class="sxs-lookup"><span data-stu-id="17d3f-161">Microsoft.Exchange.Transport.Sync.Common.Subscription.Pim</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Transport.Sync.Common.Subscription.Pim.aspx)
    
- [<span data-ttu-id="17d3f-162">Microsoft.Exchange.Transport.Sync.Common.Subscription.Pop</span><span class="sxs-lookup"><span data-stu-id="17d3f-162">Microsoft.Exchange.Transport.Sync.Common.Subscription.Pop</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Transport.Sync.Common.Subscription.Pop.aspx)
    
- [<span data-ttu-id="17d3f-163">Microsoft.Exchange.UM.Rpc</span><span class="sxs-lookup"><span data-stu-id="17d3f-163">Microsoft.Exchange.UM.Rpc</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.UM.Rpc.aspx)
    
- [<span data-ttu-id="17d3f-164">Microsoft.Exchange.UM.UMCommon</span><span class="sxs-lookup"><span data-stu-id="17d3f-164">Microsoft.Exchange.UM.UMCommon</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.UM.UMCommon.aspx)
    
- [<span data-ttu-id="17d3f-165">Microsoft.Exchange.WorkloadManagement</span><span class="sxs-lookup"><span data-stu-id="17d3f-165">Microsoft.Exchange.WorkloadManagement</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.WorkloadManagement.aspx)
    
## <a name="see-also"></a><span data-ttu-id="17d3f-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="17d3f-166">See also</span></span>

- [<span data-ttu-id="17d3f-167">Shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="17d3f-167">Exchange Management Shell</span></span>](exchange-management-shell.md)  
- [<span data-ttu-id="17d3f-168">Creación de herramientas de Shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="17d3f-168">Create Exchange Management Shell tools</span></span>](create-exchange-management-shell-tools.md) 
- [<span data-ttu-id="17d3f-169">Entrada de cmdlet del Shell de administración de Exchange y tipos de salida</span><span class="sxs-lookup"><span data-stu-id="17d3f-169">Exchange Management Shell cmdlet input and output types</span></span>](exchange-management-shell-cmdlet-input-and-output-types.md)
    

