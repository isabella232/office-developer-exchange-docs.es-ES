---
title: Requisitos de redistribución para la API administrada de EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8b206274-eaa4-40d3-b504-af27335c8f43
description: Descubra cómo puede redistribuir los ensamblados de la API administrada de EWS con su aplicación.
ms.openlocfilehash: e64b4cdb8938caa819ba30621112a25946ef0424
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463828"
---
# <a name="redistribution-requirements-for-the-ews-managed-api"></a><span data-ttu-id="36e4f-103">Requisitos de redistribución para la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="36e4f-103">Redistribution requirements for the EWS Managed API</span></span>

<span data-ttu-id="36e4f-104">Descubra cómo puede redistribuir los ensamblados de la API administrada de EWS con su aplicación.</span><span class="sxs-lookup"><span data-stu-id="36e4f-104">Find out how you can redistribute the EWS Managed API assemblies with your application.</span></span>
  
<span data-ttu-id="36e4f-105">A medida que diseña la aplicación de la API administrada de EWS, también querrá tener en cuenta cómo se lanzará a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="36e4f-105">As you design your EWS Managed API application, you'll also want to consider how you will release it to your users.</span></span> 
  
## <a name="redistributing-your-ews-managed-api-application"></a><span data-ttu-id="36e4f-106">Redistribuir la aplicación de API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="36e4f-106">Redistributing your EWS Managed API application</span></span>

<span data-ttu-id="36e4f-107">A menos que la aplicación se encuentre en el servidor de Exchange, tendrá que redistribuir los ensamblados de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="36e4f-107">Unless your application is located on the Exchange server, you will need to redistribute the EWS Managed API assemblies.</span></span> <span data-ttu-id="36e4f-108">La descarga de la API administrada de EWS contiene dos ensamblados que puede redistribuir: Microsoft. Exchange. webservices. dll y Microsoft. Exchange. webservices. auth. dll.</span><span class="sxs-lookup"><span data-stu-id="36e4f-108">The EWS Managed API download contains two assemblies that you can redistribute: Microsoft.Exchange.WebServices.dll and Microsoft.Exchange.WebServices.Auth.dll.</span></span> <span data-ttu-id="36e4f-109">Tenga en cuenta la siguiente información cuando diseñe el modo en que va a liberar la aplicación de la API administrada de EWS:</span><span class="sxs-lookup"><span data-stu-id="36e4f-109">Keep the following information in mind when you design how you will release your EWS Managed API application:</span></span>
  
- <span data-ttu-id="36e4f-110">La API administrada de EWS se diseñó para poder descargarla y distribuirla con la aplicación destinada a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="36e4f-110">The EWS Managed API was designed such that you can download it and distribute it with your application that targets an Exchange server.</span></span> <span data-ttu-id="36e4f-111">Como alternativa, la aplicación puede descargar la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="36e4f-111">Alternatively, your application can download the EWS Managed API.</span></span>
    
- <span data-ttu-id="36e4f-112">Puede usar la API administrada de EWS para comunicarse con un servidor de Exchange que ejecuta Exchange Online, Exchange online como parte de Office 365 o una versión local de Exchange a partir de Exchange Server 2007.</span><span class="sxs-lookup"><span data-stu-id="36e4f-112">You can use the EWS Managed API to communicate with an Exchange server running Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange Server 2007.</span></span>
    
- <span data-ttu-id="36e4f-113">En las versiones de la API administrada de EWS a partir de la versión 2,1, puede instalar la API en la memoria caché de ensamblados global (GAC).</span><span class="sxs-lookup"><span data-stu-id="36e4f-113">In versions of the EWS Managed API starting with version 2.1, you can install the API in the Global Assembly Cache (GAC).</span></span> <span data-ttu-id="36e4f-114">El MSI agregará automáticamente el archivo DLL a la GAC y será accesible por equipo, no por cada usuario.</span><span class="sxs-lookup"><span data-stu-id="36e4f-114">The MSI will automatically add the DLL to the GAC and will be accessible on per computer basis, not on a per user basis.</span></span>
    
<span data-ttu-id="36e4f-115">Los términos de licencia se incluyen en la descarga de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="36e4f-115">The license terms are included in the EWS Managed API download.</span></span> <span data-ttu-id="36e4f-116">Revise los términos de la información autoritativa sobre lo que puede hacer con la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="36e4f-116">Review the terms for the authoritative information about what you can do with the EWS Managed API.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="36e4f-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="36e4f-117">See also</span></span>


- [<span data-ttu-id="36e4f-118">Introducción al diseño de EWS cliente de Exchange</span><span class="sxs-lookup"><span data-stu-id="36e4f-118">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)
    
- [<span data-ttu-id="36e4f-119">API administrada de EWS (descargar)</span><span class="sxs-lookup"><span data-stu-id="36e4f-119">EWS Managed API (download)</span></span>](https://aka.ms/ews-managed-api-readme)
    

