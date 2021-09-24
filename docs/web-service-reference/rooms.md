---
title: Rooms
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Rooms
api_type:
- schema
ms.assetid: 57b6079a-3d83-4429-861e-c551e9e1a991
description: El elemento Rooms es una lista de uno o más elementos que representan salas de reuniones.
ms.openlocfilehash: bcefa1fb380599e556b7c3e99235afc2057b1017
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524486"
---
# <a name="rooms"></a>Rooms

El **elemento Rooms** es una lista de uno o más elementos que representan salas de reuniones. 
  
[GetRoomsResponse](getroomsresponse.md)
  
[Rooms](rooms.md)
  
```xml
<Rooms>   <Room/></Rooms>
```

 **ArrayOfRoomsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Sala](room.md) <br/> |Define una dirección de correo electrónico y un nombre para mostrar que representa una sala de reuniones.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetRoomsResponse](getroomsresponse.md) <br/> ||
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetRooms](getrooms-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

