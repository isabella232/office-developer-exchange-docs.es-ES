---
title: Rule
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Rule
api_type:
- schema
ms.assetid: c30f3851-bd56-4473-9106-dc85e9619486
description: El elemento Rule contiene una sola regla de protección.
ms.openlocfilehash: 45fb13ae6e1aacb78e7e8520f8678097796e339f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517878"
---
# <a name="rule"></a>Rule

El **elemento Rule** contiene una sola regla de protección. 
  
```XML
<Rule Name="" UserOverridable=="" Priority="">
   <Condition/>
   <Action/>
</Rule>
```

 **ProtectionRuleType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Name** <br/> |Identifica el nombre de la regla. Atributo obligatorio de tipo string con una longitud mínima de 1.  <br/> |
|**UserOverridable** <br/> |Especifica si la regla es obligatoria. Si la regla es obligatoria, este valor de atributo debe ser **false**. Atributo obligatorio de tipo Boolean.  <br/> |
|**Prioridad** <br/> |Especifica la prioridad de regla. Atributo obligatorio de tipo int con un valor mínimo de 1.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Condition](condition.md) <br/> |Identifica la condición que debe cumplirse para que se ejecute la parte de acción de la regla.  <br/> |
|[Action (ProtectionRuleActionType)](action-protectionruleactiontype.md) <br/> |Identifica qué acción debe ejecutarse si la parte de condición de la regla coincide.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Reglas ](rules-ex15websvcsotherref.md) <br/> |Contiene una matriz de reglas de protección.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
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

