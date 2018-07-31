---
title: Recurrence (TaskRecurrenceType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Recurrence
api_type:
- schema
ms.assetid: 99f8414a-9110-4721-a6e5-ebf225d7ed0a
description: El elemento de periodicidad contiene información de periodicidad de las tareas repetitivas.
ms.openlocfilehash: 0ec43447e47050a0bd483d8441da88e4a7f08923
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354424"
---
# <a name="recurrence-taskrecurrencetype"></a>Recurrence (TaskRecurrenceType)

El elemento de **Periodicidad** contiene información de periodicidad de las tareas repetitivas. 
  
```xml
<Recurrence>
      <RelativeYearlyRecurrence/>
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRecurrence/> 
      <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <RelativeMonthlyRecurrence/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteMonthlyRecurrence/> 
      <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <MonthlyRegeneration/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <DailyRegeneration/> 
      <EndDateRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
       <DailyRegeneration/> 
       <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <DailyRegeneration/> 
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
       <MonthlyRegeneration/> 
       <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <YearlyRegeneration/> 
      <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <YearlyRegeneration/> 
      <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteMonthlyRecurrence/> 
      <NumberedRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRegeneration/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <RelativeMonthlyRecurrence/> 
      <EndDateRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <RelativeYearlyRecurrence/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRegeneration/> 
      <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteYearlyRecurrence/> 
      <NumberedRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <RelativeMonthlyRecurrence/> 
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <YearlyRegeneration/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRecurrence/> 
      <EndDateRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <RelativeYearlyRecurrence/> 
      <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
       <MonthlyRegeneration/> 
       <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteYearlyRecurrence/> 
      <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteMonthlyRecurrence/> 
      <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
       <DailyRecurrence/> 
       <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRegeneration/> 
      <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteYearlyRecurrence/> 
      <EndDateRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <DailyRecurrence/> 
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <DailyRecurrence/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRecurrence/> 
      <NumberedRecurrence/>
</Recurrence>
```


**TaskRecurrenceType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |Describe un patrón de periodicidad anual relativa de una tarea periódica.  <br/> |
|[AbsoluteYearlyRecurrence](absoluteyearlyrecurrence.md) <br/> |Representa un patrón de periodicidad anual de una tarea periódica.  <br/> |
|[RelativeMonthlyRecurrence](relativemonthlyrecurrence.md) <br/> |Describe un patrón de periodicidad mensual relativa de una tarea periódica.  <br/> |
|[AbsoluteMonthlyRecurrence](absolutemonthlyrecurrence.md) <br/> |Representa un patrón de periodicidad mensual para una tarea periódica.  <br/> |
|[WeeklyRecurrence](weeklyrecurrence.md) <br/> |Describe la frecuencia, en semanas y los días en que se repite una tarea.  <br/> |
|[DailyRecurrence](dailyrecurrence.md) <br/> |Describe la frecuencia, en días, en el que se repite una tarea.  <br/> |
|[DailyRegeneration](dailyregeneration.md) <br/> |Describe el número de días después de la finalización de la tarea actual de la siguiente aparición será vencimiento.  <br/> |
|[WeeklyRegeneration](weeklyregeneration.md) <br/> |Describe cuántas semanas después de la finalización de la tarea actual de la siguiente aparición será vencimiento.  <br/> |
|[MonthlyRegeneration](monthlyregeneration.md) <br/> |Describe el número de meses después de la finalización de la tarea actual de la siguiente aparición será vencimiento.  <br/> |
|[YearlyRegeneration](yearlyregeneration.md) <br/> |Describe cómo muchos años después de la finalización de la tarea actual de la siguiente aparición será vencimiento.  <br/> |
|[NoEndRecurrence](noendrecurrence.md) <br/> |Describe un patrón de periodicidad que no tiene una fecha de finalización definidas.  <br/> El uso de este elemento excluye el uso de los elementos [EndDateRecurrence](enddaterecurrence.md) y [NumberedRecurrence](numberedrecurrence.md) .  <br/> |
|[EndDateRecurrence](enddaterecurrence.md) <br/> |Describe la fecha de inicio y la fecha de finalización de un patrón de periodicidad de elemento.  <br/> El uso de este elemento excluye el uso de los elementos [NoEndRecurrence](noendrecurrence.md) y [NumberedRecurrence](numberedrecurrence.md) .  <br/> [EndDateRecurrence](enddaterecurrence.md) no se puede usar junto con un patrón de regeneración.  <br/> |
|[NumberedRecurrence](numberedrecurrence.md) <br/> |Describe la fecha de inicio y el número de repeticiones de un elemento periódico.  <br/> El uso de este elemento excluye el uso de los elementos [NoEndRecurrence](noendrecurrence.md) y [EndDateRecurrence](enddaterecurrence.md) .  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Tarea](task.md) <br/> |Representa una tarea en el almacén de Exchange.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

