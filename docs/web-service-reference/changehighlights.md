---
title: ChangeHighlights
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9bd7323-44db-4d2f-aaaa-94c2dfdeead6
description: Mensaje de solicitud de la ChangeHighlights elemento especifica qué ha cambiado entre dos versiones de una reunión.
ms.openlocfilehash: 5fe7aa95f60ae95f1af24e8f7a0463ad49716f65
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763733"
---
# <a name="changehighlights"></a>ChangeHighlights

El elemento **ChangeHighlights** especifica qué ha cambiado entre dos versiones de una reunión de mensaje de solicitud. 
  
```XML
<ChangeHighlights>
    <HasLocationChanged></HasLocationChanged>
    <Location></Location>
    <HasStartTimeChanged></HasStartTimeChanged>
    <Start></Start>
    <HasEndTimeChanged></HasEndTimeChanged>
    <End></End>
</ChangeHighlights>
```

 **ChangeHighlightsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[HasLocationChanged](haslocationchanged.md) <br/> |Especifica si se ha cambiado la propiedad de ubicación de una reunión.  <br/> |
|[Location](location.md) <br/> |Representa la ubicación de una reunión o una cita.  <br/> |
|[HasStartTimeChanged](hasstarttimechanged.md) <br/> |Especifica si se ha cambiado la hora de inicio para una reunión.  <br/> |
|[Start](start.md) <br/> |Representa el inicio de la duración.  <br/> |
|[HasEndTimeChanged](hasendtimechanged.md) <br/> |Especifica si se ha cambiado la hora de finalización de una reunión.  <br/> |
|[End](end-ex15websvcsotherref.md) <br/> |Representa el final de una duración.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
   
## <a name="remarks"></a>Notas

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

