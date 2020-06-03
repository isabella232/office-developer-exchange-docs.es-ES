---
title: Operaciones de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- Exchange
api_type:
- schema
ms.assetid: cf6fd871-9a65-4f34-8557-c8c71dd7ce09
description: Busque información sobre las operaciones de EWS que están disponibles en Exchange.
localization_priority: Priority
ms.openlocfilehash: 143903d9198a7e31e876adcbbb336df34ecf01fa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526126"
---
# <a name="ews-operations-in-exchange"></a>Operaciones de EWS en Exchange

Busque información sobre las operaciones de EWS que están disponibles en Exchange.
  
Los servicios web Exchange (EWS) proporcionan muchas operaciones que permiten el acceso a la información del almacén de Exchange. En los artículos de esta sección se proporciona información acerca de la estructura general de las solicitudes, respuestas y mensajes de respuesta de error de las operaciones de EWS, así como ejemplos de XML para cada operación. Proporcionan una visión general de las estructuras de mensajes que se envían entre el cliente y el servidor. Puede usar esta información para depurar estructuras de mensajes y para buscar información sobre lo que puede hacer en una solicitud de EWS. Para obtener más información sobre lo que representa la estructura XML, vea: [elementos XML EWS en Exchange](ews-xml-elements-in-exchange.md).
  
Toda la funcionalidad de EWS está asociada con una versión del esquema. Las nuevas versiones de esquema de EWS se incluyen en las nuevas versiones de Exchange Server o Exchange Online. El elemento [RequestServerVersion](requestserverversion.md) contiene un atributo **version** que asigna la versión del servidor a la versión del esquema. En este artículo se proporciona información acerca de Cuándo se introdujo cada operación. La funcionalidad específica dentro de una operación puede requerir una versión posterior del servicio. Los esquemas con versión se implementan para que los clientes diseñados con una versión anterior de EWS funcionen con una versión más reciente de EWS. 
  
Estas operaciones pueden dirigirse al extremo de EWS que redirige el buzón de correo. Puede desplazarse al extremo de EWS usando una dirección URL similar en estructura a http:// <clientaccessserver> . com/EWS/Exchange. asmx, donde <clientaccessserver> es el servidor de acceso de cliente de Exchange que hace el servicio del buzón. Puede usar la detección automática para obtener la dirección URL del servidor de acceso de cliente que da servicio al buzón. Para obtener más información acerca de la detección automática, consulte [detección automática de Exchange](../exchange-web-services/autodiscover-for-exchange.md).
  
## <a name="ediscovery-operations"></a>operaciones de eDiscovery
<a name="bk_eDiscovery"> </a>

Las operaciones de eDiscovery proporcionan operaciones de búsqueda para las retenciones legales e identifican los datos de buzones que no se pueden indizar y devolver en los resultados de la búsqueda de detección.
  
En la siguiente tabla se enumeran las operaciones de eDiscovery.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[Operación GetDiscoverySearchConfiguration](getdiscoverysearchconfiguration-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación GetHoldOnMailboxes](getholdonmailboxes-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación GetNonIndexableItemDetails](getnonindexableitemdetails-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación GetNonIndexableItemStatistics](getnonindexableitemstatistics-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación GetSearchableMailboxes](getsearchablemailboxes-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación SearchMailboxes](searchmailboxes-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación SetHoldOnMailboxes](setholdonmailboxes-operation.md) <br/> |Exchange 2013  <br/> |
   
## <a name="exchange-mailbox-data-operations"></a>Operaciones de datos de buzones de Exchange
<a name="bk_Exchange_mailbox_data"> </a>

Las operaciones de datos de buzones de Exchange permiten a los clientes controlar y organizar elementos, carpetas y datos adjuntos, así como resolución de nombres ambiguos y expansión de la lista de distribución. Las operaciones de datos de buzones de Exchange incluyen operaciones de elemento, carpeta, datos adjuntos y utilidades.
  
En la siguiente tabla se enumeran las operaciones de datos de buzones de Exchange.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[Operación ArchiveItem](archiveitem-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación CreateItem](createitem-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación CopyItem](copyitem-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación DeleteItem](deleteitem-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación FindItem](finditem-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación GetItem](getitem-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación MarkAllItemsAsRead](markallitemsasread-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación MoveItem](moveitem-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación SendItem](senditem-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación UpdateItem](updateitem-operation.md) <br/> |Exchange 2007  <br/> |
   
En la siguiente tabla se enumeran las operaciones de carpeta de datos de buzones de Exchange.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[Operación CreateFolder](createfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación CreateFolderPath](createfolderpath-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación CreateManagedFolder](createmanagedfolder-operation.md) <br/> |Exchange 2007. Esta funcionalidad se ha deenfatizado en las versiones de Exchange a partir de Exchange 2010. Para obtener más información acerca de cómo migrar a usar etiquetas de retención y directivas para la administración de registros de mensajes, vea [migrar desde carpetas administradas](https://technet.microsoft.com/library/dd298032%28v=exchg.141%29.aspx).  <br/> |
|[Operación CopyFolder](copyfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación DeleteFolder](deletefolder-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación EmptyFolder](emptyfolder-operation.md) <br/> |Exchange 2010  <br/> |
|[Operación FindFolder](findfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación GetFolder](getfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación MoveFolder](movefolder-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación UpdateFolder](updatefolder-operation.md) <br/> |Exchange 2007  <br/> |
   
En la siguiente tabla se enumeran las operaciones de datos adjuntos del buzón de Exchange.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[Operación CreateAttachment](createattachment-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación GetAttachment](getattachment-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación DeleteAttachment](deleteattachment-operation.md) <br/> |Exchange 2007  <br/> |
   
En la siguiente tabla se enumeran las operaciones de aviso de buzón de Exchange.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[Operación GetReminders](getreminders-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación PerformReminderAction](performreminderaction-operation.md) <br/> |Exchange 2013  <br/> |
   
En la siguiente tabla se enumeran las operaciones de conversación de datos de buzones de Exchange.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[Operación ApplyConversationAction](applyconversationaction-operation.md) <br/> |Exchange 2010 Service Pack 1 (SP1)  <br/> |
|[Operación FindConversation](findconversation-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[Operación GetConversationItems](getconversationitems-operation.md) <br/> |Exchange 2013  <br/> |
   
En la siguiente tabla se enumeran las operaciones de utilidades de datos de buzones de Exchange.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[Operación ConvertId](convertid-operation.md) <br/> |Exchange 2007 Service Pack 1  <br/> |
|[Operación ExpandDL](expanddl-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación GetUserPhoto](getuserphoto-operation.md) <br/> |Exchange 2013. Esta operación tiene una implementación de SOAP y REST.  <br/> |
|[Operación MarkAsJunk](markasjunk-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación ResolveNames](resolvenames-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación GetPasswordExpirationDate](getpasswordexpirationdate-operation.md) <br/> |Exchange 2010 SP1  <br/> |
   
## <a name="availability-operations"></a>Operaciones de disponibilidad
<a name="bk_Availability"> </a>

Las operaciones de disponibilidad mejoran el calendario y la experiencia de uso compartido de disponibilidad, ya que proporcionan información más segura, actualizada y de disponibilidad enriquecida. Los datos de disponibilidad son un componente crítico de la programación de reuniones. Las operaciones de disponibilidad proporcionan una base fiable para una programación eficaz. 
  
En la siguiente tabla se enumeran las operaciones de disponibilidad.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[Operación GetUserAvailability](getuseravailability-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación GetRoomLists](getroomlists-operation.md) <br/> |Exchange 2010  <br/> |
|[Operación GetRooms](getrooms-operation.md) <br/> |Exchange 2010  <br/> |
|[Operación GetUserOofSettings](getuseroofsettings-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación SetUserOofSettings](setuseroofsettings-operation.md) <br/> |Exchange 2007  <br/> |
   
## <a name="bulk-transfer-operations"></a>Operaciones de transferencia en masa
<a name="bk_bulk_transfer"> </a>

Las operaciones de transferencia en masa permiten a los clientes transmitir y salir elementos en un buzón. 
  
En la siguiente tabla se enumeran las operaciones de transferencia masiva.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[Operación UploadItems](uploaditems-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[Operación ExportItems](exportitems-operation.md) <br/> |Exchange 2010 SP1  <br/> |
   
## <a name="delegate-management-operations"></a>Operaciones de administración de delegación
<a name="bk_delegate_management"> </a>

Las operaciones de administración de delegación permiten a los clientes agregar, obtener, actualizar y quitar delegados de sus buzones. 
  
En la siguiente tabla se enumeran las operaciones de administración de delegado.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[Operación AddDelegate](adddelegate-operation.md) <br/> |Exchange 2007 Service Pack 1 (SP1)  <br/> |
|[Operación GetDelegate](getdelegate-operation.md) <br/> |Exchange 2007 SP1  <br/> |
|[Operación UpdateDelegate](updatedelegate-operation.md) <br/> |Exchange 2007 SP1  <br/> |
|[Operación RemoveDelegate](removedelegate-operation.md) <br/> |Exchange 2007 SP1  <br/> |
   
## <a name="inbox-rules-operations"></a>Operaciones de reglas de la bandeja de entrada
<a name="bk_inbox_rules"> </a>

Las operaciones de reglas de la bandeja de entrada permiten a los clientes obtener reglas de la bandeja de entrada y actualizarlas para mensajes en el servidor. Las reglas de la bandeja de entrada son conjuntos de condiciones y acciones asociadas que permiten a los clientes organizar, clasificar y actuar automáticamente en los mensajes a medida que los mensajes se entregan a una carpeta. 
  
En la siguiente tabla se enumeran las operaciones de reglas de bandeja de entrada.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[Operación de GetInboxRules](getinboxrules-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[Operación de UpdateInboxRules](updateinboxrules-operation.md) <br/> |Exchange 2010 SP1  <br/> |
   
## <a name="mail-app-management-operations"></a>Operaciones de administración de aplicaciones de correo
<a name="bk_mail_apps"> </a>

Las operaciones de administración de aplicaciones de correo permiten administrar aplicaciones de correo para Outlook. Puede usar estas operaciones para instalar, desinstalar, deshabilitar y obtener información sobre las aplicaciones de correo que están disponibles para Outlook Web App y Outlook 2013.
  
En la siguiente tabla se enumeran las operaciones de administración de aplicaciones de correo.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[Operación DisableApp](disableapp-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación GetAppManifests](getappmanifests-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación GetAppMarketplaceUrl](getappmarketplaceurl-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación GetClientAccessToken](getclientaccesstoken-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación InstallApp](installapp-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación UninstallApp](uninstallapp-operation.md) <br/> |Exchange 2013  <br/> |
   
## <a name="mail-tips-operation"></a>Operación de sugerencias de correo
<a name="bk_mail_tips"> </a>

La operación de sugerencias de correo permite a los clientes solicitar información del servidor sobre los buzones de los destinatarios cuando un autor redacta un mensaje. En la tabla siguiente se muestra la operación de sugerencias de correo.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[Operación GetMailTips](getmailtips-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="message-tracking-operations"></a>Operaciones de seguimiento de mensajes
<a name="bk_message_tracking"> </a>

Las operaciones de seguimiento de mensajes permiten a los clientes buscar mensajes que cumplan los criterios especificados y obtener información de seguimiento detallada de cada mensaje en un informe de seguimiento de mensajes. 
  
En la siguiente tabla se enumeran las operaciones de seguimiento de mensajes.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[Operación FindMessageTrackingReport](findmessagetrackingreport-operation.md) <br/> |Exchange 2010  <br/> |
|[Operación GetMessageTrackingReport](getmessagetrackingreport-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="notification-operations"></a>Operaciones de notificación
<a name="bk_notification"> </a>

Las operaciones de notificación notifican a la aplicación cliente los eventos que están asociados a los elementos y carpetas de un buzón especificado. El modelo de suscripción se puede basar en inserción, basado en extracción o en secuencia. 
  
En la siguiente tabla se enumeran las operaciones de notificación.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[Operación GetEvents](getevents-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación GetStreamingEvents](getstreamingevents-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[Operación subscribe](subscribe-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación unsubscribe](unsubscribe-operation.md) <br/> |Exchange 2007  <br/> |
   
## <a name="persona-operations"></a>Operaciones de rol
<a name="bk_personas"> </a>

Las operaciones persona proporcionan una interfaz para buscar y obtener información sobre un contacto vinculado. En la siguiente tabla se enumeran las operaciones de roles.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[Operación FindPeople](findpeople-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación GetPersona](getpersona-operation.md) <br/> |Exchange 2013  <br/> |
   
## <a name="retention-policy-operation"></a>Operación de directiva de retención
<a name="bk_retention_policy"> </a>

La operación Directiva de retención proporciona una lista de todas las etiquetas de retención vinculadas a la Directiva de retención de un usuario. 
  
En la siguiente tabla se muestra la operación Directiva de retención.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[Operación GetUserRetentionPolicyTags](getuserretentionpolicytags-operation.md) <br/> |Exchange 2013  <br/> |
   
## <a name="service-configuration-operation"></a>Operación de configuración del servicio
<a name="bk_service_config"> </a>

La operación de configuración del servicio permite a los clientes obtener información de configuración para los servicios de mensajería unificada, reglas de protección, sugerencias de directivas y sugerencias de correo. 
  
En la tabla siguiente se muestra la operación de configuración del servicio.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[Operación GetServiceConfiguration](getserviceconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="sharing-operations"></a>Operaciones de uso compartido
<a name="bk_sharing"> </a>

Las operaciones de uso compartido permiten que los clientes compartan datos de contactos y datos de calendario. 
  
En la siguiente tabla se enumeran las operaciones de uso compartido.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[CreateItem (AcceptSharingInvitation)](createitem-acceptsharinginvitation.md) <br/> |Exchange 2010. Aunque la operación **CreateItem** es aplicable a todas las versiones de EWS, el objeto de respuesta **AcceptSharingInvitation** solo se aplica a EWS en versiones de Exchange a partir de Exchange 2010.  <br/> |
|[Operación GetSharingFolder](getsharingfolder-operation.md) <br/> |Exchange 2010  <br/> |
|[Operación GetSharingMetadata](getsharingmetadata-operation.md) <br/> |Exchange 2010  <br/> |
|[Operación RefreshSharingFolder](refreshsharingfolder-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="synchronization-operations"></a>Operaciones de sincronización
<a name="bk_synchronization"> </a>

Las operaciones de sincronización proporcionan una copia en caché sincronizada unidireccional de las carpetas y los elementos de un usuario. 
  
En la siguiente tabla se enumeran las operaciones de sincronización.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[Operación SyncFolderHierarchy](syncfolderhierarchy-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación SyncFolderItems](syncfolderitems-operation.md) <br/> |Exchange 2007  <br/> |
   
## <a name="time-zone-operation"></a>Funcionamiento de la zona horaria
<a name="bk_timezone"> </a>

La operación de zona horaria permite a los clientes obtener una lista de definiciones de zona horaria compatibles con el servidor. 
  
En la siguiente tabla se enumera la operación de zona horaria.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[Operación GetServerTimeZones](getservertimezones-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="unified-messaging-operations"></a>Operaciones de mensajería unificada
<a name="bk_um"> </a>

Las operaciones de mensajería unificada permiten a los clientes leer información sobre las propiedades de mensajería unificada y reproducir los mensajes de correo de voz a través del teléfono. 
  
En la siguiente tabla se enumeran las operaciones de mensajería unificada.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[Operación DisconnectPhoneCall](disconnectphonecall-operation.md) <br/> |Exchange 2010  <br/> |
|[Operación GetPhoneCallInformation](getphonecallinformation-operation.md) <br/> |Exchange 2010  <br/> |
|[Operación reproducir (EWS)](playonphone-operation-ews.md) <br/> |Exchange 2010  <br/> |
   
Use la [operación GetServiceConfiguration](getserviceconfiguration-operation.md) para obtener la información de configuración de mensajería unificada de un buzón. Usar el servicio Web de mensajería unificada para las aplicaciones de mensajería unificada destinadas a Exchange 2007. Para obtener más información, consulte [Unified Messaging Web Service Reference for Exchange](unified-messaging-web-service-reference-for-exchange.md).
  
## <a name="unified-contact-store-operations"></a>Operaciones del almacén de contactos unificado
<a name="bk_ucs"> </a>

El almacén de contactos unificados proporciona una experiencia de contacto coherente entre los productos de Office y actúa como un punto de integración para que las aplicaciones de terceros usen el mismo almacén de contactos. Permite a los usuarios y las aplicaciones almacenar, administrar y tener acceso a la información de contacto y hacer que esté disponible globalmente entre Lync, Exchange 2013, Outlook, Outlook Web App y cualquier otra aplicación que implemente el acceso al almacén de contactos unificado. Exchange es el almacén de contenido para la experiencia del almacén de contactos unificado.
  
En la siguiente tabla se enumeran las operaciones de almacenamiento de contactos unificadas.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[Operación AddNewImContactToGroup](addnewimcontacttogroup-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación AddImContactToGroup](addimcontacttogroup-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación AddImGroup](addimgroup-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación AddNewTelUriContactToGroup](addnewteluricontacttogroup-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación AddDistributionGroupToImList](adddistributiongrouptoimlist-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación GetImItemList](getimitemlist-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación GetImItems](getimitems-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación RemoveContactFromImList](removecontactfromimlist-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación RemoveImContactFromGroup](removeimcontactfromgroup-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación RemoveDistributionGroupFromImList](removedistributiongroupfromimlist-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación RemoveImGroup](removeimgroup-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación SetImGroup](setimgroup-operation.md) <br/> |Exchange 2013  <br/> |
   
## <a name="user-configuration-operations"></a>Operaciones de configuración de usuario
<a name="bk_user_config"> </a>

Las operaciones de configuración de usuario permiten a los clientes crear, eliminar, obtener y actualizar la información de configuración de usuario. 
  
En la siguiente tabla se enumeran las operaciones de configuración de usuario.
  
|**Nombre de operación**|**Introducido en**|
|:-----|:-----|
|[Operación CreateUserConfiguration](createuserconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
|[Operación DeleteUserConfiguration](deleteuserconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
|[Operación GetUserConfiguration](getuserconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
|[Operación UpdateUserConfiguration](updateuserconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="see-also"></a>Vea también

- [Explorar la API administrada de EWS, EWS y servicios web en Exchange](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [Empezar a usar los servicios web de Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
- [Detección automática en Exchange](../exchange-web-services/autodiscover-for-exchange.md)
    

