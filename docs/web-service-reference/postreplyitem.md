---
title: PostReplyItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PostReplyItem
api_type:
- schema
ms.assetid: e5d93d63-0a3b-470f-9a94-2d57284c6745
description: El elemento PostReplyItem contiene una respuesta a un elemento de publicación. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 657173e19d5dc1bb6a8126b62c5977d5afc1c17c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59527910"
---
# <a name="postreplyitem"></a>PostReplyItem

El **elemento PostReplyItem** contiene una respuesta a un elemento de publicación. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<PostReplyItem>
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
   <Sender/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <IsReadReceiptRequested/>
   <IsDeliveryReceiptRequested/>
   <ConversationIndex/>
   <ConversationTopic/>
   <From/>
   <InternetMessageId/>
   <IsRead/>
   <IsResponseRequested/>
   <References/>
   <ReplyTo/>
   <EffectiveRights/>
   <ReceivedBy/>
   <ReceivedRepresenting/>
   <NewBodyContent/>
</PostReplyItem>
```

 **PostReplyItemType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |Contiene la secuencia nativa Multipurpose Internet Mail Extensions (MIME) de un objeto que se representa en formato base64Binary.  <br/> |
|[ItemId](itemid.md) <br/> |Contiene el identificador único y la clave de cambio de un elemento en el Exchange almacén. Esta propiedad es de sólo lectura.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Representa el identificador de la carpeta primaria que contiene el elemento o la carpeta. Esta propiedad es de sólo lectura.  <br/> |
|[ItemClass](itemclass.md) <br/> |Representa la clase de mensaje de un elemento.  <br/> |
|[Asunto](subject.md) <br/> |Representa el asunto de los Exchange almacenar y los objetos de respuesta. El asunto está limitado a 255 caracteres.  <br/> |
|[Sensitivity](sensitivity.md) <br/> |Indica el nivel de confidencialidad de un elemento.  <br/> |
|[Cuerpo](body.md) <br/> |Representa el contenido real del cuerpo de un mensaje.  <br/> |
|[Adjuntos](attachments-ex15websvcsotherref.md) <br/> |Contiene los elementos o archivos adjuntos a un elemento del Exchange almacén.  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |Representa la fecha y hora en que se recibió un elemento de un buzón.  <br/> |
|[Tamaño](size.md) <br/> |Representa el tamaño en bytes de un elemento. Esta propiedad es de sólo lectura.  <br/> |
|[Categories](categories-ex15websvcsotherref.md) <br/> |Representa una colección de cadenas que identifican las categorías a las que pertenece un elemento del buzón.  <br/> |
|[Importance](importance.md) <br/> |Describe la importancia de un elemento.  <br/> |
|[InReplyTo](inreplyto.md) <br/> |Representa el identificador del elemento al que este elemento es una respuesta.  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |Indica si se ha enviado un elemento a la carpeta predeterminada bandeja de salida.  <br/> |
|[IsDraft](isdraft.md) <br/> |Representa si aún no se ha enviado un elemento.  <br/> |
|[IsFromMe](isfromme.md) <br/> |Indica si un usuario le envió un elemento a él o a sí mismo.  <br/> |
|[IsResend](isresend.md) <br/> |Indica si el elemento se envió anteriormente.  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |Indica si el elemento se ha modificado.  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Representa la colección de todos los encabezados de mensaje de Internet contenidos en un elemento de un buzón.  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |Representa la fecha y hora en que se envió un elemento de un buzón.  <br/> |
|[DateTimeCreated](datetimecreated.md) <br/> |Representa la fecha y hora en que se creó un elemento determinado en el buzón.  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Contiene una colección de todos los objetos de respuesta asociados con un elemento del Exchange almacén.  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |Representa la fecha y hora en que se produce el evento. El elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) lo usa para determinar cuándo se muestra el aviso.  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |Indica si se ha establecido un aviso para un elemento en el Exchange almacén.  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |Representa el número de minutos antes de un evento cuando se muestra un aviso.  <br/> |
|[DisplayCc](displaycc.md) <br/> |Representa la cadena para mostrar que se usa para el contenido de la línea Cc. Esta es la cadena concatenada de todos los nombres para mostrar de destinatarios cc.  <br/> |
|[DisplayTo](displayto.md) <br/> |Representa la cadena para mostrar que se usa para el contenido del cuadro Para. Esta es la cadena concatenada de todos los nombres para mostrar de destinatarios To.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Representa una propiedad que se establece en **true** si un elemento tiene datos adjuntos. Esta propiedad es de sólo lectura.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Identifica propiedades extendidas en carpetas y elementos.  <br/> |
|[Culture](culture.md) <br/> |Representa la referencia cultural de un elemento determinado en un buzón.  <br/> |
|[Sender](sender.md) <br/> |Identifica al remitente de un elemento.  <br/> |
|[ToRecipients](torecipients.md) <br/> |Contiene un conjunto de destinatarios de un mensaje.  <br/> |
|[CcRecipients](ccrecipients.md) <br/> |Representa una colección de destinatarios que recibirán una copia del mensaje.  <br/> |
|[BccRecipients](bccrecipients.md) <br/> |Representa una colección de destinatarios para recibir una copia a ciegas (CCO) de un correo electrónico.  <br/> |
|[IsReadReceiptRequested](isreadreceiptrequested.md) <br/> |Indica si el remitente de un elemento solicita un recibo de lectura.  <br/> |
|[IsDeliveryReceiptRequested](isdeliveryreceiptrequested.md) <br/> |Indica si el remitente de un elemento solicita un recibo de entrega.  <br/> |
|[ConversationIndex](conversationindex.md) <br/> |Contiene un identificador binario que representa el subproceso al que pertenece este mensaje.  <br/> |
|[ConversationTopic](conversationtopic.md) <br/> |Representa el identificador de conversación.  <br/> |
|[From](from.md) <br/> |Representa la dirección desde la que se envió el mensaje.  <br/> |
|[InternetMessageId](internetmessageid.md) <br/> |Representa el identificador de mensaje de Internet de un elemento.  <br/> |
|[IsRead](isread.md) <br/> |Indica si se ha leído un mensaje.  <br/> |
|[IsResponseRequested](isresponserequested.md) <br/> |Indica si se solicita una respuesta a un mensaje de correo electrónico.  <br/> |
|[Referencias](references.md) <br/> |Representa el encabezado Usenet que se usa para asociar respuestas a sus mensajes originales.  <br/> |
|[ReplyTo](replyto.md) <br/> |Identifica un conjunto de direcciones a las que se deben enviar respuestas.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Contiene los derechos del cliente en función de la configuración de permisos del elemento o carpeta. Este elemento es de solo lectura. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[ReceivedBy](receivedby.md) <br/> |Identifica al delegado en un escenario de acceso delegado. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[ReceivedRepresenting](receivedrepresenting.md) <br/> |Identifica la entidad de seguridad en un escenario de acceso delegado. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[NewBodyContent](newbodycontent.md) <br/> |Representa el nuevo contenido del cuerpo de un elemento de publicación.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Describe todos los elementos adyacentes a una hora de reunión.  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Describe todos los elementos que entren en conflicto con una hora de reunión.  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Contiene una colección de todos los objetos de respuesta asociados con un elemento del Exchange almacén.  <br/> |
|[Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Contiene una matriz de elementos para crear en la carpeta identificada por el [elemento ParentFolderId (TargetFolderIdType).](parentfolderid-targetfolderidtype.md)  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

