---
title: RetentionAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3bdf5955-1212-48a1-b3b5-743086866c91
description: El elemento RetentionAction especifica la acción que se realiza en los elementos con la etiqueta de retención.
ms.openlocfilehash: c16988413e732ddc3cd6ebc355cb73c4d96550c7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465236"
---
# <a name="retentionaction"></a>RetentionAction

El elemento **RetentionAction** especifica la acción que se realiza en los elementos con la etiqueta de retención. 
  
```XML
<RetentionAction> None | MoveToDeletedItems | MoveToFolder | DeleteAndAllowRecovery | PermanentlyDelete | MarkAsPastRetentionLimit | MoveToArchive <RetentionAction>
```

 **RetentionActionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[RetentionPolicyTag](retentionpolicytag.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **RetentionAction** es la acción que se realiza en los elementos. La lista siguiente contiene los valores de texto para el elemento **RetentionAction** . 
  
> **None** : no se realiza ninguna acción en el elemento. 
    
> **MoveToDeletedItems** : el elemento se mueve a la carpeta elementos eliminados de forma predeterminada. 
    
> **MoveToFolder** : el elemento se mueve a una carpeta especificada. 
    
> **DeleteAndAllowRecovery** : el elemento se elimina y se coloca en el contenedor. 
    
> **PermanentlyDelete** : el elemento se elimina de forma permanente del buzón de correo. 
    
> **MarkAsPastRetentionLimit** : el elemento se marca como superado el límite de tiempo de retención. 
    
> **MoveToArchive** : el elemento se mueve al buzón de archivo. 
    
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   

