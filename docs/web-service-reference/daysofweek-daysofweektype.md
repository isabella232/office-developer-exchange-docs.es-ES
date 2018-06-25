---
title: DaysOfWeek (DaysOfWeekType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DaysOfWeek
api_type:
- schema
ms.assetid: c56f997d-28f3-4590-97b0-cb71f016dbe4
description: El elemento DaysOfWeek describe los días de la semana que se usan en los patrones de periodicidad de elemento.
ms.openlocfilehash: 0b730ff5a7bc9aa6b324fc080022d056c5342296
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764061"
---
# <a name="daysofweek-daysofweektype"></a>DaysOfWeek (DaysOfWeekType)

El elemento **DaysOfWeek** describe los días de la semana que se usan en los patrones de periodicidad de elemento. 
  
```XML
<DaysOfWeek/>
```

**DaysOfWeekType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[WeeklyRecurrence](weeklyrecurrence.md) <br/> |Describe un patrón de periodicidad semanal.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. Los valores posibles son:
  
- Domingo    
- Lunes    
- Martes    
- Miércoles    
- Jueves    
- Viernes    
- Sábado    
- Día (este valor no es válido para un patrón de periodicidad semanal)    
- Weekday (este valor no es válido para un patrón de periodicidad semanal)    
- WeekendDay (este valor no es válido para un patrón de periodicidad semanal)
    
Un patrón de periodicidad semanal puede contener varios valores. Los valores están separados por un carácter de espacio. Por ejemplo, para una periodicidad semanal el martes y los jueves, el valor de texto será "Martes jueves".
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

