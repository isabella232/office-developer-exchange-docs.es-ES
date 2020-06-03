---
title: Elementos XML de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- Exchange
api_type:
- schema
ms.assetid: 4653466a-a596-456f-bbff-7da4ef1d18d3
description: Busque información de referencia para los elementos XML de EWS en Exchange.
localization_priority: Priority
ms.openlocfilehash: 29b90ad137141e30484ef804b6fcb6bb049ef3e8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526119"
---
# <a name="ews-xml-elements-in-exchange"></a><span data-ttu-id="51caa-103">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="51caa-103">EWS XML elements in Exchange</span></span>

<span data-ttu-id="51caa-104">Busque información de referencia para los elementos XML de EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="51caa-104">Find reference information for the EWS XML elements in Exchange.</span></span>
  
<span data-ttu-id="51caa-105">Servicios web Exchange (EWS) es un servicio Web basado en SOAP, lo que significa que los mensajes de solicitud y de respuesta que se envían entre el cliente y el servidor se componen de elementos XML.</span><span class="sxs-lookup"><span data-stu-id="51caa-105">Exchange Web Services (EWS) is a SOAP-based web service, which means that the request and response messages that are sent between the client and server are comprised of XML elements.</span></span> <span data-ttu-id="51caa-106">La documentación de esta sección se basa en las instancias XML que se envían entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="51caa-106">The documentation in this section is based on the XML instances that are sent between the client and server.</span></span> <span data-ttu-id="51caa-107">Las instancias XML se definen en los archivos WSDL y de esquema que se encuentran en el directorio virtual que hospeda EWS.</span><span class="sxs-lookup"><span data-stu-id="51caa-107">The XML instances are defined in the WSDL and schema files that are located in the virtual directory that hosts EWS.</span></span> <span data-ttu-id="51caa-108">Si es un usuario autenticado, puede ir a los archivos de esquema y WSDL mediante las siguientes direcciones URL, donde \<yourclientaccessserver\> es el nombre de su servidor de acceso de cliente:</span><span class="sxs-lookup"><span data-stu-id="51caa-108">If you are an authenticated user, you can browse to the WSDL and schema files by using the following URLs, where \<yourclientaccessserver\> is the name of your Client Access server:</span></span>
  
- <span data-ttu-id="51caa-109">http:// \<yourclientaccessserver\> . com/EWS/Services. wsdl: la ubicación del archivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="51caa-109">http://\<yourclientaccessserver\>.com/ews/services.wsdl — The location of the WSDL file.</span></span>
    
- <span data-ttu-id="51caa-110">http:// \<yourclientaccessserver\> . com/EWS/messages. xsd: la ubicación del esquema de mensajes.</span><span class="sxs-lookup"><span data-stu-id="51caa-110">http://\<yourclientaccessserver\>.com/ews/messages.xsd — The location of the messages schema.</span></span>
    
- <span data-ttu-id="51caa-111">http:// \<yourclientaccessserver\> . com/EWS/Types. xsd: la ubicación del esquema de tipos.</span><span class="sxs-lookup"><span data-stu-id="51caa-111">http://\<yourclientaccessserver\>.com/ews/types.xsd — The location of the types schema.</span></span>
    
<span data-ttu-id="51caa-112">Los archivos de esquema que describen los elementos XML de EWS proporcionan una guía general de la estructura XML que es posible para las interacciones de mensajes de solicitud-respuesta.</span><span class="sxs-lookup"><span data-stu-id="51caa-112">The schema files that describe the EWS XML elements provide a general roadmap of the XML structure that is possible for request-response message interactions.</span></span> <span data-ttu-id="51caa-113">La estructura XML real que se envía entre el cliente y el servidor varía según la operación a la que se llama, la información solicitada y la configuración del lado del servidor.</span><span class="sxs-lookup"><span data-stu-id="51caa-113">The actual XML structure that is sent between client and server varies according to the operation that is called, the information requested, and the server-side settings.</span></span>
  
<span data-ttu-id="51caa-114">El archivo WSDL de EWS, Services. wsdl, no es totalmente compatible con el estándar WSDL porque no incluye una definición de servicio WSDL.</span><span class="sxs-lookup"><span data-stu-id="51caa-114">The EWS WSDL file, services.wsdl, does not fully conform to the WSDL standard because it does not include a WSDL service definition.</span></span> <span data-ttu-id="51caa-115">Esto se debe a que EWS no está diseñado para hospedarse en un equipo que tenga una dirección predefinida.</span><span class="sxs-lookup"><span data-stu-id="51caa-115">This is because EWS is not designed to be hosted on a computer that has a predefined address.</span></span> <span data-ttu-id="51caa-116">Puede usar el servicio de detección automática para obtener la dirección de extremo de EWS.</span><span class="sxs-lookup"><span data-stu-id="51caa-116">You can use the Autodiscover service to get the EWS endpoint address.</span></span> <span data-ttu-id="51caa-117">Algunos generadores del modelo de objetos de cliente analizan el WSDL y pueden encontrar una condición de error porque el archivo WSDL no contiene una definición de servicio WSDL.</span><span class="sxs-lookup"><span data-stu-id="51caa-117">Some client-side object model generators parse the WSDL and can encounter an error condition because the WSDL file does not contain a WSDL service definition.</span></span> <span data-ttu-id="51caa-118">Si el generador del modelo de objetos encuentra un error, puede insertar una definición de servicio WSDL del marcador de posición.</span><span class="sxs-lookup"><span data-stu-id="51caa-118">If your object model generator encounters an error, you can insert a placeholder WSDL service definition.</span></span>
  
> [!TIP]
> <span data-ttu-id="51caa-119">Si usa .NET Framework para desarrollar la aplicación, le recomendamos que use la [API administrada de EWS](http://aka.ms/ews-managed-api-readme), en lugar de un generador de modelo de objetos.</span><span class="sxs-lookup"><span data-stu-id="51caa-119">If you are using the .NET Framework to develop your application, we recommend that you use the [EWS Managed API](http://aka.ms/ews-managed-api-readme), rather than an object model generator.</span></span> <span data-ttu-id="51caa-120">La API administrada de EWS proporciona un modelo de objetos fácil de usar para controlar la serialización y deserialización del XML EWS.</span><span class="sxs-lookup"><span data-stu-id="51caa-120">The EWS Managed API provides an easy-to-use object model to handle the serialization and deserialization of the EWS XML.</span></span> <span data-ttu-id="51caa-121">Para obtener más información, vea Introducción [a las aplicaciones cliente de la API administrada de EWS](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="51caa-121">For more information, see [Get started with EWS Managed API client applications](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="51caa-122">El archivo de esquema messages. xsd contiene las definiciones de elemento de los elementos de nivel superior del cuerpo SOAP.</span><span class="sxs-lookup"><span data-stu-id="51caa-122">The messages.xsd schema file contains the element definitions for the top-level elements in the SOAP body.</span></span> <span data-ttu-id="51caa-123">A excepción de los códigos de respuesta de error, la mayoría de las definiciones de messages. xsd son específicas de una operación.</span><span class="sxs-lookup"><span data-stu-id="51caa-123">With the exception of the error response codes, most of the definitions in messages.xsd are specific to an operation.</span></span> <span data-ttu-id="51caa-124">El esquema Types. xsd contiene las definiciones de los encabezados SOAP y todas las definiciones comunes que se comparten entre las operaciones.</span><span class="sxs-lookup"><span data-stu-id="51caa-124">The types.xsd schema contains the definitions for the SOAP headers and all the common definitions that are shared across operations.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="51caa-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="51caa-125">See also</span></span>

- [<span data-ttu-id="51caa-126">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="51caa-126">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="51caa-127">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="51caa-127">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
- [<span data-ttu-id="51caa-128">Explorar la API administrada de EWS, EWS y servicios web en Exchange</span><span class="sxs-lookup"><span data-stu-id="51caa-128">Explore the EWS Managed API, EWS, and web services in Exchange</span></span>](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [<span data-ttu-id="51caa-129">Empezar a usar los servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="51caa-129">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
- [<span data-ttu-id="51caa-130">Detección automática en Exchange</span><span class="sxs-lookup"><span data-stu-id="51caa-130">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
    

