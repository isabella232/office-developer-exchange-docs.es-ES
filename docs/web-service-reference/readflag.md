---
title: ReadFlag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9d91aa89-9f9f-4877-846d-aaf48bbeec7c
description: El elemento ReadFlag indica el estado de lectura que se debe establecer en los elementos de una carpeta.
ms.openlocfilehash: ac079f6adbdb2686221dd52d748b05ac4141d6c6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523653"
---
# <a name="readflag"></a>ReadFlag

El **elemento ReadFlag** indica el estado de lectura que se debe establecer en los elementos de una carpeta. 
  
```XML
<ReadFlag>true | false</ReadFlag>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[MarkAllItemsAsRead](markallitemsasread.md)
  
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** para el **elemento ReadFlag** indica que los elementos de la carpeta se marcarán como leídos. Un valor de **false** indica que los elementos de la carpeta se marcarán como no leídos. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

