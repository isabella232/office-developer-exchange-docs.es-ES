---
title: IsReadReceiptRequested
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IsReadReceiptRequested
api_type:
- schema
ms.assetid: 7ab6edd5-c7ed-4701-8de3-d7dc7ecfa9c2
description: El elemento IsReadReceiptRequested indica si el remitente de un elemento solicita una confirmación de lectura.
ms.openlocfilehash: 0ecc70116512103c252692295bd61fd102d7b5ea
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524143"
---
# <a name="isreadreceiptrequested"></a>IsReadReceiptRequested

El **elemento IsReadReceiptRequested** indica si el remitente de un elemento solicita una confirmación de lectura. 
  
```xml
<IsReadReceiptRequested/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RemoveItem](removeitem.md) <br/> |Quita un elemento de la Exchange almacén.  <br/> |
|[Mensaje](message-ex15websvcsotherref.md) <br/> |Representa un Exchange de correo electrónico.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el Exchange almacén.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una solicitud de reunión en Exchange almacén.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta de reunión en Exchange almacén.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en el Exchange local.  <br/> |
|[AcceptItem](acceptitem.md) <br/> |Representa una respuesta Accept a una solicitud de reunión.  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |Representa una respuesta provisional a una solicitud de reunión.  <br/> |
|[DeclineItem](declineitem.md) <br/> |Representa una respuesta de declinación a una solicitud de reunión.  <br/> |
|[ReplyToItem](replytoitem.md) <br/> |Contiene una respuesta al creador de un elemento en el Exchange almacén.  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |Contiene una respuesta a todos los destinatarios identificados de un elemento en el Exchange almacén.  <br/> |
|[ForwardItem](forwarditem.md) <br/> |Contiene un Exchange almacén para reenviar a los destinatarios.  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |Representa el objeto de respuesta que se usa para cancelar una reunión.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** indica que se solicita una confirmación de lectura al destinatario del elemento. 
  
## <a name="remarks"></a>Comentarios

Si **IsReadReceiptRequested** es **true**, al establecer [IsRead](isread.md) en **true** se envía un recibo de lectura. El destinatario puede suprimir las confirmaciones de lectura enviando el objeto de respuesta [SuppressReadReceipt](suppressreadreceipt.md) antes de establecer la **propiedad IsRead.** 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

