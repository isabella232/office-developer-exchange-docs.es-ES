---
title: Aparición (transición de la zona horaria)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Occurrence
api_type:
- schema
ms.assetid: 5c1142b1-c51f-42e1-bbb2-57e00cad0fdb
description: El elemento de repetición representa la aparición del día de la semana del mes en el que se produce la transición de la zona horaria.
ms.openlocfilehash: bc5160480cc6881bb9d724aa61323f5717d1f2fa
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836636"
---
# <a name="occurrence-time-zone-transition"></a>Aparición (transición de la zona horaria)

El elemento de **repetición** representa la aparición del día de la semana del mes en el que se produce la transición de la zona horaria. 
  
```xml
<Occurrence/>
```

**int**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Representa una transición de la zona horaria que se produce en el mismo día cada año.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto es un entero que representa la aparición del día de la semana del mes en el que se produce la transición de la zona horaria. En la siguiente tabla se enumera los valores posibles.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|1  <br/> |La primera aparición del día de la semana desde el comienzo del mes especificado.  <br/> |
|2  <br/> |La segunda aparición del día de la semana desde el comienzo del mes especificado.  <br/> |
|3  <br/> |La tercera aparición de día de la semana desde el comienzo del mes especificado.  <br/> |
|4  <br/> |La aparición cuarto de día de la semana desde el comienzo del mes especificado.  <br/> |
|-1  <br/> |La primera aparición del día de la semana, desde el final del mes especificado.  <br/> |
|-2  <br/> |La segunda aparición del día de la semana, desde el final del mes especificado.  <br/> |
|-3  <br/> |La tercera aparición de día de la semana, desde el final del mes especificado.  <br/> |
|-4  <br/> |La cuarta aparición del día de la semana, desde el final del mes especificado.  <br/> |
   
## <a name="remarks"></a>Notas

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

