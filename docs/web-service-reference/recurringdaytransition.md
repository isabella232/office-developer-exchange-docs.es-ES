---
title: RecurringDayTransition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurringDayTransition
api_type:
- schema
ms.assetid: 1ae28d14-c2b8-4084-9e76-e2e347a884ce
description: El elemento RecurringDayTransition representa una transición de zona horaria que se produce el mismo día cada año.
ms.openlocfilehash: 44c2a6ec4dbaaa52a2772cb5c35a84b14dd77f97
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468470"
---
# <a name="recurringdaytransition"></a>RecurringDayTransition

El elemento **RecurringDayTransition** representa una transición de zona horaria que se produce el mismo día cada año. 
  
```xml
<RecurringDayTransition>
   <To/>
   <TimeOffset/>
   <Month/>
   <DayOfWeek/>
   <Occurrence/>
</RecurringDayTransition>
```

 **RecurringDayTransitionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[To](to.md) <br/> |Especifica el [punto](period.md) o [TransitionsGroup](transitionsgroup.md) que es el destino de la transición de zona horaria.  <br/> |
|[TimeOffset](timeoffset.md) <br/> |Representa el desplazamiento de duración desde la hora universal coordinada (UTC) para la transición de zona horaria.  <br/> |
|[Mes (transición de zona horaria)](month-time-zone-transition.md) <br/> |Representa el mes en el que se produce la transición de zona horaria.  <br/> |
|[DayOfWeek (TimeZone)](dayofweek-timezone.md) <br/> |Representa el día de la semana en el que se produce la transición de zona horaria.  <br/> |
|[Aparición (transición de zona horaria)](occurrence-time-zone-transition.md) <br/> |Representa la ocurrencia del día de la semana del mes en que se produce la transición de zona horaria.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Transiciones](transitions.md) <br/> |Representa una colección de transiciones de zona horaria.  <br/> |
|[TransitionsGroup](transitionsgroup.md) <br/> |Representa una colección de transiciones de zona horaria.  <br/> |
   
## <a name="remarks"></a>Comentarios

Un ejemplo de una transición de zona horaria que podría representarse mediante el elemento [RecurringDayTransition](recurringdaytransition.md) es una transición que se produce el segundo martes de febrero de cada año. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

