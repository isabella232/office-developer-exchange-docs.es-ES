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
description: El elemento DaysOfWeek describe los días de la semana que se usan en los patrones de periodicidad de elementos.
ms.openlocfilehash: 3036cbe3f93ff87b9a4d5dc7bf164e3e952b06fd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463723"
---
# <a name="daysofweek-daysofweektype"></a>DaysOfWeek (DaysOfWeekType)

El elemento **DaysOfWeek** describe los días de la semana que se usan en los patrones de periodicidad de elementos. 
  
```XML
<DaysOfWeek/>
```

**DaysOfWeekType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[WeeklyRecurrence](weeklyrecurrence.md) <br/> |Describe un patrón de periodicidad semanal.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. Los valores posibles son los siguientes:
  
- Domingo    
- lunes    
- martes    
- miércoles    
- jueves    
- viernes    
- Sábado    
- Day (este valor no es válido para un patrón de periodicidad semanal)    
- WEEKDAY (este valor no es válido para un patrón de periodicidad semanal)    
- WeekendDay (este valor no es válido para un patrón de periodicidad semanal)
    
Un patrón de periodicidad semanal puede contener varios valores. Los valores están separados por un carácter de espacio. Por ejemplo, para una periodicidad semanal de los martes y los jueves, el valor de texto será "martes jueves".
  
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

