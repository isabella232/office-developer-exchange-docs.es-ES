---
title: LastModifiedTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- LastModifiedTime
api_type:
- schema
ms.assetid: 6db2cabc-e7f4-4d71-962b-789de6a192a4
description: El elemento LastModifiedTime indica cuándo se modificó por última vez un elemento. Este elemento es de sólo lectura.
ms.openlocfilehash: c410481af62ba3016d6d0855ed76598849eeaa77
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836203"
---
# <a name="lastmodifiedtime"></a>LastModifiedTime

El elemento **LastModifiedTime** indica cuándo se modificó por última vez un elemento. Este elemento es de sólo lectura. 
  
```xml
<LastModifiedTime/>
```

 **dateTime**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange.  <br/> |
|[Contact](contact.md) <br/> |Representa un elemento de contacto de Exchange.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[FileAttachment](fileattachment.md) <br/> |Representa un archivo que se adjunta a un elemento en el almacén de Exchange.  <br/> |
|[Item](item.md) <br/> |Representa un elemento genérico de Exchange.  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Representa un elemento de Exchange que está vinculado a otro elemento de Exchange.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa la cancelación de la reunión en el almacén de Exchange.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el almacén de Exchange.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta a la reunión en el almacén de Exchange.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico de Exchange.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Quita un elemento desde el almacén de Exchange.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea en el almacén de Exchange.  <br/> |
|[Objeto postItem](postitem.md) <br/> |Representa un elemento para exponer en el almacén de Exchange. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el tiempo en el que el último usuario modificó el elemento.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)
  
[Referencia EWS para Exchange](ews-reference-for-exchange.md)

