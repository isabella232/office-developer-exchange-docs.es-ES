---
title: RelativeYearlyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RelativeYearlyRecurrence
api_type:
- schema
ms.assetid: 25b67876-9979-4a30-a637-357ea10a93b8
description: El elemento RelativeYearlyRecurrence describe un patrón de periodicidad anual relativo.
ms.openlocfilehash: ce6d724735cb23fb08bf541123341ede35011c4c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512502"
---
# <a name="relativeyearlyrecurrence"></a>RelativeYearlyRecurrence

El **elemento RelativeYearlyRecurrence** describe un patrón de periodicidad anual relativo. 
  
```xml
<RelativeYearlyRecurrence>
   <DaysOfWeek/>
   <DayOfWeekIndex/>
   <Month/>
</RelativeYearlyRecurrence>
```

 **RelativeYearlyRecurrencePatternType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DaysOfWeek (DayOfWeekType)](daysofweek-dayofweektype.md) <br/> |Describe los días de la semana que se usan en los patrones de periodicidad de elementos.  <br/> |
|[DayOfWeekIndex](dayofweekindex.md) <br/> |Describe qué semana en un mes se usa en un patrón de periodicidad anual relativo.  <br/> |
|[Month (Item Recurrence)](month-item-recurrence.md) <br/> |Describe el mes en el que se produce un elemento periódico anual.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Recurrence (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |Contiene información de periodicidad para tareas periódicas.  <br/> |
|[Recurrence (RecurrenceType)](recurrence-recurrencetype.md) <br/> |Contiene el patrón de periodicidad de los elementos de calendario y las solicitudes de reunión.  <br/> |
|[Estándar](standard.md) <br/> |Representa la fecha y hora en que la hora cambia del horario de verano a la hora estándar.  <br/> |
|[Daylight](daylight.md) <br/> |Representa la fecha y la hora en que la hora cambia de la hora estándar al horario de verano.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

