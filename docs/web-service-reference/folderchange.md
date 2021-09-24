---
title: FolderChange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FolderChange
api_type:
- schema
ms.assetid: 23279750-131b-4e1a-b7d1-be235c4e0891
description: El elemento FolderChange representa una colección de cambios que se realizarán en una sola carpeta.
ms.openlocfilehash: 3ea723e6bbfcfe048256715aa5a60da98076ccb8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541297"
---
# <a name="folderchange"></a>FolderChange

El **elemento FolderChange** representa una colección de cambios que se realizarán en una sola carpeta. 
  
- [UpdateFolder](updatefolder.md) 
- [FolderChanges](folderchanges.md) 
- [FolderChange](folderchange.md)
  
```xml
<FolderChange>
   <FolderId/>
   <Updates/>
</FolderChange>
```

```xml
<FolderChange>
   <DistinguishedFolderId/>
   <Updates/>
</FolderChange>
```

**FolderChangeType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contiene el identificador y la clave de cambio de una carpeta que se actualizará.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifica las carpetas de MicrosoftExchange Server 2007 a las que se puede hacer referencia por su nombre.  <br/> |
|[Updates (Carpeta)](updates-folder.md) <br/> |Define el tipo de actualización que se realiza en una carpeta identificada por el [elemento FolderId](folderid.md) o [DistinguishedFolderId.](distinguishedfolderid.md)  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderChanges](folderchanges.md) <br/> |Representa una colección de cambios para una carpeta.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/UpdateFolder/FolderChanges` <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación UpdateFolder](updatefolder-operation.md)

