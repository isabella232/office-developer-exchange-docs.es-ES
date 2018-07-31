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
ms.openlocfilehash: 3b88429488dbecd4ed7c3adf56462f34fa0d4b17
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353395"
---
# <a name="soap-autodiscover-xml-elements-for-exchange-2013"></a>Elementos de Autodiscover XML SOAP para Exchange 2013

Busque información de referencia de elemento XML para el servicio web de detección automática de SOAP en Exchange.
  
La documentación de esta sección se basa en las instancias del elemento XML de detección automática de SOAP que se envían entre el cliente y el servidor. Esta documentación de instancia XML se basa en los archivos WSDL y el esquema que se encuentran en el directorio virtual que hospeda el servicio de detección automática de SOAP. Los usuarios autenticados pueden examinar los archivos de esquema y WSDL mediante el uso de una dirección URL que es similar a una de las siguientes:
  
- La ubicación del archivo WSDL: `http://<yourclientaccessserver>.com/autodiscover/services.wsdl` o`http://autodiscover.<yourclientaccessserver>.com/autodiscover/services.wsdl`
    
- La ubicación del esquema de mensajes: `http://<yourclientaccessserver>.com/autodiscover/messages.xsd` o`http://autodiscover.<yourclientaccessserver>.com/autodiscover/messages.xsd` 
    
La ubicación de los archivos de esquema y SOAP WSDL de detección automática varía en función de la instalación de Exchange.
  
El archivo de esquema messages.xsd describe los elementos XML que se pueden enviar en un encabezado SOAP de detección automática y el cuerpo del mensaje SOAP. Este archivo proporciona una guía general de lo que puede ser la estructura XML para una interacción de mensaje de solicitud y respuesta determinado. La estructura XML real que se envía entre el cliente y el servidor se basa en las opciones y el contexto en el que se usa. Los archivos de esquema definición lo que es posible XML. El intervalo real de XML que se envían a través de la conexión se basa en qué operación se denomina, la información solicitada y la configuración del servidor. 
  
## <a name="related-sections"></a>Secciones relacionadas

- [Referencia de servicio web de detección automática de SOAP para Exchange](soap-autodiscover-web-service-reference-for-exchange.md)    
- [Referencia EWS para Exchange](ews-reference-for-exchange.md)    
- [Referencia de servicio de web de mensajería unificada de Exchange](unified-messaging-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a>Vea también

- [Referencia de servicio web de detección automática para Exchange](autodiscover-web-service-reference-for-exchange.md)
- [Detección automática de Exchange](../exchange-web-services/autodiscover-for-exchange.md)
- [Empezar a utilizar servicios web de Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

