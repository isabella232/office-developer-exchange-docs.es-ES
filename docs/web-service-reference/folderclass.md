---
title: FolderClass
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderClass
api_type:
- schema
ms.assetid: 0041d135-2869-4612-89a5-d1aa86aa1093
description: El elemento FolderClass representa la clase de carpeta de una carpeta.
ms.openlocfilehash: ee5d382251a66ab5fbcd8054e6b5cfac82b5f994
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460060"
---
# <a name="folderclass"></a>FolderClass

El elemento **FolderClass** representa la clase de carpeta de una carpeta. 
  
```xml
<FolderClass/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Representa una carpeta en un buzón.  <br/> |
|[Hubiera](calendarfolder.md) <br/> |Representa una carpeta de calendario en un buzón.  <br/> |
|[Hubiera](contactsfolder.md) <br/> |Representa una carpeta de contactos en un buzón.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Representa una carpeta de búsqueda en un buzón.  <br/> |
|[Hubiera](tasksfolder.md) <br/> |Representa una carpeta de tareas en un buzón.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. Las clases de carpeta normalmente comienzan con "IPF".
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

