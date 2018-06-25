---
title: Elementos de Autodiscover XML SOAP para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ae18a5b3-ae44-4cff-8654-db8028565e01
description: Busque información de referencia de elemento XML para el servicio web de detección automática de SOAP en Exchange.
ms.openlocfilehash: 7201ef33060691df70b63d06b2045e1120b0610f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837517"
---
# <a name="soap-autodiscover-xml-elements-for-exchange-2013"></a><span data-ttu-id="e889c-103">Elementos de Autodiscover XML SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="e889c-103">SOAP Autodiscover XML elements for Exchange 2013</span></span>

<span data-ttu-id="e889c-104">Busque información de referencia de elemento XML para el servicio web de detección automática de SOAP en Exchange.</span><span class="sxs-lookup"><span data-stu-id="e889c-104">Find XML element reference information for the SOAP Autodiscover web service in Exchange.</span></span>
  
<span data-ttu-id="e889c-105">La documentación de esta sección se basa en las instancias del elemento XML de detección automática de SOAP que se envían entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="e889c-105">The documentation in this section is based on the SOAP Autodiscover XML element instances that are sent between the client and server.</span></span> <span data-ttu-id="e889c-106">Esta documentación de instancia XML se basa en los archivos WSDL y el esquema que se encuentran en el directorio virtual que hospeda el servicio de detección automática de SOAP.</span><span class="sxs-lookup"><span data-stu-id="e889c-106">This XML instance documentation is based on the WSDL and schema files that are located in the virtual directory that hosts the SOAP Autodiscover service.</span></span> <span data-ttu-id="e889c-107">Los usuarios autenticados pueden examinar los archivos de esquema y WSDL mediante el uso de una dirección URL que es similar a una de las siguientes:</span><span class="sxs-lookup"><span data-stu-id="e889c-107">Authenticated users can browse to the WSDL and schema files by using a URL that is similar to one of the following:</span></span>
  
- <span data-ttu-id="e889c-108">http://\<yourclientaccessserver\>.com/autodiscover/services.wsdl o http://autodiscover.\<yourclientaccessserver\>.com/autodiscover/services.wsdl : la ubicación del archivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="e889c-108">http://\<yourclientaccessserver\>.com/autodiscover/services.wsdl or http://autodiscover.\<yourclientaccessserver\>.com/autodiscover/services.wsdl — The location of the WSDL file.</span></span>
    
- <span data-ttu-id="e889c-109">http://\<yourclientaccessserver\>.com/autodiscover/messages.xsd o http://autodiscover.\<yourclientaccessserver\>.com/autodiscover/messages.xsd : la ubicación del esquema de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="e889c-109">http://\<yourclientaccessserver\>.com/autodiscover/messages.xsd or http://autodiscover.\<yourclientaccessserver\>.com/autodiscover/messages.xsd — The location of the messages schema.</span></span>
    
<span data-ttu-id="e889c-110">La ubicación de los archivos de esquema y SOAP WSDL de detección automática varía en función de la instalación de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e889c-110">The location of the SOAP Autodiscover WSDL and schema files varies based on the Exchange installation.</span></span>
  
<span data-ttu-id="e889c-111">El archivo de esquema messages.xsd describe los elementos XML que se pueden enviar en un encabezado SOAP de detección automática y el cuerpo del mensaje SOAP.</span><span class="sxs-lookup"><span data-stu-id="e889c-111">The messages.xsd schema file describes the XML elements that can be sent in an Autodiscover SOAP header and SOAP body.</span></span> <span data-ttu-id="e889c-112">Este archivo proporciona una guía general de lo que puede ser la estructura XML para una interacción de mensaje de solicitud y respuesta determinado.</span><span class="sxs-lookup"><span data-stu-id="e889c-112">This file provides a general roadmap of what the XML structure can be for a given request-response message interaction.</span></span> <span data-ttu-id="e889c-113">La estructura XML real que se envía entre el cliente y el servidor se basa en las opciones y el contexto en el que se usa.</span><span class="sxs-lookup"><span data-stu-id="e889c-113">The actual XML structure that is sent between the client and server is based on the options and the context in which it is used.</span></span> <span data-ttu-id="e889c-114">Los archivos de esquema definición lo que es posible XML.</span><span class="sxs-lookup"><span data-stu-id="e889c-114">The schema files define what XML is possible.</span></span> <span data-ttu-id="e889c-115">El intervalo real de XML que se envían a través de la conexión se basa en qué operación se denomina, la información solicitada y la configuración del servidor.</span><span class="sxs-lookup"><span data-stu-id="e889c-115">The actual range of XML that is sent over the wire is based on which operation is called, the requested information, and the server-side settings.</span></span> 
  
## <a name="related-sections"></a><span data-ttu-id="e889c-116">Secciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="e889c-116">Related sections</span></span>
<span data-ttu-id="e889c-117"><a name="bk_RelatedSections"> </a></span><span class="sxs-lookup"><span data-stu-id="e889c-117"></span></span>

- [<span data-ttu-id="e889c-118">Referencia de servicio web de detección automática de SOAP para Exchange</span><span class="sxs-lookup"><span data-stu-id="e889c-118">SOAP Autodiscover web service reference for Exchange</span></span>](soap-autodiscover-web-service-reference-for-exchange.md)
    
- [<span data-ttu-id="e889c-119">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="e889c-119">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
    
- [<span data-ttu-id="e889c-120">Referencia de servicio de web de mensajería unificada de Exchange</span><span class="sxs-lookup"><span data-stu-id="e889c-120">Unified Messaging web service reference for Exchange</span></span>](unified-messaging-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="e889c-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="e889c-121">See also</span></span>

- [<span data-ttu-id="e889c-122">Referencia de servicio web de detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="e889c-122">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="e889c-123">Detección automática de Exchange</span><span class="sxs-lookup"><span data-stu-id="e889c-123">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="e889c-124">Empezar a utilizar servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="e889c-124">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

