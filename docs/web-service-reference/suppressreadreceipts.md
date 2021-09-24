---
title: SuppressReadReceipts
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f0805560-7a2f-455b-94d2-ec4f1e3652c3
description: El elemento SuppressReadReceipts indica si se deben suprimir las confirmaciones de lectura.
ms.openlocfilehash: 1f63f46f4e74a3123661caba39b737910bc2ef30
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517654"
---
# <a name="suppressreadreceipts"></a>SuppressReadReceipts

El **elemento SuppressReadReceipts** indica si se deben suprimir las confirmaciones de lectura. 
  
```XML
<SuppressReadReceipts>true | false</SuppressReadReceipts>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[ConversationAction](conversationaction.md)  |  [MarkAllItemsAsRead](markallitemsasread.md)
  
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** para el **elemento SuppressReadReciepts** indica que se suprimen las confirmaciones de lectura. Un valor de **false** indica que se enviarán recibos de lectura al remitente. 
  
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
   

