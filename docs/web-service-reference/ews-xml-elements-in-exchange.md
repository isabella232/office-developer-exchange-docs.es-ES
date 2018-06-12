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
# <a name="ews-xml-elements-in-exchange"></a>Elementos XML de EWS de Exchange

Buscar información de referencia para el XML EWS elementos en Exchange.
  
Servicios Web de Exchange (EWS) es un servicio web basado en SOAP, lo que significa que los mensajes de solicitud y respuesta que se envían entre el cliente y el servidor se componen de los elementos XML. La documentación de esta sección se basa en las instancias XML que se envían entre el cliente y el servidor. Las instancias de XML se definen en los archivos WSDL y el esquema que se encuentran en el directorio virtual que hospeda EWS. Si es un usuario autenticado, puede buscar los archivos de esquema y WSDL mediante el uso de las siguientes direcciones URL, donde \<yourclientaccessserver\> es el nombre de su servidor de acceso de cliente:
  
- http://\<yourclientaccessserver\>.com/ews/services.wsdl: la ubicación del archivo WSDL.
    
- http://\<yourclientaccessserver\>.com/ews/messages.xsd: la ubicación del esquema de los mensajes.
    
- http://\<yourclientaccessserver\>.com/ews/types.xsd: la ubicación del esquema de tipos.
    
Los archivos de esquema que describen los elementos XML de EWS proporcionan una guía general de la estructura XML que es posible que las interacciones del mensaje de respuesta de la solicitud. La estructura XML real que se envía entre cliente y servidor varía según la operación que se llama, la información solicitada y la configuración del servidor.
  
El archivo WSDL de EWS, services.wsdl, no se ajustan totalmente para el estándar WSDL porque no incluye una definición del servicio WSDL. Esto es debido a que EWS no está diseñado para hospedarse en un equipo que tenga una dirección predefinida. Puede usar el servicio Detección automática para obtener la dirección de extremo EWS. Algunos generadores de modelo de objetos de cliente analizar el archivo WSDL y pueden encontrar una condición de error porque el archivo WSDL no contiene una definición del servicio WSDL. Si el generador de modelo de objetos encuentra un error, puede insertar un marcador de posición de definición del servicio WSDL.
  
> [!TIP]
> Si usa .NET Framework para desarrollar la aplicación, se recomienda que utilice la [API administrada de EWS](http://aka.ms/ews-managed-api-readme), en lugar de un generador de modelo de objetos. La API administrada de EWS proporciona un modelo de objetos de fácil de usar para controlar la serialización y deserialización del XML de EWS. Para obtener más información, vea [Introducción a las aplicaciones cliente de API administrada de EWS](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx). 
  
El archivo de esquema messages.xsd contiene las definiciones de elemento para los elementos de nivel superior en el cuerpo SOAP. A excepción de los códigos de respuesta de error, la mayoría de las definiciones de messages.xsd es específica de una operación. El esquema types.xsd contiene las definiciones de los encabezados SOAP y todas las definiciones comunes que se comparten en operaciones.
  
## <a name="see-also"></a>Ver también

- [Referencia EWS para Exchange](ews-reference-for-exchange.md)
- [Operaciones de EWS en Exchange](ews-operations-in-exchange.md)
- [Explore la API administrada de EWS, EWS y servicios web de Exchange](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [Empezar a utilizar servicios web de Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
- [Detección automática de Exchange](../exchange-web-services/autodiscover-for-exchange.md)
    

