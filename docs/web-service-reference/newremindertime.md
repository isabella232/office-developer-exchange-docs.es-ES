---
title: NewReminderTime
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ff1b6b1c-3557-41d4-8aa6-9528fdb3a21a
description: El elemento NewReminderTime especifica una nueva hora para un aviso.
ms.openlocfilehash: 9e6cb75396f35f606bcd974e374f24957ee5d1ec
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515449"
---
# <a name="newremindertime"></a>NewReminderTime

El **elemento NewReminderTime** especifica una nueva hora para un aviso. 
  
```XML
<NewReminderTime/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[ReminderItemAction](reminderitemaction.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento NewReminderTime** es una nueva hora para el aviso. El **elemento NewReminderTime** se usa cuando el elemento [ActionType](actiontype-reminderactiontype.md) se establece en **Snooze**, para retrasar el aviso. El valor de **NewReminderTime** debe ser mayor que [el remindertime](remindertime.md) devuelto por la [operación GetReminders](getreminders-operation.md).
  
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



[ReminderItemAction](reminderitemaction.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

