---
title: ArchiveTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c4cb0718-37cd-41aa-86e7-b492c4bb86aa
description: El elemento ArchiveTag especifica el identificador de la retención de la etiqueta de archivo establecer en una carpeta o elemento.
ms.openlocfilehash: ae9c7d512981af3bf564bcb73a9a27c5c78217fc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763551"
---
# <a name="archivetag"></a>ArchiveTag

El elemento **ArchiveTag** especifica el identificador de la retención de la etiqueta de archivo establecer en una carpeta o elemento. 
  
```XML
<ArchiveTag IsExplicit=""></ArchiveTag>
```

 **RetentionTagType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**IsExplicit** <br/> |Especifica si la directiva de retención se establezca explícitamente en una carpeta o un elemento o si se hereda de una carpeta principal.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[CalendarFolder](calendarfolder.md) <br/> |Representa una carpeta que principalmente contiene los elementos del calendario.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange.  <br/> |
|[Contact](contact.md) <br/> |Representa un elemento de contacto en el almacén de Exchange.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Representa una carpeta de contactos que se encuentra en un buzón de correo.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[Folder](folder.md) <br/> |Define una carpeta para crear, obtener, buscar, sincronizar o actualizar.  <br/> |
|[Item](item.md) <br/> |Representa un elemento genérico en el almacén de Exchange.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico de Microsoft Exchange.  <br/> |
|[Objeto postItem](postitem.md) <br/> |Representa un elemento para exponer en el almacén de Exchange.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Representa una carpeta de búsqueda que se encuentra en un buzón de correo.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea en el almacén de Exchange.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Representa una carpeta de tareas que se encuentra en un buzón de correo.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **ArchiveTag** es un GUID que identifica la directiva de retención. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

