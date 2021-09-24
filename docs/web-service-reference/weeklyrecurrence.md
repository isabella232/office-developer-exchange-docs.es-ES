---
title: WeeklyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- WeeklyRecurrence
api_type:
- schema
ms.assetid: 69c41dd5-597c-45bc-be3f-e2f2b5615aa3
description: El elemento WeeklyRecurrence describe un patrón de periodicidad semanal.
ms.openlocfilehash: 408116dd85fb31fce8f5f3b5b4cde92945783f5d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509339"
---
# <a name="weeklyrecurrence"></a>WeeklyRecurrence

El **elemento WeeklyRecurrence** describe un patrón de periodicidad semanal. 
  
```XML
<WeeklyRecurrence>
   <Interval/>
   <DaysOfWeek/>
   <FirstDayOfWeek/>
</WeeklyRecurrence>
```

 **WeeklyRecurrencePatternType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Intervalo de](interval.md) <br/> |Define el intervalo, en semanas, entre dos elementos de patrón de periodicidad semanal consecutivos. El valor puede estar en el rango de 1 a 99.  <br/> |
|[DaysOfWeek (DaysOfWeekType)](daysofweek-daysofweektype.md) <br/> |Describe qué días de la semana se encuentran en el patrón de periodicidad semanal.  <br/> |
|[FirstDayOfWeek](firstdayofweek.md) <br/> |Especifica el primer día de la semana.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Recurrence (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |Contiene información de periodicidad para tareas periódicas.  <br/> |
|[Recurrence (RecurrenceType)](recurrence-recurrencetype.md) <br/> |Contiene el patrón de periodicidad de los elementos de calendario y las solicitudes de reunión.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

La información de desplazamiento de [](start.md) zona [](end-ex15websvcsotherref.md) horaria se pierde si las fechas Inicio y Fin del elemento maestro periódico no tienen una fecha igual a la primera aparición de un patrón de periodicidad semanal. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

