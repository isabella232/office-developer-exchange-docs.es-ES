---
title: RecurringDateTransition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurringDateTransition
api_type:
- schema
ms.assetid: 52fe1e05-3c50-40a1-8752-5c3c64c9f1ed
description: El elemento RecurringDateTransition representa una transición de la zona horaria que se produce en una fecha específica de cada año.
ms.openlocfilehash: 7cd8f3452a744e0c9a98fd3698dffb9ed8721a6c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837014"
---
# <a name="recurringdatetransition"></a>RecurringDateTransition

El elemento **RecurringDateTransition** representa una transición de la zona horaria que se produce en una fecha específica de cada año. 
  
```xml
<RecurringDateTransition>
   <To/>
   <TimeOffset/>
   <Month/>
   <Day/>
</RecurringDateTransition>
```

 **RecurringDateTransitionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[To](to.md) <br/> |Especifica el [período](period.md) o [TransitionsGroup](transitionsgroup.md) que es el destino de la transición de la zona horaria.  <br/> |
|[TimeOffset](timeoffset.md) <br/> |Representa el desplazamiento de la duración de la hora Universal coordinada (UTC) para la transición de la zona horaria.  <br/> |
|[Mes (transición de la zona horaria)](month-time-zone-transition.md) <br/> |Representa el mes en el que se produce la transición de la zona horaria.  <br/> |
|[Día](day.md) <br/> |Representa el día del mes en el que se produce la transición de la zona horaria.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Transiciones](transitions.md) <br/> |Representa una colección de transiciones de zona horaria.  <br/> |
|[TransitionsGroup](transitionsgroup.md) <br/> |Representa una colección de transiciones de zona horaria.  <br/> |
   
## <a name="remarks"></a>Comentarios

Un ejemplo de una transición de la zona horaria que se puede representar en el elemento [RecurringDateTransition](recurringdatetransition.md) es una transición que se produce el 15 de marzo de cada año. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

