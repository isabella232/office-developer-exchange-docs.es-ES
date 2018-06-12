---
title: Estado (HoldStatusType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fee3f1f9-e868-49fa-a554-7ff096964718
description: El elemento Status especifica el estado de suspensión para un buzón de correo.
ms.openlocfilehash: c40dc865d2b305ac86fa40d536e2d516a14260ab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837579"
---
# <a name="status-holdstatustype"></a>Estado (HoldStatusType)

El elemento **Status** especifica el estado de suspensión para un buzón de correo. 
  
```XML
<Status> NotOnHold | Pending | OnHold | PartialHold | Failed </Status>
```

 **HoldStatusType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[MailboxHoldStatus](mailboxholdstatus.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento de **estado** es el estado de espera de un buzón de correo. El elemento de **estado** puede tener los valores de la lista siguiente. 
  
> NotOnHold - el buzón no está en espera.
    
> Pendiente: el buzón de correo está pendiente se colocan o publicado en espera. 
    
> OnHold - la suspensión se ha aplicado correctamente al buzón. 
    
> PartialHold - la suspensión se ha aplicado correctamente para algunos buzones de correo, pero no para todos los buzones.
    
> No se pudo - la suspensión no se pudieron aplicar al buzón.
    
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
   

