---
title: Referencia del servicio Web de mensajería unificada para Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- Unified
api_type:
- schema
ms.assetid: 83afea8a-c716-41df-9eb2-e1000357afb6
description: Busque contenido de referencia para el servicio Web de mensajería unificada (UM) en Exchange.
ms.openlocfilehash: e4bb63f34650dae8fc28016196c97a6b79e69df0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467378"
---
# <a name="unified-messaging-web-service-reference-for-exchange"></a><span data-ttu-id="4d54b-103">Referencia del servicio Web de mensajería unificada para Exchange</span><span class="sxs-lookup"><span data-stu-id="4d54b-103">Unified Messaging web service reference for Exchange</span></span>

<span data-ttu-id="4d54b-104">Busque contenido de referencia para el servicio Web de mensajería unificada (UM) en Exchange.</span><span class="sxs-lookup"><span data-stu-id="4d54b-104">Find reference content for the Unified Messaging (UM) web service in Exchange.</span></span>
  
<span data-ttu-id="4d54b-105">El servicio Web de mensajería unificada (UM) proporciona un punto de extensibilidad que permite a los clientes leer y cambiar información acerca de las propiedades de mensajería unificada y solicitar que los elementos del almacén de buzones se analicen y dicten a través de un dispositivo de telefonía.</span><span class="sxs-lookup"><span data-stu-id="4d54b-105">The Unified Messaging (UM) web service provides an extensibility point that enables clients to read and change information about UM properties and request that mailbox store items be parsed and dictated over a telephony device.</span></span> <span data-ttu-id="4d54b-106">Esta sección contiene información sobre las operaciones y los elementos que conforman los mensajes XML para el servicio Web de mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="4d54b-106">This section contains information about the operations and elements that make up the XML messages for the UM web service.</span></span> <span data-ttu-id="4d54b-107">Este contenido se aplica a la dirección URL del punto de conexión de servicio que es similar a https:// \<yourclientaccessserver\> . com/EWS/UM2007Legacy. asmx.</span><span class="sxs-lookup"><span data-stu-id="4d54b-107">This content applies to the service endpoint URL that is similar to https://\<yourclientaccessserver\>.com/EWS/UM2007Legacy.asmx.</span></span> 
  
<span data-ttu-id="4d54b-108">Puede usar el servicio de detección automática para obtener la dirección URL del extremo del servicio Web de mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="4d54b-108">You can use the Autodiscover service to get the URL to the UM web service endpoint.</span></span> <span data-ttu-id="4d54b-109">Para obtener más información acerca de la detección automática, consulte [detección automática de Exchange](../exchange-web-services/autodiscover-for-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="4d54b-109">For more information about Autodiscover, see [Autodiscover for Exchange](../exchange-web-services/autodiscover-for-exchange.md).</span></span>
  
> [!NOTE]
>  <span data-ttu-id="4d54b-110">Para las versiones de Exchange a partir de Exchange 2010, le recomendamos que use las operaciones de mensajería unificada que están disponibles en los [servicios web Exchange (EWS)](https://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) en lugar del servicio Web de mensajería unificada, por los siguientes motivos:</span><span class="sxs-lookup"><span data-stu-id="4d54b-110">For versions of Exchange starting with Exchange 2010, we recommend that you use the Unified Messaging operations that are available in [Exchange Web Services (EWS)](https://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) instead of the UM web service, for the following reasons:</span></span> 
> - <span data-ttu-id="4d54b-111">Las características de mensajería unificada basadas en EWS tienen compatibilidad de primera clase en la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="4d54b-111">The EWS-based UM features have first-class support in the EWS Managed API.</span></span> 
> - <span data-ttu-id="4d54b-112">En las versiones de Exchange a partir de Exchange 2010, se agregan nuevas características de mensajería unificada a EWS, pero no al servicio Web de mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="4d54b-112">In versions of Exchange starting with Exchange 2010, new UM features are added to EWS but not to the Unified Messaging web service.</span></span> 
  
<span data-ttu-id="4d54b-113">El servicio Web de mensajería unificada no tiene un esquema explícito.</span><span class="sxs-lookup"><span data-stu-id="4d54b-113">The UM web service does not have an explicit schema.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="4d54b-114">En esta sección</span><span class="sxs-lookup"><span data-stu-id="4d54b-114">In this section</span></span>
<span data-ttu-id="4d54b-115"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="4d54b-115"><a name="bk_InThisSection"> </a></span></span>

- [<span data-ttu-id="4d54b-116">Operaciones del servicio Web de mensajería unificada para Exchange</span><span class="sxs-lookup"><span data-stu-id="4d54b-116">Unified Messaging web service operations for Exchange</span></span>](unified-messaging-web-service-operations-for-exchange.md)   
- [<span data-ttu-id="4d54b-117">Elementos XML de servicio Web de mensajería unificada para Exchange</span><span class="sxs-lookup"><span data-stu-id="4d54b-117">Unified Messaging web service XML elements for Exchange</span></span>](unified-messaging-web-service-xml-elements-for-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="4d54b-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d54b-118">See also</span></span>

- [<span data-ttu-id="4d54b-119">Referencia del servicio web de Detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="4d54b-119">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="4d54b-120">Detección automática en Exchange</span><span class="sxs-lookup"><span data-stu-id="4d54b-120">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="4d54b-121">Empezar a usar los servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="4d54b-121">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

