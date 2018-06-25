---
title: GetItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItem
api_type:
- schema
ms.assetid: e3590b8b-c2a7-4dad-a014-6360197b68e4
description: Busque información sobre la EWS GetItem operación.
ms.openlocfilehash: 9b63032b2eaa3bf26027a42e38bfa06bedcbac86
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764892"
---
# <a name="getitem-operation"></a>GetItem Operation

Obtenga información acerca de la operación de EWS **GetItem** . 
  
La operación **GetItem** obtiene los elementos del almacén de Exchange. 
  
## <a name="using-the-getitem-operation"></a>Mediante la operación GetItem

La operación **GetItem** devuelve muchas propiedades de elemento. Las propiedades que se devuelven en una respuesta **GetItem** varían en función de la forma solicitada, propiedades adicionales solicitadas y el tipo de elemento devuelven. 
  
Elementos del [mensaje](message-ex15websvcsotherref.md) representan los mensajes de correo electrónico y todos los otros elementos que no están fuertemente tipados por el esquema de Exchange Web Services (EWS). Elementos como IPM. Uso compartido y IPM.InfoPath se devuelven como elementos del [mensaje](message-ex15websvcsotherref.md) . Exchange no devuelve [el elemento de base](item.md) de las respuestas. 
  
La operación **GetItem** no devuelve datos adjuntos. Devuelven los metadatos sobre un elemento adjunto o un archivo. Para devolver un dato adjunto, use la [operación GetAttachment](getattachment-operation.md).
  
## <a name="getitem-operation-soap-headers"></a>Encabezados SOAP de GetItem operación

La operación **GetItem** puede usar los encabezados SOAP que se enumeran en la siguiente tabla. 
  
|Encabezado ***|****Element****|****Descripción****|
|:-----|:-----|:-----|
|**DateTimePrecision** <br/> |[DateTimePrecision](datetimeprecision.md) <br/> |Especifica la resolución de los valores de fecha y hora en las respuestas desde el servidor, en segundos o en milisegundos.  <br/> |
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica el usuario que está realizando la suplantación de la aplicación cliente.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de la operación.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que ha respondido a la solicitud.  <br/> |
|**TimeZoneContext** <br/> |[TimeZoneContext](timezonecontext.md) <br/> |Identifica la zona horaria que se usará para todas las respuestas desde el servidor.  <br/> |
   
## <a name="in-this-section"></a>En esta sección

[Operación GetItem (mensaje de correo electrónico)](getitem-operation-email-message.md)
  
[Operación GetItem (elemento de calendario)](getitem-operation-calendar-item.md)
  
[Operación GetItem (tarea)](getitem-operation-task.md)
  
[Operación GetItem (contacto)](getitem-operation-contact.md)
  
## <a name="see-also"></a>Vea también



[Referencia EWS para Exchange](ews-reference-for-exchange.md)

