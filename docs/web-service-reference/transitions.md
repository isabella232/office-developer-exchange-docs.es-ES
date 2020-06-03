---
title: Transiciones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Transitions
api_type:
- schema
ms.assetid: 26f38f1c-96a3-440e-805c-1437886d11c5
description: El elemento Transitions representa una matriz de transiciones de zona horaria.
ms.openlocfilehash: d48fb8872b2f7e052f733c32e5dd1c9b4d04d898
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467441"
---
# <a name="transitions"></a>Transiciones

El elemento **Transitions** representa una matriz de transiciones de zona horaria. 
  
```xml
<Transitions Id="">
   <Transition/>
   <AbsoluteDateTransition/>
   <RecurringDayTransition/>
   <RecurringDateTransition/>
</Transitions>
```

 **ArrayOfTransitionsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|Id  <br/> |Representa el identificador único de la definición de zona horaria.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AbsoluteDateTransition](absolutedatetransition.md) <br/> |Representa una transición de zona horaria que se produce en una fecha específica y a una hora específica.  <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Representa una transición de zona horaria que se produce el mismo día cada año.  <br/> |
|[RecurringDateTransition](recurringdatetransition.md) <br/> |Representa una transición de zona horaria que se produce en un día del año especificado.  <br/> |
|[Transición](transition.md) <br/> |Representa una transición de zona horaria.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[StartTimeZone](starttimezone.md) <br/> |Define la zona horaria de la hora de inicio de un [CalendarItem](calendaritem.md) o [MeetingRequest](meetingrequest.md).  <br/> |
|[EndTimeZone](endtimezone.md) <br/> |Define la zona horaria de la hora de finalización de [CalendarItem](calendaritem.md) o [MeetingRequest](meetingrequest.md).  <br/> |
|[TimeZoneDefinition](timezonedefinition.md) <br/> |Define una zona horaria.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

