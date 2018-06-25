---
title: ReturnNewItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aeef79e4-31e1-4213-b627-9bac676be018
description: El elemento ReturnNewItemIds indica si se devuelven los identificadores de elemento de los elementos nuevos en la respuesta.
ms.openlocfilehash: 6d3bc83c05a82d6e448041167676f41c2620dcd4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837232"
---
# <a name="returnnewitemids"></a>ReturnNewItemIds

El elemento **ReturnNewItemIds** indica si se devuelven los identificadores de elemento de los elementos nuevos en la respuesta. 
  
```XML
<ReturnNewItemIds/>
```

 **xs: Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[CopyItem](copyitem.md) <br/> |Define una solicitud para copiar un elemento en un buzón en el almacén de Exchange.  <br/> |
|[MoveItem](moveitem.md) <br/> |Define una solicitud para mover un elemento en el almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto de **true** para el elemento **ReturnNewItemIds** indica que se devuelven los identificadores de elemento nuevo en la respuesta. Un valor de **false** indica que no se devuelven los identificadores de elemento nuevo en la respuesta. 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensaje  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   

