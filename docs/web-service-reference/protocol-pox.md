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
description: El elemento Protocol contiene las especificaciones para conectar un cliente al equipo que ejecuta Exchange Server que tiene instalado el rol de servidor acceso de clientes.
ms.openlocfilehash: 6fca347f49e27958ecb16cce345387b6a2146979
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/01/2020
ms.locfileid: "44467763"
---
# <a name="protocol-pox"></a>Protocolo (POX)

El elemento **Protocol** contiene las especificaciones para conectar un cliente al equipo que ejecuta Exchange Server que tiene instalado el rol de servidor acceso de clientes. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|Tipo  <br/> |Indica el tipo de protocolo descrito por este elemento **Protocol** . El único valor válido para este atributo es "mapiHttp". Este atributo solo está presente si la solicitud de detección automática que corresponde a esta respuesta [incluye un encabezado X-MapiHttpCapability](pox-autodiscover-request-for-exchange.md). Este atributo es aplicable a los clientes que implementan el protocolo MAPI/HTTP y tienen como objetivo Exchange Online, Exchange online como parte de Office 365 o versiones locales de Exchange que comienzan con la compilación 15.00.0847.032 (Exchange Server 2013 SP1).  <br/> |
|Versión  <br/> |Indica la versión del protocolo descrito por este elemento **Protocol** . El único valor válido para este atributo es "1". Este atributo solo está presente si la solicitud de detección automática que corresponde a esta respuesta incluye un encabezado **X-MapiHttpCapability** . Este atributo es aplicable a los clientes que implementan el protocolo MAPI/HTTP y tienen como objetivo Exchange Online, Exchange online como parte de Office 365 o versiones locales de Exchange que comienzan con la compilación 15.00.0847.032 (Exchange Server 2013 SP1).  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Tipo (POX)](type-pox.md) <br/> |Identifica el tipo de cuenta de correo configurada.  <br/> |
|[Interno (POX)](internal-pox.md) <br/> |Contiene una colección de direcciones URL que puede usar un cliente para conectarse a Exchange desde dentro de la red de la organización.  <br/> |
|[Externa (POX)](external-pox.md) <br/> |Contiene una colección de direcciones URL que puede usar un cliente para conectarse a Exchange desde fuera de la red de la organización.  <br/> |
|[TTL (POX)](ttl-pox.md) <br/> |Especifica el período de vida, en horas, durante el cual la configuración sigue siendo válida.  <br/> |
|[Servidor (POX)](server-pox.md) <br/> |Especifica el nombre del servidor de correo.  <br/> |
|[ServerDN (POX)](serverdn-pox.md) <br/> |Especifica el nombre distintivo del servidor de Exchange.  <br/> |
|[ServerVersion (POX)](serverversion-pox.md) <br/> |Representa el número de versión de Exchange Server.  <br/> |
|[MdbDN (POX)](mdbdn-pox.md) <br/> |Representa el nombre distintivo de la base de datos de buzones.  <br/> |
|[PublicFolderServer (POX)](publicfolderserver-pox.md) <br/> |Contiene el nombre de dominio completo (FQDN) del servidor de carpetas públicas del usuario.  <br/> |
|[Puerto (POX)](port-pox.md) <br/> |Especifica el puerto que se usa para conectarse al almacén.  <br/> |
|[DirectoryPort (POX)](directoryport-pox.md) <br/> |Especifica el puerto que se usa para conectarse al directorio cuando se utiliza el protocolo de interfaz del proveedor de servicio de nombres (NSPI).  <br/> |
|[ReferralPort (POX)](referralport-pox.md) <br/> |Especifica el puerto que se usa para obtener una referencia a un directorio.  <br/> |
|[ASUrl (POX)](asurl-pox.md) <br/> |Especifica la dirección URL de la mejor instancia de los servicios Web de Exchange para un usuario habilitado para correo.  <br/> |
|[EwsUrl (POX)](ewsurl-pox.md) <br/> |Especifica la dirección URL de la mejor instancia de punto de conexión para los servicios web Exchange (EWS) para un usuario habilitado para correo.  <br/> |
|[EmwsUrl (POX)](emwsurl-pox.md) <br/> |Especifica la dirección URL de la mejor instancia de punto de conexión para los servicios web Exchange (EWS) para un usuario habilitado para correo.  <br/> |
|[SharingUrl (POX)](sharingurl-pox.md) <br/> |Contiene la dirección URL del servidor de uso compartido usado para compartir entre organizaciones los calendarios y los contactos.  <br/> |
|[EcpUrl (POX)](ecpurl-pox.md) <br/> |Especifica la dirección URL del panel de control de Exchange para un usuario habilitado para correo.  <br/> |
|[EcpUrl-UM (POX)](ecpurl-um-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para obtener acceso a la configuración del correo de voz para un usuario habilitado para correo.  <br/> |
|[EcpUrl-aggr (POX)](ecpurl-aggr-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a la configuración de agregación de correo electrónico para un usuario habilitado para correo.  <br/> |
|[EcpUrl-MT (POX)](ecpurl-mt-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para obtener acceso a la configuración de seguimiento de mensajes de correo electrónico para un usuario habilitado para correo.  <br/> |
|[EcpUrl-RET (POX)](ecpurl-ret-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para obtener acceso a la configuración de la etiqueta de retención para un usuario habilitado para correo.  <br/> |
|[EcpUrl-SMS (POX)](ecpurl-sms-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para obtener acceso a la configuración del servicio de mensajes cortos (SMS) para un usuario habilitado para correo.  <br/> |
|[EcpUrl-publicación (POX)](ecpurl-publish-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para obtener acceso a la configuración de publicación del calendario para un usuario habilitado para correo.  <br/> |
|[EcpUrl-Photo (POX)](ecpurl-photo-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para ver o cambiar la foto actual de un usuario habilitado para correo.  <br/> |
|[EcpUrl-TM (POX)](ecpurl-tm-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a una lista de todos los buzones de sitio de los que un usuario habilitado para correo es actualmente miembro.  <br/> |
|[EcpUrl-tmCreating (POX)](ecpurl-tmcreating-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para crear un nuevo buzón de sitio.  <br/> |
|[EcpUrl-tmHiding (POX)](ecpurl-tmhiding-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para cancelar la suscripción del usuario a un buzón del sitio.  <br/> |
|[EcpUrl-tmEditing (POX)](ecpurl-tmediting-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para editar un buzón de sitio existente.  <br/> |
|[EcpUrl-extinstall (POX)](ecpurl-extinstall-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para ver o cambiar las aplicaciones de correo actualmente instaladas en el buzón del usuario.  <br/> |
|[OOFUrl (POX)](oofurl-pox.md) <br/> |Especifica la dirección URL de la mejor instancia del servicio de disponibilidad para un usuario habilitado para correo.  <br/> |
|[OABUrl (POX)](oaburl-pox.md) <br/> |Especifica la dirección URL del servidor de configuración de la libreta de direcciones sin conexión para una topología de Exchange.  <br/> |
|[UMUrl (POX)](umurl-pox.md) <br/> |Especifica la dirección URL de la mejor instancia del servicio Web de mensajería unificada para un usuario habilitado para correo.  <br/> |
|[EwsPartnerUrl (POX)](ewspartnerurl-pox.md) <br/> |Especifica la dirección URL de la mejor instancia de punto de conexión para los servicios web Exchange (EWS) para un usuario habilitado para correo.  <br/> |
|[LoginName (POX)](loginname-pox.md) <br/> |Especifica el nombre de inicio de sesión del usuario.  <br/> |
|[DomainRequired (POX)](domainrequired-pox.md) <br/> |Indica si el dominio es necesario para la autenticación.  <br/> |
|[Nombredominio (POX)](domainname-pox.md) <br/> |Especifica el dominio del usuario.  <br/> |
|[SPA (POX)](spa-pox.md) <br/> |Indica si se requiere la autenticación de contraseña segura.  <br/> |
|[AuthPackage (POX)](authpackage-pox.md) <br/> |Especifica el esquema de autenticación que se usa al autenticar en el equipo con Exchange 2007 que tiene instalado el rol de servidor buzón de correo.  <br/> |
|[CertPrincipalName (POX)](certprincipalname-pox.md) <br/> |Especifica el nombre principal del certificado de capa de sockets seguros (SSL) que se necesita para conectarse a la organización de Microsoft Exchange mediante SSL.  <br/> |
|[SSL (POX)](ssl-pox.md) <br/> |Especifica si el inicio de sesión seguro es necesario.  <br/> |
|[AuthRequired (POX)](authrequired-pox.md) <br/> |Especifica si se requiere autenticación.  <br/> |
|[UsePOPAuth (POX)](usepopauth-pox.md) <br/> |Indica si la información de autenticación que se proporciona para un tipo de cuenta POP3 también se usa para el Protocolo simple de transferencia de correo (SMTP).  <br/> |
|[SMTPLast (POX)](smtplast-pox.md) <br/> |Especifica si el servidor SMTP requiere que se descargue el correo electrónico antes de enviar correo electrónico mediante el servidor SMTP.  <br/> |
|[NetworkRequirements (POX)](networkrequirements-pox.md) <br/> |Contiene los criterios que se usan para determinar si el equipo cliente está en una red que cumple con los requisitos del proveedor de servicios Internet para conectarse al servidor.  <br/> |
|[AddressBook (POX)](addressbook-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al servidor de libreta de direcciones mediante el protocolo MAPI/HTTP. Este elemento solo está presente si el atributo **Type** del elemento **Protocol** está presente y se establece en "mapiHttp". El elemento **AddressBook** es aplicable a los clientes que implementan el protocolo MAPI/http y tienen como objetivo Exchange Online y las versiones de Exchange que comienzan con 15.00.0847.032.  <br/> |
|[MailStore (POX)](mailstore-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al buzón de correo del usuario mediante el protocolo MAPI/HTTP. Este elemento solo está presente si el atributo **Type** del elemento **Protocol** está presente y se establece en "mapiHttp". El elemento **MailStore** se aplica a los clientes que implementan el protocolo MAPI/http y tienen como objetivo Exchange Online y las versiones de Exchange que comienzan con 15.00.0847.032.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Cuenta (POX)](account-pox.md) <br/> |Especifica la configuración de la cuenta del usuario.  <br/> |
   
## <a name="remarks"></a>Comentarios

El elemento **Protocol** está presente en una respuesta que tiene un valor de [acción (POX)](action-pox.md) que es igual a **Settings**.
  
## <a name="see-also"></a>Vea también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

