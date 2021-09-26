---
title: InboxRules
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- InboxRules
api_type:
- schema
ms.assetid: 7bb9896c-bd12-49ae-842a-a10b5f9a2ef6
description: El elemento InboxRules representa una matriz de reglas en el buzón del usuario.
ms.openlocfilehash: 6b6b399f685accca90fbaffd3ed461aa43a3c2b3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59547235"
---
# <a name="inboxrules"></a>InboxRules

El **elemento InboxRules** representa una matriz de reglas en el buzón del usuario. 
  
[GetInboxRulesResponse](getinboxrulesresponse.md)
  
[InboxRules](inboxrules.md)
  
```XML
<InboxRules>
   <Rule/>
</InboxRules>
```

 **ArrayOfRulesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Rule (RuleType)](rule-ruletype.md) <br/> |Contiene una sola regla y representa una regla en el buzón del usuario.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetInboxRulesResponse](getinboxrulesresponse.md) <br/> |Define una respuesta a una [solicitud de operación GetInboxRules.](getinboxrules-operation.md)  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Consulte también



[GetInboxRules](getinboxrules.md)
  
[Operación de GetInboxRules](getinboxrules-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

