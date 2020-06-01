---
title: Excepciones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Exceptions
api_type:
- schema
ms.assetid: 7cd63ac2-3441-4ed4-915b-6f90af4b28fc
description: El elemento Exceptions identifica las excepciones que representan todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.
ms.openlocfilehash: 1afc2980391ee588f9b9b813b87c2c699de3a6df
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463359"
---
# <a name="exceptions"></a>Excepciones

El elemento **Exceptions** identifica las excepciones que representan todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada. 
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Categories](categories-ex15websvcsotherref.md) <br/> |Contiene las categorías que deben aplicarse a un mensaje entrante para que se aplique la condición o excepción.  <br/> |
|[ContainsBodyStrings](containsbodystrings.md) <br/> |Indica las cadenas que deben aparecer en el cuerpo de los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[ContainsHeaderStrings](containsheaderstrings.md) <br/> |Indicaqtes las cadenas que deben aparecer en los encabezados de los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[ContainsRecipientStrings](containsrecipientstrings.md) <br/> |Indica las cadenas que deben aparecer en las propiedades **ToRecipients** o **CcRecipients** de los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[ContainsSenderStrings](containssenderstrings.md) <br/> |Indica las cadenas que deben aparecer en la propiedad **from** de los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[ContainsSubjectOrBodyStrings](containssubjectorbodystrings.md) <br/> |Indica las cadenas que deben aparecer en el cuerpo o el asunto de los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[ContainsSubjectStrings](containssubjectstrings.md) <br/> |Indica las cadenas que deben aparecer en el asunto de los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[FlaggedForAction](flaggedforaction.md) <br/> |Especifica la marca para el valor de la acción que debe aparecer en los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[FromAddresses](fromaddresses.md) <br/> |Indica las direcciones de correo electrónico desde las que se deben enviar los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[FromConnectedAccounts](fromconnectedaccounts.md) <br/> |Representa los nombres de cuenta de correo electrónico desde los que se deben agregar los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Indica si los mensajes entrantes deben tener datos adjuntos para que se aplique la condición o excepción.  <br/> |
|[Importance](importance.md) <br/> |Especifica la importancia que se marca en los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[IsApprovalRequest](isapprovalrequest.md) <br/> |Indica si los mensajes entrantes deben ser solicitudes de aprobación para que se aplique la condición o excepción.  <br/> |
|[IsAutomaticForward](isautomaticforward.md) <br/> |Indica si los mensajes entrantes deben ser reenviados automáticamente para que se aplique la condición o excepción.  <br/> |
|[IsAutomaticReply](isautomaticreply.md) <br/> |Indica si los mensajes entrantes deben ser respuestas automáticas para que se aplique la condición o excepción.  <br/> |
|[IsEncrypted](isencrypted.md) <br/> |Indica si los mensajes entrantes deben ser cifrados con S/MIME para que se aplique la condición o excepción.  <br/> |
|[IsMeetingRequest](ismeetingrequest.md) <br/> |Indica si los mensajes entrantes deben ser convocatorias de reunión para que se aplique la condición o excepción.  <br/> |
|[IsMeetingResponse](ismeetingresponse.md) <br/> |Indica si los mensajes entrantes deben ser respuestas a la reunión para que se aplique la condición o excepción.  <br/> |
|[IsNDR](isndr.md) <br/> |Indica si los mensajes entrantes deben ser informes de no entrega (NDR) para que se aplique la condición o excepción.  <br/> |
|[IsPermissionControlled](ispermissioncontrolled.md) <br/> |Indica si los mensajes entrantes deben ser controlados por permisos (protegido por RMS) para que se aplique la condición o excepción  <br/> |
|[IsReadReceipt](isreadreceipt.md) <br/> |Indica si los mensajes entrantes deben ser confirmaciones de lectura para que se aplique la condición o excepción.  <br/> |
|[IsSigned](issigned.md) <br/> |Indica si los mensajes entrantes deben ser firmados con S/MIME para que se aplique la condición o excepción.  <br/> |
|[IsVoicemail](isvoicemail.md) <br/> |Indica si los mensajes entrantes deben ser mensajes de correo de voz en orden para que se aplique la condición o excepción.  <br/> |
|[ItemClasses](itemclasses.md) <br/> |Representa las clases de elementos que se deben estampar en los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[MessageClassifications](messageclassifications.md) <br/> |Representa las clasificaciones de mensajes que se deben marcar en los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[NotSentToMe](notsenttome.md) <br/> |Indica si el propietario del buzón no debe estar en la propiedad **ToRecipients** de los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[SentCcMe](sentccme.md) <br/> |Indica si el propietario del buzón tiene que estar en la propiedad **CcRecipients** de los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[SentOnlyToMe](sentonlytome.md) <br/> |Indica si el propietario del buzón tiene que ser el único de la propiedad **ToRecipients** de los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[SentToAddresses](senttoaddresses.md) <br/> |Indica las direcciones de correo electrónico a las que se deben enviar los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[SentToMe](senttome.md) <br/> |Indica si el propietario del buzón tiene que estar en la propiedad **ToRecipients** de los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[SentToOrCcMe](senttoorccme.md) <br/> |Indica si el propietario del buzón tiene que estar en la propiedad **ToRecipients** o **CcRecipients** de los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[Sensitivity](sensitivity.md) <br/> |Indica la sensibilidad que se debe estampar en los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[WithinDateRange](withindaterange.md) <br/> |Especifica el intervalo de fechas en el que se deben recibir los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[WithinSizeRange](withinsizerange.md) <br/> |Especifica los tamaños máximos y mínimos que los mensajes entrantes deben tener en orden para que se aplique la condición o excepción.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Regla (RuleType)](rule-ruletype.md) <br/> |Contiene una sola regla y representa una regla en el buzón de un usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Los predicados de regla se usan como excepciones o condiciones de regla.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[Condiciones](conditions.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

