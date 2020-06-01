---
title: Elementos XML de detección automática de SOAP para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ae18a5b3-ae44-4cff-8654-db8028565e01
description: Buscar información de referencia de elemento XML para el servicio Web de detección automática de SOAP en Exchange.
ms.openlocfilehash: 3b88429488dbecd4ed7c3adf56462f34fa0d4b17
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465187"
---
# <a name="soap-autodiscover-xml-elements-for-exchange-2013"></a><span data-ttu-id="cd842-103">Elementos XML de detección automática de SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="cd842-103">SOAP Autodiscover XML elements for Exchange 2013</span></span>

<span data-ttu-id="cd842-104">Buscar información de referencia de elemento XML para el servicio Web de detección automática de SOAP en Exchange.</span><span class="sxs-lookup"><span data-stu-id="cd842-104">Find XML element reference information for the SOAP Autodiscover web service in Exchange.</span></span>
  
<span data-ttu-id="cd842-105">La documentación de esta sección se basa en las instancias del elemento XML de detección automática de SOAP que se envían entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="cd842-105">The documentation in this section is based on the SOAP Autodiscover XML element instances that are sent between the client and server.</span></span> <span data-ttu-id="cd842-106">Esta documentación de instancia XML se basa en los archivos WSDL y de esquema que se encuentran en el directorio virtual que hospeda el servicio Detección automática de SOAP.</span><span class="sxs-lookup"><span data-stu-id="cd842-106">This XML instance documentation is based on the WSDL and schema files that are located in the virtual directory that hosts the SOAP Autodiscover service.</span></span> <span data-ttu-id="cd842-107">Los usuarios autenticados pueden ir a los archivos de esquema y WSDL mediante una dirección URL similar a una de las siguientes:</span><span class="sxs-lookup"><span data-stu-id="cd842-107">Authenticated users can browse to the WSDL and schema files by using a URL that is similar to one of the following:</span></span>
  
- <span data-ttu-id="cd842-108">La ubicación del archivo WSDL: `http://<yourclientaccessserver>.com/autodiscover/services.wsdl` o`http://autodiscover.<yourclientaccessserver>.com/autodiscover/services.wsdl`</span><span class="sxs-lookup"><span data-stu-id="cd842-108">The location of the WSDL file: `http://<yourclientaccessserver>.com/autodiscover/services.wsdl` or `http://autodiscover.<yourclientaccessserver>.com/autodiscover/services.wsdl`</span></span>
    
- <span data-ttu-id="cd842-109">La ubicación del esquema de mensajes: `http://<yourclientaccessserver>.com/autodiscover/messages.xsd` o`http://autodiscover.<yourclientaccessserver>.com/autodiscover/messages.xsd`</span><span class="sxs-lookup"><span data-stu-id="cd842-109">The location of the messages schema: `http://<yourclientaccessserver>.com/autodiscover/messages.xsd` or `http://autodiscover.<yourclientaccessserver>.com/autodiscover/messages.xsd`</span></span> 
    
<span data-ttu-id="cd842-110">La ubicación de los archivos de esquema y WSDL de detección automática de SOAP varía en función de la instalación de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cd842-110">The location of the SOAP Autodiscover WSDL and schema files varies based on the Exchange installation.</span></span>
  
<span data-ttu-id="cd842-111">El archivo de esquema messages. xsd describe los elementos XML que se pueden enviar en un encabezado SOAP de detección automática y un cuerpo SOAP.</span><span class="sxs-lookup"><span data-stu-id="cd842-111">The messages.xsd schema file describes the XML elements that can be sent in an Autodiscover SOAP header and SOAP body.</span></span> <span data-ttu-id="cd842-112">Este archivo proporciona un mapa de ruta general de la estructura XML que puede utilizarse para una interacción de mensajes de solicitud-respuesta determinada.</span><span class="sxs-lookup"><span data-stu-id="cd842-112">This file provides a general roadmap of what the XML structure can be for a given request-response message interaction.</span></span> <span data-ttu-id="cd842-113">La estructura XML real que se envía entre el cliente y el servidor se basa en las opciones y en el contexto en el que se usa.</span><span class="sxs-lookup"><span data-stu-id="cd842-113">The actual XML structure that is sent between the client and server is based on the options and the context in which it is used.</span></span> <span data-ttu-id="cd842-114">Los archivos de esquema definen qué XML es posible.</span><span class="sxs-lookup"><span data-stu-id="cd842-114">The schema files define what XML is possible.</span></span> <span data-ttu-id="cd842-115">El intervalo real de XML que se envía por el cable se basa en qué operación se llama, la información solicitada y la configuración del servidor.</span><span class="sxs-lookup"><span data-stu-id="cd842-115">The actual range of XML that is sent over the wire is based on which operation is called, the requested information, and the server-side settings.</span></span> 
  
## <a name="related-sections"></a><span data-ttu-id="cd842-116">Secciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="cd842-116">Related sections</span></span>

- [<span data-ttu-id="cd842-117">Referencia del servicio Web de detección automática de SOAP para Exchange</span><span class="sxs-lookup"><span data-stu-id="cd842-117">SOAP Autodiscover web service reference for Exchange</span></span>](soap-autodiscover-web-service-reference-for-exchange.md)    
- [<span data-ttu-id="cd842-118">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="cd842-118">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)    
- [<span data-ttu-id="cd842-119">Referencia del servicio Web de mensajería unificada para Exchange</span><span class="sxs-lookup"><span data-stu-id="cd842-119">Unified Messaging web service reference for Exchange</span></span>](unified-messaging-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="cd842-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd842-120">See also</span></span>

- [<span data-ttu-id="cd842-121">Referencia del servicio web de Detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="cd842-121">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="cd842-122">Detección automática en Exchange</span><span class="sxs-lookup"><span data-stu-id="cd842-122">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="cd842-123">Empezar a usar los servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="cd842-123">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

