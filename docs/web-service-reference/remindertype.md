---
title: ReminderType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: bfaf84eb-271a-4728-84fc-a20205a100bd
description: El elemento ReminderType especifica el tipo de avisos que se devolverán.
ms.openlocfilehash: ab10db372efb935b335868f5d212ded84b29e6eb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518004"
---
# <a name="remindertype"></a>ReminderType

El **elemento ReminderType** especifica el tipo de avisos que se devolverán. 
  
```XML
<ReminderType> All | Current | Old </ReminderType>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[GetReminders](getreminders.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento ReminderType** es el tipo de avisos que se devolverán, ya sea **All**, **Current** o **Old**. **All** es el valor recomendado para este elemento. Para obtener más información acerca de la relación entre el **elemento ReminderType** y los [elementos BeginTime](begintime.md) y [EndTime,](endtime-remindermessagedatatype.md) vea [GetReminders operation](getreminders-operation.md).
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[GetReminders](getreminders.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

