---
title: DaysOfWeek (DayOfWeekType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DaysOfWeek
api_type:
- schema
ms.assetid: ba8f990d-d37d-403d-b31f-55e5208c8ad5
description: El elemento DaysOfWeek describe los días de la semana que se usan en los patrones de periodicidad de elementos.
ms.openlocfilehash: f30184755117c7561b66e93491cbd68534064eeb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525109"
---
# <a name="daysofweek-dayofweektype"></a>DaysOfWeek (DayOfWeekType)

El **elemento DaysOfWeek** describe los días de la semana que se usan en los patrones de periodicidad de elementos. 
  
```xml
<DaysOfWeek/>
```

**DayOfWeekType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
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
- Weekday (no se usa en TimeChangePatternTypes)    
- WeekendDay (no se usa en TimeChangePatternTypes)
    
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

