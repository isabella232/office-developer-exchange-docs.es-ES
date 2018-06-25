---
title: Requisitos de redistribución para la API administrada de EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8b206274-eaa4-40d3-b504-af27335c8f43
description: Obtenga información acerca de cómo puede redistribuir los ensamblados de la API administrada de EWS con su aplicación.
ms.openlocfilehash: d8fc57c4a2b3ed7d6218aeeed0fe88c2d3e0fbe0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763294"
---
# <a name="redistribution-requirements-for-the-ews-managed-api"></a><span data-ttu-id="c80ad-103">Requisitos de redistribución para la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="c80ad-103">Redistribution requirements for the EWS Managed API</span></span>

<span data-ttu-id="c80ad-104">Obtenga información acerca de cómo puede redistribuir los ensamblados de la API administrada de EWS con su aplicación.</span><span class="sxs-lookup"><span data-stu-id="c80ad-104">Find out how you can redistribute the EWS Managed API assemblies with your application.</span></span>
  
<span data-ttu-id="c80ad-105">Al diseñar la aplicación de la API administrada de EWS, también desea tener en cuenta cómo se liberará a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="c80ad-105">As you design your EWS Managed API application, you'll also want to consider how you will release it to your users.</span></span> 
  
## <a name="redistributing-your-ews-managed-api-application"></a><span data-ttu-id="c80ad-106">Redistribuir su aplicación de API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="c80ad-106">Redistributing your EWS Managed API application</span></span>

<span data-ttu-id="c80ad-107">A menos que la aplicación se encuentra en el servidor de Exchange, necesita redistribuir los ensamblados de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="c80ad-107">Unless your application is located on the Exchange server, you will need to redistribute the EWS Managed API assemblies.</span></span> <span data-ttu-id="c80ad-108">La descarga de la API administrada de EWS contiene dos ensamblados que se pueden redistribuir: Microsoft.Exchange.WebServices.dll y Microsoft.Exchange.WebServices.Auth.dll.</span><span class="sxs-lookup"><span data-stu-id="c80ad-108">The EWS Managed API download contains two assemblies that you can redistribute: Microsoft.Exchange.WebServices.dll and Microsoft.Exchange.WebServices.Auth.dll.</span></span> <span data-ttu-id="c80ad-109">Cuando diseñe cómo se liberará a la aplicación de la API administrada de EWS, tenga en cuenta la información siguiente:</span><span class="sxs-lookup"><span data-stu-id="c80ad-109">Keep the following information in mind when you design how you will release your EWS Managed API application:</span></span>
  
- <span data-ttu-id="c80ad-110">La API administrada de EWS se ha diseñado para que puede descargarlo y distribuir con la aplicación que se dirige a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c80ad-110">The EWS Managed API was designed such that you can download it and distribute it with your application that targets an Exchange server.</span></span> <span data-ttu-id="c80ad-111">Como alternativa, la aplicación puede descargar la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="c80ad-111">Alternatively, your application can download the EWS Managed API.</span></span>
    
- <span data-ttu-id="c80ad-112">Puede usar la API administrada de EWS para comunicarse con un servidor de Exchange que ejecuta Exchange Online, Exchange Online como parte de Office 365 o una versión local de Exchange a partir de Exchange Server 2007.</span><span class="sxs-lookup"><span data-stu-id="c80ad-112">You can use the EWS Managed API to communicate with an Exchange server running Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange Server 2007.</span></span>
    
- <span data-ttu-id="c80ad-113">En las versiones de la API administrada de EWS empezando con la versión 2.1, puede instalar la API en la caché de ensamblados Global (GAC).</span><span class="sxs-lookup"><span data-stu-id="c80ad-113">In versions of the EWS Managed API starting with version 2.1, you can install the API in the Global Assembly Cache (GAC).</span></span> <span data-ttu-id="c80ad-114">El archivo MSI agregará automáticamente el archivo DLL en la GAC y estará accesible en el equipo por equipo, no en cada usuario.</span><span class="sxs-lookup"><span data-stu-id="c80ad-114">The MSI will automatically add the DLL to the GAC and will be accessible on per computer basis, not on a per user basis.</span></span>
    
<span data-ttu-id="c80ad-115">Los términos de licencia se incluyen en la descarga de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="c80ad-115">The license terms are included in the EWS Managed API download.</span></span> <span data-ttu-id="c80ad-116">Revise los términos para obtener la información relevante acerca de qué puede hacer con la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="c80ad-116">Review the terms for the authoritative information about what you can do with the EWS Managed API.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c80ad-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="c80ad-117">See also</span></span>


- [<span data-ttu-id="c80ad-118">Introducción al diseño de EWS cliente de Exchange</span><span class="sxs-lookup"><span data-stu-id="c80ad-118">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)
    
- [<span data-ttu-id="c80ad-119">API administrada de EWS (descarga)</span><span class="sxs-lookup"><span data-stu-id="c80ad-119">EWS Managed API (download)</span></span>](http://aka.ms/ews-managed-api-readme)
    

