---
title: MarkAsJunk
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bafc6-7ee3-4b2b-9fd1-7c51328f4729
description: El elemento MarkAsJunk especifica la solicitud para mover un elemento a la carpeta de correo no deseado y agregar el remitente a la lista de remitentes bloqueados.
ms.openlocfilehash: 99adc423864f3096772394ef290df20e158e457d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467084"
---
# <a name="markasjunk"></a>MarkAsJunk

El elemento **MarkAsJunk** especifica la solicitud para mover un elemento a la carpeta de correo no deseado y agregar el remitente a la lista de remitentes bloqueados. 
  
```XML
<MarkAsJunk IsJunk="true | false" MoveItem="true | false">
   <ItemIds/>
</MarkAsJunk>
```

 **MarkAsJunkType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|IsJunk  <br/> |Un valor de texto de **true** para el atributo **IsJunk** indica que el remitente de correo electrónico se agrega a la lista de remitentes bloqueados. Un valor de **false** indica que el remitente de correo electrónico se quita de la lista de remitentes bloqueados si el remitente de correo electrónico ya está en la lista.  <br/> |
|MoveItem  <br/> |Un valor de texto de **true** para el atributo **MoveItem** indica que el elemento se mueve a la carpeta de correo no deseado predeterminada. Un valor de **false** indica que el elemento no se mueve a la carpeta de correo no deseado predeterminada.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

[ItemIds](itemids.md)
  
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |messages. xsd  <br/> |
|Puede estar vacío  <br/> ||
   

