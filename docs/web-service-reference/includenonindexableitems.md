---
title: IncludeNonIndexableItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: af7f202b-2889-447e-bdeb-aaad18ce6b46
description: El elemento IncludeNonIndexableItems contiene un valor booleano para indicar si se deben incluir elementos que no se pueden indizar.
ms.openlocfilehash: 33ff8c59c3ef1d9a91f87870e0a876c5a39ce795
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514602"
---
# <a name="includenonindexableitems"></a>IncludeNonIndexableItems

El **elemento IncludeNonIndexableItems** contiene un **valor booleano** para indicar si se deben incluir elementos que no se pueden indizar. 
  
```XML
<IncludeNonIndexableItems>true | false</IncludeNonIndexableItems>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[SetHoldOnMailboxes](setholdonmailboxes.md)
  
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** para el **elemento IncludeNonIndexableItems** indica que los elementos que no se pueden indizar se incluyen con retenciones de buzones. Un valor de **false** indica que los elementos que no se pueden indizar no se incluyen en las retenciones de buzones. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |false  <br/> |
   

