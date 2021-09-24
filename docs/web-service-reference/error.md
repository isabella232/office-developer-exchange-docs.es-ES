---
title: Error
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Error
api_type:
- schema
ms.assetid: b1f54673-578a-496b-99f5-0fde2c669278
description: El elemento Error representa un único error de validación en un valor de propiedad de regla determinado, un valor de propiedad predicado o un valor de propiedad action.
ms.openlocfilehash: aeeda25ccc3e657e99bd6f2fea12322fdd3e720d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530864"
---
# <a name="error"></a>Error

El **elemento Error** representa un único error de validación en un valor de propiedad de regla determinado, un valor de propiedad predicado o un valor de propiedad action. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FieldUri (Rule)](fielduri-rule.md) <br/> |Especifica el URI del campo de regla que provocó el error de validación.  <br/> |
|[ErrorCode](errorcode.md) <br/> |Representa un código de error de validación de regla que describe qué error de validación para cada predicado o acción de regla.  <br/> |
|[ErrorMessage](errormessage.md) <br/> |Representa el motivo del error de validación.  <br/> |
|[FieldValue](fieldvalue.md) <br/> |Representa el valor del campo que provocó el error de validación.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ValidationErrors](validationerrors.md) <br/> |Representa una matriz de errores de validación de reglas en cada campo de regla que tiene un error.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

