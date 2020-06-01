---
title: DisplayName (cadena)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DisplayName
api_type:
- schema
ms.assetid: e7efbbe1-6629-4d11-bed1-ed899e3f9d77
description: El elemento DisplayName define el nombre para mostrar de una carpeta, un contacto, una lista de distribución, un usuario delegado, una ubicación o una regla.
ms.openlocfilehash: 9b566ec1938ec206e45cddf9c7f00083af2d8a9c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463619"
---
# <a name="displayname-string"></a>DisplayName (cadena)

El elemento **displayName** define el nombre para mostrar de una carpeta, un contacto, una lista de distribución, un usuario delegado, una ubicación o una regla. 
  
```XML
<DisplayName/>
```

 **String**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Hubiera](calendarfolder.md) <br/> |Representa una carpeta de calendario en un buzón.  <br/> |
|[Contacto](contact.md) <br/> |Representa un elemento de contacto de Exchange.  <br/> |
|[Hubiera](contactsfolder.md) <br/> |Representa una carpeta de contactos en un buzón.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[Folder](folder.md) <br/> |Representa una carpeta en un buzón.  <br/> |
|[Regla (RuleType)](rule-ruletype.md) <br/> |Representa una regla en el buzón de un usuario.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Representa una carpeta de búsqueda en un buzón.  <br/> |
|[Hubiera](tasksfolder.md) <br/> |Representa una carpeta de tareas en un buzón.  <br/> |
|[UserId](userid.md) <br/> |Identifica un usuario delegado o un usuario que tiene permisos de acceso a la carpeta.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Si se usa este elemento, es necesario un valor de texto que represente el nombre para mostrar.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="example"></a>Ejemplo

En el siguiente ejemplo se muestra cómo crear una carpeta nueva y establecer el valor de DisplayName de la carpeta en "TestFolder".
  
```cs
FolderType folder = new FolderType();
folder.DisplayName = "TestFolder";
```

## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

