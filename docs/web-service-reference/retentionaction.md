---
title: RetentionAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3bdf5955-1212-48a1-b3b5-743086866c91
description: El elemento RetentionAction especifica la acción realizada en los elementos con la etiqueta de retención.
ms.openlocfilehash: ecea4326f0e50460635966991cd55badf8946993
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517948"
---
# <a name="retentionaction"></a>RetentionAction

El **elemento RetentionAction** especifica la acción realizada en los elementos con la etiqueta de retención. 
  
```XML
<RetentionAction> None | MoveToDeletedItems | MoveToFolder | DeleteAndAllowRecovery | PermanentlyDelete | MarkAsPastRetentionLimit | MoveToArchive <RetentionAction>
```

 **RetentionActionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[RetentionPolicyTag](retentionpolicytag.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento RetentionAction** es la acción realizada en los elementos. La siguiente lista contiene los valores de texto del **elemento RetentionAction.** 
  
> **Ninguno:** no se realiza ninguna acción en el elemento. 
    
> **MoveToDeletedItems:** el elemento se mueve a la carpeta elementos eliminados predeterminada. 
    
> **MoveToFolder:** el elemento se mueve a una carpeta especificada. 
    
> **DeleteAndAllowRecovery:** el elemento se elimina y se coloca en el contenedor. 
    
> **PermanentlyDelete:** el elemento se elimina permanentemente del buzón. 
    
> **MarkAsPastRetentionLimit:** el elemento se marca como que ha superado el límite de tiempo de retención. 
    
> **MoveToArchive:** el elemento se mueve al buzón de archivo. 
    
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
   

