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
ms.openlocfilehash: bcb2ebf15e628a04e8507f938d385cf113f2f2a3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465901"
---
# <a name="mailtipsrequested"></a>MailTipsRequested

El elemento **MailTipsRequested** contiene los tipos de sugerencias de correo solicitados desde el servicio. 
  
```XML
<MailTipsRequested/>
```

 **MailTipTypes**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetMailTips](getmailtips.md) <br/> |Contiene los destinatarios y los tipos de sugerencias de correo que se van a recuperar.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumeran los valores posibles para el elemento **MailTipsRequested** . 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|Todo  <br/> |Representa todas las sugerencias de correo disponibles.  <br/> |
|OutOfOfficeMessage  <br/> |Representa el mensaje de fuera de la oficina (OOF).  <br/> |
|MailboxFullStatus  <br/> |Representa el estado de un buzón de correo lleno.  <br/> |
|CustomMailTip  <br/> |Representa una sugerencia de correo personalizada.  <br/> |
|ExternalMemberCount  <br/> |Representa el número de miembros externos.  <br/> |
|TotalMemberCount  <br/> |Representa el número de todos los miembros.  <br/> |
|MaxMessageSize  <br/> |Representa el tamaño máximo de mensaje que puede aceptar un destinatario.  <br/> |
|DeliveryRestriction  <br/> |Indica si las restricciones de entrega impedirán que el mensaje del remitente llegue al destinatario.  <br/> |
|ModerationStatus  <br/> |Indica si el mensaje del remitente será revisado por un moderador.  <br/> |
|InvalidRecipient  <br/> |Indica si el destinatario no es válido.  <br/> |
   
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

