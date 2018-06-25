---
title: Intervalo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Interval
api_type:
- schema
ms.assetid: d0c97a5f-96be-40c6-b7d4-abf4c3870adf
description: El elemento de intervalo define el intervalo entre dos elementos periódicos consecutivos.
ms.openlocfilehash: 55d26b5b1b51aca3effa93a2e6852c1ae57ef4b0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835962"
---
# <a name="interval"></a>Intervalo

El elemento de **intervalo** define el intervalo entre dos elementos periódicos consecutivos. 
  
```xml
<Interval/>
```

 **int**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[AbsoluteMonthlyRecurrence](absolutemonthlyrecurrence.md) <br/> |Representa un patrón de periodicidad mensual.  <br/> |
|[DailyRegeneration](dailyregeneration.md) <br/> |Describe la frecuencia, en días, en el que se vuelve a generar una tarea.  <br/> |
|[DailyRecurrence](dailyrecurrence.md) <br/> |Describe la frecuencia, en días, en el que se repite una tarea.  <br/> |
|[MonthlyRegeneration](monthlyregeneration.md) <br/> |Describe la frecuencia, en meses, en el que se vuelve a generar una tarea.  <br/> |
|[RelativeMonthlyRecurrence](relativemonthlyrecurrence.md) <br/> |Describe un patrón mensual relativo de una tarea periódica.  <br/> |
|[WeeklyRecurrence](weeklyrecurrence.md) <br/> |Describe la frecuencia, en semanas, en el que y los días en que se repite una tarea.  <br/> |
|[WeeklyRegeneration](weeklyregeneration.md) <br/> |Describe la frecuencia, en semanas, en el que se vuelve a generar una tarea.  <br/> |
|[YearlyRegeneration](yearlyregeneration.md) <br/> |Describe la frecuencia, en años, en el que se vuelve a generar una tarea.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto que representa un número entero.
  
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

