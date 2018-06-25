---
title: Sugerencias de correo electrónico
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
description: El elemento de sugerencias de correo electrónico representa los valores de distintos tipos de sugerencias de correo.
ms.openlocfilehash: 3a2e95225b09fd2d81db32f821ea3069ab7e7852
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836311"
---
# <a name="mailtips"></a>Sugerencias de correo electrónico

El elemento de **sugerencias de correo electrónico** representa los valores de distintos tipos de sugerencias de correo. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[RecipientAddress](recipientaddress.md) <br/> |Representa el buzón de correo del destinatario.  <br/> |
|[PendingMailTips](pendingmailtips.md) <br/> |Indica que las sugerencias de correo en este elemento no se podrían evaluar antes de tiempo de espera de procesamiento del servidor.  <br/> |
|[Fuera de la oficina](outofoffice.md) <br/> |Representa el mensaje de respuesta y un tiempo de duración para enviar el mensaje de respuesta.  <br/> |
|[MailboxFull](mailboxfull.md) <br/> |Indica si el buzón del destinatario está lleno.  <br/> |
|[CustomMailTip](custommailtip.md) <br/> |Representa un mensaje de sugerencia de correo personalizado.  <br/> |
|[TotalMemberCount](totalmembercount.md) <br/> |Representa el recuento de todos los miembros de un grupo.  <br/> |
|[ExternalMemberCount](externalmembercount.md) <br/> |Representa el recuento de miembros externos en un grupo.  <br/> |
|[MaxMessageSize](maxmessagesize.md) <br/> |Representa el tamaño máximo de mensaje que puede aceptar el destinatario.  <br/> |
|[DeliveryRestricted](deliveryrestricted.md) <br/> |Indica si las restricciones de entrega impedirá que el mensaje del remitente llegar al destinatario.  <br/> |
|[IsModerated](ismoderated.md) <br/> |Indica si se va a modera el buzón del destinatario.  <br/> |
|[InvalidRecipient (sugerencias de correo electrónico)](invalidrecipient-mailtips.md) <br/> |Indica si el destinatario no es válido.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[MailTipsResponseMessageType](mailtipsresponsemessagetype.md) <br/> |Representa la configuración de sugerencias de correo.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
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

