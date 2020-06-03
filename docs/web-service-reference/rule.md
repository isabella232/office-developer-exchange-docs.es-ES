---
title: Rule
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Rule
api_type:
- schema
ms.assetid: c30f3851-bd56-4473-9106-dc85e9619486
description: El elemento rule contiene una única regla de protección.
ms.openlocfilehash: 6c18a2bd026893cd333bc7007203abf04a6f0be7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465004"
---
# <a name="rule"></a>Rule

El elemento **Rule** contiene una única regla de protección. 
  
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
|**Name** <br/> |Identifica el nombre de la regla. Un atributo necesario de tipo String con una longitud mínima de 1.  <br/> |
|**UserOverridable** <br/> |Especifica si la regla es obligatoria. Si la regla es obligatoria, el valor de este atributo debe ser **false**. Un atributo obligatorio de tipo Boolean.  <br/> |
|**Prioridad** <br/> |Especifica la prioridad de la regla. Un atributo obligatorio de tipo int con un valor mínimo de 1.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Condición](condition.md) <br/> |Identifica la condición que debe cumplirse para que se ejecute la parte de acción de la regla.  <br/> |
|[Acción (ProtectionRuleActionType)](action-protectionruleactiontype.md) <br/> |Identifica qué acción debe ejecutarse si la parte de condición de la regla coincide.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Reglas](rules-ex15websvcsotherref.md) <br/> |Contiene una matriz de reglas de protección.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

