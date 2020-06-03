---
title: Culture
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Culture
api_type:
- schema
ms.assetid: 71bd62c6-3fec-48db-9a5e-02121e9bc20b
description: El elemento Culture representa la referencia cultural de un elemento determinado en un buzón.
ms.openlocfilehash: ee0fa4d25f3be769aff0a9a50c2f311ab6179b31
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458344"
---
# <a name="culture"></a>Culture

El elemento **Culture** representa la referencia cultural de un elemento determinado en un buzón. 
  
```xml
<Culture/>
```

 **Language**
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
|[Contacto](contact.md) <br/> |Representa un elemento de contacto de Exchange.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[Elemento](item.md) <br/> |Representa un elemento en el almacén de Exchange.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en el almacén de Exchange.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el almacén de Exchange.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta a una reunión en el almacén de Exchange.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico de Exchange.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Quita un elemento del almacén de Exchange.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea del almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto indica el idioma que se usa en las operaciones de servicios Web de Exchange. La referencia cultural se especifica mediante el identificador de referencia cultural RFC 1766; por ejemplo, en-US.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

