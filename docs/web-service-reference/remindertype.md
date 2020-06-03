---
title: ReminderType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfaf84eb-271a-4728-84fc-a20205a100bd
description: El elemento ReminderType especifica el tipo de avisos que se van a devolver.
ms.openlocfilehash: 4ac20143bbfb29fb8f962515f2faba224b2f973f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465530"
---
# <a name="remindertype"></a>ReminderType

El elemento **ReminderType** especifica el tipo de avisos que se van a devolver. 
  
```XML
<ReminderType> All | Current | Old </ReminderType>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[GetReminders](getreminders.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **ReminderType** es el tipo de avisos que se van a devolver, ya sea **todos**, **actual**o **antiguo**. **All** es el valor recomendado para este elemento. Para obtener más información acerca de la relación entre el elemento **ReminderType** y los elementos [BeginTime](begintime.md) y [EndTime](endtime-remindermessagedatatype.md) , consulte [GetReminders Operation](getreminders-operation.md).
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[GetReminders](getreminders.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

