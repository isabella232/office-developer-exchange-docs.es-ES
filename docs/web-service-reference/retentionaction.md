---
title: RetentionAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3bdf5955-1212-48a1-b3b5-743086866c91
description: El elemento RetentionAction especifica la acción realizada en los elementos con la etiqueta de retención.
ms.openlocfilehash: 54a1038f2e56aad66f89522423ccfbd69dc44a80
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837215"
---
# <a name="retentionaction"></a>RetentionAction

El elemento **RetentionAction** especifica la acción realizada en los elementos con la etiqueta de retención. 
  
```XML
<RetentionAction> None | MoveToDeletedItems | MoveToFolder | DeleteAndAllowRecovery | PermanentlyDelete | MarkAsPastRetentionLimit | MoveToArchive <RetentionAction>
```

 **RetentionActionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[RetentionPolicyTag](retentionpolicytag.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **RetentionAction** es la acción realizada en los elementos. En la lista siguiente contiene los valores de texto para el elemento **RetentionAction** . 
  
> **Ninguno** : ninguna acción se realiza en el elemento. 
    
> **MoveToDeletedItems** - el elemento se mueve a la carpeta Elementos eliminados de forma predeterminada. 
    
> **MoveToFolder** - el elemento se mueve a una carpeta especificada. 
    
> **DeleteAndAllowRecovery** - el elemento se elimina y se coloca el volcado de archivos. 
    
> **PermanentlyDelete** - el elemento se elimina de manera permanente del buzón de correo. 
    
> **MarkAsPastRetentionLimit** - el elemento está marcado como que se ha excedido el límite de tiempo de retención. 
    
> **MoveToArchive** - el elemento se mueve al buzón de archivo. 
    
## <a name="remarks"></a>Notas

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

