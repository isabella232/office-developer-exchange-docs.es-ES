---
title: Datos (base64Binary)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Data
api_type:
- schema
ms.assetid: 26d8c2d0-bed2-4aed-b381-20e2ace6892f
description: El elemento de datos contiene los datos de un solo elemento exportado o un elemento que se va a cargar en un buzón de correo.
ms.openlocfilehash: 9560273e31a64edb2254489961733dfe7360ad01
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764018"
---
# <a name="data-base64binary"></a>Datos (base64Binary)

El elemento de **datos** contiene los datos de un solo elemento exportado o un elemento que se va a cargar en un buzón de correo. 
  
```XML
<Data/>
```

**base64Binary**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ExportItemsResponseMessage](exportitemsresponsemessage.md) <br/> |Contiene el estado y los resultados de una solicitud para exportar un elemento de un solo buzón de correo.  <br/> |
|[Elemento (UploadItemType)](item-uploaditemtype.md) <br/> |Representa un solo elemento va a cargar en un buzón de correo.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El elemento de **datos** contiene los nombres de propiedad y valores de un elemento exportado o un elemento que se cargará en un buzón de correo. 
  
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

- [Operación ExportItems](exportitems-operation.md)
- [Operación UploadItems](uploaditems-operation.md)

