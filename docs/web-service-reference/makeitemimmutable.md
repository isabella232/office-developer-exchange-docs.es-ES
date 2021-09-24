---
title: MakeItemImmutable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: de1d2a60-aeeb-4625-8b11-23c42e1e7bae
description: El elemento MakeItemImmutable especifica un valor booleano que indica si un elemento debe hacerse de solo lectura.
ms.openlocfilehash: 0e1d28f19492bb6dc013957aa5957b59e791b24b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524829"
---
# <a name="makeitemimmutable"></a>MakeItemImmutable

El **elemento MakeItemImmutable** especifica un valor booleano que indica si un elemento debe hacerse de solo lectura. 
  
```XML
<MakeItemImmutable>true | false</MakeItemImmutable>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[UpdateItemInRecoverableItems](updateiteminrecoverableitems.md)
  
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** para el **elemento MakeItemImmutable** indica que el elemento debe hacerse de solo lectura. Un valor de **false** indica que el elemento permite el acceso de lectura y escritura. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |messages.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

