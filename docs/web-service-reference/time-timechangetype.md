---
title: Hora (TimeChangeType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Time
api_type:
- schema
ms.assetid: be12e41e-6871-4f6b-b2d4-3dfa404f9ea1
description: El elemento Time describe el momento en que cambia el tiempo entre el horario estándar y el horario de verano.
ms.openlocfilehash: c25d0bc3394fdfab42a29eab8b370bc4263618ed
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465740"
---
# <a name="time-timechangetype"></a>Hora (TimeChangeType)

El elemento **Time** describe el momento en que cambia el tiempo entre el horario estándar y el horario de verano. 
  
```xml
<Time/>
```

 **Time**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Horario](daylight.md) <br/> |Representa la fecha y la hora en que cambia el horario de verano a la hora estándar.  <br/> |
|[Estándar](standard.md) <br/> |Representa la fecha y la hora en que cambia el horario de verano a la hora estándar.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa la hora en que cambia el tiempo entre el horario estándar y el horario de verano.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

