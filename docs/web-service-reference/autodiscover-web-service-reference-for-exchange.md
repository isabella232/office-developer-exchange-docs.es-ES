---
title: Referencia del servicio web de Detección automática para Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a01124a8-a8cf-4b80-8625-d7ee05690bca
description: Busque contenido de referencia para el servicio Web de detección automática en Exchange.
ms.openlocfilehash: ce7f2bbd662a5e61959c7e3c6748f0cf40cc4fb3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466874"
---
# <a name="autodiscover-web-service-reference-for-exchange"></a><span data-ttu-id="f7fdf-103">Referencia del servicio web de Detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="f7fdf-103">Autodiscover web service reference for Exchange</span></span>

<span data-ttu-id="f7fdf-104">Busque contenido de referencia para el servicio Web de detección automática en Exchange.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-104">Find reference content for the Autodiscover web service in Exchange.</span></span>
  
<span data-ttu-id="f7fdf-105">El servicio Web de detección automática proporciona la información de configuración que la aplicación usa para crear una conexión a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-105">The Autodiscover web service provides the configuration information that your application uses to create a connection to an Exchange server.</span></span> <span data-ttu-id="f7fdf-106">Puede usar una de las siguientes opciones para conectarse a detección automática:</span><span class="sxs-lookup"><span data-stu-id="f7fdf-106">You can use one of the following options to connect to Autodiscover:</span></span>
  
- <span data-ttu-id="f7fdf-107">Servicio Detección automática de SOAP: disponible para los clientes que se conectan a las versiones de Exchange a partir de Exchange 2010, incluido Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-107">SOAP Autodiscover service —Available to clients that connect to versions of Exchange starting with Exchange 2010, including Exchange Online.</span></span>
    
- <span data-ttu-id="f7fdf-108">el servicio Detección automática "XML antiguo" (POX), disponible para los clientes que se conectan a las versiones de Exchange a partir de Exchange 2007, incluido Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-108">"plain old XML" (POX) Autodiscover service — Available to clients that connect to versions of Exchange starting with Exchange 2007, including Exchange Online.</span></span> 
    
<span data-ttu-id="f7fdf-109">El servicio Detección automática de POX y SOAP puede proporcionar la información de configuración que el cliente usará para crear una conexión a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-109">Both the SOAP and the POX Autodiscover service can provide the configuration information that your client will use to create a connection to an Exchange server.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f7fdf-110">Para las versiones de Exchange a partir de Exchange 2010, se recomienda usar el servicio Detección automática de SOAP en lugar del servicio Detección automática de POX.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-110">For versions of Exchange starting with Exchange 2010, we recommend that you use the SOAP Autodiscover service instead of the POX Autodiscover service.</span></span> <span data-ttu-id="f7fdf-111">El servicio Detección automática de SOAP proporciona solicitudes de configuración de detección automática por lotes y un control más granular sobre la configuración que se devuelve en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-111">The SOAP Autodiscover service provides batched Autodiscover setting requests and more granular control over which settings are returned in the response.</span></span> 
  
<span data-ttu-id="f7fdf-112">Esta sección contiene información de referencia para el servicio Detección automática de SOAP y el servicio Detección automática de POX.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-112">This section contains reference information for the SOAP Autodiscover service and the POX Autodiscover service.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="f7fdf-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="f7fdf-113">In this section</span></span>
<span data-ttu-id="f7fdf-114"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="f7fdf-114"><a name="bk_InThisSection"> </a></span></span>

- [<span data-ttu-id="f7fdf-115">Referencia del servicio Web de detección automática de SOAP para Exchange</span><span class="sxs-lookup"><span data-stu-id="f7fdf-115">SOAP Autodiscover web service reference for Exchange</span></span>](soap-autodiscover-web-service-reference-for-exchange.md)
    
- [<span data-ttu-id="f7fdf-116">Referencia de servicio Web de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="f7fdf-116">POX Autodiscover web service reference for Exchange</span></span>](pox-autodiscover-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="f7fdf-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7fdf-117">See also</span></span>

- [<span data-ttu-id="f7fdf-118">Referencia de servicios web para Exchange</span><span class="sxs-lookup"><span data-stu-id="f7fdf-118">Web services reference for Exchange</span></span>](web-services-reference-for-exchange.md)
- [<span data-ttu-id="f7fdf-119">Servicio Detección automática (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f7fdf-119">Autodiscover Service (SOAP)</span></span>](https://msdn.microsoft.com/library/e24d1a1f-0d20-4bd9-ae4c-9112ecacea78%28Office.15%29.aspx)
- [<span data-ttu-id="f7fdf-120">Servicio Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="f7fdf-120">Autodiscover Service (POX)</span></span>](https://msdn.microsoft.com/library/13c54de3-a91c-4424-8732-99dd8f2162ec%28Office.15%29.aspx)
    

