---
title: Configuración (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 43db26e1-f7be-49fd-b26b-fc1b10bd3458
description: El elemento Setting representa una opción de configuración que se va a devolver.
ms.openlocfilehash: df3b55fe7ba2c5ae92f8c31ec0643dbe100fa072
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466748"
---
# <a name="setting-soap"></a>Configuración (SOAP)

El elemento **Setting** representa una opción de configuración que se va a devolver. 
  
```XML
<Setting/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RequestedSettings (SOAP)](requestedsettings-soap.md) <br/> |Contiene los nombres de las opciones de configuración solicitadas.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto de este elemento es la configuración. En la siguiente tabla se enumeran las opciones de configuración posibles.
  
|**Opción de configuración**|**Descripción**|
|:-----|:-----|
|UserDisplayName  <br/> |El nombre para mostrar del usuario.  <br/> |
|UserDN  <br/> |El nombre distintivo heredado del usuario.  <br/> |
|UserDeploymentId  <br/> |El identificador de implementación del usuario.  <br/> |
|InternalMailboxServer  <br/> |El nombre de dominio completo (FQDN) del servidor de buzones de correo.  <br/> |
|InternalRpcClientServer  <br/> |Nombre de dominio completo del servidor cliente RPC.  <br/> |
|InternalMailboxServerDN  <br/> |El nombre distintivo heredado del servidor de buzones de correo.  <br/> |
|InternalEcpUrl  <br/> |La dirección URL interna del panel de control de Exchange.  <br/> |
|InternalEcpVoicemailUrl  <br/> |La dirección URL interna del panel de control de Exchange para la personalización de correo de voz.  <br/> |
|InternalEcpEmailSubscriptionsUrl  <br/> |La dirección URL interna del panel de control de Exchange para las suscripciones de correo electrónico.  <br/> |
|InternalEcpTextMessagingUrl  <br/> |La dirección URL interna del panel de control de Exchange para mensajería de texto.  <br/> |
|InternalEcpDeliveryReportUrl  <br/> |La dirección URL interna del panel de control de Exchange para informes de entrega.  <br/> |
|InternalEcpRetentionPolicyTagsUrl  <br/> |La dirección URL interna del panel de control de Exchange para las etiquetas RetentionPolicy.  <br/> |
|InternalEcpPublishingUrl  <br/> |La dirección URL interna del panel de control de Exchange para la publicación.  <br/> |
|InternalEwsUrl  <br/> |La dirección URL interna de los servicios web Exchange.  <br/> |
|InternalOABUrl  <br/> |La dirección URL interna de la libreta de direcciones sin conexión (OAB).  <br/> |
|InternalUMUrl  <br/> |La dirección URL interna de los servicios de mensajería unificada.  <br/> |
|InternalWebClientUrls  <br/> |Las direcciones URL internas del cliente web de Exchange.  <br/> |
|MailboxDN  <br/> |El nombre distintivo de la base de datos de buzones del buzón del usuario.  <br/> |
|PublicFolderServer  <br/> |El nombre del servidor de carpetas públicas.  <br/> |
|ActiveDirectoryServer  <br/> |El nombre del servidor de Active Directory.  <br/> |
|ExternalMailboxServer  <br/> |El nombre de la RPC sobre el servidor HTTP.  <br/> |
|ExternalMailboxServerRequiresSSL  <br/> |El indicador de si el servidor RPC sobre HTTP requiere SSL.  <br/> |
|ExternalMailboxServerAuthenticationMethods  <br/> |Los métodos de autenticación admitidos por el RPC sobre el servidor HTTP.  <br/> |
|EcpVoicemailUrlFragment,  <br/> |Fragmento de la dirección URL del panel de control de Exchange para la personalización de correo de voz.  <br/> |
|EcpEmailSubscriptionsUrlFragment  <br/> |Fragmento de la dirección URL del panel de control de Exchange para las suscripciones de correo electrónico.  <br/> |
|EcpTextMessagingUrlFragment  <br/> |Fragmento de la dirección URL del panel de control de Exchange para mensajería de texto.  <br/> |
|EcpDeliveryReportUrlFragment  <br/> |Fragmento de la dirección URL del panel de control de Exchange para informes de entrega.  <br/> |
|EcpRetentionPolicyTagsUrlFragment  <br/> |Fragmento de la dirección URL del panel de control de Exchange para las etiquetas RetentionPolicy.  <br/> |
|EcpPublishingUrlFragment  <br/> |Fragmento de la dirección URL del panel de control de Exchange para la publicación.  <br/> |
|ExternalEcpUrl  <br/> |Dirección URL externa del panel de control de Exchange.  <br/> |
|ExternalEcpVoicemailUrl  <br/> |Dirección URL externa del panel de control de Exchange para la personalización de correo de voz.  <br/> |
|ExternalEcpEmailSubscriptionsUrl  <br/> |Dirección URL externa del panel de control de Exchange para las suscripciones de correo electrónico.  <br/> |
|ExternalEcpTextMessagingUrl  <br/> |La dirección URL externa del panel de control de Exchange para mensajería de texto.  <br/> |
|ExternalEcpDeliveryReportUrl  <br/> |Dirección URL externa del panel de control de Exchange para informes de entrega.  <br/> |
|ExternalEcpRetentionPolicyTagsUrl  <br/> |La dirección URL externa del panel de control de Exchange para las etiquetas RetentionPolicy.  <br/> |
|ExternalEcpPublishingUrl  <br/> |Dirección URL externa del panel de control de Exchange para la publicación.  <br/> |
|ExternalEwsUrl  <br/> |La dirección URL externa de los servicios Web de Exchange.  <br/> |
|ExternalOABUrl  <br/> |La dirección URL externa de la OAB.  <br/> |
|ExternalUMUrl  <br/> |La dirección URL externa de los servicios de mensajería unificada.  <br/> |
|ExternalWebClientUrls  <br/> |Las direcciones URL externas del cliente web de Exchange.  <br/> |
|CrossOrganizationSharingEnabled  <br/> |Indica que el uso compartido entre organizaciones está habilitado.  <br/> |
|AlternateMailboxes  <br/> |Colección de buzones de correo alternativos.  <br/> |
|CasVersion  <br/> |La versión del servidor de acceso de cliente que atiende la solicitud (por ejemplo, 14. XX. YYYY. ZZZ  <br/> |
|EwsSupportedSchemas  <br/> |Una lista separada por comas de versiones de esquema compatibles con los servicios web Exchange. Los valores de versión de esquema serán los mismos que los valores de la enumeración **ExchangeServerVersion** .  <br/> |
|InternalPop3Connections  <br/> |La lista de configuración de conexión interna para conexiones de protocolo POP3.  <br/> |
|ExternalPop3Connections  <br/> |La lista de configuración de conexión externa para conexiones de protocolo POP3.  <br/> |
|InternalImap4Connections  <br/> |La lista de configuración de conexión interna para conexiones de protocolo IMAP4.  <br/> |
|ExternalImap4Connections  <br/> |La lista de configuración de conexión externa para conexiones de protocolo IMAP4.  <br/> |
|InternalSmtpConnections  <br/> |La lista de configuración de conexión interna para las conexiones SMTP.  <br/> |
|ExternalSmtpConnections  <br/> |La lista de configuración de conexión externa para las conexiones SMTP.  <br/> |
|InternalServerExclusiveConnect  <br/> |Marca de conexión exclusiva del servidor interno. Si se establece en "desactivado", los clientes no deben conectarse a través de este protocolo.  <br/> |
|ExternalServerExclusiveConnect  <br/> |La marca de conexión exclusiva del servidor externo. Si se establece en "activado", los clientes deben conectarse a través de este protocolo.  <br/> |
|ExchangeRpcUrl  <br/> |Dirección URL que se usa para las llamadas a procedimientos remotos. Esta dirección URL es interna del servidor y no la usarán los clientes.  <br/> |
|ShowGalAsDefaultView  <br/> |Especifica un valor booleano que indica si la GAL debe mostrarse como la libreta de direcciones. Un valor de texto de "true" indica que la GAL se va a mostrar de forma predeterminada. Un valor de texto de "false" indica que se va a mostrar la lista de contactos.  <br/> |
|AutoDiscoverSMTPAddress  <br/> |La dirección SMTP principal de detección automática del usuario. Esta es la dirección de proxy en lugar de la dirección de correo electrónico del usuario, si existe una dirección de proxy.  <br/> |
|InteropExternalEwsUrl  <br/> |Dirección URL externa del extremo del servicio Web del servidor. Se trata de la dirección URL de un servidor que puede atender buzones hospedados en un servidor que no tiene los servicios Web.  <br/> |
|ExternalEwsVersion  <br/> |La versión del servidor de servicios web que está entregando la solicitud especificada.  <br/> |
|InteropExternalEwsVersion  <br/> |La versión del servidor InteropExternalEwsUrl apunta a.  <br/> |
|MobileMailboxPolicyInterop  <br/> |La configuración de la Directiva de buzón móvil.  <br/> |
|GroupingInformation  <br/> |Un valor que se usa junto con la configuración ExternalEwsUrl para agrupar varios buzones de correo y [mantener la afinidad](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx) al suscribirse a las notificaciones.  <br/> |
|UserMSOnline  <br/> |Un valor booleano que indica si el buzón del usuario está hospedado en Exchange online o Exchange online como parte de Office 365.  <br/> |
|MapiHttpEnabled  <br/> |Un valor booleano que indica si se puede tener acceso al buzón del usuario a través del protocolo MAPI/HTTP.  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
  
[Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)

