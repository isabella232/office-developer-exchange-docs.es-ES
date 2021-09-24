---
title: ValidationErrors
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ValidationErrors
api_type:
- schema
ms.assetid: 009526aa-22e7-4f5c-be88-079175aa9122
description: El elemento ValidationErrors representa una matriz de errores de validación de reglas en cada campo de regla que tiene un error.
ms.openlocfilehash: 9b771addfc99a4f7fadebc64aebc484a8ae6060e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522379"
---
# <a name="validationerrors"></a>ValidationErrors

El **elemento ValidationErrors** representa una matriz de errores de validación de reglas en cada campo de regla que tiene un error. 
  
```XML
<VaidationErrors>
   <Error/>
</ValidationErrors>
```

 **ArrayOfRuleValidationErrorsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Error](error.md) <br/> |Representa un único error de validación en un valor de propiedad de regla determinado, valor de propiedad de predicado o valor de propiedad action  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RuleOperationError](ruleoperationerror.md) <br/> |Representa un error de operación de regla.  <br/> |
   
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

