---
title: Referencia de servicio web de detección automática para Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a01124a8-a8cf-4b80-8625-d7ee05690bca
description: Buscar contenido de referencia para el servicio web de detección automática en Exchange.
ms.openlocfilehash: 48ca4a93c2120079cb675eabbc460bf0e75570b2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763590"
---
# <a name="autodiscover-web-service-reference-for-exchange"></a><span data-ttu-id="a311a-103">Referencia de servicio web de detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="a311a-103">Autodiscover web service reference for Exchange</span></span>

<span data-ttu-id="a311a-104">Buscar contenido de referencia para el servicio web de detección automática en Exchange.</span><span class="sxs-lookup"><span data-stu-id="a311a-104">Find reference content for the Autodiscover web service in Exchange.</span></span>
  
<span data-ttu-id="a311a-105">El servicio web de detección automática proporciona la información de configuración que la aplicación se usa para crear una conexión a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a311a-105">The Autodiscover web service provides the configuration information that your application uses to create a connection to an Exchange server.</span></span> <span data-ttu-id="a311a-106">Puede usar una de las siguientes opciones para conectarse a la detección automática:</span><span class="sxs-lookup"><span data-stu-id="a311a-106">You can use one of the following options to connect to Autodiscover:</span></span>
  
- <span data-ttu-id="a311a-107">Servicio de detección automática SOAP: disponible para los clientes que se conectan a las versiones de Exchange a partir de Exchange 2010, incluido Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="a311a-107">SOAP Autodiscover service —Available to clients that connect to versions of Exchange starting with Exchange 2010, including Exchange Online.</span></span>
    
- <span data-ttu-id="a311a-108">"sin formato XML antiguo" servicio de detección automática (POX): disponible para los clientes que se conectan a las versiones de Exchange a partir de Exchange 2007, incluido Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="a311a-108">"plain old XML" (POX) Autodiscover service — Available to clients that connect to versions of Exchange starting with Exchange 2007, including Exchange Online.</span></span> 
    
<span data-ttu-id="a311a-109">El mensaje SOAP y el servicio Detección automática POX pueden proporcionar la información de configuración que va a usar el cliente para crear una conexión a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a311a-109">Both the SOAP and the POX Autodiscover service can provide the configuration information that your client will use to create a connection to an Exchange server.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a311a-110">Para las versiones de Exchange 2010 a partir de Exchange, se recomienda que use el servicio Detección automática de SOAP en lugar del servicio de detección automática de POX.</span><span class="sxs-lookup"><span data-stu-id="a311a-110">For versions of Exchange starting with Exchange 2010, we recommend that you use the SOAP Autodiscover service instead of the POX Autodiscover service.</span></span> <span data-ttu-id="a311a-111">El servicio de detección automática de SOAP proporciona solicitudes por lotes de configuración de detección automática y un mayor control sobre qué configuración se devuelve en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a311a-111">The SOAP Autodiscover service provides batched Autodiscover setting requests and more granular control over which settings are returned in the response.</span></span> 
  
<span data-ttu-id="a311a-112">Esta sección contiene información de referencia para el servicio Detección automática de SOAP y el servicio de detección automática de POX.</span><span class="sxs-lookup"><span data-stu-id="a311a-112">This section contains reference information for the SOAP Autodiscover service and the POX Autodiscover service.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="a311a-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="a311a-113">In this section</span></span>
<span data-ttu-id="a311a-114"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="a311a-114"></span></span>

- [<span data-ttu-id="a311a-115">Referencia de servicio web de detección automática de SOAP para Exchange</span><span class="sxs-lookup"><span data-stu-id="a311a-115">SOAP Autodiscover web service reference for Exchange</span></span>](soap-autodiscover-web-service-reference-for-exchange.md)
    
- [<span data-ttu-id="a311a-116">Referencia de servicio web POX de detección automática de Exchange</span><span class="sxs-lookup"><span data-stu-id="a311a-116">POX Autodiscover web service reference for Exchange</span></span>](pox-autodiscover-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="a311a-117">Ver también</span><span class="sxs-lookup"><span data-stu-id="a311a-117">See also</span></span>

- [<span data-ttu-id="a311a-118">Referencia de servicios Web de Exchange</span><span class="sxs-lookup"><span data-stu-id="a311a-118">Web services reference for Exchange</span></span>](web-services-reference-for-exchange.md)
- [<span data-ttu-id="a311a-119">Servicio de detección automática (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a311a-119">Autodiscover Service (SOAP)</span></span>](http://msdn.microsoft.com/library/e24d1a1f-0d20-4bd9-ae4c-9112ecacea78%28Office.15%29.aspx)
- [<span data-ttu-id="a311a-120">Servicio de detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="a311a-120">Autodiscover Service (POX)</span></span>](http://msdn.microsoft.com/library/13c54de3-a91c-4424-8732-99dd8f2162ec%28Office.15%29.aspx)
    

