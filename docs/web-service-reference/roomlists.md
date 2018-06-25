---
title: RoomLists
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RoomLists
api_type:
- schema
ms.assetid: 2b190823-b11e-4635-97e4-3aba5865fd05
description: El elemento RoomLists es una lista de una o varias direcciones que representan una lista de las salas de reuniones.
ms.openlocfilehash: eb03c34aeb5d80c4a9c6c92471e4094c63f04c87
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837252"
---
# <a name="roomlists"></a>RoomLists

El elemento **RoomLists** es una lista de una o varias direcciones que representan una lista de las salas de reuniones. 
  
[GetRoomListsResponse](getroomlistsresponse.md)
  
[RoomLists](roomlists.md)
  
```xml
<RoomLists>   <Address/></RoomLists>
```

 **ArrayOfEmailAddressesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Dirección (EmailAddressType)](address-emailaddresstype.md) <br/> |Define la dirección de correo electrónico y el nombre para mostrar que representa la lista de salas. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GetRoomListsResponse](getroomlistsresponse.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación GetRoomLists](getroomlists-operation.md) .  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con la función de servidor de acceso de cliente instalada.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetRoomLists](getroomlists-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

