---
title: Occurrence (Time Zone Transition)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Occurrence
api_type:
- schema
ms.assetid: 5c1142b1-c51f-42e1-bbb2-57e00cad0fdb
description: El elemento Occurrence representa la ocurrencia del día de la semana en el mes en que se produce la transición de zona horaria.
ms.openlocfilehash: 9790b0e9541da0c22f2eac59850b8a361645c7b4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539288"
---
# <a name="occurrence-time-zone-transition"></a>Occurrence (Time Zone Transition)

El **elemento Occurrence** representa la ocurrencia del día de la semana en el mes en que se produce la transición de zona horaria. 
  
```xml
<Occurrence/>
```

**int**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Representa una transición de zona horaria que se produce el mismo día de cada año.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto es un entero que representa la aparición del día de la semana en el mes en que se produce la transición de zona horaria. En la tabla siguiente se enumeran los valores posibles.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|1  <br/> |La primera aparición del día especificado de la semana desde el principio del mes.  <br/> |
|2  <br/> |La segunda aparición del día especificado de la semana desde el principio del mes.  <br/> |
|3  <br/> |La tercera aparición del día especificado de la semana desde el principio del mes.  <br/> |
|4   <br/> |La cuarta aparición del día especificado de la semana desde el principio del mes.  <br/> |
|-1  <br/> |La primera aparición del día especificado de la semana desde el final del mes.  <br/> |
|-2  <br/> |La segunda aparición del día especificado de la semana a partir del final del mes.  <br/> |
|-3  <br/> |La tercera aparición del día especificado de la semana desde el final del mes.  <br/> |
|-4  <br/> |La cuarta aparición del día especificado de la semana a partir del final del mes.  <br/> |
   
## <a name="remarks"></a>Comentarios

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

