---
title: RecurringDateTransition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RecurringDateTransition
api_type:
- schema
ms.assetid: 52fe1e05-3c50-40a1-8752-5c3c64c9f1ed
description: El elemento RecurringDateTransition representa una transición de zona horaria que se produce en una fecha específica cada año.
ms.openlocfilehash: 864f3f539c5440fbfc539ca6c2042b3d9edca267
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59529366"
---
# <a name="recurringdatetransition"></a>RecurringDateTransition

El **elemento RecurringDateTransition** representa una transición de zona horaria que se produce en una fecha específica cada año. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[To](to.md) <br/> |Especifica el [Period](period.md) o [TransitionsGroup](transitionsgroup.md) que es el destino de la transición de zona horaria.  <br/> |
|[TimeOffset](timeoffset.md) <br/> |Representa el desplazamiento de duración de la hora universal coordinada (UTC) para la transición de zona horaria.  <br/> |
|[Month (Time Zone Transition)](month-time-zone-transition.md) <br/> |Representa el mes en el que se produce la transición de zona horaria.  <br/> |
|[Day](day.md) <br/> |Representa el día del mes en el que se produce la transición de zona horaria.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Transitions](transitions.md) <br/> |Representa una colección de transiciones de zona horaria.  <br/> |
|[TransitionsGroup](transitionsgroup.md) <br/> |Representa una colección de transiciones de zona horaria.  <br/> |
   
## <a name="remarks"></a>Comentarios

Un ejemplo de una transición de zona horaria que podría representarse mediante el elemento [RecurringDateTransition](recurringdatetransition.md) es una transición que se produce el 15 de marzo de cada año. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

