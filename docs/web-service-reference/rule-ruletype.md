---
title: Rule (RuleType)
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
ms.assetid: 259a1f62-b235-4964-88bf-2d1f1c05a563
description: El elemento Rule contiene una sola regla y representa una regla en el buzón de un usuario.
ms.openlocfilehash: 0e7d7284d561ea374f66106072df0c4f850c590c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59527519"
---
# <a name="rule-ruletype"></a>Rule (RuleType)

El **elemento Rule** contiene una sola regla y representa una regla en el buzón de un usuario. 
  
```XML
<Rule>
    <RuleId>
    <DisplayName>
    <Priority>
    <IsEnabled>
    <IsNotSupported>
    <IsInError>
    <Conditions>
    <Exceptions>
    <Actions>
</Rule>
```

 **RuleType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RuleId](ruleid.md) <br/> |Especifica el identificador de regla.  <br/> |
|[DisplayName (cadena)](displayname-string.md) <br/> |Contiene el nombre para mostrar de una regla.  <br/> |
|[Prioridad](priority.md) <br/> |Indica el orden en que se va a ejecutar una regla.  <br/> |
|[IsEnabled](isenabled.md) <br/> |Indica si la regla está habilitada.  <br/> |
|[IsNotSupported](isnotsupported.md) <br/> |Indica si la regla no se puede modificar con las API de código administrado.  <br/> |
|[IsInError](isinerror.md) <br/> |Indica si la regla es una condición de error.  <br/> |
|[Condiciones](conditions.md) <br/> |Identifica las condiciones que, cuando se cumplan, desencadenarán las acciones de regla para una regla.  <br/> |
|[Excepciones](exceptions.md) <br/> |Identifica las excepciones que representan todas las condiciones de excepción de regla disponibles para la regla de bandeja de entrada.  <br/> |
|[Actions](actions.md) <br/> |Representa las acciones que se deben realizar en un mensaje cuando se cumplan las condiciones.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CreateRuleOperation](createruleoperation.md) <br/> |Representa una operación para crear una nueva regla.  <br/> |
|[InboxRules](inboxrules.md) <br/> |Representa una matriz de reglas en el buzón del usuario.  <br/> |
|[SetRuleOperation](setruleoperation.md) <br/> |Representa una operación para actualizar una regla existente.  <br/> |
   
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
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



[UpdateInboxRules](updateinboxrules.md)
  
[SetRuleOperation](setruleoperation.md)
  
[CreateRuleOperation](createruleoperation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

