---
title: ArchiveTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c4cb0718-37cd-41aa-86e7-b492c4bb86aa
description: El elemento ArchiveTag especifica el identificador de retención de la etiqueta de archivo establecida en un elemento o carpeta.
ms.openlocfilehash: c3545b505dc0596d7465154e0be7d6c758b24ec9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525242"
---
# <a name="archivetag"></a>ArchiveTag

El **elemento ArchiveTag** especifica el identificador de retención de la etiqueta de archivo establecida en un elemento o carpeta. 
  
```XML
<ArchiveTag IsExplicit=""></ArchiveTag>
```

 **RetentionTagType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**IsExplicit** <br/> |Especifica si la directiva de retención se establece explícitamente en un elemento o carpeta o si se hereda de una carpeta primaria.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarFolder](calendarfolder.md) <br/> |Representa una carpeta que contiene principalmente elementos de calendario.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un Exchange de calendario.  <br/> |
|[Contact](contact.md) <br/> |Representa un elemento de contacto en el Exchange almacén.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Representa una carpeta de contactos que se encuentra en un buzón.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[Folder](folder.md) <br/> |Define una carpeta para crear, obtener, buscar, sincronizar o actualizar.  <br/> |
|[Elemento](item.md) <br/> |Representa un elemento genérico en el Exchange almacén.  <br/> |
|[Mensaje](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo Exchange microsoft.  <br/> |
|[PostItem](postitem.md) <br/> |Representa un elemento de publicación en el Exchange almacén.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Representa una carpeta de búsqueda que se encuentra en un buzón.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea en el Exchange almacén.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Representa una carpeta de tareas que se encuentra en un buzón.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento ArchiveTag** es un GUID que identifica la directiva de retención. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Ver también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

