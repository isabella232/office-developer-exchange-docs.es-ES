---
title: MailTipsConfiguration (MailTipsServiceConfiguration)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MailTipsConfiguration
api_type:
- schema
ms.assetid: 9a34515e-815b-4c61-b118-d5f66b80238f
description: El elemento MailTipsConfiguration contiene información de configuración del servicio de sugerencias de correo.
ms.openlocfilehash: eb86291572f6854710d01badcee2db24406844c6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524038"
---
# <a name="mailtipsconfiguration-mailtipsserviceconfiguration"></a>MailTipsConfiguration (MailTipsServiceConfiguration)

El **elemento MailTipsConfiguration** contiene información de configuración del servicio de sugerencias de correo. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MailTipsEnabled](mailtipsenabled.md) <br/> |Indica si el servicio de sugerencias de correo está disponible. Se requiere este elemento.  <br/> |
|[MaxRecipientsPerGetMailTipsRequest](maxrecipientspergetmailtipsrequest.md) <br/> |Indica el número máximo de destinatarios que se pueden pasar a la [operación GetMailTips](getmailtips-operation.md). Se requiere este elemento.  <br/> |
|[MaxMessageSize](maxmessagesize.md) <br/> |Representa el tamaño máximo de mensaje que un destinatario puede aceptar. Se requiere este elemento.  <br/> |
|[LargeAudienceThreshold](largeaudiencethreshold.md) <br/> |Representa el umbral de audiencia grande para un cliente. Se requiere este elemento.  <br/> |
|[ShowExternalRecipientCount](showexternalrecipientcount.md) <br/> |Indica si los consumidores de la operación [GetMailTips](getmailtips-operation.md) deben mostrar sugerencias de correo que indiquen el número de destinatarios externos a los que se dirige un mensaje. Se requiere este elemento.  <br/> |
|[InternalDomains (SmtpDomainList)](internaldomains-smtpdomainlist.md) <br/> |Identifica la lista de dominios SMTP internos de la organización. Se requiere este elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |Contiene opciones de configuración de servicio.  <br/> |
   
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

