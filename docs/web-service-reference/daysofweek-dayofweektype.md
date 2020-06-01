---
title: DaysOfWeek (DayOfWeekType)
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
ms.assetid: ba8f990d-d37d-403d-b31f-55e5208c8ad5
description: El elemento DaysOfWeek describe los días de la semana que se usan en los patrones de periodicidad de elementos.
ms.openlocfilehash: 44552350679df1fec3d237d9b09f1a5feb9cc4b6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458827"
---
# <a name="daysofweek-dayofweektype"></a>DaysOfWeek (DayOfWeekType)

El elemento **DaysOfWeek** describe los días de la semana que se usan en los patrones de periodicidad de elementos. 
  
```xml
<DaysOfWeek/>
```

**DayOfWeekType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |Describe un patrón de periodicidad anual relativo.  <br/> |
|[RelativeMonthlyRecurrence](relativemonthlyrecurrence.md) <br/> |Describe un patrón de periodicidad mensual relativo.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. Los valores posibles son los siguientes:
  
- Domingo    
- lunes    
- martes   
- miércoles    
- jueves    
- viernes    
- Sábado    
- Day (no se usa en TimeChangePatternTypes)    
- WEEKDAY (no se usa en TimeChangePatternTypes)    
- WeekendDay (no se usa en el TimeChangePatternTypes)
    
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

