---
title: Referencia de servicio de web de mensajería unificada de Exchange
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
description: Buscar contenido de referencia para el servicio web de mensajería unificada (UM) de Exchange.
ms.openlocfilehash: 12ee91c5a8b7e1ba23b937f142a9ae2835697fef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840756"
---
# <a name="unified-messaging-web-service-reference-for-exchange"></a><span data-ttu-id="5578c-103">Referencia de servicio de web de mensajería unificada de Exchange</span><span class="sxs-lookup"><span data-stu-id="5578c-103">Unified Messaging web service reference for Exchange</span></span>

<span data-ttu-id="5578c-104">Buscar contenido de referencia para el servicio web de mensajería unificada (UM) de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5578c-104">Find reference content for the Unified Messaging (UM) web service in Exchange.</span></span>
  
<span data-ttu-id="5578c-105">El servicio web de mensajería unificada (UM) proporciona un punto de extensibilidad que permite a los clientes leer y cambiar la información acerca de las propiedades de mensajería unificada y solicitar que los elementos del almacén de buzón se analizado y determinados a través de un dispositivo de telefonía.</span><span class="sxs-lookup"><span data-stu-id="5578c-105">The Unified Messaging (UM) web service provides an extensibility point that enables clients to read and change information about UM properties and request that mailbox store items be parsed and dictated over a telephony device.</span></span> <span data-ttu-id="5578c-106">Esta sección contiene información acerca de las operaciones y los elementos que componen los mensajes XML para el servicio web de mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="5578c-106">This section contains information about the operations and elements that make up the XML messages for the UM web service.</span></span> <span data-ttu-id="5578c-107">Este contenido se aplica a la dirección URL de extremo de servicio que es similar a https://\<yourclientaccessserver\>.com/EWS/UM2007Legacy.asmx.</span><span class="sxs-lookup"><span data-stu-id="5578c-107">This content applies to the service endpoint URL that is similar to https://\<yourclientaccessserver\>.com/EWS/UM2007Legacy.asmx.</span></span> 
  
<span data-ttu-id="5578c-108">Puede usar el servicio Detección automática para obtener la dirección URL para el extremo de servicio web de mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="5578c-108">You can use the Autodiscover service to get the URL to the UM web service endpoint.</span></span> <span data-ttu-id="5578c-109">Para obtener más información acerca de la detección automática, vea [detección automática de Exchange](../exchange-web-services/autodiscover-for-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="5578c-109">For more information about Autodiscover, see [Autodiscover for Exchange](../exchange-web-services/autodiscover-for-exchange.md).</span></span>
  
> [!NOTE]
>  <span data-ttu-id="5578c-110">Para las versiones de Exchange 2010 a partir de Exchange, se recomienda que use las operaciones de mensajería unificada que están disponibles en [Exchange Web Services (EWS)](http://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) en lugar del servicio web de mensajería unificada, por los motivos siguientes: > tienen características de mensajería unificada en función de la dirección URL de EWS soporte de primera clase en la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="5578c-110">For versions of Exchange starting with Exchange 2010, we recommend that you use the Unified Messaging operations that are available in [Exchange Web Services (EWS)](http://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) instead of the UM web service, for the following reasons: >  The EWS-based UM features have first-class support in the EWS Managed API.</span></span> <span data-ttu-id="5578c-111">> En las versiones de Exchange a partir de Exchange 2010, se agregan nuevas características de mensajería unificada para EWS, pero no para el servicio web de mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="5578c-111">>  In versions of Exchange starting with Exchange 2010, new UM features are added to EWS but not to the Unified Messaging web service.</span></span> 
  
<span data-ttu-id="5578c-112">El servicio web de mensajería unificada no tiene un esquema explícito.</span><span class="sxs-lookup"><span data-stu-id="5578c-112">The UM web service does not have an explicit schema.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="5578c-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="5578c-113">In this section</span></span>
<span data-ttu-id="5578c-114"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="5578c-114"></span></span>

- [<span data-ttu-id="5578c-115">Operaciones de servicio de web de mensajería unificadas para Exchange</span><span class="sxs-lookup"><span data-stu-id="5578c-115">Unified Messaging web service operations for Exchange</span></span>](unified-messaging-web-service-operations-for-exchange.md)
    
- [<span data-ttu-id="5578c-116">Elementos XML de servicio de web de Unified Messaging para Exchange</span><span class="sxs-lookup"><span data-stu-id="5578c-116">Unified Messaging web service XML elements for Exchange</span></span>](unified-messaging-web-service-xml-elements-for-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="5578c-117">Ver también</span><span class="sxs-lookup"><span data-stu-id="5578c-117">See also</span></span>

- [<span data-ttu-id="5578c-118">Referencia de servicio web de detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="5578c-118">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="5578c-119">Detección automática de Exchange</span><span class="sxs-lookup"><span data-stu-id="5578c-119">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="5578c-120">Empezar a utilizar servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="5578c-120">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

