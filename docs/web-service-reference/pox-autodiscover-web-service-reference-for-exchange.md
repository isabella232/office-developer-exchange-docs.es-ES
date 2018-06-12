---
title: Referencia de servicio web POX de detección automática de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 877152f0-f4b1-4f63-b2ce-924f4bdf2d20
description: Busque información de referencia para el servicio Detección automática POX en Exchange.
ms.openlocfilehash: a8797fe714fd23049094c3ec2475b93fec4282c0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836867"
---
# <a name="pox-autodiscover-web-service-reference-for-exchange"></a><span data-ttu-id="41eeb-103">Referencia de servicio web POX de detección automática de Exchange</span><span class="sxs-lookup"><span data-stu-id="41eeb-103">POX Autodiscover web service reference for Exchange</span></span>

<span data-ttu-id="41eeb-104">Busque información de referencia para el servicio Detección automática POX en Exchange.</span><span class="sxs-lookup"><span data-stu-id="41eeb-104">Find reference information for the POX Autodiscover service in Exchange.</span></span>
  
<span data-ttu-id="41eeb-105">El servicio Detección automática proporciona la información de configuración que la aplicación se usa para crear una conexión a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="41eeb-105">The Autodiscover service provides the configuration information that your application uses to create a connection to an Exchange server.</span></span> <span data-ttu-id="41eeb-106">Puede usar el "XML sin formato antiguo" servicio de detección automática (POX) para enviar mensajes que sólo consisten en cargas XML, sin los sobres SOAP envolventes, con el fin de buscar la configuración de una aplicación de cliente debe tener para poder conectarse a Exchange.</span><span class="sxs-lookup"><span data-stu-id="41eeb-106">You can use the "plain old XML" (POX) Autodiscover service to send messages that consist only of XML payloads, without any enclosing SOAP envelopes, in order to locate the settings that a client application must have in order to connect to Exchange.</span></span>
  
> [!NOTE]
> <span data-ttu-id="41eeb-107">Para los clientes que estén destinados a las versiones de Exchange Server 2010 a partir de Exchange, se recomienda que use el servicio Detección automática de SOAP en lugar del servicio de detección automática de POX.</span><span class="sxs-lookup"><span data-stu-id="41eeb-107">For clients that target versions of Exchange starting with Exchange Server 2010, we recommend that you use the SOAP Autodiscover service instead of the POX Autodiscover service.</span></span> <span data-ttu-id="41eeb-108">Los clientes que estén destinados a Exchange 2007 deben usar el servicio Detección automática POX.</span><span class="sxs-lookup"><span data-stu-id="41eeb-108">Clients that target Exchange 2007 have to use the POX Autodiscover service.</span></span> <span data-ttu-id="41eeb-109">Se recomienda que los clientes que utilicen .NET Framework usan la API administrada de EWS porque contiene a un cliente de detección automática de POX robusto y probado.</span><span class="sxs-lookup"><span data-stu-id="41eeb-109">We recommend that clients that use the .NET Framework use the EWS Managed API because it contains a robust and well-tested POX Autodiscover client.</span></span> <span data-ttu-id="41eeb-110">Para obtener más información acerca de la API administrada de EWS, vea [Introducción a las aplicaciones cliente de API administrada de EWS](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="41eeb-110">For more information about the EWS Managed API, see [Get started with EWS Managed API client applications](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="41eeb-111">En esta sección se proporciona información acerca de los elementos XML que se envían entre el cliente y el servidor durante el redireccionamiento de la solicitud de detección automática POX y la configuración del usuario que se devuelve en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="41eeb-111">This section provides information about the XML elements that are sent between the client and server during POX Autodiscover request redirections and the user settings that are returned in a response.</span></span> <span data-ttu-id="41eeb-112">La referencia de elemento XML contiene resúmenes de los elementos que representan y una descripción de las posibles jerarquías de elemento que usa el elemento.</span><span class="sxs-lookup"><span data-stu-id="41eeb-112">The XML element reference contains summaries of what the elements represent and a description of the potential element hierarchies that use the element.</span></span> <span data-ttu-id="41eeb-113">Esta documentación describen las instancias XML que se envían entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="41eeb-113">This documentation covers the XML instances that are sent between the client and server.</span></span> <span data-ttu-id="41eeb-114">El servicio Detección automática POX no tiene un esquema explícito.</span><span class="sxs-lookup"><span data-stu-id="41eeb-114">The POX Autodiscover service does not have an explicit schema.</span></span>
  
<span data-ttu-id="41eeb-115">Los artículos de esta sección proporcionan ejemplos y descripciones de los mensajes que se usan para recuperar información de configuración de detección automática mediante el servicio de detección automática de POX.</span><span class="sxs-lookup"><span data-stu-id="41eeb-115">The articles in this section provide examples and descriptions of the messages that are used to retrieve Autodiscover configuration information by using the POX Autodiscover service.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="41eeb-116">En esta sección</span><span class="sxs-lookup"><span data-stu-id="41eeb-116">In this section</span></span>
<span data-ttu-id="41eeb-117"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="41eeb-117"></span></span>

- [<span data-ttu-id="41eeb-118">Solicitud de detección automática POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="41eeb-118">POX Autodiscover request for Exchange</span></span>](pox-autodiscover-request-for-exchange.md)
    
- [<span data-ttu-id="41eeb-119">Respuesta de detección automática POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="41eeb-119">POX Autodiscover response for Exchange</span></span>](pox-autodiscover-response-for-exchange.md)
    
- [<span data-ttu-id="41eeb-120">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="41eeb-120">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="41eeb-121">Ver también</span><span class="sxs-lookup"><span data-stu-id="41eeb-121">See also</span></span>

- [<span data-ttu-id="41eeb-122">Referencia de servicio web de detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="41eeb-122">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="41eeb-123">Detección automática de Exchange</span><span class="sxs-lookup"><span data-stu-id="41eeb-123">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)   
- [<span data-ttu-id="41eeb-124">Referencia de servicio web de detección automática de SOAP para Exchange</span><span class="sxs-lookup"><span data-stu-id="41eeb-124">SOAP Autodiscover web service reference for Exchange</span></span>](soap-autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="41eeb-125">Empezar a utilizar servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="41eeb-125">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

