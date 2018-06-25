---
title: MailTipsRequested
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTipsRequested
api_type:
- schema
ms.assetid: 8037bbe5-a37f-4f77-8209-27a94f9095ef
description: El elemento MailTipsRequested contiene los tipos de sugerencias de correo solicitados desde el servicio.
ms.openlocfilehash: fa2bef394ea8473aa65bdc2f1d39c0794186fdc6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836348"
---
# <a name="mailtipsrequested"></a>MailTipsRequested

El elemento **MailTipsRequested** contiene los tipos de sugerencias de correo solicitados desde el servicio. 
  
```XML
<MailTipsRequested/>
```

 **MailTipTypes**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GetMailTips](getmailtips.md) <br/> |Contiene los destinatarios y los tipos de sugerencias de correo para recuperar.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumera los valores posibles para el elemento **MailTipsRequested** . 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|Todos  <br/> |Representa todas las sugerencias de correo disponibles.  <br/> |
|OutOfOfficeMessage  <br/> |Representa el mensaje de fuera de oficina (OOF).  <br/> |
|MailboxFullStatus  <br/> |Representa el estado de un buzón de correo que está lleno.  <br/> |
|CustomMailTip  <br/> |Representa una sugerencia de correo personalizado.  <br/> |
|ExternalMemberCount  <br/> |Representa el recuento de miembros externos.  <br/> |
|TotalMemberCount  <br/> |Representa el recuento de todos los miembros.  <br/> |
|MaxMessageSize  <br/> |Representa el tamaño máximo de mensaje que puede aceptar un destinatario.  <br/> |
|DeliveryRestriction  <br/> |Indica si las restricciones de entrega impedirá que el mensaje del remitente llegar al destinatario.  <br/> |
|ModerationStatus  <br/> |Indica si el mensaje del remitente será revisado por un moderador.  <br/> |
|InvalidRecipient  <br/> |Indica si el destinatario no es válido.  <br/> |
   
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

