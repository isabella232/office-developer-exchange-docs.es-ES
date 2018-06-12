---
title: Condiciones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Conditions
api_type:
- schema
ms.assetid: f049a48c-9585-43f7-8549-0b8cb19a5eea
description: El elemento de condiciones identifica las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla para una regla.
ms.openlocfilehash: f66777e82892122c4c7dac45bdef3c42f5c4a577
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763766"
---
# <a name="conditions"></a>Condiciones

El elemento de **condiciones** identifica las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla para una regla. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Categories](categories-ex15websvcsotherref.md) <br/> |Contiene las categorías que se deben aplicar a un mensaje entrante en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[ContainsBodyStrings](containsbodystrings.md) <br/> |Indica las cadenas que deben aparecer en el cuerpo de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[ContainsHeaderStrings](containsheaderstrings.md) <br/> |Indica las cadenas que deben aparecer en los encabezados de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[ContainsRecipientStrings](containsrecipientstrings.md) <br/> |Indica las cadenas que deben aparecer en la **ToRecipients** o **CcRecipients** propiedades de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[ContainsSenderStrings](containssenderstrings.md) <br/> |Indica las cadenas que deben aparecer en la propiedad **From** de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[ContainsSubjectOrBodyStrings](containssubjectorbodystrings.md) <br/> |Indica las cadenas que deben aparecer en el cuerpo o el asunto de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[ContainsSubjectStrings](containssubjectstrings.md) <br/> |Indica las cadenas que deben aparecer en el asunto de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[FlaggedForAction](flaggedforaction.md) <br/> |Especifica la marca para el valor de la acción que debe aparecer en los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[FromAddresses](fromaddresses.md) <br/> |Indica las direcciones de correo electrónico desde la que se deben enviar los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[FromConnectedAccounts](fromconnectedaccounts.md) <br/> |Representa los nombres de cuenta de correo electrónico desde la que los mensajes entrantes tienen que agregadas en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Indica si los mensajes entrantes tienen que tener los datos adjuntos en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[Importancia](importance.md) <br/> |Especifica la importancia que se mostrará en los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[IsApprovalRequest](isapprovalrequest.md) <br/> |Indica si los mensajes entrantes deben ser solicitudes de aprobación en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[IsAutomaticForward](isautomaticforward.md) <br/> |Indica si los mensajes entrantes deben ser reenvíos automáticos en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[IsAutomaticReply](isautomaticreply.md) <br/> |Indica si los mensajes entrantes deben ser las respuestas automáticas en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[IsEncrypted](isencrypted.md) <br/> |Indica si los mensajes entrantes deben ser S/MIME cifrado en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[IsMeetingRequest](ismeetingrequest.md) <br/> |Indica si los mensajes entrantes deben ser las convocatorias de reunión en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[IsMeetingResponse](ismeetingresponse.md) <br/> |Indica si los mensajes entrantes deben ser respuestas de reunión en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[IsNDR](isndr.md) <br/> |Indica si los mensajes entrantes deben ser informes de no entrega (NDR) en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[IsPermissionControlled](ispermissioncontrolled.md) <br/> |Indica si los mensajes entrantes deben ser permiso controlado (protegido con RMS) en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[IsReadReceipt](isreadreceipt.md) <br/> |Indica si los mensajes entrantes deben ser confirmaciones de lectura en el orden de la condición o excepción que se debe aplicar.  <br/> |
|[IsSigned](issigned.md) <br/> |Indica si los mensajes entrantes deben ser QUE S/MIME firmados para la condición o la excepción que se debe aplicar.  <br/> |
|[IsVoicemail](isvoicemail.md) <br/> |Indica si los mensajes entrantes deben ser los mensajes de correo de voz en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[ItemClasses](itemclasses.md) <br/> |Representa las clases de elemento deben estar marcados en los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[MessageClassifications](messageclassifications.md) <br/> |Representa las clasificaciones de mensajes deben estar marcados en los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[NotSentToMe](notsenttome.md) <br/> |Indica si el propietario del buzón no debe estar en la propiedad **ToRecipients** de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[SentCcMe](sentccme.md) <br/> |Indica si el propietario del buzón tiene que estar en la propiedad **CcRecipients** de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[SentOnlyToMe](sentonlytome.md) <br/> |Indica si el propietario del buzón tiene que ser el único existente en la propiedad **ToRecipients** de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[SentToAddresses](senttoaddresses.md) <br/> |Indica las direcciones de correo electrónico que se han enviado en orden para la condición o la excepción que se debe aplicar a los mensajes entrantes.  <br/> |
|[SentToMe](senttome.md) <br/> |Indica si el propietario del buzón tiene que estar en la propiedad **ToRecipients** de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[SentToOrCcMe](senttoorccme.md) <br/> |Indica si el propietario del buzón tiene que estar en un **ToRecipients** o **CcRecipients** propiedad de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[Sensibilidad](sensitivity.md) <br/> |Indica la confidencialidad debe estar marcados en los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[WithinDateRange](withindaterange.md) <br/> |Especifica el intervalo de fechas dentro del cual los mensajes entrantes tienen que se han recibido en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[WithinSizeRange](withinsizerange.md) <br/> |Especifica los tamaños máximos y mínimos que deben ser los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Regla (RuleType)](rule-ruletype.md) <br/> |Contiene una sola regla y representa una regla en el buzón del usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Observaciones

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



[Excepciones](exceptions.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

