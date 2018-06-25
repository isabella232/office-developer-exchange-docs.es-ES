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
description: El elemento de configuración representa una opción de configuración que se va a devolver.
ms.openlocfilehash: cb5b1d6ab2109b48810b96221b76c6b8fc9803ac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837472"
---
# <a name="setting-soap"></a>Configuración (SOAP)

El elemento de **configuración** representa una opción de configuración que se va a devolver. 
  
```XML
<Setting/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[RequestedSettings (SOAP)](requestedsettings-soap.md) <br/> |Contiene los nombres de las opciones de configuración solicitado.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto para este elemento es el valor de configuración. En la siguiente tabla se enumera las opciones de configuración posibles.
  
|**Opción de configuración**|**Descripción**|
|:-----|:-----|
|UserDisplayName  <br/> |El nombre para mostrar del usuario.  <br/> |
|DnUsuario  <br/> |El nombre distintivo (DN) heredado del usuario.  <br/> |
|UserDeploymentId  <br/> |El identificador de implementación del usuario.  <br/> |
|InternalMailboxServer  <br/> |El nombre de dominio completo (FQDN) del servidor de buzones.  <br/> |
|InternalRpcClientServer  <br/> |El nombre de dominio completo del servidor de cliente RPC.  <br/> |
|InternalMailboxServerDN  <br/> |El nombre distintivo (DN) heredado del servidor de buzones.  <br/> |
|InternalEcpUrl  <br/> |La dirección URL interna del Panel de Control de Exchange.  <br/> |
|InternalEcpVoicemailUrl  <br/> |La dirección URL interna del Panel de Control de Exchange para la personalización de correo de voz.  <br/> |
|InternalEcpEmailSubscriptionsUrl  <br/> |La dirección URL interna del Panel de Control de Exchange para las suscripciones de correo electrónico.  <br/> |
|InternalEcpTextMessagingUrl  <br/> |La dirección URL interna del Panel de Control de Exchange para la mensajería de texto.  <br/> |
|InternalEcpDeliveryReportUrl  <br/> |La dirección URL interna del Panel de Control de Exchange para los informes de entrega.  <br/> |
|InternalEcpRetentionPolicyTagsUrl  <br/> |La dirección URL interna del Panel de Control de Exchange para las etiquetas de RetentionPolicy.  <br/> |
|InternalEcpPublishingUrl  <br/> |La dirección URL interna del Panel de Control de Exchange para la publicación.  <br/> |
|InternalEwsUrl  <br/> |La dirección URL de Exchange servicios Web internos.  <br/> |
|InternalOABUrl  <br/> |La dirección URL interna de la libreta de direcciones sin conexión (OAB).  <br/> |
|InternalUMUrl  <br/> |La dirección URL interna de los servicios de mensajería unificada.  <br/> |
|InternalWebClientUrls  <br/> |Las direcciones URL internas del cliente Web de Exchange.  <br/> |
|MailboxDN  <br/> |El nombre distintivo (DN) de la base de datos de buzón de correo del buzón del usuario.  <br/> |
|PublicFolderServer  <br/> |El nombre del servidor de carpetas públicas.  <br/> |
|ActiveDirectoryServer  <br/> |El nombre del servidor de Active Directory.  <br/> |
|ExternalMailboxServer  <br/> |El nombre de la RPC a través de servidor HTTP.  <br/> |
|ExternalMailboxServerRequiresSSL  <br/> |El indicador de si la RPC a través de servidor HTTP requiere SSL.  <br/> |
|ExternalMailboxServerAuthenticationMethods  <br/> |Los métodos de autenticación que se admiten por la RPC a través de servidor HTTP.  <br/> |
|EcpVoicemailUrlFragment,  <br/> |El fragmento de dirección URL del Panel de Control de Exchange para la personalización de correo de voz.  <br/> |
|EcpEmailSubscriptionsUrlFragment  <br/> |El fragmento de dirección URL del Panel de Control de Exchange para las suscripciones de correo electrónico.  <br/> |
|EcpTextMessagingUrlFragment  <br/> |El fragmento de dirección URL del Panel de Control de Exchange para la mensajería de texto.  <br/> |
|EcpDeliveryReportUrlFragment  <br/> |El fragmento de dirección URL del Panel de Control de Exchange para los informes de entrega.  <br/> |
|EcpRetentionPolicyTagsUrlFragment  <br/> |El fragmento de dirección URL del Panel de Control de Exchange para las etiquetas de RetentionPolicy.  <br/> |
|EcpPublishingUrlFragment  <br/> |El fragmento de dirección URL del Panel de Control de Exchange para la publicación.  <br/> |
|ExternalEcpUrl  <br/> |La dirección URL externa del Panel de Control de Exchange.  <br/> |
|ExternalEcpVoicemailUrl  <br/> |La dirección URL externa del Panel de Control de Exchange para la personalización de correo de voz.  <br/> |
|ExternalEcpEmailSubscriptionsUrl  <br/> |La dirección URL externa del Panel de Control de Exchange para las suscripciones de correo electrónico.  <br/> |
|ExternalEcpTextMessagingUrl  <br/> |La dirección URL externa del Panel de Control de Exchange para la mensajería de texto.  <br/> |
|ExternalEcpDeliveryReportUrl  <br/> |La dirección URL externa del Panel de Control de Exchange para los informes de entrega.  <br/> |
|ExternalEcpRetentionPolicyTagsUrl  <br/> |La dirección URL externa del Panel de Control de Exchange para las etiquetas de RetentionPolicy.  <br/> |
|ExternalEcpPublishingUrl  <br/> |La dirección URL externa del Panel de Control de Exchange para la publicación.  <br/> |
|ExternalEwsUrl  <br/> |La dirección URL externa de los servicios Web de Exchange.  <br/> |
|ExternalOABUrl  <br/> |La dirección URL externa de la OAB.  <br/> |
|ExternalUMUrl  <br/> |La dirección URL externa de los servicios de mensajería unificada.  <br/> |
|ExternalWebClientUrls  <br/> |Las direcciones URL externas del cliente Web de Exchange.  <br/> |
|CrossOrganizationSharingEnabled  <br/> |Indica que está habilitado el uso compartido de toda la organización.  <br/> |
|AlternateMailboxes  <br/> |Colección de los buzones de correo alternativas.  <br/> |
|CasVersion  <br/> |La versión del servidor acceso de cliente que es atender la solicitud (por ejemplo, 14.XX. AAAA. ZZZ)  <br/> |
|EwsSupportedSchemas  <br/> |Una lista separada por comas de las versiones de esquema compatibles con servicios Web de Exchange. Los valores de la versión de esquema será el mismo que los valores de la enumeración **ExchangeServerVersion** .  <br/> |
|InternalPop3Connections  <br/> |La lista de configuración de conexión interna para las conexiones de protocolo POP3.  <br/> |
|ExternalPop3Connections  <br/> |La lista de configuración de conexión externo para las conexiones de protocolo POP3.  <br/> |
|InternalImap4Connections  <br/> |La lista de configuración de conexión interna para las conexiones de protocolo de IMAP4.  <br/> |
|ExternalImap4Connections  <br/> |La lista de configuración de conexión externo para las conexiones de protocolo de IMAP4.  <br/> |
|InternalSmtpConnections  <br/> |La lista de configuración de conexión interna para las conexiones SMTP.  <br/> |
|ExternalSmtpConnections  <br/> |La lista de configuración de conexión externo para las conexiones SMTP.  <br/> |
|InternalServerExclusiveConnect  <br/> |El servidor interno exclusivo conectar marca. Si establece en "Off" a los clientes, a continuación, debe no conectarse a través de este protocolo.  <br/> |
|ExternalServerExclusiveConnect  <br/> |El servidor externo exclusivo conectar marca. Si se establece en "Activado" clientes, a continuación, debe conectarse a través de este protocolo.  <br/> |
|ExchangeRpcUrl  <br/> |La dirección URL que usa para llamadas a procedimiento remoto. Esta dirección URL es interna en el servidor y no es debe ser usado por los clientes.  <br/> |
|ShowGalAsDefaultView  <br/> |Especifica un valor booleano que indica si se debe mostrar la lista global de direcciones como la libreta de direcciones. Un valor de texto de "true" indica que la lista global de direcciones es para que se muestren de forma predeterminada. Un valor de texto de "false" indica que la lista de contactos es que se debe mostrar.  <br/> |
|AutoDiscoverSMTPAddress  <br/> |La detección automática dirección SMTP principal para el usuario. Esta es la dirección de proxy en lugar de la dirección de correo electrónico del usuario, si existe una dirección de proxy.  <br/> |
|InteropExternalEwsUrl  <br/> |La dirección URL externa del extremo de servicio Web del servidor. Esta es la dirección URL de un servidor que puede atender buzones alojados en un servidor que no tiene los servicios Web.  <br/> |
|ExternalEwsVersion  <br/> |La versión del servidor de servicios Web que entrega la solicitud especificada.  <br/> |
|InteropExternalEwsVersion  <br/> |La versión del servidor InteropExternalEwsUrl está señalando al.  <br/> |
|MobileMailboxPolicyInterop  <br/> |La configuración de directiva de buzón móvil.  <br/> |
|GroupingInformation  <br/> |Un valor que se utiliza junto con la configuración de ExternalEwsUrl para agrupar varios buzones conjuntamente para [mantener la afinidad](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx) al suscribirse a las notificaciones.  <br/> |
|UserMSOnline  <br/> |Un valor booleano que indica si el buzón del usuario está hospedado en Exchange Online o Exchange Online como parte de Office 365.  <br/> |
|MapiHttpEnabled  <br/> |Un valor booleano que indica si el buzón del usuario es accesible a través del protocolo HTTP/MAPI.  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
  
[Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)

