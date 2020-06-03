---
title: RuleOperationErrors
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f15c7b9e-a670-4a11-bb62-2a298c91f142
description: El elemento RuleOperationErrors representa una matriz de errores de validación de regla en cada campo de regla que tiene un error.
ms.openlocfilehash: d547155f3cbf9eedd0f9bfac7bf3768b3630b50e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464955"
---
# <a name="ruleoperationerrors"></a>RuleOperationErrors

El elemento **RuleOperationErrors** representa una matriz de errores de validación de regla en cada campo de regla que tiene un error. 
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RuleOperationError](ruleoperationerror.md) <br/> |Representa un error de operación de regla.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[UpdateInboxRulesResponse](updateinboxrulesresponse.md) <br/> |Define una respuesta a una solicitud [UpdateInboxRules](updateinboxrules.md) .  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[UpdateInboxRules](updateinboxrules.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

