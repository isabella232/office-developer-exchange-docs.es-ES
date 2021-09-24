---
title: IsFromMe
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IsFromMe
api_type:
- schema
ms.assetid: d3c5fbf0-a95c-46e5-890f-953e50ac49d6
description: El elemento IsFromMe indica si un usuario le envió un elemento.
ms.openlocfilehash: b29e56eb58f30604e8155bbdca821991a4201f62
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524213"
---
# <a name="isfromme"></a>IsFromMe

El **elemento IsFromMe** indica si un usuario le envió un elemento. 
  
```xml
<IsFromMe/>
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
|[CalendarItem](calendaritem.md) <br/> |Representa un Exchange de calendario.  <br/> |
|[Contact](contact.md) <br/> |Representa un Exchange de contacto.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[Elemento](item.md) <br/> |Representa un elemento en el Exchange almacén.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en el Exchange local.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el Exchange almacén.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una solicitud de reunión en Exchange almacén.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta de reunión en Exchange almacén.  <br/> |
|[Mensaje](message-ex15websvcsotherref.md) <br/> |Representa un Exchange de correo electrónico.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Quita un elemento de la Exchange almacén.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea en el Exchange almacén.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** indica que el elemento lo envió un usuario a él o a sí mismo. Un valor de **false** indica que el usuario no envió el elemento a él o a ella misma. 
  
## <a name="remarks"></a>Comentarios

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

