---
title: ReminderItemAction
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fe67512c-5b15-4f07-8628-74cf873c2d71
description: El elemento ReminderItemAction especifica la acción para un elemento de recordatorio.
ms.openlocfilehash: 60722235ed3e73e6a9923df8d3c63a6fc123599a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466230"
---
# <a name="reminderitemaction"></a>ReminderItemAction

El elemento **ReminderItemAction** especifica la acción para un elemento de recordatorio. 
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

[ActionType (ReminderActionType)](actiontype-reminderactiontype.md)  |  [Itemid](itemid.md)  |  [NewReminderTime](newremindertime.md)
  
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
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[ReminderItemActions](reminderitemactions.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

