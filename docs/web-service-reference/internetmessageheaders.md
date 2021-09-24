---
title: InternetMessageHeaders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- InternetMessageHeaders
api_type:
- schema
ms.assetid: 4dcf8671-96df-4a2d-9836-7e8e3a67e0db
description: El elemento InternetMessageHeaders contiene una colección de algunos de los encabezados de mensaje de Internet contenidos en un elemento de un buzón. Para obtener toda la colección de encabezados de mensajes de Internet, use la PR_TRANSPORT_MESSAGE_HEADERS propiedad. Para obtener más información acerca de los encabezados de mensajes ews e Internet, veaGetting Internet message headersin EWS, MIME, and the missing Internet message headers.
ms.openlocfilehash: 1ea49f2d5cc31aef09a9bc6d38dff25652696842
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541088"
---
# <a name="internetmessageheaders"></a>InternetMessageHeaders

El **elemento InternetMessageHeaders** contiene una colección de algunos de los encabezados de mensaje de Internet contenidos en un elemento de un buzón. Para obtener toda la colección de encabezados de mensajes de Internet, use la **PR_TRANSPORT_MESSAGE_HEADERS** propiedad. Para obtener más información acerca de los encabezados de mensajes ews e Internet, vea "Getting Internet message headers" in [EWS, MIME, and the missing Internet message headers](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx).
  
```XML
<InternetMessageHeaders>
   <InternetMessageHeader/>
</InternetMessageHeaders>
```

 **NonEmptyArrayOfInternetHeadersType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[InternetMessageHeader](internetmessageheader.md) <br/> |Representa el encabezado de mensaje de Internet de un encabezado determinado dentro de la colección de encabezados.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AcceptItem](acceptitem.md) <br/> |Representa una respuesta Accept a una solicitud de reunión.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un Exchange de calendario.  <br/> |
|[Contact](contact.md) <br/> |Representa un Exchange de contacto.  <br/> |
|[DeclineItem](declineitem.md) <br/> |Representa una respuesta de declinación a una solicitud de reunión.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[Elemento](item.md) <br/> |Representa un elemento en el Exchange almacén.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en el Exchange local.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el Exchange almacén.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una solicitud de reunión en Exchange almacén.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta de reunión en Exchange almacén.  <br/> |
|[Mensaje](message-ex15websvcsotherref.md) <br/> |Representa un Exchange de correo electrónico.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Quita un elemento de la Exchange almacén.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea en el Exchange almacén.  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |Representa una respuesta aceptada provisionalmente a una solicitud de reunión.  <br/> |
   
## <a name="remarks"></a>Comentarios

A continuación se muestra la definición de propiedad extendida de la API administrada ews **para la PR_TRANSPORT_MESSAGE_HEADERS** propiedad. 
  
```cs
ExtendedPropertyDefinition transportMsgHdr = new ExtendedPropertyDefinition(0x007D, MapiPropertyType.String);
```

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


[EWS, MIME y los encabezados de mensajes de Internet que faltan](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx)

