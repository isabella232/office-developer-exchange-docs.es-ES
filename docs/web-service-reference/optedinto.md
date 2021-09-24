---
title: OptedInto
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 083a23d9-acc3-4c15-9d30-c20bf7e6808d
description: El elemento OptedInto especifica un valor booleano que indica si el usuario optó por la directiva de retención.
ms.openlocfilehash: 6dbfe898ad6eb3141b265d51c8ec0cb830916a9d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518067"
---
# <a name="optedinto"></a>OptedInto

El **elemento OptedInto** especifica un valor booleano que indica si el usuario optó por la directiva de retención. 
  
```XML
<OptedInto>true | false</OptedInto>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[RetentionPolicyTag](retentionpolicytag.md)
  
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** para el **elemento OptedInto** indica que el usuario optó por la directiva de retención. Un valor de **false** indica que el usuario no ha optado por la directiva de retención. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

