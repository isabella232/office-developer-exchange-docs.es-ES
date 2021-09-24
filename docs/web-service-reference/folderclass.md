---
title: FolderClass
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FolderClass
api_type:
- schema
ms.assetid: 0041d135-2869-4612-89a5-d1aa86aa1093
description: El elemento FolderClass representa la clase de carpeta de una carpeta.
ms.openlocfilehash: c94fd7aa889e9b4ba3fbd22df6c8593f4592a0d1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511744"
---
# <a name="folderclass"></a>FolderClass

El **elemento FolderClass** representa la clase de carpeta de una carpeta. 
  
```xml
<FolderClass/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Representa una carpeta de un buzón.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Representa una carpeta de calendario en un buzón.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Representa una carpeta de contactos en un buzón.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Representa una carpeta de búsqueda en un buzón.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Representa una carpeta de tareas en un buzón.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. Las clases de carpeta suelen empezar por "IPF".
  
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



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

