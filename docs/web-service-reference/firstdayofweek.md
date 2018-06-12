---
title: FirstDayOfWeek
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FirstDayOfWeek
api_type:
- schema
ms.assetid: d6cf1bd3-a19b-4d5f-9e25-8e337a4939e0
description: El elemento de FirstDayOfWeek especifica el primer día de la semana.
ms.openlocfilehash: 99858d17213d077ce7c51ad1c746588f2f3939a7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764660"
---
# <a name="firstdayofweek"></a>FirstDayOfWeek

El elemento de **FirstDayOfWeek** especifica el primer día de la semana. 
  
```XML
<FirstDayOfWeek> Sunday | Monday | Tuesday | Wednesday | Thursday | Friday | Saturday</FirstDayOfWeek>
```

 **DayOfWeekType**
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

El valor de texto del elemento **FirstDayOfWeek** indica qué día de la semana se utiliza como el primer día de la semana. Los siguientes son los valores de texto posibles: 
  
- Domingo
    
- Lunes
    
- Martes
    
- Miércoles
    
- Jueves
    
- Viernes
    
- Sábado
    
## <a name="remarks"></a>Notas

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

