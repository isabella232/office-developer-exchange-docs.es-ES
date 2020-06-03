---
title: FieldUri (regla)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecdea78-de9c-48be-ae31-03877feafeec
description: El elemento FieldURI especifica el URI al campo de regla que causó el error de validación.
ms.openlocfilehash: 3d88efdf951af580f81b5e2e7a544dcdf70ea830
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461250"
---
# <a name="fielduri-rule"></a>FieldUri (regla)

El elemento **FieldURI** especifica el URI al campo de regla que causó el error de validación. 
  
```XML
<FieldURI/>
```

 **RuleFieldURIType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Error](error.md) <br/> |Representa un error de validación único en un valor de propiedad de regla, un valor de propiedad de predicado o un valor de propiedad de acción específicos.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto de este elemento está restringido a una de las siguientes cadenas:
  
- RuleId
    
- DisplayName
    
- Priority
    
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
    
- Condición: confidencialidad
    
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
    
- Excepción: confidencialidad
    
- Excepción: WithinDateRange
    
- Excepción: WithinSizeRange
    
- Acción: AssignCategories
    
- Acción: CopyToFolder
    
- Acción: eliminar
    
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
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

