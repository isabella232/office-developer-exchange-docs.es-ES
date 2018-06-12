---
title: Elementos XML de EWS de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Exchange
api_type:
- schema
ms.assetid: 4653466a-a596-456f-bbff-7da4ef1d18d3
description: Buscar información de referencia para el XML EWS elementos en Exchange.
ms.openlocfilehash: 046a985ae4696616d28a0891ffe0aa8cc0552307
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764470"
---
# <a name="ews-xml-elements-in-exchange"></a><span data-ttu-id="85697-103">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="85697-103">EWS XML elements in Exchange</span></span>

<span data-ttu-id="85697-104">Buscar información de referencia para el XML EWS elementos en Exchange.</span><span class="sxs-lookup"><span data-stu-id="85697-104">Find reference information for the EWS XML elements in Exchange.</span></span>
  
<span data-ttu-id="85697-105">Servicios Web de Exchange (EWS) es un servicio web basado en SOAP, lo que significa que los mensajes de solicitud y respuesta que se envían entre el cliente y el servidor se componen de los elementos XML.</span><span class="sxs-lookup"><span data-stu-id="85697-105">Exchange Web Services (EWS) is a SOAP-based web service, which means that the request and response messages that are sent between the client and server are comprised of XML elements.</span></span> <span data-ttu-id="85697-106">La documentación de esta sección se basa en las instancias XML que se envían entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="85697-106">The documentation in this section is based on the XML instances that are sent between the client and server.</span></span> <span data-ttu-id="85697-107">Las instancias de XML se definen en los archivos WSDL y el esquema que se encuentran en el directorio virtual que hospeda EWS.</span><span class="sxs-lookup"><span data-stu-id="85697-107">The XML instances are defined in the WSDL and schema files that are located in the virtual directory that hosts EWS.</span></span> <span data-ttu-id="85697-108">Si es un usuario autenticado, puede buscar los archivos de esquema y WSDL mediante el uso de las siguientes direcciones URL, donde \<yourclientaccessserver\> es el nombre de su servidor de acceso de cliente:</span><span class="sxs-lookup"><span data-stu-id="85697-108">If you are an authenticated user, you can browse to the WSDL and schema files by using the following URLs, where \<yourclientaccessserver\> is the name of your Client Access server:</span></span>
  
- <span data-ttu-id="85697-109">http://\<yourclientaccessserver\>.com/ews/services.wsdl: la ubicación del archivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="85697-109">http://\<yourclientaccessserver\>.com/ews/services.wsdl — The location of the WSDL file.</span></span>
    
- <span data-ttu-id="85697-110">http://\<yourclientaccessserver\>.com/ews/messages.xsd: la ubicación del esquema de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="85697-110">http://\<yourclientaccessserver\>.com/ews/messages.xsd — The location of the messages schema.</span></span>
    
- <span data-ttu-id="85697-111">http://\<yourclientaccessserver\>.com/ews/types.xsd: la ubicación del esquema de tipos.</span><span class="sxs-lookup"><span data-stu-id="85697-111">http://\<yourclientaccessserver\>.com/ews/types.xsd — The location of the types schema.</span></span>
    
<span data-ttu-id="85697-112">Los archivos de esquema que describen los elementos XML de EWS proporcionan una guía general de la estructura XML que es posible que las interacciones del mensaje de respuesta de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="85697-112">The schema files that describe the EWS XML elements provide a general roadmap of the XML structure that is possible for request-response message interactions.</span></span> <span data-ttu-id="85697-113">La estructura XML real que se envía entre cliente y servidor varía según la operación que se llama, la información solicitada y la configuración del servidor.</span><span class="sxs-lookup"><span data-stu-id="85697-113">The actual XML structure that is sent between client and server varies according to the operation that is called, the information requested, and the server-side settings.</span></span>
  
<span data-ttu-id="85697-114">El archivo WSDL de EWS, services.wsdl, no se ajustan totalmente para el estándar WSDL porque no incluye una definición del servicio WSDL.</span><span class="sxs-lookup"><span data-stu-id="85697-114">The EWS WSDL file, services.wsdl, does not fully conform to the WSDL standard because it does not include a WSDL service definition.</span></span> <span data-ttu-id="85697-115">Esto es debido a que EWS no está diseñado para hospedarse en un equipo que tenga una dirección predefinida.</span><span class="sxs-lookup"><span data-stu-id="85697-115">This is because EWS is not designed to be hosted on a computer that has a predefined address.</span></span> <span data-ttu-id="85697-116">Puede usar el servicio Detección automática para obtener la dirección de extremo EWS.</span><span class="sxs-lookup"><span data-stu-id="85697-116">You can use the Autodiscover service to get the EWS endpoint address.</span></span> <span data-ttu-id="85697-117">Algunos generadores de modelo de objetos de cliente analizar el archivo WSDL y pueden encontrar una condición de error porque el archivo WSDL no contiene una definición del servicio WSDL.</span><span class="sxs-lookup"><span data-stu-id="85697-117">Some client-side object model generators parse the WSDL and can encounter an error condition because the WSDL file does not contain a WSDL service definition.</span></span> <span data-ttu-id="85697-118">Si el generador de modelo de objetos encuentra un error, puede insertar un marcador de posición de definición del servicio WSDL.</span><span class="sxs-lookup"><span data-stu-id="85697-118">If your object model generator encounters an error, you can insert a placeholder WSDL service definition.</span></span>
  
> [!TIP]
> <span data-ttu-id="85697-119">Si usa .NET Framework para desarrollar la aplicación, se recomienda que utilice la [API administrada de EWS](http://aka.ms/ews-managed-api-readme), en lugar de un generador de modelo de objetos.</span><span class="sxs-lookup"><span data-stu-id="85697-119">If you are using the .NET Framework to develop your application, we recommend that you use the [EWS Managed API](http://aka.ms/ews-managed-api-readme), rather than an object model generator.</span></span> <span data-ttu-id="85697-120">La API administrada de EWS proporciona un modelo de objetos de fácil de usar para controlar la serialización y deserialización del XML de EWS.</span><span class="sxs-lookup"><span data-stu-id="85697-120">The EWS Managed API provides an easy-to-use object model to handle the serialization and deserialization of the EWS XML.</span></span> <span data-ttu-id="85697-121">Para obtener más información, vea [Introducción a las aplicaciones cliente de API administrada de EWS](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="85697-121">For more information, see [Get started with EWS Managed API client applications](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="85697-122">El archivo de esquema messages.xsd contiene las definiciones de elemento para los elementos de nivel superior en el cuerpo SOAP.</span><span class="sxs-lookup"><span data-stu-id="85697-122">The messages.xsd schema file contains the element definitions for the top-level elements in the SOAP body.</span></span> <span data-ttu-id="85697-123">A excepción de los códigos de respuesta de error, la mayoría de las definiciones de messages.xsd es específica de una operación.</span><span class="sxs-lookup"><span data-stu-id="85697-123">With the exception of the error response codes, most of the definitions in messages.xsd are specific to an operation.</span></span> <span data-ttu-id="85697-124">El esquema types.xsd contiene las definiciones de los encabezados SOAP y todas las definiciones comunes que se comparten en operaciones.</span><span class="sxs-lookup"><span data-stu-id="85697-124">The types.xsd schema contains the definitions for the SOAP headers and all the common definitions that are shared across operations.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="85697-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="85697-125">See also</span></span>

- [<span data-ttu-id="85697-126">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="85697-126">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="85697-127">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="85697-127">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
- [<span data-ttu-id="85697-128">Explore la API administrada de EWS, EWS y servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="85697-128">Explore the EWS Managed API, EWS, and web services in Exchange</span></span>](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [<span data-ttu-id="85697-129">Empezar a utilizar servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="85697-129">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
- [<span data-ttu-id="85697-130">Detección automática de Exchange</span><span class="sxs-lookup"><span data-stu-id="85697-130">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
    

