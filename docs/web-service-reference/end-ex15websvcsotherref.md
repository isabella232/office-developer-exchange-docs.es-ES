---
title: End
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- End
api_type:
- schema
ms.assetid: 72329821-32ff-495d-b6e5-fdc011003c2e
description: El elemento final representa el final de una duración.
ms.openlocfilehash: 90eea4fc545fae083e5675225665e517b502ba6f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764400"
---
# <a name="end"></a>End

El elemento **final** representa el final de una duración. 
  
```xml
<End/>
```

 **DateTime**
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
|[FirstOccurrence](firstoccurrence.md) <br/> |Representa la primera aparición de un elemento periódico del calendario.  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |Representa la última aparición de un elemento periódico del calendario.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|[Repetición](occurrence.md) <br/> |Representa una sola aparición de modificación de un elemento periódico del calendario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el final de una duración.
  
## <a name="remarks"></a>Comentarios

La operación UpdateItem puede establecer la hora de [Inicio](start.md) y **final** de un elemento del almacén de Exchange. En una solicitud UpdateItem, puede establecer la hora de [Inicio](start.md) sin establecer también la hora de **finalización** . Esto puede producir un error si la hora de [Inicio](start.md) es posterior a la hora de **finalización** . Tenga en cuenta que las aplicaciones cliente deben realizar ajustes en la hora de **finalización** cuando se cambia la hora de [Inicio](start.md) con el fin de conservar la duración. 
  
 **Nota** Si las fechas de [comienzo](start.md) y de **finalización** del elemento maestro periódico no tienen una fecha que es igual a la primera aparición de un patrón de periodicidad semanal, se pierde la información de desplazamiento de zona horaria. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[WeeklyRecurrence](weeklyrecurrence.md)
  
 **End**


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

