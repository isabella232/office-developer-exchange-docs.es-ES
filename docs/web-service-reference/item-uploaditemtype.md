---
title: Elemento (UploadItemType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ab7058f2-615f-4393-a0d4-af76727f37e9
description: El elemento representa un solo elemento va a cargar en un buzón de correo.
ms.openlocfilehash: 8fecef9a2368a44e38633eb9fddaa8197620f6a1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836138"
---
# <a name="item-uploaditemtype"></a>Elemento (UploadItemType)

**El elemento** representa un solo elemento va a cargar en un buzón de correo. 
  
[UploadItems](uploaditems.md)
  
[Elementos (NonEmptyArrayOfUploadItemsType)](items-nonemptyarrayofuploaditemstype.md)
  
[Elemento (UploadItemType)](item-uploaditemtype.md)
  
```XML
<Item CreateAction="" IsAssociated="">
   <ParentFolderId/>
   <ItemId/>
   <Data/>
</Item>
```

 **UploadItemType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**CreateAction** <br/> |Especifica la acción para cargar un elemento en un buzón de correo. Este atributo es necesario.  <br/> |
|**IsAssociated** <br/> |Especifica si el elemento que se cargan es un elemento de la carpeta asociada. Este atributo es un valor de tipo Boolean. Un valor de **true** indica que el elemento es una carpeta asociada de elemento. Este atributo es opcional.  <br/> |
   
#### <a name="createaction-attribute"></a>Atributo CreateAction

|**Valor**|**Descripción**|
|:-----|:-----|
|**CreateNew** <br/> |Indica que se ha cargado una nueva copia del elemento original en el buzón de correo. El elemento de [ItemId](itemid.md) no debe estar presente si se usa el valor CreateNew. Se devuelve el identificador del elemento nuevo en la respuesta.  <br/> |
|**Actualizar** <br/> |Especifica que se actualizará el elemento indicado por el elemento **ItemId** . Se devuelve un error si el elemento de **ItemId** no está presente o si el elemento no existe en la carpeta identificada por el elemento [ID](parentfolderid.md) .  <br/> |
|**UpdateOrCreate** <br/> |Indica que se realiza en primer lugar un intento para actualizar el elemento. Si el elemento no existe en la carpeta especificada por el elemento **ID** , se crea un nuevo elemento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Id](parentfolderid.md) <br/> |Representa el identificador de la carpeta principal donde se crea un nuevo elemento o que contiene el elemento que se debe actualizar.  <br/> |
|[ItemId](itemid.md) <br/> |Contiene el único identificador y cambiar la clave de un elemento para crear o actualizar en el almacén de Exchange.  <br/> |
|[Datos (base64Binary)](data-base64binary.md) <br/> |Contiene los datos de un solo elemento va a cargar en un buzón de correo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Elementos (NonEmptyArrayOfUploadItemsType)](items-nonemptyarrayofuploaditemstype.md) <br/> |Contiene una matriz de elemento que se va a cargar en un buzón de correo.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Observaciones

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación ExportItems](exportitems-operation.md)
  
[Operación UploadItems](uploaditems-operation.md)

