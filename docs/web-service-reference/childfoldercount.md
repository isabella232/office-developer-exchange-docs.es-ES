---
title: ChildFolderCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ChildFolderCount
api_type:
- schema
ms.assetid: e0e4eabd-802f-4dd0-9911-89e08c66a15e
description: El elemento ChildFolderCount representa el número de carpetas secundarias inmediatas que se encuentran dentro de una carpeta. Esta propiedad es de sólo lectura.
ms.openlocfilehash: c05d93e3f9df2d2acbb1b65f1116dab1aea24a3b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59537004"
---
# <a name="childfoldercount"></a>ChildFolderCount

El **elemento ChildFolderCount** representa el número de carpetas secundarias inmediatas que se encuentran dentro de una carpeta. Esta propiedad es de sólo lectura. 
  
```xml
<ChildFolderCount/>
```

 **int**
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
|[CalendarFolder](calendarfolder.md) <br/> |Representa una carpeta Calendar en un buzón.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Representa una carpeta Contactos de un buzón.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Representa una carpeta de búsqueda en un buzón.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Representa una carpeta Tareas en un buzón.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa un número entero. Esta propiedad es de sólo lectura.
  
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

