---
title: Controlar el acceso a EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 61e29e54-e3e5-404a-84c0-93b61a25ca58
description: Encuentre información acerca de cómo controlar el acceso a EWS para los usuarios, aplicaciones o toda la organización.
ms.openlocfilehash: 956c28faba105ecf2a6b1452abe629ea2fc930e1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763044"
---
# <a name="control-access-to-ews-in-exchange"></a><span data-ttu-id="1d789-103">Controlar el acceso a EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1d789-103">Control access to EWS in Exchange</span></span>

<span data-ttu-id="1d789-104">Encuentre información acerca de cómo controlar el acceso a EWS para los usuarios, aplicaciones o toda la organización.</span><span class="sxs-lookup"><span data-stu-id="1d789-104">Find out how to control access to EWS for users, applications, or the entire organization.</span></span>
  
<span data-ttu-id="1d789-105">Si está utilizando la API administrada de EWS o EWS directamente, en la aplicación, puede controlar el acceso a servicios Web de Exchange (EWS).</span><span class="sxs-lookup"><span data-stu-id="1d789-105">Whether you are using the EWS Managed API, or EWS directly, in your application, you can control access to Exchange Web Services (EWS).</span></span> <span data-ttu-id="1d789-106">Si dispone de acceso de administrador al servidor de Exchange, puede administrar el acceso a EWS mediante el uso de la consola de administración de Exchange para controlar el acceso de forma global, para cada usuario y para cada aplicación.</span><span class="sxs-lookup"><span data-stu-id="1d789-106">If you have administrator access to your Exchange server, you can manage access to EWS by using the Exchange Management Shell to control access globally, for each user, and for each application.</span></span>
  
## <a name="exchange-management-shell-cmdlets-for-configuring-access-control"></a><span data-ttu-id="1d789-107">Cmdlets del Shell de administración de Exchange para configurar el control de acceso</span><span class="sxs-lookup"><span data-stu-id="1d789-107">Exchange Management Shell cmdlets for configuring access control</span></span>
<span data-ttu-id="1d789-108"><a name="bk_Cmdlets"> </a></span><span class="sxs-lookup"><span data-stu-id="1d789-108"></span></span>

<span data-ttu-id="1d789-109">Puede usar los siguientes cmdlets del Shell de administración de Exchange para ver la configuración actual de acceso y configurar el acceso a controles de EWS:</span><span class="sxs-lookup"><span data-stu-id="1d789-109">You can use the following Exchange Management Shell cmdlets to view the current access configuration and set EWS access controls:</span></span>
  
- <span data-ttu-id="1d789-110">[Get-CASMailbox](http://technet.microsoft.com/en-us/library/bb124754.aspx) - muestra qué parámetros se establecen para un buzón determinado.</span><span class="sxs-lookup"><span data-stu-id="1d789-110">[Get-CASMailbox](http://technet.microsoft.com/en-us/library/bb124754.aspx) - Shows you what parameters are set for a particular mailbox.</span></span>   
- <span data-ttu-id="1d789-111">[Set-CASMailbox](http://technet.microsoft.com/en-us/library/bb125264.aspx) - parámetros de conjuntos de un buzón determinado.</span><span class="sxs-lookup"><span data-stu-id="1d789-111">[Set-CASMailbox](http://technet.microsoft.com/en-us/library/bb125264.aspx) - Sets parameters for a particular mailbox.</span></span>    
- <span data-ttu-id="1d789-112">[Get-OrganizationConfig](http://technet.microsoft.com/en-us/library/aa997571.aspx) - muestra los parámetros para toda la organización.</span><span class="sxs-lookup"><span data-stu-id="1d789-112">[Get-OrganizationConfig](http://technet.microsoft.com/en-us/library/aa997571.aspx) - Shows you the parameters for the entire organization.</span></span>    
- <span data-ttu-id="1d789-113">[Set-OrganizationConfig](http://technet.microsoft.com/en-us/library/aa997443.aspx) - establece los parámetros para toda la organización.</span><span class="sxs-lookup"><span data-stu-id="1d789-113">[Set-OrganizationConfig](http://technet.microsoft.com/en-us/library/aa997443.aspx) - Sets the parameters for the entire organization.</span></span> 

<span data-ttu-id="1d789-114"><a name="bk_Examples"> </a></span><span class="sxs-lookup"><span data-stu-id="1d789-114"></span></span>

## <a name="examples-controlling-access-to-ews"></a><span data-ttu-id="1d789-115">Ejemplos: Controlar el acceso a EWS</span><span class="sxs-lookup"><span data-stu-id="1d789-115">Examples: Controlling access to EWS</span></span>

<span data-ttu-id="1d789-116">Vamos a echar un vistazo a algunos escenarios que muestran cómo se puede controlar el acceso a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1d789-116">Let's take a look at a few scenarios that show you how you can control access to your application.</span></span>
  
<span data-ttu-id="1d789-117">**La tabla 1. Comandos para controlar el acceso a EWS**</span><span class="sxs-lookup"><span data-stu-id="1d789-117">**Table 1. Commands for controlling access to EWS**</span></span>

|<span data-ttu-id="1d789-118">Si desea</span><span class="sxs-lookup"><span data-stu-id="1d789-118">If you want to</span></span> |<span data-ttu-id="1d789-119">Use este comando</span><span class="sxs-lookup"><span data-stu-id="1d789-119">Use this command</span></span>|
|:-----|:-----|
|<span data-ttu-id="1d789-120">Bloquear todas las aplicaciones cliente de uso de EWS.</span><span class="sxs-lookup"><span data-stu-id="1d789-120">Block all client applications from using EWS.</span></span> | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceAllowList`<br/><br/><span data-ttu-id="1d789-121">Esto permite que las aplicaciones que aparecen en la AllowList para conectarse.</span><span class="sxs-lookup"><span data-stu-id="1d789-121">This allows applications listed in the AllowList to connect.</span></span> <span data-ttu-id="1d789-122">En este ejemplo, no hay aplicaciones se incluyen en el AllowList, por lo que no hay aplicaciones de pueden usar EWS.</span><span class="sxs-lookup"><span data-stu-id="1d789-122">In this example, no applications are included in the AllowList, so no applications can use EWS.</span></span> |
|<span data-ttu-id="1d789-123">Permitir que las aplicaciones usar EWS de una lista de cliente.</span><span class="sxs-lookup"><span data-stu-id="1d789-123">Allow a list of client applications to use EWS.</span></span> | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceAllowList -EwsAllowList:"OWA/*"`<br/><br/><span data-ttu-id="1d789-124">Esto permite aplicaciones específicas para el uso de EWS.</span><span class="sxs-lookup"><span data-stu-id="1d789-124">This allows specific applications to use EWS.</span></span> <span data-ttu-id="1d789-125">En este ejemplo, cualquier aplicación que tenga un agente de usuario de la cadena que comienza por "OWA /" se permitió el acceso.</span><span class="sxs-lookup"><span data-stu-id="1d789-125">In this example, any application that has a user agent string that starts with "OWA/" is allowed access.</span></span> |
|<span data-ttu-id="1d789-126">Permitir que todas las aplicaciones de cliente usar EWS excepto aquellos que estén bloqueados específicamente.</span><span class="sxs-lookup"><span data-stu-id="1d789-126">Allow all client applications to use EWS except those that are specifically blocked.</span></span> | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceBlockList -EwsBlockList:"OWA/*"`<br/> <br/><span data-ttu-id="1d789-127">En este ejemplo se bloquea sólo aplicaciones desde mediante EWS que tienen una cadena de agente de usuario que comienza por "OWA /".</span><span class="sxs-lookup"><span data-stu-id="1d789-127">This example only blocks applications from using EWS that have a user agent string that starts with "OWA/".</span></span> |
|<span data-ttu-id="1d789-128">Permitir que todas las aplicaciones de cliente usar EWS.</span><span class="sxs-lookup"><span data-stu-id="1d789-128">Allow all client applications to use EWS.</span></span> | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceBlockList` <br/><br/> <span data-ttu-id="1d789-129">Debido a que no se ha especificado ninguna lista de bloqueo, todas las aplicaciones pueden usar EWS.</span><span class="sxs-lookup"><span data-stu-id="1d789-129">Because no BlockList is specified, all applications can use EWS.</span></span> |
|<span data-ttu-id="1d789-130">Bloquear toda la organización de uso de EWS.</span><span class="sxs-lookup"><span data-stu-id="1d789-130">Block the entire organization from using EWS.</span></span> | `Set-OrganizationConfig -EwsEnabled:$false` |
|<span data-ttu-id="1d789-131">Permitir que toda la organización para uso de EWS.</span><span class="sxs-lookup"><span data-stu-id="1d789-131">Allow the entire organization to use EWS.</span></span> | `Set-OrganizationConfig -EwsEnabled:$true`|
|<span data-ttu-id="1d789-132">Bloquear un buzón individual de uso de EWS.</span><span class="sxs-lookup"><span data-stu-id="1d789-132">Block an individual mailbox from using EWS.</span></span> | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$false`|
|<span data-ttu-id="1d789-133">Permitir que un buzón individual para uso de EWS.</span><span class="sxs-lookup"><span data-stu-id="1d789-133">Allow an individual mailbox to use EWS.</span></span> | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$true`|
   
## <a name="see-also"></a><span data-ttu-id="1d789-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d789-134">See also</span></span>

- [<span data-ttu-id="1d789-135">Configurar una aplicación de EWS</span><span class="sxs-lookup"><span data-stu-id="1d789-135">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)    
- [<span data-ttu-id="1d789-136">Controlar el acceso de la aplicación de cliente para EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1d789-136">Controlling client application access to EWS in Exchange</span></span>](controlling-client-application-access-to-ews-in-exchange.md)   
- [<span data-ttu-id="1d789-137">Exchange Server PowerShell (Shell de administración de Exchange)</span><span class="sxs-lookup"><span data-stu-id="1d789-137">Exchange Server PowerShell (Exchange Management Shell)</span></span>](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps) 
- [<span data-ttu-id="1d789-138">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="1d789-138">Windows PowerShell</span></span>](http://msdn.microsoft.com/en-us/library/dd835506%28v=vs.85%29.aspx)
    

