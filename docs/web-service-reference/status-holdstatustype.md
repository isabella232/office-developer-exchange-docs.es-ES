---
title: Estado (HoldStatusType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fee3f1f9-e868-49fa-a554-7ff096964718
description: El elemento status especifica el estado de retención de un buzón.
ms.openlocfilehash: cecfdfaf67b00b6f8cf02188e7a4df7062a732e4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459990"
---
# <a name="status-holdstatustype"></a>Estado (HoldStatusType)

El elemento **status** especifica el estado de retención de un buzón. 
  
```XML
<Status> NotOnHold | Pending | OnHold | PartialHold | Failed </Status>
```

 **HoldStatusType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[MailboxHoldStatus](mailboxholdstatus.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento de **Estado** es el estado de conservación de un buzón. El elemento **status** puede tener los valores de la siguiente lista. 
  
> NotOnHold: el buzón de correo no está en suspensión.
    
> Pending: el buzón de correo está pendiente de ser colocado o lanzado en espera. 
    
> Cohold: la suspensión se aplicó correctamente al buzón de correo. 
    
> PartialHold: la retención se aplicó correctamente a algunos buzones, pero no a todos los buzones.
    
> Failed: no se pudo aplicar la retención al buzón.
    
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
   

