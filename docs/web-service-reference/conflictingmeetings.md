---
title: ConflictingMeetings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ConflictingMeetings
api_type:
- schema
ms.assetid: cfff7a11-7b3a-4995-9815-afedd45ebb0f
description: El elemento ConflictingMeetings identifica todos los elementos de calendario que entren en conflicto con una hora de reunión.
ms.openlocfilehash: 59cefb5e276f559f448788e3b1c411337dd5eb35
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518753"
---
# <a name="conflictingmeetings"></a>ConflictingMeetings

El **elemento ConflictingMeetings** identifica todos los elementos de calendario que entren en conflicto con una hora de reunión. 
  
```xml
<ConflictingMeetings>
   <CalendarItem/>
</ConflictingMeetings>
```

 **NonEmptyArrayOfAllItemsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Representa un Exchange de calendario.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |Representa una solicitud de reunión en Exchange almacén.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un Exchange de calendario.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si se usa este elemento, debe contener uno o varios elementos secundarios.
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor Acceso de cliente.
  
> [!NOTE]
> Aunque los elementos secundarios adicionales son válidos para el esquema, el elemento [CalendarItem](calendaritem.md) es el único elemento secundario que Exchange Web Services (EWS) devolverá dentro del elemento **ConflictingMeetings.** En este tema no se enumeran los elementos secundarios que son válidos para el esquema pero que EWS no devolverá. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

