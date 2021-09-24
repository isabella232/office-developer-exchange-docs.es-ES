---
title: TimeOffset
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- TimeOffset
api_type:
- schema
ms.assetid: b70bf498-cc3a-4fa6-8236-514acb973b33
description: El elemento TimeOffset representa el desplazamiento de tiempo de la hora universal coordinada (UTC) para la transición de zona horaria.
ms.openlocfilehash: ac2da7d6ab1d59d075111390513b1a3dd58a892e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522547"
---
# <a name="timeoffset"></a>TimeOffset

El **elemento TimeOffset** representa el desplazamiento de tiempo de la hora universal coordinada (UTC) para la transición de zona horaria. 
  
```XML
<TimeOffset/>
```

 **duration**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RecurringDateTransition](recurringdatetransition.md) <br/> |Representa una transición de zona horaria que se produce en una fecha específica cada año.  <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Representa una transición de zona horaria que se produce el mismo día de cada año.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento TimeOffset** es una duración que especifica el desplazamiento de tiempo desde UTC para la transición de zona horaria. 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

