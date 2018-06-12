---
title: Objeto postItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PostItem
api_type:
- schema
ms.assetid: 7727ed84-9591-4a1c-bb04-12129926499b
description: El elemento PostItem representa un elemento para exponer en el almacén de Exchange.
ms.openlocfilehash: 3fb6d6cfe334999c93ca0238547dd5aee8150a5f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836866"
---
# <a name="postitem"></a>Objeto postItem

El elemento **PostItem** representa un elemento para exponer en el almacén de Exchange. 
  
```xml
<PostItem>
   <MimeContent/>
   <ItemId/>
   <ParentFolderId/>
   <ItemClass/>
   <Subject/>
   <Sensitivity/>
   <Body/>
   <Attachments/>
   <DateTimeReceived/>
   <Size/>
   <Categories/>
   <Importance/>
   <InReplyTo/>
   <IsSubmitted/>
   <IsDraft/>
   <IsFromMe/>
   <IsResend/>
   <IsUnmodified/>
   <InternetMessageHeaders/>
   <DateTimeSent/>
   <DateTimeCreated/>
   <ResponseObjects/>
   <ReminderDueBy/>
   <ReminderIsSet/>
   <ReminderMinutesBeforeStart/>
   <DisplayCc/>
   <DisplayTo/>
   <HasAttachments/>
   <ExtendedProperty/>
   <Culture/>
   <EffectiveRights/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
   <ConversationIndex/>
   <ConversationTopic/>
   <From/>
   <InternetMessageId/>
   <IsRead/>
   <PostedTime/>
   <References/>
   <Sender/>
</PostItem>
```

 **PostItemType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |Contiene la secuencia de extensiones multipropósito de correo Internet (MIME) nativo de un objeto que se representa en formato base64Binary.  <br/> |
|[ItemId](itemid.md) <br/> |Contiene el único identificador y cambiar la clave de un elemento en el almacén de Exchange. Esta propiedad es de sólo lectura.  <br/> |
|[Id](parentfolderid.md) <br/> |Representa el identificador de la carpeta primaria que contiene el elemento o la carpeta. Esta propiedad es de sólo lectura.  <br/> |
|[ItemClass](itemclass.md) <br/> |Representa la clase de mensaje de un elemento.  <br/> |
|[Subject](subject.md) <br/> |Representa al asunto de los elementos del almacén de Exchange y objetos de respuesta. El asunto está limitado a 255 caracteres.  <br/> |
|[Sensibilidad](sensitivity.md) <br/> |Indica el nivel de confidencialidad de un elemento.  <br/> |
|[Body](body.md) <br/> |Representa el contenido real del cuerpo de un mensaje.  <br/> |
|[Datos adjuntos](attachments-ex15websvcsotherref.md) <br/> |Contiene los elementos o archivos que se adjuntan a un elemento en el almacén de Exchange.  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |Representa la fecha y hora en que se recibió un elemento en un buzón de correo.  <br/> |
|[Size](size.md) <br/> |Representa el tamaño en bytes de un elemento. Esta propiedad es de sólo lectura.  <br/> |
|[Categories](categories-ex15websvcsotherref.md) <br/> |Representa una colección de cadenas que identifican las categorías a la que pertenece un elemento en el buzón de correo.  <br/> |
|[Importancia](importance.md) <br/> |Describe la importancia de un elemento.  <br/> |
|[InReplyTo](inreplyto.md) <br/> |Representa el identificador del elemento al que este elemento es una respuesta.  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |Indica si un elemento se ha enviado a la carpeta predeterminada Bandeja de salida.  <br/> |
|[IsDraft](isdraft.md) <br/> |Representa si un elemento aún no se ha enviado.  <br/> |
|[IsFromMe](isfromme.md) <br/> |Indica si un usuario envía un elemento a él o a sí mismo.  <br/> |
|[IsResend](isresend.md) <br/> |Indica si el elemento se había enviado anteriormente.  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |Indica si el elemento se ha modificado.  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Representa la colección de todos los encabezados de mensaje de Internet que están contenidos en un elemento en un buzón de correo.  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |Representa la fecha y hora en que se envió un elemento en un buzón de correo.  <br/> |
|[DateTimeCreated](datetimecreated.md) <br/> |Representa la fecha y hora en que se creó un elemento determinado en el buzón de correo.  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Contiene una colección de todos los objetos de respuesta que están asociados con un elemento en el almacén de Exchange.  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |Representa la fecha y hora cuando se produce el evento. Esto se usa en el elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) para determinar cuándo se muestra el aviso.  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |Indica si se ha establecido un aviso para un elemento en el almacén de Exchange.  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |Representa el número de minutos antes de un evento cuando se muestra un aviso.  <br/> |
|[DisplayCc](displaycc.md) <br/> |Representa la cadena para mostrar que se usa para el contenido del cuadro Cc. Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios de Cc.  <br/> |
|[DisplayTo](displayto.md) <br/> |Representa la cadena para mostrar que se usa para el contenido del cuadro para. Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Representa una propiedad que se establece en **true** si un elemento tiene al menos un dato adjunto. Esta propiedad es de sólo lectura.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Identifica las propiedades extendidas en carpetas y elementos.  <br/> |
|[Referencia cultural](culture.md) <br/> |Representa la referencia cultural para un elemento determinado en un buzón de correo.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Contiene los derechos del cliente en función de la configuración de permisos para el elemento o la carpeta. Este elemento es de sólo lectura.  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |Contiene el nombre para mostrar del último usuario para modificar un elemento.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Indica cuándo se modificó por última vez un elemento.  <br/> |
|[IsAssociated](isassociated.md) <br/> |Indica si el elemento está asociado a una carpeta.  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |Representa una dirección URL a concatene al extremo de Microsoft Office Outlook Web App para leer un elemento en Outlook Web App.  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |Representa una dirección URL a concatene al extremo de Outlook Web App para editar un elemento en Outlook Web App.  <br/> |
|[ConversationId](conversationid.md) <br/> |Contiene el identificador de un elemento o conversación.  <br/> |
|[UniqueBody](uniquebody.md) <br/> |Representa un fragmento HTML o texto sin formato que representa el cuerpo único de esta conversación.  <br/> |
|[ConversationIndex](conversationindex.md) <br/> |Contiene un identificador binario que representa el subproceso al que pertenece este mensaje.  <br/> |
|[ConversationTopic](conversationtopic.md) <br/> |Representa el identificador de conversación.  <br/> |
|[From](from.md) <br/> |Representa la dirección desde la que se envió el elemento para exponer. El elemento **de** solo se puede establecer en tiempo de creación.  <br/> |
|[InternetMessageId](internetmessageid.md) <br/> |Representa el identificador de mensaje de Internet de un elemento.  <br/> |
|[Estáleído](isread.md) <br/> |Indica si se ha leído un mensaje.  <br/> |
|[PostedTime](postedtime.md) <br/> |Representa el tiempo que se ha registrado un [objeto PostItem](postitem.md) .  <br/> |
|[Referencias](references.md) <br/> |Representa el encabezado de Usenet que se usa para asociar las respuestas a los mensajes originales.  <br/> |
|[Sender](sender.md) <br/> |Identifica el remitente de un elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[SetItemField](setitemfield.md) <br/> |Representa una actualización para una única propiedad de un elemento en una operación UpdateItem.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifica los datos que se anexará a una propiedad única de una carpeta o elemento durante una [operación de UpdateItem](updateitem-operation.md).  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Representa un elemento de Exchange que está vinculado a otro elemento de Exchange.  <br/> |
|[Crear (ItemSync)](create-itemsync.md) <br/> |Identifica un solo elemento para crear en el almacén de cliente local.  <br/> |
|[Actualización (ItemSync)](update-itemsync.md) <br/> |Identifica un solo elemento que se debe actualizar en el almacén de cliente local.  <br/> |
|[ReadFlagChange](readflagchange.md) <br/> |Devuelto en [SyncFolderItems](syncfolderitems.md) respuestas cuando se leyó un elemento. Esta propiedad es de sólo lectura. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[Items](items.md) <br/> |Contiene una matriz de elementos.  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifica todos los elementos que entran en conflicto con un tiempo de la reunión.  <br/> |
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Describe todos los elementos de calendario que están junto a una hora de reunión.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Observaciones

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

