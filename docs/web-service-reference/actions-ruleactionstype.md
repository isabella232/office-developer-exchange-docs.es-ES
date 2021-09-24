---
title: Actions (RuleActionsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2afba70c-65f7-458c-a4e6-a2cd9bccc0f9
description: El elemento Actions contiene una lista de acciones asociadas con las reglas de la Bandeja de entrada.
ms.openlocfilehash: d91a76889778b363ea931afb98ae9817e3b7c3c1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520181"
---
# <a name="actions-ruleactionstype"></a>Actions (RuleActionsType)

El **elemento Actions** contiene una lista de acciones asociadas con las reglas de la Bandeja de entrada. 
  
```XML
<Actions>
   <AssignCategories/>
   <CopyToFolder/>
   <Delete/>
   <ForwardAsAttachmentToRecipients/>
   <ForwardToRecipients/>
   <MarkImportance/>
   <MarkAsRead/>
   <MoveToFolder/>
   <PermanentDelete/>
   <RedirectToRecipients/>
   <SendSMSAlertToRecipients/>
   <ServerReplyWithMessage/>
   <StopProcessingRules/>
</Actions>
```

 **RuleActionsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[AssignCategories](assigncategories.md)  |  [CopyToFolder](copytofolder.md)  |  [Eliminar](delete.md)  |  [ForwardAsAttachmentToRecipients](forwardasattachmenttorecipients.md)  |  [ForwardToRecipients](forwardtorecipients.md)  |  [MarkImportance](markimportance.md)  |  [MarkAsRead](markasread.md)  |  [MoveToFolder](movetofolder.md)  |  [PermanentDelete](permanentdelete.md)  |  [RedirectToRecipients](redirecttorecipients.md)  |  [SendSMSAlertToRecipients](sendsmsalerttorecipients.md)  |  [ServerReplyWithMessage](serverreplywithmessage.md)  |  [StopProcessingRules](stopprocessingrules.md)
  
### <a name="parent-elements"></a>Elementos principales

[Rule (RuleType)](rule-ruletype.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |false  <br/> |
   

