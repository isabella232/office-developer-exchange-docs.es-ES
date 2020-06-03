---
title: Controlar el acceso a EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 61e29e54-e3e5-404a-84c0-93b61a25ca58
description: Descubra cómo controlar el acceso a EWS para usuarios, aplicaciones o toda la organización.
localization_priority: Priority
ms.openlocfilehash: bd65b099ab15c1514945d8a1cfa4e9b1428a4755
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456881"
---
# <a name="control-access-to-ews-in-exchange"></a><span data-ttu-id="c538f-103">Controlar el acceso a EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c538f-103">Control access to EWS in Exchange</span></span>

<span data-ttu-id="c538f-104">Descubra cómo controlar el acceso a EWS para usuarios, aplicaciones o toda la organización.</span><span class="sxs-lookup"><span data-stu-id="c538f-104">Find out how to control access to EWS for users, applications, or the entire organization.</span></span>
  
<span data-ttu-id="c538f-105">Independientemente de si usa la API administrada de EWS, o EWS directamente, en su aplicación, puede controlar el acceso a los servicios web Exchange (EWS).</span><span class="sxs-lookup"><span data-stu-id="c538f-105">Whether you are using the EWS Managed API, or EWS directly, in your application, you can control access to Exchange Web Services (EWS).</span></span> <span data-ttu-id="c538f-106">Si tiene acceso de administrador a su servidor de Exchange, puede administrar el acceso a EWS mediante el shell de administración de Exchange para controlar el acceso globalmente, para cada usuario y para cada aplicación.</span><span class="sxs-lookup"><span data-stu-id="c538f-106">If you have administrator access to your Exchange server, you can manage access to EWS by using the Exchange Management Shell to control access globally, for each user, and for each application.</span></span>
  
## <a name="exchange-management-shell-cmdlets-for-configuring-access-control"></a><span data-ttu-id="c538f-107">Cmdlets del shell de administración de Exchange para configurar el control de acceso</span><span class="sxs-lookup"><span data-stu-id="c538f-107">Exchange Management Shell cmdlets for configuring access control</span></span>
<span data-ttu-id="c538f-108"><a name="bk_Cmdlets"> </a></span><span class="sxs-lookup"><span data-stu-id="c538f-108"><a name="bk_Cmdlets"> </a></span></span>

<span data-ttu-id="c538f-109">Puede usar los siguientes cmdlets del shell de administración de Exchange para ver la configuración de acceso actual y establecer los controles de acceso EWS:</span><span class="sxs-lookup"><span data-stu-id="c538f-109">You can use the following Exchange Management Shell cmdlets to view the current access configuration and set EWS access controls:</span></span>
  
- <span data-ttu-id="c538f-110">[Get-CASMailbox](https://technet.microsoft.com/library/bb124754.aspx) : muestra qué parámetros se establecen para un buzón en particular.</span><span class="sxs-lookup"><span data-stu-id="c538f-110">[Get-CASMailbox](https://technet.microsoft.com/library/bb124754.aspx) - Shows you what parameters are set for a particular mailbox.</span></span>   
- <span data-ttu-id="c538f-111">[Set-CASMailbox](https://technet.microsoft.com/library/bb125264.aspx) : establece parámetros para un buzón en particular.</span><span class="sxs-lookup"><span data-stu-id="c538f-111">[Set-CASMailbox](https://technet.microsoft.com/library/bb125264.aspx) - Sets parameters for a particular mailbox.</span></span>    
- <span data-ttu-id="c538f-112">[Get-OrganizationConfig](https://technet.microsoft.com/library/aa997571.aspx) : muestra los parámetros para toda la organización.</span><span class="sxs-lookup"><span data-stu-id="c538f-112">[Get-OrganizationConfig](https://technet.microsoft.com/library/aa997571.aspx) - Shows you the parameters for the entire organization.</span></span>    
- <span data-ttu-id="c538f-113">[Set-OrganizationConfig](https://technet.microsoft.com/library/aa997443.aspx) : establece los parámetros para toda la organización.</span><span class="sxs-lookup"><span data-stu-id="c538f-113">[Set-OrganizationConfig](https://technet.microsoft.com/library/aa997443.aspx) - Sets the parameters for the entire organization.</span></span> 

<span data-ttu-id="c538f-114"><a name="bk_Examples"> </a></span><span class="sxs-lookup"><span data-stu-id="c538f-114"><a name="bk_Examples"> </a></span></span>

## <a name="examples-controlling-access-to-ews"></a><span data-ttu-id="c538f-115">Ejemplos: controlar el acceso a EWS</span><span class="sxs-lookup"><span data-stu-id="c538f-115">Examples: Controlling access to EWS</span></span>

<span data-ttu-id="c538f-116">Echemos un vistazo a algunos escenarios que muestran cómo se puede controlar el acceso a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c538f-116">Let's take a look at a few scenarios that show you how you can control access to your application.</span></span>
  
<span data-ttu-id="c538f-117">**Tabla 1. Comandos para controlar el acceso a EWS**</span><span class="sxs-lookup"><span data-stu-id="c538f-117">**Table 1. Commands for controlling access to EWS**</span></span>

|<span data-ttu-id="c538f-118">Si desea</span><span class="sxs-lookup"><span data-stu-id="c538f-118">If you want to</span></span> |<span data-ttu-id="c538f-119">Use este comando</span><span class="sxs-lookup"><span data-stu-id="c538f-119">Use this command</span></span>|
|:-----|:-----|
|<span data-ttu-id="c538f-120">Bloquear todas las aplicaciones cliente para que no usen EWS.</span><span class="sxs-lookup"><span data-stu-id="c538f-120">Block all client applications from using EWS.</span></span> | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceAllowList`<br/><br/><span data-ttu-id="c538f-121">Esto permite que las aplicaciones enumeradas en AllowList se conecten.</span><span class="sxs-lookup"><span data-stu-id="c538f-121">This allows applications listed in the AllowList to connect.</span></span> <span data-ttu-id="c538f-122">En este ejemplo, no se incluye ninguna aplicación en la AllowList, por lo que ninguna aplicación puede usar EWS.</span><span class="sxs-lookup"><span data-stu-id="c538f-122">In this example, no applications are included in the AllowList, so no applications can use EWS.</span></span> |
|<span data-ttu-id="c538f-123">Permitir una lista de aplicaciones cliente para usar EWS.</span><span class="sxs-lookup"><span data-stu-id="c538f-123">Allow a list of client applications to use EWS.</span></span> | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceAllowList -EwsAllowList:"OWA/*"`<br/><br/><span data-ttu-id="c538f-124">Esto permite que aplicaciones específicas usen EWS.</span><span class="sxs-lookup"><span data-stu-id="c538f-124">This allows specific applications to use EWS.</span></span> <span data-ttu-id="c538f-125">En este ejemplo, se permite el acceso a cualquier aplicación que tenga una cadena de agente de usuario que comience por "OWA/".</span><span class="sxs-lookup"><span data-stu-id="c538f-125">In this example, any application that has a user agent string that starts with "OWA/" is allowed access.</span></span> |
|<span data-ttu-id="c538f-126">Permitir que todas las aplicaciones cliente usen EWS, excepto aquellas que se bloquean específicamente.</span><span class="sxs-lookup"><span data-stu-id="c538f-126">Allow all client applications to use EWS except those that are specifically blocked.</span></span> | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceBlockList -EwsBlockList:"OWA/*"`<br/> <br/><span data-ttu-id="c538f-127">En este ejemplo solo se impide que las aplicaciones usen EWS que tienen una cadena de agente de usuario que comienza con "OWA/".</span><span class="sxs-lookup"><span data-stu-id="c538f-127">This example only blocks applications from using EWS that have a user agent string that starts with "OWA/".</span></span> |
|<span data-ttu-id="c538f-128">Permitir que todas las aplicaciones cliente usen EWS.</span><span class="sxs-lookup"><span data-stu-id="c538f-128">Allow all client applications to use EWS.</span></span> | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceBlockList` <br/><br/> <span data-ttu-id="c538f-129">Como no se especifica ninguna lista de bloqueo, todas las aplicaciones pueden usar EWS.</span><span class="sxs-lookup"><span data-stu-id="c538f-129">Because no BlockList is specified, all applications can use EWS.</span></span> |
|<span data-ttu-id="c538f-130">Impedir que toda la organización use EWS.</span><span class="sxs-lookup"><span data-stu-id="c538f-130">Block the entire organization from using EWS.</span></span> | `Set-OrganizationConfig -EwsEnabled:$false` |
|<span data-ttu-id="c538f-131">Permitir a toda la organización usar EWS.</span><span class="sxs-lookup"><span data-stu-id="c538f-131">Allow the entire organization to use EWS.</span></span> | `Set-OrganizationConfig -EwsEnabled:$true`|
|<span data-ttu-id="c538f-132">Impedir que un buzón individual use EWS.</span><span class="sxs-lookup"><span data-stu-id="c538f-132">Block an individual mailbox from using EWS.</span></span> | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$false`|
|<span data-ttu-id="c538f-133">Permitir a un buzón individual usar EWS.</span><span class="sxs-lookup"><span data-stu-id="c538f-133">Allow an individual mailbox to use EWS.</span></span> | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$true`|
   
## <a name="see-also"></a><span data-ttu-id="c538f-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="c538f-134">See also</span></span>

- [<span data-ttu-id="c538f-135">Configurar la aplicación EWS</span><span class="sxs-lookup"><span data-stu-id="c538f-135">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)    
- [<span data-ttu-id="c538f-136">Controlar el acceso de la aplicación cliente a EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c538f-136">Controlling client application access to EWS in Exchange</span></span>](controlling-client-application-access-to-ews-in-exchange.md)   
- [<span data-ttu-id="c538f-137">PowerShell de Exchange Server (Shell de administración de Exchange)</span><span class="sxs-lookup"><span data-stu-id="c538f-137">Exchange Server PowerShell (Exchange Management Shell)</span></span>](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps) 
- [<span data-ttu-id="c538f-138">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c538f-138">Windows PowerShell</span></span>](https://msdn.microsoft.com/library/dd835506%28v=vs.85%29.aspx)
    

