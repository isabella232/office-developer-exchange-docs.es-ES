---
title: Notificaciones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Notifications
api_type:
- schema
ms.assetid: 153cc420-d2fe-42f1-afb2-9a31ee09a750
description: El elemento de notificaciones contiene una matriz de información acerca de la suscripción y los eventos que se han producido desde la última notificación.
ms.openlocfilehash: f576bf579c91b77dcde8646a6af7fdc47145aef7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836550"
---
# <a name="notifications"></a>Notificaciones

El elemento de **notificaciones** contiene una matriz de información acerca de la suscripción y los eventos que se han producido desde la última notificación. 
  
```xml
<Notifications>
   <Notification/>
</Notifications>
```

 **NonEmptyArrayOfNotificationsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Notificación](notification-ex15websvcsotherref.md) <br/> |Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GetStreamingEventsResponseMessage](getstreamingeventsresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación GetStreamingEvents](getstreamingevents-operation.md) .  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages y http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de los mensajes; Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Messages.xsd; Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetFolder](getfolder-operation.md)
  
[Operación DeleteFolder](deletefolder-operation.md)
  
[Operación MoveFolder](movefolder-operation.md)
  
[Operación CopyFolder](copyfolder-operation.md)
  
[Operación de suscripción](subscribe-operation.md)

