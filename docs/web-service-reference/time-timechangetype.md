---
title: Tiempo (TimeChangeType)
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
description: El elemento de tiempo describe la hora cuando se cambia el tiempo entre la hora estándar y el horario de verano.
ms.openlocfilehash: db44ef494561b75dc55c93229cec3901f04235ad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840645"
---
# <a name="time-timechangetype"></a>Tiempo (TimeChangeType)

El elemento de **tiempo** describe la hora cuando se cambia el tiempo entre la hora estándar y el horario de verano. 
  
```xml
<Time/>
```

 **Time**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Horario de verano](daylight.md) <br/> |Representa la fecha y hora cuando se cambia la hora del horario de verano a la hora estándar.  <br/> |
|[Standard](standard.md) <br/> |Representa la fecha y hora cuando se cambia la hora del horario de verano a la hora estándar.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa la hora cuando se cambia el tiempo entre la hora estándar y el horario de verano.
  
## <a name="remarks"></a>Notas

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

