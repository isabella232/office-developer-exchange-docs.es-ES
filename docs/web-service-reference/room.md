---
title: Sala
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Room
api_type:
- schema
ms.assetid: a2cde8b8-2d31-4ebf-8171-f4dfd650d079
description: El elemento Room representa una sala de reuniones.
ms.openlocfilehash: 3d5d587853e435016fdff6b9d268892a35fea825
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460536"
---
# <a name="room"></a>Sala

El elemento **Room** representa una sala de reuniones. 
  
[Sala](rooms.md)
  
[Sala](room.md)
  
```XML
<Room>
   <Id/>
</Room>
```

 **RoomType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Identificador (EmailAddressType)](id-emailaddresstype.md) <br/> |Un identificador que contiene una dirección de correo electrónico y un nombre para mostrar que representa la sala de reuniones.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Sala](rooms.md) <br/> |Define una lista de salas de reuniones asociadas con una característica común, como la ubicación en el mismo edificio.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetRooms](getrooms-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

