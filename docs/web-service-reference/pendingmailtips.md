---
title: PendingMailTips
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PendingMailTips
api_type:
- schema
ms.assetid: 0cd70eea-8d36-4b1b-bf80-5edf359e7ba7
description: El elemento PendingMailTips indica que no se podrían evaluar las sugerencias de correo en este elemento antes de tiempo de espera de procesamiento del servidor.
ms.openlocfilehash: 73d597f6534ea29f7d26d6526c48631251521ae5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836704"
---
# <a name="pendingmailtips"></a>PendingMailTips

El elemento **PendingMailTips** indica que no se podrían evaluar las sugerencias de correo en este elemento antes de tiempo de espera de procesamiento del servidor. 
  
```XML
<PendingMailTips>All | OutOfOfficeMessage | MailboxFullStatus | CustomMailTip | ExternalMemberCount | TotalMemberCount | MaxMessageSize | DeliveryRestriction | ModerateStatus | InvalidRecipient</PendingMailTips>
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
|[Sugerencias de correo electrónico](mailtips.md) <br/> |Representa los valores de distintos tipos de sugerencias de correo.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumera los valores posibles para el elemento **PendingMailTips** . 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|Todos  <br/> |Representa todas las sugerencias de correo disponibles.  <br/> |
|OutOfOfficeMessage  <br/> |Representa el mensaje de fuera de oficina (OOF).  <br/> |
|MailboxFullStatus  <br/> |Representa el estado de un buzón que se está completa.  <br/> |
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
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

