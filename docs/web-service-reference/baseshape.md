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
description: El elemento BaseShape identifica el conjunto de propiedades que se devolverá en una respuesta de elemento o carpeta.
ms.openlocfilehash: 9b3f00ff94fbfe6ad6373b16ad95eb9136f81c64
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464493"
---
# <a name="baseshape"></a>BaseShape

El elemento **BaseShape** identifica el conjunto de propiedades que se devolverá en una respuesta de elemento o carpeta. 
  
```xml
<BaseShape>IdOnly or Default or AllProperties</BaseShape>
```

 **DefaultShapeNamesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> | Identifica las propiedades de carpeta que se incluirán en la respuesta GetFolder, FindFolder o SyncFolderHierarchy.<br/><br/>Las siguientes son las expresiones XPath de este elemento:<br/><br/>`/GetFolder/FolderShape` <br/>  `/FindFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[ItemShape](itemshape.md) <br/> | Identifica el contenido y las propiedades de los elementos que se van a incluir en una respuesta GetItem, FindItem o SyncFolderItems.<br/><br/>Las siguientes son las expresiones XPath de este elemento:<br/><br/>`/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. En la siguiente tabla se enumeran los valores de texto posibles.
  
**Valores de texto para el elemento BaseShape**

|**Valor**|**Descripción**|
|:-----|:-----|
|IdOnly  <br/> |Devuelve solo el identificador de elemento o carpeta.  <br/> |
|Predeterminado  <br/> |Devuelve un conjunto de propiedades que se definen como valores predeterminados para el elemento o carpeta.  <br/> |
|AllProperties  <br/> |Devuelve todas las propiedades usadas por la capa de lógica empresarial de Exchange para crear una carpeta.  <br/> |
   
En la siguiente tabla se enumeran las propiedades predeterminadas que se devuelven para una solicitud FindFolder. Todas las subcarpetas de una carpeta determinada se devuelven en orden por nombre.
  
**Propiedades predeterminadas**

|**Folder**|**Propiedades predeterminadas**|
|:-----|:-----|
|Bandeja de entrada  <br/> |FolderId, nombre para mostrar, número de no leídos, recuento total, número de subcarpetas  <br/> |
|Contactos  <br/> |FolderId, nombre para mostrar, recuento total, número de subcarpetas  <br/> |
|Calendar  <br/> |FolderId, nombre para mostrar, número de subcarpetas  <br/> |
|Borradores  <br/> |FolderId, nombre para mostrar, número de no leídos, recuento total, número de subcarpetas  <br/> |
|Elementos eliminados  <br/> |FolderId, nombre para mostrar, número de no leídos, recuento total, número de subcarpetas  <br/> |
|Otras carpetas  <br/> |FolderId, nombre para mostrar, número de no leídos, recuento total, número de subcarpetas  <br/> |
|Bandeja de salida  <br/> |FolderId, nombre para mostrar, número de no leídos, recuento total, número de subcarpetas  <br/> |
|Tareas  <br/> |FolderId, nombre para mostrar, recuento de vencidas, recuento total, número de subcarpetas  <br/> |
|Notas  <br/> |FolderId, nombre para mostrar, recuento total, número de subcarpetas  <br/> |
   
## <a name="remarks"></a>Comentarios

Para devolver propiedades además de las identificadas por el elemento [BaseShape](baseshape.md) , use el elemento [AdditionalProperties](additionalproperties.md) . 
  
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
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [FolderShape](foldershape.md)
- [ItemShape](itemshape.md)

