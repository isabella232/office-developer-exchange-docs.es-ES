---
title: Setting (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 43db26e1-f7be-49fd-b26b-fc1b10bd3458
description: El elemento Setting representa una configuración que se va a devolver.
ms.openlocfilehash: 2e03bfacaf36676ee4687c148f3b08732a9f17b1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539146"
---
# <a name="setting-soap"></a>Setting (SOAP)

El **elemento Setting** representa una configuración que se va a devolver. 
  
```XML
<Setting/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RequestedSettings (SOAP)](requestedsettings-soap.md) <br/> |Contiene los nombres de las opciones de configuración solicitadas.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto de este elemento es la configuración. En la tabla siguiente se enumeran las opciones de configuración posibles.
  
|**Opción de configuración**|**Descripción**|
|:-----|:-----|
|UserDisplayName  <br/> |El nombre para mostrar del usuario.  <br/> |
|UserDN  <br/> |Nombre distintivo heredado del usuario.  <br/> |
|UserDeploymentId  <br/> |Identificador de implementación del usuario.  <br/> |
|InternalMailboxServer  <br/> |Nombre de dominio completo (FQDN) del servidor de buzones de correo.  <br/> |
|InternalRpcClientServer  <br/> |Nombre de dominio completo del servidor cliente RPC.  <br/> |
|InternalMailboxServerDN  <br/> |Nombre distintivo heredado del servidor de buzones de correo.  <br/> |
|InternalEcpUrl  <br/> |Dirección URL interna del panel Exchange control.  <br/> |
|InternalEcpVoicemailUrl  <br/> |La dirección URL interna del panel Exchange control para la personalización de VoiceMail.  <br/> |
|InternalEcpEmailSubscriptionsUrl  <br/> |Dirección URL interna del panel de control Exchange para suscripciones de correo electrónico.  <br/> |
|InternalEcpTextMessagingUrl  <br/> |La dirección URL interna del panel Exchange control para mensajería de texto.  <br/> |
|InternalEcpDeliveryReportUrl  <br/> |Dirección URL interna del panel de control Exchange para informes de entrega.  <br/> |
|InternalEcpRetentionPolicyTagsUrl  <br/> |Dirección URL interna del panel Exchange control para etiquetas RetentionPolicy.  <br/> |
|InternalEcpPublishingUrl  <br/> |Dirección URL interna del panel de control Exchange para publicación.  <br/> |
|InternalEwsUrl  <br/> |Dirección URL interna de Exchange Web Services.  <br/> |
|InternalOABUrl  <br/> |La dirección URL interna de la libreta de direcciones sin conexión (OAB).  <br/> |
|InternalUMUrl  <br/> |Dirección URL interna de los servicios de mensajería unificada.  <br/> |
|InternalWebClientUrls  <br/> |Las direcciones URL internas del Exchange cliente web.  <br/> |
|MailboxDN  <br/> |Nombre distintivo de la base de datos de buzones de correo del buzón del usuario.  <br/> |
|PublicFolderServer  <br/> |Nombre del servidor de carpetas públicas.  <br/> |
|ActiveDirectoryServer  <br/> |Nombre del servidor de Active Directory.  <br/> |
|ExternalMailboxServer  <br/> |Nombre del servidor RPC sobre HTTP.  <br/> |
|ExternalMailboxServerRequiresSSL  <br/> |Indicador de si el servidor RPC sobre HTTP requiere SSL.  <br/> |
|ExternalMailboxServerAuthenticationMethods  <br/> |Los métodos de autenticación compatibles con el servidor RPC sobre HTTP.  <br/> |
|EcpVoicemailUrlFragment,  <br/> |Fragmento de dirección URL del panel Exchange control para la personalización de VoiceMail.  <br/> |
|EcpEmailSubscriptionsUrlFragment  <br/> |Fragmento de dirección URL del panel Exchange control de suscripciones de correo electrónico.  <br/> |
|EcpTextMessagingUrlFragment  <br/> |Fragmento de dirección URL del panel Exchange control para mensajería de texto.  <br/> |
|EcpDeliveryReportUrlFragment  <br/> |Fragmento de dirección URL del panel Exchange control para informes de entrega.  <br/> |
|EcpRetentionPolicyTagsUrlFragment  <br/> |Fragmento de dirección URL del panel Exchange control para etiquetas RetentionPolicy.  <br/> |
|EcpPublishingUrlFragment  <br/> |Fragmento de dirección URL del panel Exchange control de publicación.  <br/> |
|ExternalEcpUrl  <br/> |La dirección URL externa del panel Exchange control.  <br/> |
|ExternalEcpVoicemailUrl  <br/> |La dirección URL externa del panel Exchange control para la personalización de VoiceMail.  <br/> |
|ExternalEcpEmailSubscriptionsUrl  <br/> |La dirección URL externa del panel Exchange control de suscripciones de correo electrónico.  <br/> |
|ExternalEcpTextMessagingUrl  <br/> |La dirección URL externa del panel Exchange control para mensajería de texto.  <br/> |
|ExternalEcpDeliveryReportUrl  <br/> |La dirección URL externa del panel Exchange control para informes de entrega.  <br/> |
|ExternalEcpRetentionPolicyTagsUrl  <br/> |La dirección URL externa del panel Exchange control para etiquetas RetentionPolicy.  <br/> |
|ExternalEcpPublishingUrl  <br/> |La dirección URL externa del panel Exchange control de publicación.  <br/> |
|ExternalEwsUrl  <br/> |La dirección URL externa de Exchange Web Services.  <br/> |
|ExternalOABUrl  <br/> |Dirección URL externa de la OAB.  <br/> |
|ExternalUMUrl  <br/> |La dirección URL externa de los servicios de mensajería unificada.  <br/> |
|ExternalWebClientUrls  <br/> |Las direcciones URL externas del Exchange web.  <br/> |
|CrossOrganizationSharingEnabled  <br/> |Indica que el uso compartido entre organizaciones está habilitado.  <br/> |
|AlternateMailboxes  <br/> |Colección de buzones alternativos.  <br/> |
|CasVersion  <br/> |La versión del servidor de acceso de cliente que está atendiendo la solicitud (por ejemplo, 14.XX.YYYYY. ZZZ)  <br/> |
|EwsSupportedSchemas  <br/> |Una lista separada por comas de las versiones de esquema admitidas por Exchange Web Services. Los valores de versión del esquema serán los mismos que los valores de la **enumeración ExchangeServerVersion.**  <br/> |
|InternalPop3Connections  <br/> |La lista de configuración de conexión interna para las conexiones de protocolo POP3.  <br/> |
|ExternalPop3Connections  <br/> |La lista de configuración de conexión externa para las conexiones de protocolo POP3.  <br/> |
|InternalImap4Connections  <br/> |La lista de configuración de conexión interna para las conexiones de protocolo IMAP4.  <br/> |
|ExternalImap4Connections  <br/> |Lista de configuración de conexión externa para conexiones de protocolo IMAP4.  <br/> |
|InternalSmtpConnections  <br/> |La lista de configuración de conexión interna para las conexiones SMTP.  <br/> |
|ExternalSmtpConnections  <br/> |La lista de configuración de conexión externa para las conexiones SMTP.  <br/> |
|InternalServerExclusiveConnect  <br/> |La marca de conexión exclusiva del servidor interno. Si se establece en "Desactivado", los clientes no deben conectarse a través de este protocolo.  <br/> |
|ExternalServerExclusiveConnect  <br/> |La marca de conexión exclusiva del servidor externo. Si se establece en "On", los clientes DEBEN conectarse a través de este protocolo.  <br/> |
|ExchangeRpcUrl  <br/> |Dirección URL que se usa para llamadas a procedimientos remotos. Esta dirección URL es interna del servidor y no la deben usar los clientes.  <br/> |
|ShowGalAsDefaultView  <br/> |Especifica un valor booleano que indica si la GAL debe mostrarse como la libreta de direcciones. Un valor de texto de "true" indica que la GAL se va a mostrar de forma predeterminada. Un valor de texto de "false" indica que se mostrará la lista de contactos.  <br/> |
|AutoDiscoverSMTPAddress  <br/> |La dirección SMTP principal de detección automática para el usuario. Esta es la dirección proxy en lugar de la dirección de correo electrónico del usuario, si existe una dirección proxy.  <br/> |
|InteropExternalEwsUrl  <br/> |Dirección URL externa del punto de conexión del servicio web del servidor. Esta es la dirección URL de un servidor que puede servir buzones hospedados en un servidor que no tiene los servicios web.  <br/> |
|ExternalEwsVersion  <br/> |La versión del servidor de servicios web que está entregando la solicitud especificada.  <br/> |
|InteropExternalEwsVersion  <br/> |La versión del servidor InteropExternalEwsUrl apunta.  <br/> |
|MobileMailboxPolicyInterop  <br/> |La configuración de la directiva de buzón de correo móvil.  <br/> |
|GroupingInformation  <br/> |Valor que se usa junto con la configuración ExternalEwsUrl para agrupar varios buzones para mantener la afinidad al suscribirse a notificaciones. [](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)  <br/> |
|UserMSOnline  <br/> |Valor booleano que indica si el buzón del usuario está hospedado en Exchange Online o Exchange Online como parte de Office 365.  <br/> |
|MapiHttpEnabled  <br/> |Valor booleano que indica si el buzón del usuario es accesible a través del protocolo MAPI/HTTP.  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
  
[Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)

