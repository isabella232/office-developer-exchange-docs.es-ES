---
title: ChangeHighlights
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f9bd7323-44db-4d2f-aaaa-94c2dfdeead6
description: El elemento ChangeHighlights especifica lo que ha cambiado entre dos versiones de un mensaje de solicitud de reunión.
ms.openlocfilehash: 95f665f30c62d723cd97eaa2bd3eb3b2ed479967
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512215"
---
# <a name="changehighlights"></a>ChangeHighlights

El **elemento ChangeHighlights** especifica lo que ha cambiado entre dos versiones de un mensaje de solicitud de reunión. 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[HasLocationChanged](haslocationchanged.md) <br/> |Especifica si la propiedad location de una reunión ha cambiado.  <br/> |
|[Location](location.md) <br/> |Representa la ubicación de una reunión o cita.  <br/> |
|[HasStartTimeChanged](hasstarttimechanged.md) <br/> |Especifica si la hora de inicio de una reunión ha cambiado.  <br/> |
|[Start](start.md) <br/> |Representa el inicio de una duración.  <br/> |
|[HasEndTimeChanged](hasendtimechanged.md) <br/> |Especifica si la hora de finalización de una reunión ha cambiado.  <br/> |
|[Fin ](end-ex15websvcsotherref.md) <br/> |Representa el final de una duración.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |Representa una solicitud de reunión en Exchange almacén.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

