---
title: DaysOfWeek (DaysOfWeekType)
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
ms.assetid: c56f997d-28f3-4590-97b0-cb71f016dbe4
description: El elemento DaysOfWeek describe los días de la semana que se usan en los patrones de periodicidad de elementos.
ms.openlocfilehash: 9b0786149f943c47ab77bcb69b74542cbc08edd5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519873"
---
# <a name="daysofweek-daysofweektype"></a>DaysOfWeek (DaysOfWeekType)

El **elemento DaysOfWeek** describe los días de la semana que se usan en los patrones de periodicidad de elementos. 
  
```XML
<DaysOfWeek/>
```

**DaysOfWeekType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
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
- Weekday (este valor no es válido para un patrón de periodicidad semanal)    
- WeekendDay (este valor no es válido para un patrón de periodicidad semanal)
    
Un patrón de periodicidad semanal puede contener varios valores. Los valores están separados por un carácter de espacio. Por ejemplo, para una periodicidad semanal los martes y jueves, el valor de texto será "Martes jueves".
  
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

