---
title: Actualizaciones (carpeta)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Updates
api_type:
- schema
ms.assetid: b047e3a4-a5ab-4098-b7a0-273bc809e702
description: El elemento de actualizaciones contiene un conjunto de elementos que definen append, establecer y eliminar los cambios realizados en las propiedades de la carpeta.
ms.openlocfilehash: 31f25b1e88fb8756f189a6d75259dd4fc198582f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840867"
---
# <a name="updates-folder"></a>Actualizaciones (carpeta)

El elemento de **actualizaciones** contiene un conjunto de elementos que definen append, establecer y eliminar los cambios realizados en las propiedades de la carpeta. 
  
- [UpdateFolder](updatefolder.md)
  
- [FolderChanges](folderchanges.md)
  
- [FolderChange](folderchange.md)
  
- [Actualizaciones (carpeta)](updates-folder.md)
  
```xml
<Updates>
   <AppendToFolderField/>
   <SetFolderField/>
   <DeleteFolderField/>
</Updates>
```

**NonEmptyArrayOfFolderChangeDescriptionsType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[AppendToFolderField](appendtofolderfield.md) <br/> |Representa los datos que se anexará a una propiedad de la carpeta durante una [operación de UpdateFolder](updatefolder-operation.md).  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |Representa una actualización a una propiedad única en una carpeta en una [operación de UpdateFolder](updatefolder-operation.md).  <br/> |
|[DeleteFolderField](deletefolderfield.md) <br/> |Representa una operación para eliminar una propiedad determinada de una carpeta durante una [operación de UpdateFolder](updatefolder-operation.md).  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[FolderChange](folderchange.md) <br/> |Representa una colección de los cambios que se debe realizar en una sola carpeta.  <br/> La siguiente es la expresión de XPath para este elemento:`/UpdateFolder/FolderChanges/FolderChange[i]` <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación UpdateFolder](updatefolder-operation.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

