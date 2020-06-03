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
description: El elemento Action identifica qué acción debe ejecutarse si la parte de condición de la regla coincide.
ms.openlocfilehash: 220a6fea16abb9ea823ae6239537b8c121702589
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527512"
---
# <a name="action-protectionruleactiontype"></a>Acción (ProtectionRuleActionType)

El elemento **Action** identifica qué acción debe ejecutarse si la parte de condición de la regla coincide. 
  
```xml
<Action Name="">
   <Argument/>
</Action>

```

 **ProtectionRuleActionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Name** <br/> |Identifica el nombre de la acción.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Argumento](argument.md) <br/> |Especifica los argumentos de la acción. Este elemento no se producirá si la acción especificada no requiere que se especifiquen argumentos. Este elemento puede producirse una o varias veces si una acción requiere uno o más argumentos. La acción **RightsProtectMessage** contendrá un solo argumento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Rule](rule.md) <br/> |Contiene una regla de protección única.  <br/> |
   
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

