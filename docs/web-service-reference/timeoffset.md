---
title: TimeOffset
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeOffset
api_type:
- schema
ms.assetid: b70bf498-cc3a-4fa6-8236-514acb973b33
description: El elemento TimeOffset representa el desplazamiento de tiempo de la hora Universal coordinada (UTC) para la transición de la zona horaria.
ms.openlocfilehash: 46b1b2c8eec9bae871b4dafe43036e9d725075ae
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840653"
---
# <a name="timeoffset"></a>TimeOffset

El elemento **TimeOffset** representa el desplazamiento de tiempo de la hora Universal coordinada (UTC) para la transición de la zona horaria. 
  
```XML
<TimeOffset/>
```

 **duration**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[RecurringDateTransition](recurringdatetransition.md) <br/> |Representa una transición de la zona horaria que se produce en una fecha específica de cada año.  <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Representa una transición de la zona horaria que se produce en el mismo día cada año.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **TimeOffset** es una duración que especifica el desplazamiento de tiempo de la hora UTC para la transición de la zona horaria. 
  
## <a name="remarks"></a>Notas

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

