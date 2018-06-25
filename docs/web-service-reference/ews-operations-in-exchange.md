---
title: Operaciones de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Exchange
api_type:
- schema
ms.assetid: cf6fd871-9a65-4f34-8557-c8c71dd7ce09
description: Busque información sobre las operaciones de EWS que están disponibles en Exchange.
ms.openlocfilehash: c56c3be746138cec251836fcb61ee3738d168869
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764482"
---
# <a name="ews-operations-in-exchange"></a>Operaciones de EWS en Exchange

Busque información sobre las operaciones de EWS que están disponibles en Exchange.
  
Servicios Web de Exchange (EWS) proporciona muchas operaciones que le permiten obtener acceso a información desde el almacén de Exchange. Los artículos de esta sección proporcionan información acerca de la estructura general de las solicitudes, respuestas y los mensajes de respuesta de error para las operaciones de EWS, así como ejemplos XML para cada operación. Proporcionan una visión general de las estructuras de mensaje que se envían entre el cliente y el servidor. Puede usar esta información para depurar las estructuras de mensaje y para obtener información acerca de qué se puede hacer en una solicitud de EWS. Para obtener más información acerca de qué que represente de estructura XML, vea - [elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md).
  
Toda la funcionalidad de EWS está asociada con una versión del esquema. Nuevas versiones de esquema EWS se introdujeron en nuevas versiones de Exchange Server o Exchange Online. El elemento [RequestServerVersion](requestserverversion.md) contiene un atributo de **versión** que se asigna la versión del servidor a la versión del esquema. En este artículo se proporciona información acerca de cuándo se introdujo cada operación. Funciones específicas dentro de una operación podrían requerir una versión posterior del servicio. Para que los clientes que se han diseñado con una versión anterior de EWS funcionará con una versión más reciente de EWS, se implementan los esquemas entre versiones. 
  
Estas operaciones pueden dirigir el extremo EWS que los servicios de su buzón de correo. Puede examinar el extremo EWS mediante el uso de una dirección URL que es una estructura similar a http://<clientaccessserver>.com/ews/exchange.asmx, donde <clientaccessserver> es el servidor de acceso de cliente de Exchange que los servicios de su buzón de correo. Puede usar la detección automática para obtener la dirección URL para el servidor de acceso de cliente que los servicios de su buzón de correo. Para obtener más información acerca de la detección automática, vea [detección automática de Exchange](../exchange-web-services/autodiscover-for-exchange.md).
  
## <a name="ediscovery-operations"></a>operaciones de exhibición de documentos electrónicos
<a name="bk_eDiscovery"> </a>

Las operaciones de exhibición de documentos electrónicos proporcionan operaciones de búsqueda para las suspensiones legales e identifican los datos de buzón de correo que no se pueden indizar y devueltos en los resultados de búsqueda de detección.
  
En la siguiente tabla se enumera las operaciones de exhibición de documentos electrónicos.
  
|**Nombre de la operación**|**Introducido en**|
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

Las operaciones de datos de buzón de correo de Exchange que los clientes puedan administrar y organizar los elementos, carpetas y los datos adjuntos, así como la expansión de listas de distribución y la resolución de nombre ambiguo. Operaciones de datos de buzones de Exchange incluyen el elemento, carpeta, datos adjuntos y las operaciones de utilidades.
  
En la siguiente tabla se enumera las operaciones de datos de buzón de correo de Exchange.
  
|**Nombre de la operación**|**Introducido en**|
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
   
En la siguiente tabla se enumera las operaciones de carpeta de datos de buzón de correo de Exchange.
  
|**Nombre de la operación**|**Introducido en**|
|:-----|:-----|
|[Operación CreateFolder](createfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación CreateFolderPath](createfolderpath-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación CreateManagedFolder](createmanagedfolder-operation.md) <br/> |Exchange 2007. Esta funcionalidad ha sido deemphasized en las versiones de Exchange a partir de Exchange 2010. Para obtener más información acerca de cómo migrar al uso de las etiquetas de retención y directivas para la administración de registros de mensajería, vea [migración de carpetas administradas](http://technet.microsoft.com/en-us/library/dd298032%28v=exchg.141%29.aspx).  <br/> |
|[Operación CopyFolder](copyfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación DeleteFolder](deletefolder-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación EmptyFolder](emptyfolder-operation.md) <br/> |Exchange 2010  <br/> |
|[Operación FindFolder](findfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación GetFolder](getfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación MoveFolder](movefolder-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación UpdateFolder](updatefolder-operation.md) <br/> |Exchange 2007  <br/> |
   
En la siguiente tabla se enumera las operaciones de datos adjuntos de datos de buzón de correo de Exchange.
  
|**Nombre de la operación**|**Introducido en**|
|:-----|:-----|
|[Operación CreateAttachment](createattachment-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación GetAttachment](getattachment-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación DeleteAttachment](deleteattachment-operation.md) <br/> |Exchange 2007  <br/> |
   
En la siguiente tabla se enumera las operaciones de aviso de buzón de correo de Exchange.
  
|**Nombre de la operación**|**Introducido en**|
|:-----|:-----|
|[Operación GetReminders](getreminders-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación PerformReminderAction](performreminderaction-operation.md) <br/> |Exchange 2013  <br/> |
   
En la siguiente tabla se enumera las operaciones de conversación de datos de buzón de correo de Exchange.
  
|**Nombre de la operación**|**Introducido en**|
|:-----|:-----|
|[Operación ApplyConversationAction](applyconversationaction-operation.md) <br/> |Service Pack 1 (SP1) de Exchange 2010  <br/> |
|[Operación de FindConversation](findconversation-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[Operación GetConversationItems](getconversationitems-operation.md) <br/> |Exchange 2013  <br/> |
   
En la siguiente tabla se enumera las operaciones de utilidades de datos de buzón de correo de Exchange.
  
|**Nombre de la operación**|**Introducido en**|
|:-----|:-----|
|[Operación ConvertId](convertid-operation.md) <br/> |Service Pack 1 de Exchange 2007  <br/> |
|[Operación de ExpandDL](expanddl-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación GetUserPhoto](getuserphoto-operation.md) <br/> |Exchange 2013. Esta operación tiene un REST y una implementación de SOAP.  <br/> |
|[MarkAsJunk Operation](markasjunk-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación ResolveNames](resolvenames-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación GetPasswordExpirationDate](getpasswordexpirationdate-operation.md) <br/> |Exchange 2010 SP1  <br/> |
   
## <a name="availability-operations"></a>Operaciones de disponibilidad
<a name="bk_Availability"> </a>

Las operaciones de disponibilidad mejoran el calendario y la disponibilidad uso compartido de experiencia proporcionando más segura, actualizada y enriquecida información de disponibilidad. Datos de disponibilidad están un componente esencial de la programación de reuniones. Las operaciones de disponibilidad proporcionan una base confiable para programación eficaz. 
  
En la siguiente tabla se enumera las operaciones de disponibilidad.
  
|**Nombre de la operación**|**Introducido en**|
|:-----|:-----|
|[Operación GetUserAvailability](getuseravailability-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación GetRoomLists](getroomlists-operation.md) <br/> |Exchange 2010  <br/> |
|[Operación GetRooms](getrooms-operation.md) <br/> |Exchange 2010  <br/> |
|[Operación GetUserOofSettings](getuseroofsettings-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación SetUserOofSettings](setuseroofsettings-operation.md) <br/> |Exchange 2007  <br/> |
   
## <a name="bulk-transfer-operations"></a>Operaciones de transferencia masiva
<a name="bk_bulk_transfer"> </a>

Las operaciones de transferencia masiva permiten a los clientes a los elementos de la secuencia y desconectarse de un buzón de correo. 
  
En la siguiente tabla se enumera las operaciones de transferencia masiva.
  
|**Nombre de la operación**|**Introducido en**|
|:-----|:-----|
|[Operación UploadItems](uploaditems-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[Operación ExportItems](exportitems-operation.md) <br/> |Exchange 2010 SP1  <br/> |
   
## <a name="delegate-management-operations"></a>Delegar las operaciones de administración
<a name="bk_delegate_management"> </a>

Las operaciones de administración de delegado que los clientes puedan agregar, obtener, actualizar y quitar delegados de sus buzones de correo. 
  
En la siguiente tabla se enumera las operaciones de administración de delegado.
  
|**Nombre de la operación**|**Introducido en**|
|:-----|:-----|
|[Operación AddDelegate](adddelegate-operation.md) <br/> |Service Pack 1 (SP1) de Exchange 2007  <br/> |
|[Operación GetDelegate](getdelegate-operation.md) <br/> |Exchange 2007 SP1  <br/> |
|[Operación UpdateDelegate](updatedelegate-operation.md) <br/> |Exchange 2007 SP1  <br/> |
|[Operación RemoveDelegate](removedelegate-operation.md) <br/> |Exchange 2007 SP1  <br/> |
   
## <a name="inbox-rules-operations"></a>Operaciones de reglas de bandeja de entrada
<a name="bk_inbox_rules"> </a>

Las operaciones de las reglas de bandeja de entrada que los clientes puedan obtener las reglas de bandeja de entrada y actualizarlos para los mensajes en el servidor. Las reglas de bandeja de entrada son conjuntos de condiciones y acciones asociadas que les permiten a los clientes puedan organizar, clasificar y actuar sobre los mensajes, como los mensajes se coloquen en una carpeta automáticamente. 
  
En la siguiente tabla se enumera las operaciones de las reglas de bandeja de entrada.
  
|**Nombre de la operación**|**Introducido en**|
|:-----|:-----|
|[Operación de GetInboxRules](getinboxrules-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[Operación de UpdateInboxRules](updateinboxrules-operation.md) <br/> |Exchange 2010 SP1  <br/> |
   
## <a name="mail-app-management-operations"></a>Las operaciones de administración de la aplicación de correo
<a name="bk_mail_apps"> </a>

Las operaciones de administración de la aplicación de correo permiten administrar las aplicaciones de correo para Outlook. Puede usar estas operaciones para instalar, desinstalar, deshabilitar y obtener información acerca de las aplicaciones de correo que están disponibles para Outlook Web App y Outlook 2013.
  
En la siguiente tabla se enumera las operaciones de administración de la aplicación de correo.
  
|**Nombre de la operación**|**Introducido en**|
|:-----|:-----|
|[Operación DisableApp](disableapp-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación GetAppManifests](getappmanifests-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación GetAppMarketplaceUrl](getappmarketplaceurl-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación GetClientAccessToken](getclientaccesstoken-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación InstallApp](installapp-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación UninstallApp](uninstallapp-operation.md) <br/> |Exchange 2013  <br/> |
   
## <a name="mail-tips-operation"></a>Operación de sugerencias de correo
<a name="bk_mail_tips"> </a>

La operación de sugerencias de correo permite a los clientes información de la solicitud desde el servidor acerca de los buzones de destinatarios cuando un autor redacta un mensaje. En la siguiente tabla se enumera la operación de sugerencias de correo.
  
|**Nombre de la operación**|**Introducido en**|
|:-----|:-----|
|[Operación GetMailTips](getmailtips-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="message-tracking-operations"></a>Operaciones de seguimiento de mensajes
<a name="bk_message_tracking"> </a>

Las operaciones de seguimiento de mensajes permiten a los clientes para buscar mensajes que cumplen los criterios especificados y para obtener información de seguimiento detallada acerca de cada mensaje en un informe de seguimiento de mensajes. 
  
En la siguiente tabla se enumera las operaciones de seguimiento de mensajes.
  
|**Nombre de la operación**|**Introducido en**|
|:-----|:-----|
|[Operación FindMessageTrackingReport](findmessagetrackingreport-operation.md) <br/> |Exchange 2010  <br/> |
|[Operación GetMessageTrackingReport](getmessagetrackingreport-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="notification-operations"></a>Operaciones de notificación
<a name="bk_notification"> </a>

Las operaciones de notificación notificar a la aplicación cliente de eventos que están asociados con los elementos y carpetas de un buzón especificado. El modelo de suscripción puede ser basada en inserción, extracción o basada en transmisión por secuencias. 
  
En la siguiente tabla se enumera las operaciones de notificación.
  
|**Nombre de la operación**|**Introducido en**|
|:-----|:-----|
|[Operación GetEvents](getevents-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación GetStreamingEvents](getstreamingevents-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[Operación de suscripción](subscribe-operation.md) <br/> |Exchange 2007  <br/> |
|[Cancelar la operación de suscripción](unsubscribe-operation.md) <br/> |Exchange 2007  <br/> |
   
## <a name="persona-operations"></a>Operaciones de rol
<a name="bk_personas"> </a>

Las operaciones de rol proporcionan una interfaz para buscar y obtener información acerca de un contacto vinculado. En la siguiente tabla se enumera las operaciones de rol.
  
|**Nombre de la operación**|**Introducido en**|
|:-----|:-----|
|[Operación FindPeople](findpeople-operation.md) <br/> |Exchange 2013  <br/> |
|[Operación GetPersona](getpersona-operation.md) <br/> |Exchange 2013  <br/> |
   
## <a name="retention-policy-operation"></a>Operación de la directiva de retención
<a name="bk_retention_policy"> </a>

La operación de la directiva de retención proporciona una lista de todas las etiquetas de retención que están vinculados a la directiva de retención de un usuario. 
  
En la siguiente tabla se enumera la operación de la directiva de retención.
  
|**Nombre de la operación**|**Introducido en**|
|:-----|:-----|
|[Operación GetUserRetentionPolicyTags](getuserretentionpolicytags-operation.md) <br/> |Exchange 2013  <br/> |
   
## <a name="service-configuration-operation"></a>Operación de configuración del servicio
<a name="bk_service_config"> </a>

La operación de configuración de servicio permite a los clientes obtener información de configuración de los servicios de mensajería unificada, las reglas de protección, sugerencias de directivas y sugerencias de correo. 
  
En la siguiente tabla se enumera la operación de configuración de servicio.
  
|**Nombre de la operación**|**Introducido en**|
|:-----|:-----|
|[Operación GetServiceConfiguration](getserviceconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="sharing-operations"></a>Uso compartido de las operaciones
<a name="bk_sharing"> </a>

Las operaciones de uso compartidas que los clientes puedan compartir datos de calendario y datos de los contactos. 
  
En la siguiente tabla se enumera las operaciones de uso compartidas.
  
|**Nombre de la operación**|**Introducido en**|
|:-----|:-----|
|[CreateItem (AcceptSharingInvitation)](createitem-acceptsharinginvitation.md) <br/> |Exchange 2010. Aunque la operación **CreateItem** es aplicable a todas las versiones de EWS, el objeto de respuesta **AcceptSharingInvitation** sólo es aplicable a EWS en las versiones de Exchange a partir de Exchange 2010.  <br/> |
|[Operación GetSharingFolder](getsharingfolder-operation.md) <br/> |Exchange 2010  <br/> |
|[Operación GetSharingMetadata](getsharingmetadata-operation.md) <br/> |Exchange 2010  <br/> |
|[Operación RefreshSharingFolder](refreshsharingfolder-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="synchronization-operations"></a>Operaciones de sincronización
<a name="bk_synchronization"> </a>

Las operaciones de sincronización proporcionan una copia en caché sincronizada unidireccional de carpetas y elementos de un usuario. 
  
En la siguiente tabla se enumera las operaciones de sincronización.
  
|**Nombre de la operación**|**Introducido en**|
|:-----|:-----|
|[Operación SyncFolderHierarchy](syncfolderhierarchy-operation.md) <br/> |Exchange 2007  <br/> |
|[Operación SyncFolderItems](syncfolderitems-operation.md) <br/> |Exchange 2007  <br/> |
   
## <a name="time-zone-operation"></a>Operación de zona horaria
<a name="bk_timezone"> </a>

La operación de zona horaria permite a los clientes obtener una lista de las definiciones de zona horaria que son compatibles con el servidor. 
  
En la siguiente tabla se enumera la operación de zona horaria.
  
|**Nombre de la operación**|**Introducido en**|
|:-----|:-----|
|[Operación GetServerTimeZones](getservertimezones-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="unified-messaging-operations"></a>Operaciones de mensajería unificadas
<a name="bk_um"> </a>

Las operaciones de mensajería unificada permiten a los clientes para leer información acerca de las propiedades de mensajería unificada y para reproducir los mensajes de correo de voz a través del teléfono. 
  
En la siguiente tabla se enumera las operaciones de mensajería unificada.
  
|**Nombre de la operación**|**Introducido en**|
|:-----|:-----|
|[Operación DisconnectPhoneCall](disconnectphonecall-operation.md) <br/> |Exchange 2010  <br/> |
|[Operación GetPhoneCallInformation](getphonecallinformation-operation.md) <br/> |Exchange 2010  <br/> |
|[Operación PlayOnPhone (EWS)](playonphone-operation-ews.md) <br/> |Exchange 2010  <br/> |
   
Use la [operación de GetServiceConfiguration](getserviceconfiguration-operation.md) para obtener la información de configuración de mensajería unificada para un buzón de correo. Usar el servicio web de mensajería unificada para aplicaciones de mensajería unificada que estén destinados a Exchange 2007. Para obtener más información, vea la [referencia de servicio de web mensajería unificada de Exchange](unified-messaging-web-service-reference-for-exchange.md).
  
## <a name="unified-contact-store-operations"></a>Operaciones de almacén de contactos unificadas
<a name="bk_ucs"> </a>

El almacén de contactos unificados proporciona una experiencia coherente de contacto a través de productos de Office y actúa como un punto de integración de aplicaciones de terceros para usar el mismo almacén de contactos. Permite a los usuarios y las aplicaciones almacenar, administrar y tener acceso a información de contacto y hacer que esté disponible globalmente entre Lync, Exchange 2013, Outlook, Outlook Web App y cualquier otra aplicación que implementa el acceso para el almacén de contactos unificados. Exchange es el almacén de contenido para la experiencia del almacén de contactos unificados.
  
En la siguiente tabla se enumera las operaciones de almacén de contactos unificados.
  
|**Nombre de la operación**|**Introducido en**|
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

Las operaciones de configuración de usuario que los clientes puedan crear, eliminar, obtener y actualización la información de configuración de usuario. 
  
En la siguiente tabla se enumera las operaciones de configuración de usuario.
  
|**Nombre de la operación**|**Introducido en**|
|:-----|:-----|
|[Operación CreateUserConfiguration](createuserconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
|[Operación DeleteUserConfiguration](deleteuserconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
|[Operación GetUserConfiguration](getuserconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
|[Operación UpdateUserConfiguration](updateuserconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="see-also"></a>Vea también

- [Explore la API administrada de EWS, EWS y servicios web de Exchange](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [Empezar a utilizar servicios web de Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
- [Detección automática de Exchange](../exchange-web-services/autodiscover-for-exchange.md)
    

