---
title: Periodicidad (TaskRecurrenceType)
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
description: El elemento recurrence contiene información de periodicidad para tareas periódicas.
ms.openlocfilehash: 933fd6b003d8d193e1561f2a22b65ac00237c345
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528835"
---
# <a name="recurrence-taskrecurrencetype"></a>Periodicidad (TaskRecurrenceType)

El elemento **recurrence** contiene información de periodicidad para tareas periódicas. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |Describe un patrón de periodicidad anual relativo para una tarea repetitiva.  <br/> |
|[AbsoluteYearlyRecurrence](absoluteyearlyrecurrence.md) <br/> |Representa un patrón de periodicidad anual para una tarea repetitiva.  <br/> |
|[RelativeMonthlyRecurrence](relativemonthlyrecurrence.md) <br/> |Describe un patrón de periodicidad mensual relativo para una tarea repetitiva.  <br/> |
|[AbsoluteMonthlyRecurrence](absolutemonthlyrecurrence.md) <br/> |Representa un patrón de periodicidad mensual para una tarea repetitiva.  <br/> |
|[WeeklyRecurrence](weeklyrecurrence.md) <br/> |Describe la frecuencia, en semanas, y los días que una tarea se repite.  <br/> |
|[DailyRecurrence](dailyrecurrence.md) <br/> |Describe la frecuencia, en días, en la que una tarea se repite.  <br/> |
|[DailyRegeneration](dailyregeneration.md) <br/> |Describe cuántos días tras la finalización de la tarea actual vencerá la próxima vez que se produzca.  <br/> |
|[WeeklyRegeneration](weeklyregeneration.md) <br/> |Describe el número de semanas después de la finalización de la tarea actual, la próxima vez que se deba.  <br/> |
|[MonthlyRegeneration](monthlyregeneration.md) <br/> |Describe cuántos meses después de la finalización de la tarea actual vencerá la próxima vez que se produzca.  <br/> |
|[YearlyRegeneration](yearlyregeneration.md) <br/> |Describe cuántos años tras la finalización de la tarea actual vencerá la próxima vez que se produzca.  <br/> |
|[NoEndRecurrence](noendrecurrence.md) <br/> |Describe un patrón de periodicidad que no tiene una fecha de finalización definida.  <br/> El uso de este elemento excluye el uso de los elementos [EndDateRecurrence](enddaterecurrence.md) y [NumberedRecurrence](numberedrecurrence.md) .  <br/> |
|[EndDateRecurrence](enddaterecurrence.md) <br/> |Describe la fecha de inicio y la fecha de finalización de un patrón de periodicidad de un elemento.  <br/> El uso de este elemento excluye el uso de los elementos [NoEndRecurrence](noendrecurrence.md) y [NumberedRecurrence](numberedrecurrence.md) .  <br/> [EndDateRecurrence](enddaterecurrence.md) no se puede usar junto con un patrón de regeneración.  <br/> |
|[NumberedRecurrence](numberedrecurrence.md) <br/> |Describe la fecha de inicio y el número de repeticiones de un elemento periódico.  <br/> El uso de este elemento excluye el uso de los elementos [NoEndRecurrence](noendrecurrence.md) y [EndDateRecurrence](enddaterecurrence.md) .  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Tarea](task.md) <br/> |Representa una tarea del almacén de Exchange.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

