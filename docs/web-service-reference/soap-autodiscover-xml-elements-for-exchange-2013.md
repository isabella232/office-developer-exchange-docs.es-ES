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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465187"
---
# <a name="soap-autodiscover-xml-elements-for-exchange-2013"></a>Elementos XML de detección automática de SOAP para Exchange 2013

Buscar información de referencia de elemento XML para el servicio Web de detección automática de SOAP en Exchange.
  
La documentación de esta sección se basa en las instancias del elemento XML de detección automática de SOAP que se envían entre el cliente y el servidor. Esta documentación de instancia XML se basa en los archivos WSDL y de esquema que se encuentran en el directorio virtual que hospeda el servicio Detección automática de SOAP. Los usuarios autenticados pueden ir a los archivos de esquema y WSDL mediante una dirección URL similar a una de las siguientes:
  
- La ubicación del archivo WSDL: `http://<yourclientaccessserver>.com/autodiscover/services.wsdl` o`http://autodiscover.<yourclientaccessserver>.com/autodiscover/services.wsdl`
    
- La ubicación del esquema de mensajes: `http://<yourclientaccessserver>.com/autodiscover/messages.xsd` o`http://autodiscover.<yourclientaccessserver>.com/autodiscover/messages.xsd` 
    
La ubicación de los archivos de esquema y WSDL de detección automática de SOAP varía en función de la instalación de Exchange.
  
El archivo de esquema messages. xsd describe los elementos XML que se pueden enviar en un encabezado SOAP de detección automática y un cuerpo SOAP. Este archivo proporciona un mapa de ruta general de la estructura XML que puede utilizarse para una interacción de mensajes de solicitud-respuesta determinada. La estructura XML real que se envía entre el cliente y el servidor se basa en las opciones y en el contexto en el que se usa. Los archivos de esquema definen qué XML es posible. El intervalo real de XML que se envía por el cable se basa en qué operación se llama, la información solicitada y la configuración del servidor. 
  
## <a name="related-sections"></a>Secciones relacionadas

- [Referencia del servicio Web de detección automática de SOAP para Exchange](soap-autodiscover-web-service-reference-for-exchange.md)    
- [Referencia EWS para Exchange](ews-reference-for-exchange.md)    
- [Referencia del servicio Web de mensajería unificada para Exchange](unified-messaging-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a>Vea también

- [Referencia del servicio web de Detección automática para Exchange](autodiscover-web-service-reference-for-exchange.md)
- [Detección automática en Exchange](../exchange-web-services/autodiscover-for-exchange.md)
- [Empezar a usar los servicios web de Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

