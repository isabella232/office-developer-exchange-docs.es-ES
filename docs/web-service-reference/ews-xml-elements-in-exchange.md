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
# <a name="ews-xml-elements-in-exchange"></a>Elementos XML de EWS en Exchange

Busque información de referencia para los elementos XML de EWS en Exchange.
  
Servicios web Exchange (EWS) es un servicio Web basado en SOAP, lo que significa que los mensajes de solicitud y de respuesta que se envían entre el cliente y el servidor se componen de elementos XML. La documentación de esta sección se basa en las instancias XML que se envían entre el cliente y el servidor. Las instancias XML se definen en los archivos WSDL y de esquema que se encuentran en el directorio virtual que hospeda EWS. Si es un usuario autenticado, puede ir a los archivos de esquema y WSDL mediante las siguientes direcciones URL, donde \<yourclientaccessserver\> es el nombre de su servidor de acceso de cliente:
  
- http:// \<yourclientaccessserver\> . com/EWS/Services. wsdl: la ubicación del archivo WSDL.
    
- http:// \<yourclientaccessserver\> . com/EWS/messages. xsd: la ubicación del esquema de mensajes.
    
- http:// \<yourclientaccessserver\> . com/EWS/Types. xsd: la ubicación del esquema de tipos.
    
Los archivos de esquema que describen los elementos XML de EWS proporcionan una guía general de la estructura XML que es posible para las interacciones de mensajes de solicitud-respuesta. La estructura XML real que se envía entre el cliente y el servidor varía según la operación a la que se llama, la información solicitada y la configuración del lado del servidor.
  
El archivo WSDL de EWS, Services. wsdl, no es totalmente compatible con el estándar WSDL porque no incluye una definición de servicio WSDL. Esto se debe a que EWS no está diseñado para hospedarse en un equipo que tenga una dirección predefinida. Puede usar el servicio de detección automática para obtener la dirección de extremo de EWS. Algunos generadores del modelo de objetos de cliente analizan el WSDL y pueden encontrar una condición de error porque el archivo WSDL no contiene una definición de servicio WSDL. Si el generador del modelo de objetos encuentra un error, puede insertar una definición de servicio WSDL del marcador de posición.
  
> [!TIP]
> Si usa .NET Framework para desarrollar la aplicación, le recomendamos que use la [API administrada de EWS](http://aka.ms/ews-managed-api-readme), en lugar de un generador de modelo de objetos. La API administrada de EWS proporciona un modelo de objetos fácil de usar para controlar la serialización y deserialización del XML EWS. Para obtener más información, vea Introducción [a las aplicaciones cliente de la API administrada de EWS](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx). 
  
El archivo de esquema messages. xsd contiene las definiciones de elemento de los elementos de nivel superior del cuerpo SOAP. A excepción de los códigos de respuesta de error, la mayoría de las definiciones de messages. xsd son específicas de una operación. El esquema Types. xsd contiene las definiciones de los encabezados SOAP y todas las definiciones comunes que se comparten entre las operaciones.
  
## <a name="see-also"></a>Vea también

- [Referencia EWS para Exchange](ews-reference-for-exchange.md)
- [Operaciones de EWS en Exchange](ews-operations-in-exchange.md)
- [Explorar la API administrada de EWS, EWS y servicios web en Exchange](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [Empezar a usar los servicios web de Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
- [Detección automática en Exchange](../exchange-web-services/autodiscover-for-exchange.md)
    

