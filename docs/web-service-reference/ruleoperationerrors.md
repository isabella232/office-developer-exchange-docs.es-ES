---
title: RuleOperationErrors
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f15c7b9e-a670-4a11-bb62-2a298c91f142
description: El elemento RuleOperationErrors representa una matriz de errores de validación de reglas en cada campo de regla que tiene un error.
ms.openlocfilehash: 2428d68719e7d9ef5d1fdf87ec94f1f9390bf631
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524500"
---
# <a name="ruleoperationerrors"></a>RuleOperationErrors

El **elemento RuleOperationErrors** representa una matriz de errores de validación de reglas en cada campo de regla que tiene un error. 
  
[UpdateInboxRulesResponse](updateinboxrulesresponse.md)
  
[RuleOperationErrors](ruleoperationerrors.md)
  
```XML
<RuleOperationErrors>
    <RuleOperationError>
</RuleOperationErrors>
```

 **ArrayOfRuleOperationErrorsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RuleOperationError](ruleoperationerror.md) <br/> |Representa un error de operación de regla.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[UpdateInboxRulesResponse](updateinboxrulesresponse.md) <br/> |Define una respuesta a una [solicitud UpdateInboxRules.](updateinboxrules.md)  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



[UpdateInboxRules](updateinboxrules.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

