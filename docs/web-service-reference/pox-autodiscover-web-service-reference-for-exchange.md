---
title: Referencia de servicio Web de detección automática de POX para Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 877152f0-f4b1-4f63-b2ce-924f4bdf2d20
description: Busque información de referencia para el servicio Detección automática de POX en Exchange.
ms.openlocfilehash: 3c0ca368f4427be7759e2db58fb418b4822dea8e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465656"
---
# <a name="pox-autodiscover-web-service-reference-for-exchange"></a><span data-ttu-id="8e818-103">Referencia de servicio Web de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="8e818-103">POX Autodiscover web service reference for Exchange</span></span>

<span data-ttu-id="8e818-104">Busque información de referencia para el servicio Detección automática de POX en Exchange.</span><span class="sxs-lookup"><span data-stu-id="8e818-104">Find reference information for the POX Autodiscover service in Exchange.</span></span>
  
<span data-ttu-id="8e818-105">El servicio Detección automática proporciona la información de configuración que la aplicación usa para crear una conexión a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8e818-105">The Autodiscover service provides the configuration information that your application uses to create a connection to an Exchange server.</span></span> <span data-ttu-id="8e818-106">Puede usar el servicio de detección automática "XML anterior" (POX) para enviar mensajes que consten solo de cargas XML, sin ningún envoltorio SOAP envolvente, para localizar la configuración que debe tener una aplicación cliente para conectarse a Exchange.</span><span class="sxs-lookup"><span data-stu-id="8e818-106">You can use the "plain old XML" (POX) Autodiscover service to send messages that consist only of XML payloads, without any enclosing SOAP envelopes, in order to locate the settings that a client application must have in order to connect to Exchange.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8e818-107">Para los clientes que tienen como destino versiones de Exchange que comienzan con Exchange Server 2010, se recomienda usar el servicio de detección automática de SOAP en lugar del servicio Detección automática de POX.</span><span class="sxs-lookup"><span data-stu-id="8e818-107">For clients that target versions of Exchange starting with Exchange Server 2010, we recommend that you use the SOAP Autodiscover service instead of the POX Autodiscover service.</span></span> <span data-ttu-id="8e818-108">Los clientes que tienen el destino de Exchange 2007 deben usar el servicio Detección automática de POX.</span><span class="sxs-lookup"><span data-stu-id="8e818-108">Clients that target Exchange 2007 have to use the POX Autodiscover service.</span></span> <span data-ttu-id="8e818-109">Se recomienda que los clientes que usan .NET Framework usen la API administrada de EWS porque contiene un cliente de detección automática de POX sólido y bien probado.</span><span class="sxs-lookup"><span data-stu-id="8e818-109">We recommend that clients that use the .NET Framework use the EWS Managed API because it contains a robust and well-tested POX Autodiscover client.</span></span> <span data-ttu-id="8e818-110">Para obtener más información sobre la API administrada de EWS, vea Introducción [a las aplicaciones cliente de la API administrada de EWS](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8e818-110">For more information about the EWS Managed API, see [Get started with EWS Managed API client applications](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="8e818-111">En esta sección se proporciona información sobre los elementos XML que se envían entre el cliente y el servidor durante la redirección de la solicitud de detección automática de POX y la configuración de usuario que se devuelve en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="8e818-111">This section provides information about the XML elements that are sent between the client and server during POX Autodiscover request redirections and the user settings that are returned in a response.</span></span> <span data-ttu-id="8e818-112">La referencia del elemento XML contiene resúmenes de lo que representan los elementos y una descripción de las jerarquías de elementos potenciales que usan el elemento.</span><span class="sxs-lookup"><span data-stu-id="8e818-112">The XML element reference contains summaries of what the elements represent and a description of the potential element hierarchies that use the element.</span></span> <span data-ttu-id="8e818-113">En esta documentación se describen las instancias de XML que se envían entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="8e818-113">This documentation covers the XML instances that are sent between the client and server.</span></span> <span data-ttu-id="8e818-114">El servicio Detección automática de POX no tiene un esquema explícito.</span><span class="sxs-lookup"><span data-stu-id="8e818-114">The POX Autodiscover service does not have an explicit schema.</span></span>
  
<span data-ttu-id="8e818-115">En los artículos de esta sección se proporcionan ejemplos y descripciones de los mensajes que se usan para recuperar información de configuración de detección automática mediante el servicio Detección automática de POX.</span><span class="sxs-lookup"><span data-stu-id="8e818-115">The articles in this section provide examples and descriptions of the messages that are used to retrieve Autodiscover configuration information by using the POX Autodiscover service.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="8e818-116">En esta sección</span><span class="sxs-lookup"><span data-stu-id="8e818-116">In this section</span></span>
<span data-ttu-id="8e818-117"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="8e818-117"><a name="bk_InThisSection"> </a></span></span>

- [<span data-ttu-id="8e818-118">Solicitud de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="8e818-118">POX Autodiscover request for Exchange</span></span>](pox-autodiscover-request-for-exchange.md)
    
- [<span data-ttu-id="8e818-119">Respuesta de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="8e818-119">POX Autodiscover response for Exchange</span></span>](pox-autodiscover-response-for-exchange.md)
    
- [<span data-ttu-id="8e818-120">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="8e818-120">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="8e818-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e818-121">See also</span></span>

- [<span data-ttu-id="8e818-122">Referencia del servicio web de Detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="8e818-122">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="8e818-123">Detección automática en Exchange</span><span class="sxs-lookup"><span data-stu-id="8e818-123">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)   
- [<span data-ttu-id="8e818-124">Referencia del servicio Web de detección automática de SOAP para Exchange</span><span class="sxs-lookup"><span data-stu-id="8e818-124">SOAP Autodiscover web service reference for Exchange</span></span>](soap-autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="8e818-125">Empezar a usar los servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="8e818-125">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

