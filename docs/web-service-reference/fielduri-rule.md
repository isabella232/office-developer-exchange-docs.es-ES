---
title: FieldUri (regla)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecdea78-de9c-48be-ae31-03877feafeec
description: El elemento FieldURI especifica el URI para el campo de regla que causó el error de validación.
ms.openlocfilehash: 88ba54994625d3a950b58e900f28c986c31eddac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764585"
---
# <a name="fielduri-rule"></a>FieldUri (regla)

El elemento **FieldURI** especifica el URI para el campo de regla que causó el error de validación. 
  
```XML
<FieldURI/>
```

 **RuleFieldURIType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Error](error.md) <br/> |Representa un error de validación único en un valor de la propiedad de regla concreto, valor de la propiedad predicado o valor de la propiedad acción.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto para este elemento está restringido a una de las siguientes cadenas:
  
- Identificador de regla
    
- DisplayName
    
- Prioridad
    
- IsNotSupported
    
- Acciones
    
- Condición: categorías
    
- Condición: ContainsBodyStrings
    
- Condición: ContainsHeaderStrings
    
- Condición: ContainsRecipientStrings
    
- Condición: ContainsSenderStrings
    
- Condición: ContainsSubjectOrBodyStrings
    
- Condición: ContainsSubjectStrings
    
- Condición: FlaggedForAction
    
- Condición: FromAddresses
    
- Condición: FromConnectedAccounts
    
- Condición: HasAttachments
    
- Condición: importancia
    
- Condición: IsApprovalRequest
    
- Condición: IsAutomaticForward
    
- Condición: IsAutomaticReply
    
- Condición: IsEncrypted
    
- Condición: IsMeetingRequest
    
- Condición: IsMeetingResponse
    
- Condición: IsNDR
    
- Condición: IsPermissionControlled
    
- Condición: IsReadReceipt
    
- Condición: IsSigned
    
- Condición: IsVoicemail
    
- Condición: ItemClasses
    
- Condición: MessageClassifications
    
- Condición: NotSentToMe
    
- Condición: SentCcMe
    
- Condición: SentOnlyToMe
    
- Condición: SentToAddresses
    
- Condición: SentToMe
    
- Condición: SentToOrCcMe
    
- Condición: sensibilidad
    
- Condición: WithinDateRange
    
- Condición: WithinSizeRange
    
- Excepción: categorías
    
- Excepción: ContainsBodyStrings
    
- Excepción: ContainsHeaderStrings
    
- Excepción: ContainsRecipientStrings
    
- Excepción: ContainsSenderStrings
    
- Excepción: ContainsSubjectOrBodyStrings
    
- Excepción: ContainsSubjectStrings
    
- Excepción: FlaggedForAction
    
- Excepción: FromAddresses
    
- Excepción: FromConnectedAccounts
    
- Excepción: HasAttachments
    
- Excepción: importancia
    
- Excepción: IsApprovalRequest
    
- Excepción: IsAutomaticForward
    
- Excepción: IsAutomaticReply
    
- Excepción: IsEncrypted
    
- Excepción: IsMeetingRequest
    
- Excepción: IsMeetingResponse
    
- Excepción: IsNDR
    
- Excepción: IsPermissionControlled
    
- Excepción: IsReadReceipt
    
- Excepción: IsSigned
    
- Excepción: IsVoicemail
    
- Excepción: ItemClasses
    
- Excepción: MessageClassifications
    
- Excepción: NotSentToMe
    
- Excepción: SentCcMe
    
- Excepción: SentOnlyToMe
    
- Excepción: SentToAddresses
    
- Excepción: SentToMe
    
- Excepción: SentToOrCcMe
    
- Excepción: sensibilidad
    
- Excepción: WithinDateRange
    
- Excepción: WithinSizeRange
    
- Acción: AssignCategories
    
- Acción: CopyToFolder
    
- Eliminación de la acción:
    
- Acción: ForwardAsAttachmentToRecipients
    
- Acción: ForwardToRecipients
    
- Acción: MarkImportance
    
- Acción: MarkAsRead
    
- Acción: MoveToFolder
    
- Acción: PermanentDelete
    
- Acción: RedirectToRecipients
    
- Acción: SendSMSAlertToRecipients
    
- Acción: ServerReplyWithMessage
    
- Acción: StopProcessingRules
    
- IsEnabled
    
- IsInError
    
- Condiciones
    
- Excepciones
    
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

