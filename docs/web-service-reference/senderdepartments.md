---
title: SenderDepartments
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SenderDepartments
api_type:
- schema
ms.assetid: b016cdde-d597-40ac-87c4-63ca68bd539d
description: El elemento SenderDepartments especifica que el departamento del remitente coincide con cualquiera de los departamentos especificados en los elementos value secundarios (ProtectionRuleValueType).
ms.openlocfilehash: 20feef066646cff988c1a26ee90da7dcade07e90
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59527533"
---
# <a name="senderdepartments"></a>SenderDepartments

El **elemento SenderDepartments** especifica que el departamento del remitente coincide con cualquiera de los departamentos especificados en los elementos [value secundarios (ProtectionRuleValueType).](value-protectionrulevaluetype.md) 
  
```XML
<SenderDepartments>
   <Value/>
</SenderDepartments>
```

 **ProtectionRuleSenderDepartmentsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) <br/> |Identifica un único departamento de remitente.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Condition](condition.md) <br/> |Identifica la condición que debe cumplirse para que se ejecute la parte de acción de la regla.  <br/> |
|[And (ProtectionRuleAndType)](and-protectionruleandtype.md) <br/> |Especifica que todos los elementos secundarios deben coincidir para evaluar a **true**. Especifica que debe haber más de una condición secundaria de regla de protección.  <br/> |
   
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

