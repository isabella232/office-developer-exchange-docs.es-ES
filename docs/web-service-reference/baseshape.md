---
title: BaseShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BaseShape
api_type:
- schema
ms.assetid: 42c04f3b-abaa-4197-a3d6-d21677ffb1c0
description: El elemento BaseShape identifica el conjunto de propiedades para devolver una respuesta de elemento o carpeta.
ms.openlocfilehash: 69b27d23fd75d4c1a274f31dfa419b759dbb2bbe
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763613"
---
# <a name="baseshape"></a>BaseShape

El elemento **BaseShape** identifica el conjunto de propiedades para devolver una respuesta de elemento o carpeta. 
  
```xml
<BaseShape>IdOnly or Default or AllProperties</BaseShape>
```

 **DefaultShapeNamesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> | Identifica las propiedades de carpeta para incluir en la respuesta GetFolder, FindFolder o SyncFolderHierarchy.<br/><br/>Los siguientes son las expresiones de XPath para este elemento:<br/><br/>`/GetFolder/FolderShape` <br/>  `/FindFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[ItemShape](itemshape.md) <br/> | Identifica las propiedades de elemento y el contenido que desea incluir en una respuesta GetItem, FindItem o SyncFolderItems.<br/><br/>Los siguientes son las expresiones de XPath para este elemento:<br/><br/>`/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. En la siguiente tabla se enumera los posibles valores de texto.
  
**Valores de texto para el elemento BaseShape**

|**Valor**|**Descripción**|
|:-----|:-----|
|IdOnly  <br/> |Devuelve sólo el elemento o carpeta Id.  <br/> |
|Default  <br/> |Devuelve un conjunto de propiedades que se definen como el valor predeterminado para el elemento o la carpeta.  <br/> |
|AllProperties  <br/> |Devuelve todas las propiedades de la capa de lógica de negocios de Exchange utilizadas para construir una carpeta.  <br/> |
   
En la siguiente tabla se enumera las propiedades predeterminadas que se devuelven para una solicitud de FindFolder. Todas las subcarpetas de una carpeta determinada se devuelven en orden por su nombre.
  
**Propiedades predeterminadas**

|**Folder**|**Propiedades predeterminadas**|
|:-----|:-----|
|Bandeja de entrada  <br/> |FolderId, nombre para mostrar, count no leído, recuento total, recuento de subcarpeta  <br/> |
|Contactos  <br/> |FolderId, nombre para mostrar, el recuento total, el recuento de subcarpeta  <br/> |
|Calendario  <br/> |FolderId, nombre para mostrar, el recuento de subcarpeta  <br/> |
|Drafts  <br/> |FolderId, nombre para mostrar, count no leído, recuento total, recuento de subcarpeta  <br/> |
|Elementos eliminados  <br/> |FolderId, nombre para mostrar, count no leído, recuento total, recuento de subcarpeta  <br/> |
|Otras carpetas  <br/> |FolderId, nombre para mostrar, count no leído, recuento total, recuento de subcarpeta  <br/> |
|Bandeja de salida  <br/> |FolderId, nombre para mostrar, count no leído, recuento total, recuento de subcarpeta  <br/> |
|Tareas  <br/> |FolderId, nombre para mostrar, vencida count, recuento total, recuento de subcarpeta  <br/> |
|Notas  <br/> |FolderId, nombre para mostrar, el recuento total, el recuento de subcarpeta  <br/> |
   
## <a name="remarks"></a>Comentarios

Para devolver propiedades además de las identificado por el elemento [BaseShape](baseshape.md) , use el elemento [AdditionalProperties](additionalproperties.md) . 
  
## <a name="example"></a>Ejemplo

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindFolder>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [FolderShape](foldershape.md)
- [ItemShape](itemshape.md)

