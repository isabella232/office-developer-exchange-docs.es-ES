---
title: MarkAsJunk
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bafc6-7ee3-4b2b-9fd1-7c51328f4729
description: El elemento MarkAsJunk especifica la solicitud para mover un elemento a la carpeta correo electrónico no deseado y para agregar el remitente a la lista de remitentes bloqueados.
ms.openlocfilehash: fbb3eee7ce350954888931ca55b27f596656b161
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836350"
---
# <a name="markasjunk"></a>MarkAsJunk

El elemento **MarkAsJunk** especifica la solicitud para mover un elemento a la carpeta correo electrónico no deseado y para agregar el remitente a la lista de remitentes bloqueados. 
  
```XML
<MarkAsJunk IsJunk="true | false" MoveItem="true | false">
   <ItemIds/>
</MarkAsJunk>
```

 **MarkAsJunkType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|IsJunk  <br/> |Un valor de texto de **true** para el atributo **IsJunk** indica que el remitente de correo electrónico se agrega a la lista de remitentes bloqueados. Un valor de **false** indica que el remitente de correo electrónico se elimina de la lista de remitentes bloqueados, si el remitente de correo electrónico ya está en la lista.  <br/> |
|MoveItem  <br/> |Un valor de texto de **true** para el atributo **MoveItem** indica que el elemento se mueve a la carpeta de correo electrónico no deseado de forma predeterminada. Un valor de **false** indica que el elemento no se mueve a la carpeta de correo electrónico no deseado de forma predeterminada.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

[ItemId](itemids.md)
  
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Observaciones

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

