---
title: IsReadReceipt
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsReadReceipt
api_type:
- schema
ms.assetid: e60e525f-c136-469a-b68b-b3dc01f400a6
description: El elemento IsReadReceipt indica si los mensajes entrantes deben ser confirmaciones de lectura en el orden de la condición o excepción que se debe aplicar.
ms.openlocfilehash: 78714aafb116a609a69d77b3b4f0fd15695bda34
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836094"
---
# <a name="isreadreceipt"></a>IsReadReceipt

El elemento **IsReadReceipt** indica si los mensajes entrantes deben ser confirmaciones de lectura en el orden de la condición o excepción que se debe aplicar. 
  
```XML
<IsReadReceipt> true | false</IsReadReceipt>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Condiciones](conditions.md) <br/> |Representa las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla de esa regla.  <br/> |
|[Excepciones](exceptions.md) <br/> |Representa todas las condiciones de excepción de regla disponibles para la regla de bandeja de entrada.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto de **true** indica que el mensaje debe ser una confirmación de lectura en el orden de la condición o excepción que se debe aplicar. Si el mensaje no tiene que ser una confirmación de lectura para la condición o la excepción que se debe aplicar, el valor es **false**.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

