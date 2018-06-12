---
title: Acción (ProtectionRuleActionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Action
api_type:
- schema
ms.assetid: ca090dec-e2c5-49c8-a057-8d1f2409147f
description: El elemento de acción identifica qué acción se debe ejecutar si coincide con la parte de la condición de la regla.
ms.openlocfilehash: 8f699e698d3159c5ff2636da506542da3b218251
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764562"
---
# <a name="action-protectionruleactiontype"></a>Acción (ProtectionRuleActionType)

El elemento de **acción** identifica qué acción se debe ejecutar si coincide con la parte de la condición de la regla. 
  
```xml
<Action Name="">
   <Argument/>
</Action>

```

 **ProtectionRuleActionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**Name** <br/> |Identifica el nombre de la acción.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Argumento](argument.md) <br/> |Especifica los argumentos para la acción. Este elemento no se producirá si la acción especificada no requiere argumentos que se especifique. Este elemento puede producirse una o varias veces, si una acción requiere uno o más argumentos. La acción **RightsProtectMessage** contendrá un único argumento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Rule](rule.md) <br/> |Contiene una regla de protección única.  <br/> |
   
## <a name="remarks"></a>Notas

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

