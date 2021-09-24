---
title: Condición
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Condition
api_type:
- schema
ms.assetid: 0790a3f2-cb31-4036-a757-7821aa0722cb
description: El elemento Condition identifica la condición que debe cumplirse para que se ejecute la parte de acción de la regla.
ms.openlocfilehash: 80efb2121e813a966faf419233cac4d23e971bc6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512010"
---
# <a name="condition"></a>Condición

El **elemento Condition** identifica la condición que debe cumplirse para que se ejecute la parte de acción de la regla. 
  
```xml
<Condition>
   <AllInternal/>
</Condition>
```

```xml
<Condition> 
    <SenderDepartments/> 
</Condition>
```

```xml
<Condition> 
    <True/> 
</Condition>
```

```xml
<Condition> 
    <Recipients/> 
</Condition>
```

```xml
<Condition> 
    <And/> 
</Condition>
```

**ProtectionRuleConditionType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AllInternal](allinternal.md) <br/> |Se evalúa como **true** si todos los destinatarios de un mensaje de correo electrónico son internos de la organización del remitente.  <br/> |
|[And (ProtectionRuleAndType)](and-protectionruleandtype.md) <br/> |Especifica que todos los elementos secundarios deben coincidir para evaluar a **true**. Especifica que debe haber más de una condición secundaria de regla de protección.  <br/> |
|[RecipientIs](recipientis.md) <br/> |Especifica que cualquier destinatario del mensaje de correo electrónico coincide con cualquiera de los destinatarios especificados en los elementos [Value secundarios (ProtectionRuleValueType).](value-protectionrulevaluetype.md)  <br/> |
|[SenderDepartments](senderdepartments.md) <br/> |Especifica que el departamento del remitente coincide con cualquiera de los departamentos especificados en los elementos [value secundarios (ProtectionRuleValueType).](value-protectionrulevaluetype.md)  <br/> |
|[True](true.md) <br/> |Especifica una condición que siempre coincide.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Rule](rule.md) <br/> |Contiene una sola regla de protección.  <br/> |
   
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

