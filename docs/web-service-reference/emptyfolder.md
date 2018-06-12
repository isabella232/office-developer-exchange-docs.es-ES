---
title: EmptyFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 502b2841-103d-4340-97d5-51a1db813fb2
description: El elemento EmptyFolder define una solicitud para vaciar una carpeta en un buzón en el almacén de Exchange. De forma opcional, también se pueden eliminar las subcarpetas cuando se vacía la carpeta.
ms.openlocfilehash: c72e11cea29e2e55c9c29754eec60e73bd1e4d9c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764385"
---
# <a name="emptyfolder"></a>EmptyFolder

El elemento **EmptyFolder** define una solicitud para vaciar una carpeta en un buzón en el almacén de Exchange. De forma opcional, también se pueden eliminar las subcarpetas cuando se vacía la carpeta. 
  
```XML
<EmptyFolder>
   <FolderIds/>
</EmptyFolder>
```

 **EmptyFolderType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**DeleteType** <br/> |Especifica cómo se vacía una carpeta. Este atributo es necesario.  <br/> |
|**DeleteSubFolders** <br/> |Especifica si las subcarpetas se va a eliminar. Este atributo es necesario.  <br/> |
   
#### <a name="deletetype-attribute"></a>Atributo DeleteType

|**Valor**|**Descripción**|
|:-----|:-----|
|HardDelete  <br/> |A los mensajes y carpetas se quitan definitivamente desde el almacén.  <br/> |
|SoftDelete  <br/> |A los mensajes y carpetas se mueven al volcado de archivos si el volcado de archivos está habilitado.  <br/> |
|MoveToDeletedItems  <br/> |A los mensajes y carpetas se mueven a la carpeta Elementos eliminados.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |Contiene una matriz de identificadores de carpeta que se usa para identificar las carpetas para eliminar.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Observaciones

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensaje  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación EmptyFolder](emptyfolder-operation.md)

