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
description: El elemento Notifications contiene una matriz de información sobre la suscripción y los eventos que se han producido desde la última notificación.
ms.openlocfilehash: 88fc56ba6e672e3dea7a1d31f7cc1fda018b9a15
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462622"
---
# <a name="notifications"></a>Notificaciones

El elemento **Notifications** contiene una matriz de información sobre la suscripción y los eventos que se han producido desde la última notificación. 
  
```xml
<Notifications>
   <Notification/>
</Notifications>
```

 **NonEmptyArrayOfNotificationsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Notificación](notification-ex15websvcsotherref.md) <br/> |Contiene información sobre la suscripción y los eventos que se han producido desde la última notificación.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetStreamingEventsResponseMessage](getstreamingeventsresponsemessage.md) <br/> |Contiene el estado y el resultado de una sola solicitud de [operación GetStreamingEvents](getstreamingevents-operation.md) .  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages y https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes; Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Messages. xsd; Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetFolder](getfolder-operation.md)
  
[Operación DeleteFolder](deletefolder-operation.md)
  
[Operación MoveFolder](movefolder-operation.md)
  
[Operación CopyFolder](copyfolder-operation.md)
  
[Operación subscribe](subscribe-operation.md)

