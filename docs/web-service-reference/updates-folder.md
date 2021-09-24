---
title: Updates (Carpeta)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Updates
api_type:
- schema
ms.assetid: b047e3a4-a5ab-4098-b7a0-273bc809e702
description: El elemento Updates contiene un conjunto de elementos que definen los cambios de anexar, establecer y eliminar a las propiedades de la carpeta.
ms.openlocfilehash: cb40f2a5b66f407b02c636c5115bcab5d382a6fd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510767"
---
# <a name="updates-folder"></a>Updates (Carpeta)

El **elemento Updates** contiene un conjunto de elementos que definen los cambios de anexar, establecer y eliminar a las propiedades de la carpeta. 
  
- [UpdateFolder](updatefolder.md)
  
- [FolderChanges](folderchanges.md)
  
- [FolderChange](folderchange.md)
  
- [Updates (Carpeta)](updates-folder.md)
  
```xml
<Updates>
   <AppendToFolderField/>
   <SetFolderField/>
   <DeleteFolderField/>
</Updates>
```

**NonEmptyArrayOfFolderChangeDescriptionsType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AppendToFolderField](appendtofolderfield.md) <br/> |Representa los datos que se anexarán a una propiedad de carpeta durante una [operación UpdateFolder](updatefolder-operation.md).  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |Representa una actualización de una sola propiedad de una carpeta en una [operación UpdateFolder](updatefolder-operation.md).  <br/> |
|[DeleteFolderField](deletefolderfield.md) <br/> |Representa una operación para eliminar una propiedad determinada de una carpeta durante una [operación UpdateFolder](updatefolder-operation.md).  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderChange](folderchange.md) <br/> |Representa una colección de cambios que se deben realizar en una sola carpeta.  <br/> A continuación se muestra la expresión XPath de este elemento:  `/UpdateFolder/FolderChanges/FolderChange[i]` <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación UpdateFolder](updatefolder-operation.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

