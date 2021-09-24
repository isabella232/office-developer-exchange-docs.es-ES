---
title: Elementos XML de detección automática soap para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: ae18a5b3-ae44-4cff-8654-db8028565e01
description: Busque información de referencia de elemento XML para el servicio web de detección automática SOAP en Exchange.
ms.openlocfilehash: 5dcf4d6cd7a2b0b2987e59530dfbaae7b9993242
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539103"
---
# <a name="soap-autodiscover-xml-elements-for-exchange-2013"></a>Elementos XML de detección automática soap para Exchange 2013

Busque información de referencia de elemento XML para el servicio web de detección automática SOAP en Exchange.
  
La documentación de esta sección se basa en las instancias del elemento XML de detección automática SOAP que se envían entre el cliente y el servidor. Esta documentación de instancia XML se basa en los archivos WSDL y de esquema que se encuentran en el directorio virtual que hospeda el servicio de detección automática SOAP. Los usuarios autenticados pueden examinar el WSDL y los archivos de esquema mediante una dirección URL similar a una de las siguientes:
  
- La ubicación del archivo WSDL: `http://<yourclientaccessserver>.com/autodiscover/services.wsdl` o `http://autodiscover.<yourclientaccessserver>.com/autodiscover/services.wsdl`
    
- La ubicación del esquema de mensajes: `http://<yourclientaccessserver>.com/autodiscover/messages.xsd` o `http://autodiscover.<yourclientaccessserver>.com/autodiscover/messages.xsd` 
    
La ubicación del WSDL de detección automática soap y los archivos de esquema varía en función de la Exchange instalación.
  
El archivo de esquema messages.xsd describe los elementos XML que se pueden enviar en un encabezado SOAP de detección automática y el cuerpo SOAP. Este archivo proporciona una guía general de lo que puede ser la estructura XML para una interacción de mensaje de solicitud y respuesta determinada. La estructura XML real que se envía entre el cliente y el servidor se basa en las opciones y el contexto en el que se usa. Los archivos de esquema definen qué XML es posible. El intervalo real de XML que se envía a través de la conexión se basa en la operación a la que se llama, la información solicitada y la configuración del lado servidor. 
  
## <a name="related-sections"></a>Secciones relacionadas

- [Referencia de servicio web de detección automática SOAP para Exchange](soap-autodiscover-web-service-reference-for-exchange.md)    
- [Referencia EWS para Exchange](ews-reference-for-exchange.md)    
- [Referencia del servicio web de mensajería unificada para Exchange](unified-messaging-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a>Ver también

- [Referencia del servicio web de Detección automática para Exchange](autodiscover-web-service-reference-for-exchange.md)
- [Detección automática en Exchange](../exchange-web-services/autodiscover-for-exchange.md)
- [Empezar a usar los servicios web de Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

