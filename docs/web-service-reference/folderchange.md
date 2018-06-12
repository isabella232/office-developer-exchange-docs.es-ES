---
title: FolderChange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderChange
api_type:
- schema
ms.assetid: 23279750-131b-4e1a-b7d1-be235c4e0891
description: El elemento FolderChange representa una colección de los cambios que se debe realizar en una sola carpeta.
ms.openlocfilehash: 3f8b42ff4ac88eaef53d1d4ec1d61212bc14b8c7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764679"
---
# <a name="folderchange"></a>FolderChange

El elemento **FolderChange** representa una colección de los cambios que se debe realizar en una sola carpeta. 
  
[UpdateFolder](updatefolder.md)
  
[FolderChanges](folderchanges.md)
  
[FolderChange](folderchange.md)
  
```xml
<FolderChange>
   <FolderId/>
   <Updates/>
</FolderChange>
```

 **FolderChangeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contiene el identificador y cambiar la clave de una carpeta que se va a actualizar.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifica las carpetas de MicrosoftExchange Server 2007 que se pueden hacer referencia por su nombre.  <br/> |
|[Actualizaciones (carpeta)](updates-folder.md) <br/> |Define el tipo de actualización que se lleva a cabo en una carpeta que se identifica con el elemento el [FolderId](folderid.md) o [DistinguishedFolderId](distinguishedfolderid.md) .  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[FolderChanges](folderchanges.md) <br/> |Representa una colección de cambios para una carpeta.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/UpdateFolder/FolderChanges` <br/> |
   
## <a name="remarks"></a>Notas

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación UpdateFolder](updatefolder-operation.md)

