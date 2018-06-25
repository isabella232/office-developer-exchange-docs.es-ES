---
title: Protocolo (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: f77e4d66-6fdd-4999-9339-f7d7f9c86f44
description: El elemento de protocolo contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Exchange Server que tiene instalada la función del servidor acceso de cliente.
ms.openlocfilehash: e58ae82ea5ec9d39db0f9219f6019df7da24a343
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836926"
---
# <a name="protocol-pox"></a>Protocolo (POX)

El elemento de **protocolo** contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Exchange Server que tiene instalada la función del servidor acceso de cliente. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
[Protocolo (POX)](protocol-pox.md)
  
```xml
<Protocol>
   <Type/>
   <Internal/>
   <External/>
   <TTL/>
   <Server/>
   <ServerDN/>
   <ServerVersion/>
   <MdbDN/>
   <PublicFolderServer/>
   <Port/>
   <DirectoryPort/>
   <ReferralPort/>
   <ASUrl/>
   <EwsUrl/>
   <EmwsUrl/>
   <SharingUrl/>
   <EcpUrl/>
   <EcpUrl-um/>
   <EcpUrl-aggr/>
   <EcpUrl-mt/>
   <EcpUrl-ret/>
   <EcpUrl-sms/>
   <EcpUrl-publish/>
   <EcpUrl-photo/>
   <EcpUrl-tm/>
   <EcpUrl-tmCreating/>
   <EcpUrl-tmHiding/>
   <EcpUrl-tmEditing/>
   <EcpUrl-extinstall/>
   <OOFUrl/>
   <OABUrl/>
   <UMUrl/>
   <EwsPartnerUrl/>
   <LoginName/>
   <DomainRequired/>
   <DomainName/>
   <SPA/>
   <AuthPackage/>
   <CertPrincipalName/>
   <SSL/>
   <AuthRequired/>
   <UsePOPAuth/>
   <SMTPLast/>
   <NetworkRequirements/>
   <AddressBook/>
   <MailStore/>
</Protocol>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|Tipo  <br/> |Indica el tipo de protocolo que se describe mediante este elemento de **protocolo** . El valor sólo es válido para este atributo es "mapiHttp". Este atributo es sólo está presente si la detección automática de solicitudes que corresponde a esta respuesta [incluye un encabezado X-MapiHttpCapability](pox-autodiscover-request-for-exchange.md). Este atributo es aplicable a los clientes que implementan el protocolo HTTP/MAPI y destino Exchange Online, Exchange Online como parte de Office 365, o versiones locales de Exchange a partir de con compilación 15.00.0847.032 (Exchange Server 2013 SP1).  <br/> |
|Versión  <br/> |Indica la versión del protocolo que se describe mediante este elemento de **protocolo** . El valor sólo es válido para este atributo es "1". Este atributo sólo está presente si la solicitud de detección automática que corresponde a esta respuesta incluido un encabezado **X-MapiHttpCapability** . Este atributo es aplicable a los clientes que implementan el protocolo HTTP/MAPI y destino Exchange Online, Exchange Online como parte de Office 365, o versiones locales de Exchange a partir de con compilación 15.00.0847.032 (Exchange Server 2013 SP1).  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Tipo (POX)](type-pox.md) <br/> |Identifica el tipo de la cuenta de correo configurada.  <br/> |
|[Interno (POX)](internal-pox.md) <br/> |Contiene una colección de direcciones URL que puede utilizar un cliente para conectarse a Exchange desde dentro de la red de la organización.  <br/> |
|[Externo (POX)](external-pox.md) <br/> |Contiene una colección de direcciones URL que puede utilizar un cliente para conectarse a Exchange desde fuera de la red de la organización.  <br/> |
|[TTL (POX)](ttl-pox.md) <br/> |Especifica el período de vida, en horas, durante el cual la configuración permanece válida.  <br/> |
|[Servidor (POX)](server-pox.md) <br/> |Especifica el nombre del servidor de correo.  <br/> |
|[ServerDN (POX)](serverdn-pox.md) <br/> |Especifica el nombre distintivo (DN) de Exchange Server.  <br/> |
|[ServerVersion (POX)](serverversion-pox.md) <br/> |Representa el número de versión de Exchange Server.  <br/> |
|[MdbDN (POX)](mdbdn-pox.md) <br/> |Representa el nombre distintivo (DN) de la base de datos de buzón de correo.  <br/> |
|[PublicFolderServer (POX)](publicfolderserver-pox.md) <br/> |Contiene el nombre de dominio completo (FQDN) del servidor de carpetas públicas para el usuario.  <br/> |
|[Puerto (POX)](port-pox.md) <br/> |Especifica el puerto que se usa para conectarse a la tienda.  <br/> |
|[DirectoryPort (POX)](directoryport-pox.md) <br/> |Especifica el puerto que se usa para conectarse al directorio cuando se usa el protocolo de interfaz de proveedor de servicio de nombres (NSPI).  <br/> |
|[ReferralPort (POX)](referralport-pox.md) <br/> |Especifica el puerto que se utiliza para obtener una referencia a un directorio.  <br/> |
|[ASUrl (POX)](asurl-pox.md) <br/> |Especifica la dirección URL de la instancia de procedimientos de los servicios Web de Exchange para un usuario habilitado para correo.  <br/> |
|[EwsUrl (POX)](ewsurl-pox.md) <br/> |Especifica la dirección URL de la instancia de extremo procedimientos de Exchange Web Services (EWS) para un usuario habilitado para correo.  <br/> |
|[EmwsUrl (POX)](emwsurl-pox.md) <br/> |Especifica la dirección URL de la instancia de extremo procedimientos de Exchange Web Services (EWS) para un usuario habilitado para correo.  <br/> |
|[SharingUrl (POX)](sharingurl-pox.md) <br/> |Contiene la dirección URL del servidor de uso compartido usado para toda la organización de uso compartido de calendarios y contactos.  <br/> |
|[EcpUrl (POX)](ecpurl-pox.md) <br/> |Especifica la dirección URL del Panel de Control de Exchange para un usuario habilitado para correo.  <br/> |
|[EcpUrl-mensajería unificada (POX)](ecpurl-um-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a la configuración de correo de voz para un usuario habilitado para correo.  <br/> |
|[EcpUrl-aggr (POX)](ecpurl-aggr-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a la configuración de agregación de correo electrónico para un usuario habilitado para correo.  <br/> |
|[EcpUrl-mt (POX)](ecpurl-mt-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a la configuración de un usuario habilitado para correo de seguimiento de mensajes de correo electrónico.  <br/> |
|[EcpUrl-devuelve (POX)](ecpurl-ret-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a la configuración de la etiqueta de retención para un usuario habilitado para correo.  <br/> |
|[EcpUrl-sms (POX)](ecpurl-sms-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a la configuración del servicio de mensajes cortos (SMS) para un usuario habilitado para correo.  <br/> |
|[EcpUrl-publicar (POX)](ecpurl-publish-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a la configuración de publicación de calendario de un usuario habilitado para correo.  <br/> |
|[EcpUrl-foto (POX)](ecpurl-photo-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que puede usarse para ver o cambiar la foto actual de un usuario habilitado para correo.  <br/> |
|[EcpUrl-tm (POX)](ecpurl-tm-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a una lista de todos los buzones del sitio de que un usuario habilitado para correo actualmente es un miembro.  <br/> |
|[EcpUrl-tmCreating (POX)](ecpurl-tmcreating-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para crear un nuevo buzón de sitio.  <br/> |
|[EcpUrl-tmHiding (POX)](ecpurl-tmhiding-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para cancelar la suscripción al usuario de un buzón del sitio.  <br/> |
|[EcpUrl-tmEditing (POX)](ecpurl-tmediting-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para editar un buzón de sitio existente.  <br/> |
|[EcpUrl-extinstall (POX)](ecpurl-extinstall-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que puede usarse para ver o cambiar las aplicaciones de correo instaladas actualmente en el buzón del usuario.  <br/> |
|[OOFUrl (POX)](oofurl-pox.md) <br/> |Especifica la dirección URL de la instancia del servicio de disponibilidad para un usuario habilitado para correo de procedimientos.  <br/> |
|[OABUrl (POX)](oaburl-pox.md) <br/> |Especifica la dirección URL de servidor de libreta de direcciones sin conexión configuración para una topología de Exchange.  <br/> |
|[UMUrl (POX)](umurl-pox.md) <br/> |Especifica la dirección URL de la instancia del servicio Web de mensajería unificada para un usuario habilitado para correo de procedimientos.  <br/> |
|[EwsPartnerUrl (POX)](ewspartnerurl-pox.md) <br/> |Especifica la dirección URL de la instancia de extremo procedimientos de Exchange Web Services (EWS) para un usuario habilitado para correo.  <br/> |
|[LoginName (POX)](loginname-pox.md) <br/> |Especifica el nombre de inicio de sesión del usuario.  <br/> |
|[Domain (POX)](domainrequired-pox.md) <br/> |Indica si el dominio es necesario para la autenticación.  <br/> |
|[DomainName (POX)](domainname-pox.md) <br/> |Especifica el dominio del usuario.  <br/> |
|[SPA (POX)](spa-pox.md) <br/> |Indica si se requiere autenticación de contraseña segura.  <br/> |
|[AuthPackage (POX)](authpackage-pox.md) <br/> |Especifica el esquema de autenticación que se usa al autenticarse en el equipo de Exchange 2007 que tenga instalado el rol de servidor de buzón de correo.  <br/> |
|[CertPrincipalName (POX)](certprincipalname-pox.md) <br/> |Especifica el nombre de entidad de seguridad de certificado de capa de Sockets seguros (SSL) que es necesario para conectarse a la organización de Microsoft Exchange mediante el uso de SSL.  <br/> |
|[SSL (POX)](ssl-pox.md) <br/> |Especifica si se necesita el inicio de sesión seguro.  <br/> |
|[AuthRequired (POX)](authrequired-pox.md) <br/> |Especifica si se requiere autenticación.  <br/> |
|[UsePOPAuth (POX)](usepopauth-pox.md) <br/> |Indica si la información de autenticación que se proporciona para un tipo de POP3 de cuenta también se usa para el protocolo Simple de transferencia de correo (SMTP).  <br/> |
|[SMTPLast (POX)](smtplast-pox.md) <br/> |Especifica si el servidor SMTP requiere que el correo electrónico se descargue antes de enviar correo electrónico mediante el servidor SMTP.  <br/> |
|[NetworkRequirements (POX)](networkrequirements-pox.md) <br/> |Contiene los criterios que se usan para determinar si el equipo cliente está en una red que cumpla los requisitos del proveedor de servicios de Internet para conectarse al servidor.  <br/> |
|[Libreta de direcciones (POX)](addressbook-pox.md) <br/> |Contiene las especificaciones para conectar a un cliente con el servidor de la libreta de direcciones mediante el protocolo HTTP/MAPI. Este elemento sólo está presente si el atributo de **tipo** en el elemento de **protocolo** está presente y establecido en "mapiHttp". El elemento de la **Libreta de direcciones** es aplicable a los clientes que implementan el protocolo HTTP/MAPI y Exchange Online de destino y versiones de Exchange a partir de 15.00.0847.032.  <br/> |
|[Almacenamiento de correo (POX)](mailstore-pox.md) <br/> |Contiene las especificaciones para conectar a un cliente con el buzón del usuario mediante el protocolo HTTP/MAPI. Este elemento sólo está presente si el atributo de **tipo** en el elemento de **protocolo** está presente y establecido en "mapiHttp". El elemento de **almacenamiento de correo** es aplicable a los clientes que implementan el protocolo HTTP/MAPI y Exchange Online de destino y versiones de Exchange a partir de 15.00.0847.032.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Cuenta (POX)](account-pox.md) <br/> |Especifica la configuración de cuenta para el usuario.  <br/> |
   
## <a name="remarks"></a>Comentarios

El elemento de **protocolo** está presente en una respuesta que tiene un valor de [Acción (POX)](action-pox.md) es igual a la **configuración**.
  
## <a name="see-also"></a>Vea también



[Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

