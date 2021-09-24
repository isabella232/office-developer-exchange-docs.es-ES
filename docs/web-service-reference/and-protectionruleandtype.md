---
title: And (ProtectionRuleAndType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- And
api_type:
- schema
ms.assetid: 7fafd1c8-cd29-43a0-b383-f6595f934f48
description: El elemento And especifica que todos los elementos secundarios deben coincidir para evaluarse como true.
ms.openlocfilehash: 01721b460d87d3282a1a793966b0259e0f1342dd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518942"
---
# <a name="and-protectionruleandtype"></a>And (ProtectionRuleAndType)

El **elemento And** especifica que todos los elementos secundarios deben coincidir para evaluar como **true**.
  
```xml
<And>
   <AllInternal/>
   <And/>
   <RecipientIs/>
   <SenderDepartments/>
   <True/>
</And>
```

 **ProtectionRuleAndType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AllInternal](allinternal.md) <br/> |Se evalúa como **true** si todos los destinatarios de un mensaje de correo electrónico son internos de la organización del remitente.  <br/> |
|**And** <br/> |Especifica que todos los elementos secundarios deben coincidir para evaluar a **true**.  <br/> |
|[RecipientIs](recipientis.md) <br/> |Especifica que cualquier destinatario del mensaje de correo electrónico coincide con cualquiera de los destinatarios especificados en los elementos [Value secundarios (ProtectionRuleValueType).](value-protectionrulevaluetype.md)  <br/> |
|[SenderDepartments](senderdepartments.md) <br/> |Especifica que el departamento del remitente coincide con cualquiera de los departamentos especificados en los elementos [value secundarios (ProtectionRuleValueType).](value-protectionrulevaluetype.md)  <br/> |
|[True](true.md) <br/> |Especifica una condición que siempre coincide.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Condition](condition.md) <br/> |Identifica la condición que debe cumplirse para que se ejecute la parte de acción de la regla.  <br/> |
|**And** <br/> |Especifica que todos los elementos secundarios deben coincidir para evaluar a **true**.  <br/> |
   
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

