---
title: FolderChanges
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FolderChanges
api_type:
- schema
ms.assetid: d3f611ed-56a4-43f8-aa65-cbd7844b827f
description: El elemento FolderChanges representa una colección de cambios para una carpeta.
ms.openlocfilehash: 2c3bfc3081e323771e9d909138f7ed03e3d50a84
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541290"
---
# <a name="folderchanges"></a>FolderChanges

El **elemento FolderChanges** representa una colección de cambios para una carpeta. 
  
[UpdateFolder](updatefolder.md)
  
[FolderChanges](folderchanges.md)
  
```xml
<FolderChanges>
   <FolderChange/>
</FolderChanges>
```

 **NonEmptyArrayOfFolderChangesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderChange](folderchange.md) <br/> |Representa un único cambio que se debe realizar en una sola carpeta.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[UpdateFolder](updatefolder.md) <br/> |Representa la operación que se usa para actualizar las propiedades de una carpeta.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/UpdateFolder` <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación UpdateFolder](updatefolder-operation.md)

