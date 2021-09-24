---
title: Item (UploadItemType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ab7058f2-615f-4393-a0d4-af76727f37e9
description: El elemento Item representa un único elemento que se cargará en un buzón.
ms.openlocfilehash: bd4681a19df2018db9e54ee39095cd602662650a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514448"
---
# <a name="item-uploaditemtype"></a>Item (UploadItemType)

El **elemento Item** representa un único elemento que se cargará en un buzón. 
  
[UploadItems](uploaditems.md)
  
[Items (NonEmptyArrayOfUploadItemsType)](items-nonemptyarrayofuploaditemstype.md)
  
[Item (UploadItemType)](item-uploaditemtype.md)
  
```XML
<Item CreateAction="" IsAssociated="">
   <ParentFolderId/>
   <ItemId/>
   <Data/>
</Item>
```

 **UploadItemType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**CreateAction** <br/> |Especifica la acción para cargar un elemento en un buzón. Este atributo es obligatorio.  <br/> |
|**IsAssociated** <br/> |Especifica si el elemento cargado es un elemento asociado a la carpeta. Este atributo es un valor booleano. Un valor **true** indica que el elemento es un elemento asociado a la carpeta. Este atributo es opcional.  <br/> |
   
#### <a name="createaction-attribute"></a>Atributo CreateAction

|**Valor**|**Descripción**|
|:-----|:-----|
|**CreateNew** <br/> |Indica que se carga una nueva copia del elemento original en el buzón. El [elemento ItemId](itemid.md) no debe estar presente si se usa el valor CreateNew. El nuevo identificador de elemento se devuelve en la respuesta.  <br/> |
|**Actualización** <br/> |Especifica que se actualizará el elemento indicado por **el elemento ItemId.** Se devuelve un error si el **elemento ItemId** no está presente o si el elemento no existe en la carpeta identificada por el [elemento ParentFolderId.](parentfolderid.md)  <br/> |
|**UpdateOrCreate** <br/> |Indica que primero se intenta actualizar el elemento. Si el elemento no existe en la carpeta especificada por el **elemento ParentFolderId,** se crea un nuevo elemento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ParentFolderId](parentfolderid.md) <br/> |Representa el identificador de la carpeta principal donde se crea un nuevo elemento o que contiene el elemento que se va a actualizar.  <br/> |
|[ItemId](itemid.md) <br/> |Contiene el identificador único y la clave de cambio de un elemento para crear o actualizar en el Exchange almacén.  <br/> |
|[Data (base64Binary)](data-base64binary.md) <br/> |Contiene los datos de un solo elemento que se cargarán en un buzón.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Items (NonEmptyArrayOfUploadItemsType)](items-nonemptyarrayofuploaditemstype.md) <br/> |Contiene una matriz de elementos para cargar en un buzón.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda Exchange Web Services.Este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación ExportItems](exportitems-operation.md)
  
[Operación UploadItems](uploaditems-operation.md)

