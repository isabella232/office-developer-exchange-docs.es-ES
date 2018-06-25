---
title: Regla
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
description: El elemento de regla contiene una regla de protección única.
ms.openlocfilehash: 9abbb70381c214211172d2d5ba1ed43ee4797f17
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837263"
---
# <a name="rule"></a>Regla

El elemento de **regla** contiene una regla de protección única. 
  
```XML
<Rule Name="" UserOverridable=="" Priority="">
   <Condition/>
   <Action/>
</Rule>
```

 **ProtectionRuleType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**Name** <br/> |Identifica el nombre de la regla. Un atributo requerido de tipo string con una longitud mínima de 1.  <br/> |
|**UserOverridable** <br/> |Especifica si la regla es obligatoria. Si la regla es obligatoria, este valor de atributo debe ser **false**. Un atributo requerido de tipo Boolean.  <br/> |
|**Priority** <br/> |Especifica la prioridad de la regla. Requiere un atributo de tipo int, con un valor mínimo de 1.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Condición](condition.md) <br/> |Identifica la condición que debe cumplirse para el elemento de acción de la regla que se va a ejecutar.  <br/> |
|[Acción (ProtectionRuleActionType)](action-protectionruleactiontype.md) <br/> |Identifica la acción que se debe ejecutar si coincide con la parte de la condición de la regla.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Reglas](rules-ex15websvcsotherref.md) <br/> |Contiene una matriz de las reglas de protección.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

