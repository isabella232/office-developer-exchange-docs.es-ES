---
title: Elementos (NonEmptyArrayOfUploadItemsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Items
api_type:
- schema
ms.assetid: 402bfa6d-11d7-4547-b8bd-197e9922ab49
description: El elemento de elementos contiene una matriz de elementos que desea cargar en un buzón de correo.
ms.openlocfilehash: ac508b2026c3e0ec730154efeeff0a9669e6eff8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836156"
---
# <a name="items-nonemptyarrayofuploaditemstype"></a>Elementos (NonEmptyArrayOfUploadItemsType)

El elemento de **elementos** contiene una matriz de elementos que desea cargar en un buzón de correo. 
  
[UploadItems](uploaditems.md)
  
[Elementos (NonEmptyArrayOfUploadItemsType)](items-nonemptyarrayofuploaditemstype.md)
  
```XML
<Items>
   <Item/>
</Items>
```

 **NonEmptyArrayOfUploadItemsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Elemento (UploadItemType)](item-uploaditemtype.md) <br/> |Representa un solo elemento va a cargar en un buzón de correo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[UploadItems](uploaditems.md) <br/> |Representa una solicitud para cargar los elementos en un buzón de correo.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensaje  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación ExportItems](exportitems-operation.md)
  
[Operación UploadItems](uploaditems-operation.md)

