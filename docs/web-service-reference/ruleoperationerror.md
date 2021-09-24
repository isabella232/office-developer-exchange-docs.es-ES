---
title: RuleOperationError
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RuleOperationError
api_type:
- schema
ms.assetid: b447e610-d37c-40d3-9158-aa108a9f248e
description: El elemento RuleOperationError representa un error de operación de regla.
ms.openlocfilehash: 39010d276dc24f966208c07b3d757fde166d82cb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517857"
---
# <a name="ruleoperationerror"></a>RuleOperationError

El **elemento RuleOperationError** representa un error de operación de regla. 
  
```XML
<RuleOperationError>
    <OperationIndex/>
    <ValidationErrors/>
</RuleOperationError>
```

 **RuleOperationErrorType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[OperationIndex](operationindex.md) <br/> |Indica el índice de la operación en la solicitud que provocó el error de operación de regla.  <br/> |
|[ValidationErrors](validationerrors.md) <br/> |Representa una matriz de errores de validación de reglas en cada campo de regla que tiene un error.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RuleOperationErrors](ruleoperationerrors.md) <br/> |Representa una matriz de errores de validación de reglas en cada campo de regla que tiene un error.  <br/> |
   
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

