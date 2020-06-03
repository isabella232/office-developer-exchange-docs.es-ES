---
title: IsReadReceiptRequested
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsReadReceiptRequested
api_type:
- schema
ms.assetid: 7ab6edd5-c7ed-4701-8de3-d7dc7ecfa9c2
description: El elemento IsReadReceiptRequested indica si el remitente de un elemento solicita una confirmación de lectura.
ms.openlocfilehash: ff0c512ef23b315d4de1194432408f5b408029d9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457791"
---
# <a name="isreadreceiptrequested"></a>IsReadReceiptRequested

El elemento **IsReadReceiptRequested** indica si el remitente de un elemento solicita una confirmación de lectura. 
  
```xml
<IsReadReceiptRequested/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RemoveItem](removeitem.md) <br/> |Quita un elemento del almacén de Exchange.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico de Exchange.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el almacén de Exchange.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta a una reunión en el almacén de Exchange.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en el almacén de Exchange.  <br/> |
|[AcceptItem](acceptitem.md) <br/> |Representa una respuesta de aceptación para una convocatoria de reunión.  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |Representa una respuesta provisional a una convocatoria de reunión.  <br/> |
|[DeclineItem](declineitem.md) <br/> |Representa una respuesta de rechazo a una convocatoria de reunión.  <br/> |
|[ReplyToItem](replytoitem.md) <br/> |Contiene una respuesta al creador de un elemento en el almacén de Exchange.  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |Contiene una respuesta a todos los destinatarios identificados de un elemento en el almacén de Exchange.  <br/> |
|[ForwardItem](forwarditem.md) <br/> |Contiene un elemento de almacén de Exchange que se va a reenviar a los destinatarios.  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |Representa el objeto de respuesta que se usa para cancelar una reunión.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto de **true** indica que se solicita confirmación de lectura del destinatario del elemento. 
  
## <a name="remarks"></a>Comentarios

Si **IsReadReceiptRequested** es **true**, al establecer [IsRead](isread.md) en **true** , se envía una confirmación de lectura. El destinatario puede suprimir las confirmaciones de lectura enviando el objeto de respuesta [SuppressReadReceipt](suppressreadreceipt.md) antes de establecer la propiedad **IsRead** . 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

