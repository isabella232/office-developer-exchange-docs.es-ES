---
title: MailTipsConfiguration (MailTipsServiceConfiguration)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTipsConfiguration
api_type:
- schema
ms.assetid: 9a34515e-815b-4c61-b118-d5f66b80238f
description: El elemento MailTipsConfiguration contiene información de configuración de servicio para el servicio de sugerencias de correo.
ms.openlocfilehash: ea92af3ebb2d2f720e5823c5317d09d5bcdb3978
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836321"
---
# <a name="mailtipsconfiguration-mailtipsserviceconfiguration"></a>MailTipsConfiguration (MailTipsServiceConfiguration)

El elemento **MailTipsConfiguration** contiene información de configuración de servicio para el servicio de sugerencias de correo. 
  
```XML
<MailTipsConfiguration>
   <MailTipsEnabled/>
   <MaxRecipientsPerGetMailTipsRequest/>
   <MaxMessageSize/>
   <LargeAudienceThreshold/>
   <ShowExternalRecipientCount/>
   <InternalDomains/>
</MailTipsConfiguration>
```

 **MailTipsServiceConfiguration**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[MailTipsEnabled](mailtipsenabled.md) <br/> |Indica si el servicio de sugerencias de correo está disponible. Se requiere este elemento.  <br/> |
|[MaxRecipientsPerGetMailTipsRequest](maxrecipientspergetmailtipsrequest.md) <br/> |Indica el número máximo de destinatarios que se pueden pasar a la [operación de GetMailTips](getmailtips-operation.md). Se requiere este elemento.  <br/> |
|[MaxMessageSize](maxmessagesize.md) <br/> |Representa el tamaño máximo de mensaje que puede aceptar un destinatario. Se requiere este elemento.  <br/> |
|[LargeAudienceThreshold](largeaudiencethreshold.md) <br/> |Representa el umbral de audiencia grande para un cliente. Se requiere este elemento.  <br/> |
|[ShowExternalRecipientCount](showexternalrecipientcount.md) <br/> |Indica si los consumidores de la [operación de GetMailTips](getmailtips-operation.md) tienen que mostrar sugerencias de correo que indican el número de destinatarios externos a la que se envía un mensaje. Se requiere este elemento.  <br/> |
|[InternalDomains (SmtpDomainList)](internaldomains-smtpdomainlist.md) <br/> |Identifica la lista de dominios SMTP internos de la organización. Se requiere este elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |Contiene la configuración del servicio.  <br/> |
   
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

