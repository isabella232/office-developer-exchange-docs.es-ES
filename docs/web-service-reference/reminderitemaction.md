---
title: ReminderItemAction
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: fe67512c-5b15-4f07-8628-74cf873c2d71
description: El elemento ReminderItemAction especifica la acción de un elemento de aviso.
ms.openlocfilehash: 7cd6898bb44ecd442a02f162008225d904396ba0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512467"
---
# <a name="reminderitemaction"></a>ReminderItemAction

El **elemento ReminderItemAction** especifica la acción de un elemento de aviso. 
  
```XML
<ReminderItemAction>
   <ActionType></ActionType>
   <ItemId></ItemId>
   <NewReminderTime></NewReminderTime>
</ReminderItemAction>
```

 **ReminderItemActionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[ActionType (ReminderActionType)](actiontype-reminderactiontype.md)  |  [ItemId](itemid.md)  |  [NewReminderTime](newremindertime.md)
  
### <a name="parent-elements"></a>Elementos principales

[ReminderItemActions](reminderitemactions.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[ReminderItemActions](reminderitemactions.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

