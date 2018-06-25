---
title: NewReminderTime
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ff1b6b1c-3557-41d4-8aa6-9528fdb3a21a
description: El elemento NewReminderTime especifica una nueva hora para un aviso.
ms.openlocfilehash: 9f3f509942c673c916cc646cd9519240aef6ea06
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836531"
---
# <a name="newremindertime"></a>NewReminderTime

El elemento **NewReminderTime** especifica una nueva hora para un aviso. 
  
```XML
<NewReminderTime/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[ReminderItemAction](reminderitemaction.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **NewReminderTime** es una nueva hora para el aviso. El elemento **NewReminderTime** se usa cuando se establece el elemento de [ActionType](actiontype-reminderactiontype.md) para **Posponer**, con el fin de retraso el aviso. El valor de la **NewReminderTime** debe ser mayor que el [ReminderTime](remindertime.md) devuelto por la [operación de GetReminders](getreminders-operation.md).
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[ReminderItemAction](reminderitemaction.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

