---
title: InternetMessageHeaders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InternetMessageHeaders
api_type:
- schema
ms.assetid: 4dcf8671-96df-4a2d-9836-7e8e3a67e0db
description: El elemento InternetMessageHeaders contiene una colección de algunos encabezados de mensajes de Internet incluidos en un elemento de un buzón. Para obtener toda la colección de encabezados de mensajes de Internet, use la propiedad PR_TRANSPORT_MESSAGE_HEADERS. Para obtener más información sobre los encabezados de mensajes de EWS e Internet, Consulteobtener Internet Message headersin EWS, MIME y los encabezados de mensajes de Internet que faltan.
ms.openlocfilehash: 4719050c02590e021b29173c234466de3fdc58a4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467329"
---
# <a name="internetmessageheaders"></a>InternetMessageHeaders

El elemento **InternetMessageHeaders** contiene una colección de algunos encabezados de mensajes de Internet incluidos en un elemento de un buzón. Para obtener toda la colección de encabezados de mensajes de Internet, use la propiedad **PR_TRANSPORT_MESSAGE_HEADERS** . Para obtener más información acerca de los encabezados de mensajes de Internet y EWS, vea "obtener encabezados de mensajes de Internet" en [EWS, MIME y los encabezados de mensajes de Internet que faltan](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx).
  
```XML
<InternetMessageHeaders>
   <InternetMessageHeader/>
</InternetMessageHeaders>
```

 **NonEmptyArrayOfInternetHeadersType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[InternetMessageHeader](internetmessageheader.md) <br/> |Representa el encabezado de un mensaje de Internet para un encabezado determinado dentro de la colección de encabezados.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AcceptItem](acceptitem.md) <br/> |Representa una respuesta de aceptación para una convocatoria de reunión.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange.  <br/> |
|[Contacto](contact.md) <br/> |Representa un elemento de contacto de Exchange.  <br/> |
|[DeclineItem](declineitem.md) <br/> |Representa una respuesta de rechazo a una convocatoria de reunión.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[Elemento](item.md) <br/> |Representa un elemento en el almacén de Exchange.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en el almacén de Exchange.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el almacén de Exchange.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta a una reunión en el almacén de Exchange.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico de Exchange.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Quita un elemento del almacén de Exchange.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea del almacén de Exchange.  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |Representa una respuesta aceptada provisionalmente a una convocatoria de reunión.  <br/> |
   
## <a name="remarks"></a>Comentarios

La siguiente es la definición de propiedad extendida de la API administrada de EWS para la propiedad **PR_TRANSPORT_MESSAGE_HEADERS** . 
  
```cs
ExtendedPropertyDefinition transportMsgHdr = new ExtendedPropertyDefinition(0x007D, MapiPropertyType.String);
```

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


[EWS, MIME y los encabezados de mensajes de Internet que faltan](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx)

