---
title: Status (HoldStatusType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: fee3f1f9-e868-49fa-a554-7ff096964718
description: El elemento Status especifica el estado de retención de un buzón.
ms.openlocfilehash: a055dde61ae52c266f2349036c881d2b00557171
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521238"
---
# <a name="status-holdstatustype"></a>Status (HoldStatusType)

El **elemento Status** especifica el estado de retención de un buzón. 
  
```XML
<Status> NotOnHold | Pending | OnHold | PartialHold | Failed </Status>
```

 **HoldStatusType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[MailboxHoldStatus](mailboxholdstatus.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento Status** es el estado de retención de un buzón. El **elemento Status** puede tener los valores de la siguiente lista. 
  
> NotOnHold: el buzón no está en espera.
    
> Pendiente: el buzón está pendiente de colocarse o liberarse en espera. 
    
> OnHold: la retención se aplicó correctamente al buzón. 
    
> PartialHold: la retención se aplicó correctamente a algunos buzones, pero no a todos los buzones.
    
> Error: la retención no se pudo aplicar al buzón.
    
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
   

