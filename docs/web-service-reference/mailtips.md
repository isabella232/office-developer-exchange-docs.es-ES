---
title: MailTips
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MailTips
api_type:
- schema
ms.assetid: c1cba493-bccc-4b8e-be8e-bfa8a8b10882
description: El elemento MailTips representa valores para varios tipos de sugerencias de correo.
ms.openlocfilehash: bf7ed542d51f2a8cb3172275be12cb72104bc5b2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511141"
---
# <a name="mailtips"></a>MailTips

El **elemento MailTips** representa valores para varios tipos de sugerencias de correo. 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RecipientAddress](recipientaddress.md) <br/> |Representa el buzón del destinatario.  <br/> |
|[PendingMailTips](pendingmailtips.md) <br/> |Indica que las sugerencias de correo de este elemento no se pudieron evaluar antes de que expirara el tiempo de espera de procesamiento del servidor.  <br/> |
|[OutOfOffice](outofoffice.md) <br/> |Representa el mensaje de respuesta y el tiempo de duración para enviar el mensaje de respuesta.  <br/> |
|[MailboxFull](mailboxfull.md) <br/> |Indica si el buzón del destinatario está lleno.  <br/> |
|[CustomMailTip](custommailtip.md) <br/> |Representa un mensaje de sugerencia de correo personalizado.  <br/> |
|[TotalMemberCount](totalmembercount.md) <br/> |Representa el recuento de todos los miembros de un grupo.  <br/> |
|[ExternalMemberCount](externalmembercount.md) <br/> |Representa el recuento de miembros externos de un grupo.  <br/> |
|[MaxMessageSize](maxmessagesize.md) <br/> |Representa el tamaño máximo del mensaje que el destinatario puede aceptar.  <br/> |
|[DeliveryRestricted](deliveryrestricted.md) <br/> |Indica si las restricciones de entrega impedirán que el mensaje del remitente llegue al destinatario.  <br/> |
|[IsModerated](ismoderated.md) <br/> |Indica si se está moderando el buzón del destinatario.  <br/> |
|[InvalidRecipient (MailTips)](invalidrecipient-mailtips.md) <br/> |Indica si el destinatario no es válido.  <br/> |
   
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
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

