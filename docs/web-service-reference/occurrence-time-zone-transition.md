---
title: Aparición (transición de zona horaria)
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
description: El elemento Representation representa la ocurrencia del día de la semana del mes en que se produce la transición de zona horaria.
ms.openlocfilehash: 846f6b22f43bcda07b9408d768d0845a5acfe668
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467980"
---
# <a name="occurrence-time-zone-transition"></a>Aparición (transición de zona horaria)

El **elemento** Representation representa la ocurrencia del día de la semana del mes en que se produce la transición de zona horaria. 
  
```xml
<Occurrence/>
```

**int**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Representa una transición de zona horaria que se produce el mismo día cada año.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto es un entero que representa la ocurrencia del día de la semana del mes en que se produce la transición de zona horaria. En la siguiente tabla se enumeran los valores posibles.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|1  <br/> |Primera aparición del día de la semana especificado desde el principio del mes.  <br/> |
|segundo  <br/> |Segunda aparición del día de la semana especificado desde el principio del mes.  <br/> |
|3  <br/> |La tercera repetición del día de la semana especificado desde el principio del mes.  <br/> |
|4   <br/> |La cuarta aparición del día de la semana especificado desde el principio del mes.  <br/> |
|-1  <br/> |Primera aparición del día de la semana especificado a partir del final del mes.  <br/> |
|-2  <br/> |Segunda aparición del día de la semana especificado a partir del final del mes.  <br/> |
|-3  <br/> |Tercera aparición del día de la semana especificado a partir del final del mes.  <br/> |
|-4  <br/> |La cuarta aparición del día de la semana especificado a partir del final del mes.  <br/> |
   
## <a name="remarks"></a>Comentarios

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

