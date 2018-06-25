---
title: DeleteFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteFolder
api_type:
- schema
ms.assetid: e37963f4-af9e-4481-b389-16175711e66d
description: El elemento DeleteFolder define una solicitud para eliminar las carpetas de un buzón en el almacén de Exchange.
ms.openlocfilehash: d31f98f26f537104e40b303de4199f45c65f49c7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764094"
---
# <a name="deletefolder"></a>DeleteFolder

El elemento **DeleteFolder** define una solicitud para eliminar las carpetas de un buzón en el almacén de Exchange. 
  
```XML
<DeleteFolder DeleteType="">
   <FolderIds/>
</DeleteFolder>
```

 **DeleteFolderType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**DeleteType** <br/> |Describe cómo se elimina una carpeta. Este atributo es necesario.  <br/> |
   
#### <a name="deletetype-attribute"></a>Atributo DeleteType

|**Valor**|**Descripción**|
|:-----|:-----|
|HardDelete  <br/> |Permanentemente se quita una carpeta desde el almacén.  <br/> |
|SoftDelete  <br/> |Se mueve una carpeta para el volcado de archivos si el volcado de archivos está habilitado.  <br/> |
|MoveToDeletedItems  <br/> |Una carpeta se mueve a la carpeta Elementos eliminados.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |Contiene una matriz de identificadores de carpeta que se usa para identificar las carpetas para eliminar.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Las opciones **MoveToDeletedItems** y **HardDelete** son transaccionales, lo que significa que el tiempo de una llamada al servicio Web completa, la base de datos ha movido el elemento a la carpeta Elementos eliminados o quita permanentemente el elemento de la base de datos de Exchange. Este comportamiento es el mismo para MicrosoftExchange Server 2007 y Exchange Server 2010. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensaje  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación DeleteFolder](deletefolder-operation.md)

