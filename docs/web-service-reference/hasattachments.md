---
title: HasAttachments
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HasAttachments
api_type:
- schema
ms.assetid: 538b7a85-11d7-4daa-8458-09b540760e8b
description: El elemento HasAttachments representa una propiedad que se establece en true si un elemento tiene al menos un archivo de datos adjuntos visible o si una conversación contiene al menos un elemento que tiene datos adjuntos. Esta propiedad es de sólo lectura.
ms.openlocfilehash: cc4e4ec0eac1c749723facc8cd780da41b0d8150
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462925"
---
# <a name="hasattachments"></a>HasAttachments

El elemento **HasAttachments** representa una propiedad que se establece en **true** si un elemento tiene al menos un archivo de datos adjuntos visible o si una conversación contiene al menos un elemento que tiene datos adjuntos. Esta propiedad es de sólo lectura. 
  
```XML
<HasAttachments/>
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
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange.  <br/> |
|[Condiciones](conditions.md) <br/> |Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla para esa regla.  <br/> |
|[Contacto](contact.md) <br/> |Representa un elemento de contacto de Exchange.  <br/> |
|[Conversación (ConversationType)](conversation-conversationtype.md) <br/> |Representa una sola conversación.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[Excepciones](exceptions.md) <br/> |Representa todas las condiciones de excepción de regla disponibles para la regla de bandeja de entrada.  <br/> |
|[Elemento](item.md) <br/> |Representa un elemento en el almacén de Exchange.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en el almacén de Exchange.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el almacén de Exchange.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta a una reunión en el almacén de Exchange.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico de Exchange.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea del almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto que representa un valor booleano. Un valor de **true** significa que el elemento o la conversación tiene al menos un archivo de datos adjuntos visible. Un valor de **false** significa que el elemento o la conversación no tiene datos adjuntos o solo tiene datos adjuntos ocultos. 
  
## <a name="remarks"></a>Comentarios

La propiedad **HasAttachments** se calcula a partir de la propiedad booleana **AllAttachmentsHidden** MAPI. Si un elemento no tiene datos adjuntos, la propiedad **AllAttachmentsHidden** no existe. Si todos los datos adjuntos del elemento están ocultos, la propiedad **AllAttachmentsHidden** es **true**. La propiedad **AllAttachmentsHidden** es **false** si tiene al menos un archivo adjunto y al menos uno de los datos adjuntos está visible. Use la propiedad MAPI **AllAttachmentsHidden** para buscar, agrupar y ordenar elementos. 
  
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
  
[Referencia EWS para Exchange](ews-reference-for-exchange.md)

