---
title: MailTipsRequested
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MailTipsRequested
api_type:
- schema
ms.assetid: 8037bbe5-a37f-4f77-8209-27a94f9095ef
description: El elemento MailTipsRequested contiene los tipos de sugerencias de correo solicitadas desde el servicio.
ms.openlocfilehash: 14a463d3b00a9f8b3e2aa2e822209ff87a221f9b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524857"
---
# <a name="mailtipsrequested"></a>MailTipsRequested

El **elemento MailTipsRequested** contiene los tipos de sugerencias de correo solicitadas desde el servicio. 
  
```XML
<MailTipsRequested/>
```

 **MailTipTypes**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetMailTips](getmailtips.md) <br/> |Contiene los destinatarios y los tipos de sugerencias de correo que se recuperarán.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la tabla siguiente se enumeran los valores posibles para el **elemento MailTipsRequested.** 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|Todo  <br/> |Representa todas las sugerencias de correo disponibles.  <br/> |
|OutOfOfficeMessage  <br/> |Representa el mensaje De Office (OOF).  <br/> |
|MailboxFullStatus  <br/> |Representa el estado de un buzón que está lleno.  <br/> |
|CustomMailTip  <br/> |Representa una sugerencia de correo personalizada.  <br/> |
|ExternalMemberCount  <br/> |Representa el recuento de miembros externos.  <br/> |
|TotalMemberCount  <br/> |Representa el recuento de todos los miembros.  <br/> |
|MaxMessageSize  <br/> |Representa el tamaño máximo de mensaje que un destinatario puede aceptar.  <br/> |
|DeliveryRestriction  <br/> |Indica si las restricciones de entrega impedirán que el mensaje del remitente llegue al destinatario.  <br/> |
|ModerationStatus  <br/> |Indica si un moderador revisará el mensaje del remitente.  <br/> |
|InvalidRecipient  <br/> |Indica si el destinatario no es válido.  <br/> |
   
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

