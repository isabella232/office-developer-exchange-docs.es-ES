---
title: AddressListId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a3334bb2-90dc-4fe1-96d9-890b13d9ff30
description: El elemento AddressListId especifica el identificador de una lista de direcciones.
ms.openlocfilehash: c33944bf6e41903a5de596628e1ce7ba9f7421e1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463611"
---
# <a name="addresslistid"></a>AddressListId

El elemento **AddressListId** especifica el identificador de una lista de direcciones. 
  
```XML
<AddressListId Id="">
</AddressListId>
```

 **AddressListIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Id** <br/> |Identificador de lista de direcciones de cadena. Este atributo es obligatorio.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ContextFolderId](contextfolderid.md) <br/> |Indica la carpeta que está destinada a las acciones que usan carpetas. Este elemento debe estar presente al copiar, eliminar, mover y establecer el estado de lectura en los elementos de la conversación de una carpeta de destino.  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |Especifica el identificador de la carpeta en la que se copian los elementos de correo electrónico.  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |Indica la carpeta de destino para las acciones de copiar y mover.  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |Especifica el identificador de la carpeta a la que se mueven los elementos de correo electrónico  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

