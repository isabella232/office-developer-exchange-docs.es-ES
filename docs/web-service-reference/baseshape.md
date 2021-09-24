---
title: BaseShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- BaseShape
api_type:
- schema
ms.assetid: 42c04f3b-abaa-4197-a3d6-d21677ffb1c0
description: El elemento BaseShape identifica el conjunto de propiedades que se devolverán en una respuesta de elemento o carpeta.
ms.openlocfilehash: b4e7f5c6d6520e7338f274b6275e371366b1bed5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514861"
---
# <a name="baseshape"></a>BaseShape

El **elemento BaseShape** identifica el conjunto de propiedades que se devolverán en una respuesta de elemento o carpeta. 
  
```xml
<BaseShape>IdOnly or Default or AllProperties</BaseShape>
```

 **DefaultShapeNamesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> | Identifica las propiedades de carpeta que se incluirán en la respuesta GetFolder, FindFolder o SyncFolderHierarchy.<br/><br/>Las siguientes son las expresiones XPath de este elemento:<br/><br/>`/GetFolder/FolderShape` <br/>  `/FindFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[ItemShape](itemshape.md) <br/> | Identifica las propiedades y el contenido del elemento que se incluirán en una respuesta GetItem, FindItem o SyncFolderItems.<br/><br/>Las siguientes son las expresiones XPath de este elemento:<br/><br/>`/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. En la tabla siguiente se enumeran los posibles valores de texto.
  
**Valores de texto para el elemento BaseShape**

|**Valor**|**Descripción**|
|:-----|:-----|
|IdOnly  <br/> |Devuelve solo el identificador de elemento o carpeta.  <br/> |
|Predeterminado  <br/> |Devuelve un conjunto de propiedades que se definen como el valor predeterminado para el elemento o carpeta.  <br/> |
|AllProperties  <br/> |Devuelve todas las propiedades usadas por la Exchange lógica empresarial para construir una carpeta.  <br/> |
   
En la tabla siguiente se enumeran las propiedades predeterminadas que se devuelven para una solicitud FindFolder. Todas las subcarpetas de una carpeta determinada se devuelven en orden por nombre.
  
**Propiedades predeterminadas**

|**Folder**|**Propiedades predeterminadas**|
|:-----|:-----|
|Bandeja de entrada  <br/> |FolderId, nombre para mostrar, recuento no leído, recuento total, recuento de subcarpetas  <br/> |
|Contactos  <br/> |FolderId, nombre para mostrar, recuento total, recuento de subcarpetas  <br/> |
|Calendario  <br/> |FolderId, nombre para mostrar, recuento de subcarpetas  <br/> |
|Borradores  <br/> |FolderId, nombre para mostrar, recuento no leído, recuento total, recuento de subcarpetas  <br/> |
|Elementos eliminados  <br/> |FolderId, nombre para mostrar, recuento no leído, recuento total, recuento de subcarpetas  <br/> |
|Otras carpetas  <br/> |FolderId, nombre para mostrar, recuento no leído, recuento total, recuento de subcarpetas  <br/> |
|Bandeja de salida  <br/> |FolderId, nombre para mostrar, recuento no leído, recuento total, recuento de subcarpetas  <br/> |
|Tareas  <br/> |FolderId, display name, past due count, total count, subfolder count  <br/> |
|Notas  <br/> |FolderId, nombre para mostrar, recuento total, recuento de subcarpetas  <br/> |
   
## <a name="remarks"></a>Comentarios

Para devolver propiedades además de las identificadas por el [elemento BaseShape,](baseshape.md) use el [elemento AdditionalProperties.](additionalproperties.md) 
  
## <a name="example"></a>Ejemplo

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [FolderShape](foldershape.md)
- [ItemShape](itemshape.md)

