---
title: Protocol (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: f77e4d66-6fdd-4999-9339-f7d7f9c86f44
description: El elemento Protocol contiene las especificaciones para conectar un cliente al equipo que ejecuta Exchange Server que tiene instalado el rol de servidor Acceso de cliente.
ms.openlocfilehash: 4f308951c74612936755e6d4c16620e38277aecb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516407"
---
# <a name="protocol-pox"></a>Protocol (POX)

El **elemento Protocol** contiene las especificaciones para conectar un cliente al equipo que ejecuta Exchange Server que tiene instalado el rol de servidor Acceso de cliente. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
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
|Tipo  <br/> |Indica el tipo de protocolo descrito por este **elemento Protocol.** El único valor válido para este atributo es "mapiHttp". Este atributo solo está presente si la solicitud de detección automática que corresponde a esta respuesta incluía un encabezado [X-MapiHttpCapability](pox-autodiscover-request-for-exchange.md). Este atributo se aplica a los clientes que implementan el protocolo MAPI/HTTP y el Exchange Online de destino, Exchange Online como parte de Office 365 o versiones locales de Exchange a partir de la compilación 15.00.0847.032 (Exchange Server 2013 SP1).  <br/> |
|Versión  <br/> |Indica la versión del protocolo descrita por este **elemento Protocol.** El único valor válido para este atributo es "1". Este atributo solo está presente si la solicitud de detección automática que corresponde a esta respuesta incluía un **encabezado X-MapiHttpCapability.** Este atributo se aplica a los clientes que implementan el protocolo MAPI/HTTP y el Exchange Online de destino, Exchange Online como parte de Office 365 o versiones locales de Exchange a partir de la compilación 15.00.0847.032 (Exchange Server 2013 SP1).  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Type (POX)](type-pox.md) <br/> |Identifica el tipo de la cuenta de correo configurada.  <br/> |
|[Internal (POX)](internal-pox.md) <br/> |Contiene una colección de direcciones URL que un cliente puede usar para conectarse a Exchange desde dentro de la red de la organización.  <br/> |
|[External (POX)](external-pox.md) <br/> |Contiene una colección de direcciones URL que un cliente puede usar para conectarse a Exchange desde fuera de la red de la organización.  <br/> |
|[TTL (POX)](ttl-pox.md) <br/> |Especifica el tiempo de vida, en horas, durante el cual la configuración permanece válida.  <br/> |
|[Server (POX)](server-pox.md) <br/> |Especifica el nombre del servidor de correo.  <br/> |
|[ServerDN (POX)](serverdn-pox.md) <br/> |Especifica el Exchange Server nombre distintivo.  <br/> |
|[ServerVersion (POX)](serverversion-pox.md) <br/> |Representa el número Exchange Server versión.  <br/> |
|[MdbDN (POX)](mdbdn-pox.md) <br/> |Representa el nombre distintivo de la base de datos de buzones de correo.  <br/> |
|[PublicFolderServer (POX)](publicfolderserver-pox.md) <br/> |Contiene el nombre de dominio completo (FQDN) del servidor de carpetas públicas para el usuario.  <br/> |
|[Port (POX)](port-pox.md) <br/> |Especifica el puerto que se usa para conectarse al almacén.  <br/> |
|[DirectoryPort (POX)](directoryport-pox.md) <br/> |Especifica el puerto que se usa para conectarse al directorio cuando se usa el protocolo de interfaz de proveedor de servicios de nombres (NSPI).  <br/> |
|[ReferralPort (POX)](referralport-pox.md) <br/> |Especifica el puerto que se usa para obtener una referencia a un directorio.  <br/> |
|[ASUrl (POX)](asurl-pox.md) <br/> |Especifica la dirección URL de la mejor instancia de Exchange Web Services para un usuario habilitado para correo.  <br/> |
|[EwsUrl (POX)](ewsurl-pox.md) <br/> |Especifica la dirección URL de la mejor instancia de extremo para Exchange Web Services (EWS) para un usuario habilitado para correo.  <br/> |
|[EmwsUrl (POX)](emwsurl-pox.md) <br/> |Especifica la dirección URL de la mejor instancia de extremo para Exchange Web Services (EWS) para un usuario habilitado para correo.  <br/> |
|[SharingUrl (POX)](sharingurl-pox.md) <br/> |Contiene la dirección URL del servidor de uso compartido usado para el uso compartido entre organizaciones de calendarios y contactos.  <br/> |
|[EcpUrl (POX)](ecpurl-pox.md) <br/> |Especifica la dirección URL del panel de control Exchange para un usuario habilitado para correo.  <br/> |
|[EcpUrl-um (POX)](ecpurl-um-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para obtener acceso a la configuración de correo de voz de un usuario habilitado para correo.  <br/> |
|[EcpUrl-aggr (POX)](ecpurl-aggr-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para obtener acceso a la configuración de agregación de correo electrónico de un usuario habilitado para correo.  <br/> |
|[EcpUrl-mt (POX)](ecpurl-mt-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para obtener acceso a la configuración de seguimiento de mensajes de correo electrónico de un usuario habilitado para correo.  <br/> |
|[EcpUrl-ret (POX)](ecpurl-ret-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para obtener acceso a la configuración de etiquetas de retención de un usuario habilitado para correo.  <br/> |
|[EcpUrl-sms (POX)](ecpurl-sms-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a la configuración del servicio de mensajes cortos (SMS) para un usuario habilitado para correo.  <br/> |
|[EcpUrl-publish (POX)](ecpurl-publish-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para obtener acceso a la configuración de publicación de calendario para un usuario habilitado para correo.  <br/> |
|[EcpUrl-photo (POX)](ecpurl-photo-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para ver o cambiar la foto actual de un usuario habilitado para correo.  <br/> |
|[EcpUrl-tm (POX)](ecpurl-tm-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para obtener acceso a una lista de todos los buzones de sitio de los que un usuario habilitado para correo es actualmente miembro.  <br/> |
|[EcpUrl-tmCreating (POX)](ecpurl-tmcreating-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para crear un nuevo buzón de sitio.  <br/> |
|[EcpUrl-tmHiding (POX)](ecpurl-tmhiding-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para cancelar la suscripción al usuario de un buzón de sitio.  <br/> |
|[EcpUrl-tmEditing (POX)](ecpurl-tmediting-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para editar un buzón de sitio existente.  <br/> |
|[EcpUrl-extinstall (POX)](ecpurl-extinstall-pox.md) <br/> |Especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para ver o cambiar las aplicaciones de correo instaladas actualmente en el buzón del usuario.  <br/> |
|[OOFUrl (POX)](oofurl-pox.md) <br/> |Especifica la dirección URL de la mejor instancia del servicio de disponibilidad para un usuario habilitado para correo.  <br/> |
|[OABUrl (POX)](oaburl-pox.md) <br/> |Especifica la dirección URL del servidor de configuración de libreta de direcciones sin conexión para una Exchange topología.  <br/> |
|[UMUrl (POX)](umurl-pox.md) <br/> |Especifica la dirección URL de la mejor instancia del servicio web de mensajería unificada para un usuario habilitado para correo.  <br/> |
|[EwsPartnerUrl (POX)](ewspartnerurl-pox.md) <br/> |Especifica la dirección URL de la mejor instancia de extremo para Exchange Web Services (EWS) para un usuario habilitado para correo.  <br/> |
|[LoginName (POX)](loginname-pox.md) <br/> |Especifica el nombre de inicio de sesión del usuario.  <br/> |
|[DomainRequired (POX)](domainrequired-pox.md) <br/> |Indica si el dominio es necesario para la autenticación.  <br/> |
|[DomainName (POX)](domainname-pox.md) <br/> |Especifica el dominio del usuario.  <br/> |
|[SPA (POX)](spa-pox.md) <br/> |Indica si es necesaria la autenticación de contraseña segura.  <br/> |
|[AuthPackage (POX)](authpackage-pox.md) <br/> |Especifica el esquema de autenticación que se usa al autenticarse en el equipo Exchange 2007 que tiene instalado el rol de servidor Buzón de correo.  <br/> |
|[CertPrincipalName (POX)](certprincipalname-pox.md) <br/> |Especifica el nombre de entidad de seguridad del certificado capa de sockets seguros (SSL) necesario para conectarse a la organización de Microsoft Exchange mediante SSL.  <br/> |
|[SSL (POX)](ssl-pox.md) <br/> |Especifica si se necesita un inicio de sesión seguro.  <br/> |
|[AuthRequired (POX)](authrequired-pox.md) <br/> |Especifica si se requiere autenticación.  <br/> |
|[UsePOPAuth (POX)](usepopauth-pox.md) <br/> |Indica si la información de autenticación que se proporciona para un tipo de cuenta POP3 también se usa para el Protocolo simple de transferencia de correo (SMTP).  <br/> |
|[SMTPLast (POX)](smtplast-pox.md) <br/> |Especifica si el servidor SMTP requiere que el correo electrónico se descargue antes de enviar correo electrónico mediante el servidor SMTP.  <br/> |
|[NetworkRequirements (POX)](networkrequirements-pox.md) <br/> |Contiene los criterios que se usan para determinar si el equipo cliente está en una red que cumple los requisitos del proveedor de servicios de Internet para conectarse al servidor.  <br/> |
|[AddressBook (POX)](addressbook-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al servidor de libreta de direcciones mediante el protocolo MAPI/HTTP. Este elemento solo está presente si el atributo **Type** del **elemento Protocol** está presente y se establece en "mapiHttp". El **elemento AddressBook** se aplica a los clientes que implementan el protocolo MAPI/HTTP y las Exchange Online de destino y las versiones de Exchange a partir de la 15.00.0847.032.  <br/> |
|[MailStore (POX)](mailstore-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al buzón del usuario mediante el protocolo MAPI/HTTP. Este elemento solo está presente si el atributo **Type** del **elemento Protocol** está presente y se establece en "mapiHttp". El **elemento MailStore** se aplica a los clientes que implementan el protocolo MAPI/HTTP y las Exchange Online de destino y las versiones de Exchange a partir de la 15.00.0847.032.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Account (POX)](account-pox.md) <br/> |Especifica la configuración de la cuenta para el usuario.  <br/> |
   
## <a name="remarks"></a>Comentarios

El **elemento Protocol** está presente en una respuesta que tiene un valor action [(POX)](action-pox.md) que es igual a la **configuración**.
  
## <a name="see-also"></a>Ver también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

