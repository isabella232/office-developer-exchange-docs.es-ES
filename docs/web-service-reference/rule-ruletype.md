---
title: Regla (RuleType)
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
ms.assetid: 259a1f62-b235-4964-88bf-2d1f1c05a563
description: El elemento de regla contiene una única regla y representa una regla en el buzón del usuario.
ms.openlocfilehash: b1f9f058213543633335db11f03729964baf98ad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837259"
---
# <a name="rule-ruletype"></a>Regla (RuleType)

El elemento de **regla** contiene una única regla y representa una regla en el buzón del usuario. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Identificador de regla](ruleid.md) <br/> |Especifica el identificador de regla.  <br/> |
|[DisplayName (cadena)](displayname-string.md) <br/> |Contiene el nombre para mostrar de una regla.  <br/> |
|[Priority](priority.md) <br/> |Indica el orden en el que es una regla para ejecutarse.  <br/> |
|[IsEnabled](isenabled.md) <br/> |Indica si la regla está habilitada.  <br/> |
|[IsNotSupported](isnotsupported.md) <br/> |Indica si la regla no se puede modificar con la API de código administrado.  <br/> |
|[IsInError](isinerror.md) <br/> |Indica si la regla es una condición de error.  <br/> |
|[Condiciones](conditions.md) <br/> |Identifica las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla para una regla.  <br/> |
|[Excepciones](exceptions.md) <br/> |Identifica las excepciones que representan todas las condiciones de excepción de regla disponibles para la regla de bandeja de entrada.  <br/> |
|[Acciones](actions.md) <br/> |Representa las acciones que deben tomarse en un mensaje cuando se cumplen las condiciones.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[CreateRuleOperation](createruleoperation.md) <br/> |Representa una operación para crear una nueva regla.  <br/> |
|[InboxRules](inboxrules.md) <br/> |Representa una matriz de las reglas en el buzón del usuario.  <br/> |
|[SetRuleOperation](setruleoperation.md) <br/> |Representa una operación para actualizar una regla existente.  <br/> |
   
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
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[UpdateInboxRules](updateinboxrules.md)
  
[SetRuleOperation](setruleoperation.md)
  
[CreateRuleOperation](createruleoperation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

