---
title: Inicio
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Start
api_type:
- schema
ms.assetid: 7cfe9979-c893-4f9b-b3a1-8f9e17515a4b
description: El elemento de inicio representa el inicio de la duración.
ms.openlocfilehash: 8d013990e650b497abfa947938a69eed3fed7474
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837545"
---
# <a name="start"></a>Inicio

El elemento de **Inicio** representa el inicio de la duración. 
  
```xml
<Start/>
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
|[DeletedOccurrence](deletedoccurrence.md) <br/> |Representa una repetición eliminada de un elemento periódico del calendario.  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |Representa la primera aparición de un elemento periódico del calendario.  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |Representa la última aparición de un elemento periódico del calendario.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|[Repetición](occurrence.md) <br/> |Representa una sola aparición de modificación de un elemento periódico del calendario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el inicio de la duración.
  
## <a name="remarks"></a>Comentarios

La operación UpdateItem puede establecer la hora de [Inicio](start.md) y [final](end-ex15websvcsotherref.md) de un elemento del almacén de Exchange. En una solicitud UpdateItem, se puede establecer la hora de **Inicio** sin establecer también la hora de **finalización** . Esto puede producir un error si la hora de **Inicio** es posterior a la hora de **finalización** . Tenga en cuenta que las aplicaciones cliente deben realizar ajustes en la hora de **finalización** cuando se cambia la hora de **Inicio** con el fin de conservar la duración. 
  
> [!NOTE]
> Si las fechas de [comienzo](start.md) y de [finalización](end-ex15websvcsotherref.md) del elemento maestro periódico no tienen una fecha que es igual a la primera aparición de un patrón de periodicidad semanal, se pierde la información de desplazamiento de zona horaria. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [WeeklyRecurrence](weeklyrecurrence.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

