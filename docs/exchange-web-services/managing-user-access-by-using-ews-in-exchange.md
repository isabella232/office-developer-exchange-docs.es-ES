---
title: Administrar el acceso de usuario mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 48f0170c-8786-405f-86cb-568b7314a425
description: Averigüe cuáles son las opciones para administrar el acceso de la cuenta de usuario a su servidor de Exchange.
ms.openlocfilehash: d93f521f08f93b44b4ecc1f258b03ed24ebdd3dd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763205"
---
# <a name="managing-user-access-by-using-ews-in-exchange"></a><span data-ttu-id="2034f-103">Administrar el acceso de usuario mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2034f-103">Managing user access by using EWS in Exchange</span></span>

<span data-ttu-id="2034f-104">Averigüe cuáles son las opciones para administrar el acceso de la cuenta de usuario a su servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2034f-104">Find out what your options are for managing user account access to your Exchange server.</span></span>
  
<span data-ttu-id="2034f-105">API administrada de servicios de Web Exchange (EWS) y la dirección URL de EWS proporcionar un número limitado de operaciones que puede usar para administrar las cuentas de Exchange Online, Exchange Online como parte de Office 365 o una versión de Exchange a partir de Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="2034f-105">Exchange Web Services (EWS) and the EWS managed API provide a limited number of operations that you can use to manage accounts on Exchange Online, Exchange Online as part of Office 365, or a version of Exchange starting with Exchange 2013.</span></span> <span data-ttu-id="2034f-106">Puede usar las operaciones que se muestra en la ilustración siguiente para administrar los delegados y para establecer permisos de acceso de carpeta para otras cuentas.</span><span class="sxs-lookup"><span data-stu-id="2034f-106">You can use the operations shown in the following figure to manage delegates and to set folder access permissions for other accounts.</span></span> 
  
<span data-ttu-id="2034f-107">**Operaciones de EWS para el acceso de delegado y carpeta**</span><span class="sxs-lookup"><span data-stu-id="2034f-107">**EWS operations for delegate and folder access**</span></span>

![Opciones de administración de usuarios de EWS.](media/Exchange_ManagingUserAccess_1.png)
  
<span data-ttu-id="2034f-109">Si la aplicación necesita un control adicional sobre las cuentas en un servidor de Exchange, puede usar los cmdlets del Shell de administración de Exchange para administrar las cuentas.</span><span class="sxs-lookup"><span data-stu-id="2034f-109">If your application needs additional control over the accounts on an Exchange server, you can use Exchange Management Shell cmdlets to manage the accounts.</span></span> <span data-ttu-id="2034f-110">Puede llamar a los cmdlets del Shell de administración de Exchange, realice una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="2034f-110">You can call the Exchange Management Shell cmdlets by doing one of the following:</span></span>
  
- <span data-ttu-id="2034f-111">Escribir una aplicación con C# o Visual Basic que llama a los cmdlets del Shell de administración de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2034f-111">Writing an application using C# or Visual Basic that calls the Exchange Management Shell cmdlets.</span></span> <span data-ttu-id="2034f-112">Puede buscar en el código de ejemplo en la [documentación de la API de Shell de administración de Exchange](../management/exchange-management-shell.md) para obtener información sobre cómo llamar a un cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2034f-112">You can look at the sample code in the [Exchange Management Shell API documentation](../management/exchange-management-shell.md) to learn how to call a cmdlet.</span></span> 
    
- <span data-ttu-id="2034f-113">Uso de Windows PowerShell y scripts de Windows PowerShell para llamar a los cmdlets del Shell de administración de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2034f-113">Using Windows PowerShell and Windows PowerShell scripts to call Exchange Management Shell cmdlets.</span></span> <span data-ttu-id="2034f-114">Puede encontrar una lista completa de la [Exchange Server PowerShell (Shell de administración de Exchange)](https://docs.microsoft.com/es-es/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps), junto con ejemplos que muestran cómo usarlas.</span><span class="sxs-lookup"><span data-stu-id="2034f-114">You can find a complete list of the [Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/es-es/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps), along with examples that show how to use them.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2034f-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="2034f-115">See also</span></span>

- [<span data-ttu-id="2034f-116">Configurar una aplicación de EWS</span><span class="sxs-lookup"><span data-stu-id="2034f-116">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)   
- [<span data-ttu-id="2034f-117">Cmdlets de Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="2034f-117">Exchange 2013 Cmdlets</span></span>](https://docs.microsoft.com/es-es/powershell/exchange/?view=exchange-ps)  
    

