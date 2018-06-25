---
title: InstanceKey
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bb4dbe9b-aea0-4527-b7d6-e928066caf38
description: El elemento InstanceKey especifica una clave de instancia de un elemento o conversación.
ms.openlocfilehash: a0e4f9390d5dc368388b5a20e38796c6c0157a40
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835943"
---
# <a name="instancekey"></a>InstanceKey

El elemento **InstanceKey** especifica una clave de instancia de un elemento o conversación. 
  
```XML
<InstanceKey></InstanceKey>
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
|[Conversación (ConversationType)](conversation-conversationtype.md) <br/> |Representa una sola conversación.  <br/> |
|[Item](item.md) <br/> |Representa un elemento genérico en el almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **InstanceKey** es la clave de instancia de un elemento o conversación. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

