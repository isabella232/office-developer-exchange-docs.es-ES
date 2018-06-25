---
title: UnreadCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnreadCount
api_type:
- schema
ms.assetid: 53b22647-1453-4707-9ea0-6a8369748d56
description: El elemento UnreadCount contiene el recuento de elementos no leídos dentro de una carpeta.
ms.openlocfilehash: fbe887f8f6d83fbcf48ed9593b3d19322a7f48be
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840790"
---
# <a name="unreadcount"></a>UnreadCount

El elemento **UnreadCount** contiene el recuento de elementos no leídos dentro de una carpeta. 
  
```XML
<UnreadCount/>
```

 **xs: int**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Conversación (ConversationType)](conversation-conversationtype.md) <br/> |Representa una sola conversación.  <br/> |
|[Folder](folder.md) <br/> |Representa una carpeta en un buzón de correo.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Representa un evento que se modifica una carpeta o elemento.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Representa una carpeta de búsqueda en un buzón de correo.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Representa una carpeta de tareas en un buzón de correo.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa un valor entero. Esta propiedad es de sólo lectura.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

