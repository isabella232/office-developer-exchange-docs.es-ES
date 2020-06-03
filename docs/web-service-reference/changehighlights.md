---
title: ChangeHighlights
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9bd7323-44db-4d2f-aaaa-94c2dfdeead6
description: El elemento ChangeHighlights especifica lo que ha cambiado entre dos versiones de un mensaje de convocatoria de reunión.
ms.openlocfilehash: 6c78d2c96449ee41032859f90bf51d6e0faa92ae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463282"
---
# <a name="changehighlights"></a>ChangeHighlights

El elemento **ChangeHighlights** especifica lo que ha cambiado entre dos versiones de un mensaje de convocatoria de reunión. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[HasLocationChanged](haslocationchanged.md) <br/> |Especifica si la propiedad Location de una reunión ha cambiado.  <br/> |
|[Ubicación](location.md) <br/> |Representa la ubicación de una reunión o cita.  <br/> |
|[HasStartTimeChanged](hasstarttimechanged.md) <br/> |Especifica si la hora de inicio de una reunión ha cambiado.  <br/> |
|[Start](start.md) <br/> |Representa el inicio de una duración.  <br/> |
|[HasEndTimeChanged](hasendtimechanged.md) <br/> |Especifica si ha cambiado la hora de finalización de una reunión.  <br/> |
|[Centraliza](end-ex15websvcsotherref.md) <br/> |Representa el final de una duración.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

