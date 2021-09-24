---
title: ActionType (ReminderActionType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 0ffcdcf4-8ea3-483c-bb7f-0cd84126120c
description: El elemento ActionType especifica la acción que se debe realizar en el aviso.
ms.openlocfilehash: d78725c75ad13a71d69d7749f0a71cd99d606929
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522260"
---
# <a name="actiontype-reminderactiontype"></a>ActionType (ReminderActionType)

El **elemento ActionType** especifica la acción que se debe realizar en el aviso. 
  
```XML
<ActionType> Dismiss | Snooze </ActionType>
```

 **ReminderActionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[ReminderItemAction](reminderitemaction.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento ActionType** especifica la acción que se debe realizar en el aviso. El valor de texto **de Dismiss** indica que se debe descartar el aviso. El valor de texto **de Snooze** indica que el aviso debe retrasarse hasta la hora especificada por el [elemento NewReminderTime.](newremindertime.md) 
  
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

- [ReminderItemAction](reminderitemaction.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

