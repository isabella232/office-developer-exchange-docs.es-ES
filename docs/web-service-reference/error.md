---
title: Error
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Error
api_type:
- schema
ms.assetid: b1f54673-578a-496b-99f5-0fde2c669278
description: El elemento Error representa un error de validación único en un valor de la propiedad de regla concreto, valor de la propiedad predicado o valor de la propiedad acción.
ms.openlocfilehash: adb2de56b7610aa92b5bf5b8d43ac22f35021b64
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764437"
---
# <a name="error"></a>Error

El elemento **Error** representa un error de validación único en un valor de la propiedad de regla concreto, valor de la propiedad predicado o valor de la propiedad acción. 
  
```XML
<Error>
   <FieldUri/>
   <ErrorCode/>
   <ErrorMessage/>
   <FieldValue/>
</Error>
```

 **RuleValidationErrorType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[FieldUri (regla)](fielduri-rule.md) <br/> |Especifica el URI para el campo de regla que causó el error de validación.  <br/> |
|[ErrorCode](errorcode.md) <br/> |Representa un código de error de validación de regla que describe qué error de validación para cada predicado de la regla o la acción.  <br/> |
|[ErrorMessage](errormessage.md) <br/> |Representa el motivo del error de validación.  <br/> |
|[FieldValue](fieldvalue.md) <br/> |Representa el valor del campo que causó el error de validación.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ValidationErrors](validationerrors.md) <br/> |Representa una matriz de errores de validación de la regla en cada campo de regla que tiene un error.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Observaciones

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

