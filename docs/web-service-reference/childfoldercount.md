---
title: ChildFolderCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ChildFolderCount
api_type:
- schema
ms.assetid: e0e4eabd-802f-4dd0-9911-89e08c66a15e
description: El elemento ChildFolderCount representa el número de carpetas secundarias inmediatas que se encuentran dentro de una carpeta. Esta propiedad es de sólo lectura.
ms.openlocfilehash: 6ea3b9c000c7836b55c6bf359c95870ed28350e0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463947"
---
# <a name="childfoldercount"></a>ChildFolderCount

El elemento **ChildFolderCount** representa el número de carpetas secundarias inmediatas que se encuentran dentro de una carpeta. Esta propiedad es de sólo lectura. 
  
```xml
<ChildFolderCount/>
```

 **int**
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

El valor de texto representa un número entero. Esta propiedad es de sólo lectura.
  
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

