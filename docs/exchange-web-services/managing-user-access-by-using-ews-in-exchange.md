---
title: Administración del acceso de usuarios mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 48f0170c-8786-405f-86cb-568b7314a425
description: Descubra Cuáles son sus opciones para administrar el acceso de las cuentas de usuario a su servidor de Exchange.
ms.openlocfilehash: 476292d4db206f22cd84134ce2b46957e9fe85fc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456248"
---
# <a name="managing-user-access-by-using-ews-in-exchange"></a><span data-ttu-id="7d248-103">Administración del acceso de usuarios mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="7d248-103">Managing user access by using EWS in Exchange</span></span>

<span data-ttu-id="7d248-104">Descubra Cuáles son sus opciones para administrar el acceso de las cuentas de usuario a su servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7d248-104">Find out what your options are for managing user account access to your Exchange server.</span></span>
  
<span data-ttu-id="7d248-105">Los servicios web Exchange (EWS) y la API administrada de EWS proporcionan un número limitado de operaciones que puede usar para administrar cuentas en Exchange Online, Exchange online como parte de Office 365 o una versión de Exchange que empiece por Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="7d248-105">Exchange Web Services (EWS) and the EWS managed API provide a limited number of operations that you can use to manage accounts on Exchange Online, Exchange Online as part of Office 365, or a version of Exchange starting with Exchange 2013.</span></span> <span data-ttu-id="7d248-106">Puede usar las operaciones que se muestran en la figura siguiente para administrar los delegados y establecer los permisos de acceso a la carpeta para otras cuentas.</span><span class="sxs-lookup"><span data-stu-id="7d248-106">You can use the operations shown in the following figure to manage delegates and to set folder access permissions for other accounts.</span></span> 
  
<span data-ttu-id="7d248-107">**Operaciones de EWS para acceso delegado y de carpeta**</span><span class="sxs-lookup"><span data-stu-id="7d248-107">**EWS operations for delegate and folder access**</span></span>

![Opciones de administración de usuarios de EWS.](media/Exchange_ManagingUserAccess_1.png)
  
<span data-ttu-id="7d248-109">Si la aplicación necesita un control adicional sobre las cuentas en un servidor de Exchange, puede usar los cmdlets del shell de administración de Exchange para administrar las cuentas.</span><span class="sxs-lookup"><span data-stu-id="7d248-109">If your application needs additional control over the accounts on an Exchange server, you can use Exchange Management Shell cmdlets to manage the accounts.</span></span> <span data-ttu-id="7d248-110">Puede llamar a los cmdlets del shell de administración de Exchange mediante uno de los siguientes procedimientos:</span><span class="sxs-lookup"><span data-stu-id="7d248-110">You can call the Exchange Management Shell cmdlets by doing one of the following:</span></span>
  
- <span data-ttu-id="7d248-111">Escribir una aplicación con C# o Visual Basic que llame a los cmdlets del shell de administración de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7d248-111">Writing an application using C# or Visual Basic that calls the Exchange Management Shell cmdlets.</span></span> <span data-ttu-id="7d248-112">Puede consultar el código de ejemplo de la documentación de la [API del shell de administración de Exchange](../management/exchange-management-shell.md) para obtener información sobre cómo llamar a un cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d248-112">You can look at the sample code in the [Exchange Management Shell API documentation](../management/exchange-management-shell.md) to learn how to call a cmdlet.</span></span> 
    
- <span data-ttu-id="7d248-113">Uso de Windows PowerShell y scripts de Windows PowerShell para llamar a los cmdlets del shell de administración de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7d248-113">Using Windows PowerShell and Windows PowerShell scripts to call Exchange Management Shell cmdlets.</span></span> <span data-ttu-id="7d248-114">Puede encontrar una lista completa de [Exchange Server PowerShell (Shell de administración de Exchange)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps), junto con ejemplos que muestran cómo usarlas.</span><span class="sxs-lookup"><span data-stu-id="7d248-114">You can find a complete list of the [Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps), along with examples that show how to use them.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7d248-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d248-115">See also</span></span>

- [<span data-ttu-id="7d248-116">Configurar la aplicación EWS</span><span class="sxs-lookup"><span data-stu-id="7d248-116">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)   
- [<span data-ttu-id="7d248-117">Cmdlets de Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="7d248-117">Exchange 2013 Cmdlets</span></span>](https://docs.microsoft.com/powershell/exchange/?view=exchange-ps)  
    

