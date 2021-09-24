---
title: Condiciones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Conditions
api_type:
- schema
ms.assetid: f049a48c-9585-43f7-8549-0b8cb19a5eea
description: El elemento Conditions identifica las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.
ms.openlocfilehash: 55e569c2aa393c79eb4e712711fb2e7b4107023b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515981"
---
# <a name="conditions"></a>Condiciones

El **elemento Conditions** identifica las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla. 
  
```XML
<Conditions>
   <Categories/>
   <ContainsBodyStrings/>
   <ContainsHeaderStrings/>
   <ContainsRecipientStrings/>
   <ContainsSenderStrings/>
   <ContainsSubjectOrBodyStrings/>
   <ContainsSubjectStrings/>
   <FlaggedForAction/>
   <FromAddresses/>
   <FromConnectedAccounts/>
   <HasAttachments/>
   <Importance/>
   <IsApprovalRequest/>
   <IsAutomaticForward/>
   <IsAutomaticReply/>
   <IsEncrypted/>
   <IsMeetingRequest/>
   <IsMeetingResponse/>
   <IsNDR/>
   <IsPermissionControlled/>
   <IsReadReceipt/>
   <IsSigned/>
   <IsVoicemail/>
   <ItemClasses/>
   <MessageClassifications/>
   <NotSentToMe/>
   <SentCcMe/>
   <SentOnlyToMe/>
   <SentToAddresses/>
   <SentToMe/>
   <SentToOrCcMe/>
   <Sensitivity/>
   <WithinDateRange/>
   <WithinSizeRange/>
</Conditions>
```

 **RulePredicatesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Categories](categories-ex15websvcsotherref.md) <br/> |Contiene las categorías que se deben aplicar a un mensaje entrante para que se aplique la condición o excepción.  <br/> |
|[ContainsBodyStrings](containsbodystrings.md) <br/> |Indica las cadenas que deben aparecer en el cuerpo de los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[ContainsHeaderStrings](containsheaderstrings.md) <br/> |Indica las cadenas que deben aparecer en los encabezados de los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[ContainsRecipientStrings](containsrecipientstrings.md) <br/> |Indica las cadenas que deben aparecer en las propiedades **ToRecipients** o **CcRecipients** de los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[ContainsSenderStrings](containssenderstrings.md) <br/> |Indica las cadenas que deben aparecer en la **propiedad From** de los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[ContainsSubjectOrBodyStrings](containssubjectorbodystrings.md) <br/> |Indica las cadenas que deben aparecer en el cuerpo o el asunto de los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[ContainsSubjectStrings](containssubjectstrings.md) <br/> |Indica las cadenas que deben aparecer en el asunto de los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[FlaggedForAction](flaggedforaction.md) <br/> |Especifica la marca del valor de acción que debe aparecer en los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[FromAddresses](fromaddresses.md) <br/> |Indica las direcciones de correo electrónico desde las que se deben enviar los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[FromConnectedAccounts](fromconnectedaccounts.md) <br/> |Representa los nombres de cuenta de correo electrónico desde los que los mensajes entrantes deben haber sido agregados para que se aplique la condición o excepción.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Indica si los mensajes entrantes deben tener datos adjuntos para que se aplique la condición o excepción.  <br/> |
|[Importance](importance.md) <br/> |Especifica la importancia que se marca en los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[IsApprovalRequest](isapprovalrequest.md) <br/> |Indica si los mensajes entrantes deben ser solicitudes de aprobación para que se aplique la condición o excepción.  <br/> |
|[IsAutomaticForward](isautomaticforward.md) <br/> |Indica si los mensajes entrantes deben ser reenvíos automáticos para que se aplique la condición o excepción.  <br/> |
|[IsAutomaticReply](isautomaticreply.md) <br/> |Indica si los mensajes entrantes deben ser respuestas automáticas para que se aplique la condición o excepción.  <br/> |
|[IsEncrypted](isencrypted.md) <br/> |Indica si los mensajes entrantes deben estar cifrados con S/MIME para que se aplique la condición o excepción.  <br/> |
|[IsMeetingRequest](ismeetingrequest.md) <br/> |Indica si los mensajes entrantes deben ser solicitudes de reunión para que se aplique la condición o excepción.  <br/> |
|[IsMeetingResponse](ismeetingresponse.md) <br/> |Indica si los mensajes entrantes deben ser respuestas de reunión para que se aplique la condición o excepción.  <br/> |
|[IsNDR](isndr.md) <br/> |Indica si los mensajes entrantes deben ser informes de no entrega (NDR) para que se aplique la condición o excepción.  <br/> |
|[IsPermissionControlled](ispermissioncontrolled.md) <br/> |Indica si los mensajes entrantes deben estar controlados por permisos (protegidos por RMS) para que se aplique la condición o excepción.  <br/> |
|[IsReadReceipt](isreadreceipt.md) <br/> |Indica si los mensajes entrantes deben ser recibos de lectura para que se aplique la condición o excepción.  <br/> |
|[IsSigned](issigned.md) <br/> |Indica si los mensajes entrantes deben estar firmados por S/MIME para que se aplique la condición o excepción.  <br/> |
|[IsVoicemail](isvoicemail.md) <br/> |Indica si los mensajes entrantes deben ser mensajes de correo de voz para que se aplique la condición o excepción.  <br/> |
|[ItemClasses](itemclasses.md) <br/> |Representa las clases de elemento que se deben marcar en los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[MessageClassifications](messageclassifications.md) <br/> |Representa las clasificaciones de mensajes que se deben marcar en los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[NotSentToMe](notsenttome.md) <br/> |Indica si el propietario del buzón no debe estar en la propiedad **ToRecipients** de los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[SentCcMe](sentccme.md) <br/> |Indica si el propietario del buzón debe estar en la **propiedad CcRecipients** de los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[SentOnlyToMe](sentonlytome.md) <br/> |Indica si el propietario del buzón debe ser el único de la propiedad **ToRecipients** de los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[SentToAddresses](senttoaddresses.md) <br/> |Indica las direcciones de correo electrónico a las que deben enviarse los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[SentToMe](senttome.md) <br/> |Indica si el propietario del buzón debe estar en la propiedad **ToRecipients** de los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[SentToOrCcMe](senttoorccme.md) <br/> |Indica si el propietario del buzón debe estar en una propiedad **ToRecipients** o **CcRecipients** de los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[Sensitivity](sensitivity.md) <br/> |Indica la confidencialidad que debe marcarse en los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[WithinDateRange](withindaterange.md) <br/> |Especifica el intervalo de fechas dentro del cual los mensajes entrantes deben haber sido recibidos para que se aplique la condición o excepción.  <br/> |
|[WithinSizeRange](withinsizerange.md) <br/> |Especifica los tamaños mínimos y máximos que deben tener los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Rule (RuleType)](rule-ruletype.md) <br/> |Contiene una sola regla y representa una regla en el buzón de un usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



[Excepciones](exceptions.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

