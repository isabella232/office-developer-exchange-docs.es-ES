---
title: ReminderType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfaf84eb-271a-4728-84fc-a20205a100bd
description: El elemento ReminderType especifica el tipo de avisos para devolver.
ms.openlocfilehash: 11739d2068a1009b2840b2169e86b113151cbfa9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837077"
---
# <a name="remindertype"></a>ReminderType

El elemento **ReminderType** especifica el tipo de avisos para devolver. 
  
```XML
<ReminderType> All | Current | Old </ReminderType>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[GetReminders](getreminders.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **ReminderType** es el tipo de avisos para devolver **todos los**, **actual**o **anterior**. **Todos los** es el valor recomendado para este elemento. Para obtener más información acerca de la relación entre el elemento de **ReminderType** y los elementos [BeginTime](begintime.md) y [EndTime](endtime-remindermessagedatatype.md) , vea [GetReminders operación](getreminders-operation.md).
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[GetReminders](getreminders.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

