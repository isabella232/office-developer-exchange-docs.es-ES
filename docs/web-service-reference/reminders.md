---
title: Reminders
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 19294300-ab84-4784-8aa7-3395a08de640
description: El elemento Reminders especifica los avisos devueltos en la respuesta a una solicitud GetReminders.
ms.openlocfilehash: 0b760e93bf27f0fdaad9464580fad924367dea32
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513412"
---
# <a name="reminders"></a>Reminders

El **elemento Reminders** especifica los avisos devueltos en la respuesta a una **solicitud GetReminders.** 
  
```XML
<Reminders>
   <Reminder></Reminder>
</Reminders>
```

 **ArrayOfRemindersType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[Aviso](reminder.md)
  
### <a name="parent-elements"></a>Elementos principales

[GetRemindersResponse](getremindersresponse.md)
  
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



[GetRemindersResponse](getremindersresponse.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

