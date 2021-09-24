---
title: SetHoldOnMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: fd5b9f0e-23e8-428c-8168-2d6b4ecd6beb
description: El elemento SetHoldOnMailboxes contiene una solicitud SetHoldOnMailboxes.
ms.openlocfilehash: 82ebbbdce04a5b70eae790a899ca089e38aa76d9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516379"
---
# <a name="setholdonmailboxes"></a>SetHoldOnMailboxes

El **elemento SetHoldOnMailboxes** contiene una **solicitud SetHoldOnMailboxes.** 
  
```XML
<SetHoldOnMailboxes>
   <ActionType/>
   <HoldId/>
   <Query/>
   <Mailboxes/>
   <Language/>
   <IncludeNonIndexableItems/>
   <Deduplication/>
   <InPlaceHoldIdentity/>
</SetHoldOnMailboxes>
```

 **SetHoldOnMailboxesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[ActionType (HoldActionType)](actiontype-holdactiontype.md)  |  [HoldId](holdid.md)  |  [Consulta](query.md)  |  [Buzones (ArrayOfStringsType)](mailboxes-arrayofstringstype.md)  |  [Idioma](language.md)  |  [IncludeNonIndexableItems](includenonindexableitems.md)  |  [Desduplicación](deduplication.md)  |  [InPlaceHoldIdentity](inplaceholdidentity.md)
  
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
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
   

