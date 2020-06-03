---
title: ActionType (ReminderActionType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0ffcdcf4-8ea3-483c-bb7f-0cd84126120c
description: El elemento ActionType especifica la acción que se llevará a cabo en el aviso.
ms.openlocfilehash: 5c62b2dd945b23a5ff2bb824385c45dbc617a5a5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465061"
---
# <a name="actiontype-reminderactiontype"></a>ActionType (ReminderActionType)

El elemento **ActionType** especifica la acción que se llevará a cabo en el aviso. 
  
```XML
<ActionType> Dismiss | Snooze </ActionType>
```

 **ReminderActionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[ReminderItemAction](reminderitemaction.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **ActionType** especifica la acción que se llevará a cabo en el aviso. El valor de texto **descartado** indica que el aviso debe descartarse. El valor de texto de **SNOOZE** indica que el aviso debe retrasarse hasta el tiempo especificado por el elemento [NewReminderTime](newremindertime.md) . 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [ReminderItemAction](reminderitemaction.md)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

