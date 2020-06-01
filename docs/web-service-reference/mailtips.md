---
title: MailTips
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTips
api_type:
- schema
ms.assetid: c1cba493-bccc-4b8e-be8e-bfa8a8b10882
description: El elemento de sugerencias de correo electrónico representa los valores para varios tipos de sugerencias de correo.
ms.openlocfilehash: 9bacdea7b4f3108f700ed102025445e01a73e69d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44447599"
---
# <a name="mailtips"></a>MailTips

El elemento de **sugerencias** de correo electrónico representa los valores para varios tipos de sugerencias de correo. 
  
```XML
<MailTips>
   <RecipientAddress/>
   <PendingMailTips/>
   <OutOfOffice/>
   <MailboxFull/>
   <CustomMailTip/>
   <TotalMemberCount/>
   <ExternalMemberCount/>
   <MaxMessageSize/>
   <DeliveryRestricted/>
   <IsModerated/>
   <InvalidRecipient/>
</MailTips>
```

 **Sugerencias de correo electrónico**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RecipientAddress](recipientaddress.md) <br/> |Representa el buzón del destinatario.  <br/> |
|[PendingMailTips](pendingmailtips.md) <br/> |Indica que las sugerencias de correo de este elemento no se pudieron evaluar antes de que se agote el tiempo de espera de procesamiento del servidor.  <br/> |
|[Oficina](outofoffice.md) <br/> |Representa el mensaje de respuesta y una hora de duración para el envío del mensaje de respuesta.  <br/> |
|[MailboxFull](mailboxfull.md) <br/> |Indica si el buzón del destinatario está lleno.  <br/> |
|[CustomMailTip](custommailtip.md) <br/> |Representa un mensaje personalizado de sugerencia de correo.  <br/> |
|[TotalMemberCount](totalmembercount.md) <br/> |Representa el número de todos los miembros de un grupo.  <br/> |
|[ExternalMemberCount](externalmembercount.md) <br/> |Representa el número de miembros externos de un grupo.  <br/> |
|[MaxMessageSize](maxmessagesize.md) <br/> |Representa el tamaño máximo de mensaje que puede aceptar el destinatario.  <br/> |
|[DeliveryRestricted](deliveryrestricted.md) <br/> |Indica si las restricciones de entrega impedirán que el mensaje del remitente llegue al destinatario.  <br/> |
|[IsModerated](ismoderated.md) <br/> |Indica si el buzón del destinatario se modera.  <br/> |
|[InvalidRecipient (sugerencias de correo)](invalidrecipient-mailtips.md) <br/> |Indica si el destinatario no es válido.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MailTipsResponseMessageType](mailtipsresponsemessagetype.md) <br/> |Representa la configuración de sugerencias de correo.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
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

