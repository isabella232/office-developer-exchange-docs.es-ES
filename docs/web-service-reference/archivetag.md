---
title: ArchiveTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c4cb0718-37cd-41aa-86e7-b492c4bb86aa
description: El elemento ArchiveTag especifica el identificador de retención de la etiqueta de archivo establecida en un elemento o carpeta.
ms.openlocfilehash: 23167f3c96a6756fe4c6d915a4de91e815e620d9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464766"
---
# <a name="archivetag"></a>ArchiveTag

El elemento **ArchiveTag** especifica el identificador de retención de la etiqueta de archivo establecida en un elemento o carpeta. 
  
```XML
<ArchiveTag IsExplicit=""></ArchiveTag>
```

 **RetentionTagType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**IsExplicit** <br/> |Especifica si la Directiva de retención se establece explícitamente en un elemento o una carpeta o si se hereda de una carpeta principal.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Hubiera](calendarfolder.md) <br/> |Representa una carpeta que contiene principalmente elementos de calendario.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange.  <br/> |
|[Contacto](contact.md) <br/> |Representa un elemento de contacto en el almacén de Exchange.  <br/> |
|[Hubiera](contactsfolder.md) <br/> |Representa una carpeta de contactos contenida en un buzón.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[Folder](folder.md) <br/> |Define una carpeta para crear, obtener, buscar, sincronizar o actualizar.  <br/> |
|[Elemento](item.md) <br/> |Representa un elemento genérico del almacén de Exchange.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico de Microsoft Exchange.  <br/> |
|[PostItem](postitem.md) <br/> |Representa un elemento post en el almacén de Exchange.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Representa una carpeta de búsqueda contenida en un buzón.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea del almacén de Exchange.  <br/> |
|[Hubiera](tasksfolder.md) <br/> |Representa una carpeta de tareas contenida en un buzón.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **ArchiveTag** es un GUID que identifica la Directiva de retención. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

