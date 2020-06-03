---
title: Operación GetItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- GetItem
api_type:
- schema
ms.assetid: e3590b8b-c2a7-4dad-a014-6360197b68e4
description: Busque información sobre la operación de EWS de GetItem.
localization_priority: Priority
ms.openlocfilehash: 8871dde183974454fc27dbddda489e6b0a70f3aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463331"
---
# <a name="getitem-operation"></a>Operación GetItem

Busque información sobre la operación de EWS de **GetItem** . 
  
La operación **GetItem** obtiene elementos del almacén de Exchange. 
  
## <a name="using-the-getitem-operation"></a>Uso de la operación GetItem

La operación **GetItem** devuelve muchas propiedades de elemento. Las propiedades que se devuelven en una respuesta **GetItem** varían en función de la forma solicitada, las propiedades adicionales solicitadas y el tipo de elemento devuelto. 
  
Los elementos de [mensaje](message-ex15websvcsotherref.md) representan mensajes de correo electrónico y todos los demás elementos que no son fuertemente tipados por el esquema de servicios web Exchange (EWS). Elementos como IPM. Uso compartido e IPM. InfoPath se devuelven como elementos del [mensaje](message-ex15websvcsotherref.md) . Exchange no devuelve el elemento de [elemento](item.md) base en las respuestas. 
  
La operación **GetItem** no devuelve datos adjuntos. Devuelve los metadatos de un archivo o elemento adjunto. Para devolver un dato adjunto, use la [operación GetAttachment](getattachment-operation.md).
  
## <a name="getitem-operation-soap-headers"></a>Encabezados SOAP de la operación GetItem

La operación **GetItem** puede usar los encabezados SOAP que se enumeran en la tabla siguiente. 
  
|Encabezado * * * *|****Element****|****Descripción****|
|:-----|:-----|:-----|
|**DateTimePrecision** <br/> |[DateTimePrecision](datetimeprecision.md) <br/> |Especifica la resolución de los valores de datos/tiempo en respuestas del servidor, en segundos o en milisegundos.  <br/> |
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica al usuario que está suplantando la aplicación cliente.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural, tal y como se define en RFC 3066, "etiquetas para la identificación de idiomas", que se va a usar para obtener acceso al buzón.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud.  <br/> |
|**TimeZoneContext** <br/> |[TimeZoneContext](timezonecontext.md) <br/> |Identifica la zona horaria que se va a usar para todas las respuestas del servidor.  <br/> |
   
## <a name="in-this-section"></a>En esta sección

[Operación GetItem (mensaje de correo electrónico)](getitem-operation-email-message.md)
  
[Operación GetItem (elemento de calendario)](getitem-operation-calendar-item.md)
  
[Operación GetItem (tarea)](getitem-operation-task.md)
  
[Operación GetItem (contacto)](getitem-operation-contact.md)
  
## <a name="see-also"></a>Vea también



[Referencia EWS para Exchange](ews-reference-for-exchange.md)

