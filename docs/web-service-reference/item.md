---
title: Item
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Item
api_type:
- schema
ms.assetid: 4dfe8f48-e7b4-444d-bdf9-a34e180f598b
description: El elemento Item representa un elemento genérico en el Exchange almacén.
ms.openlocfilehash: bf634949d440b5c8223aeb90c04e63825e1198e9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540947"
---
# <a name="item"></a>Item

El **elemento Item** representa un elemento genérico en el Exchange almacén. 
  
```xml
<Item>
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
</Item>
```

 **ItemType**
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
|[Categories](categories-ex15websvcsotherref.md) <br/> |Representa una colección de cadenas que identifican a qué categorías pertenece un elemento del buzón.  <br/> |
|[Importance](importance.md) <br/> |Describe la importancia de un elemento.  <br/> |
|[InReplyTo](inreplyto.md) <br/> |Representa el identificador del elemento al que este elemento es una respuesta.  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |Indica si se ha enviado un elemento a la carpeta predeterminada bandeja de salida.  <br/> |
|[IsDraft](isdraft.md) <br/> |Representa si aún no se ha enviado un elemento.  <br/> |
|[IsFromMe](isfromme.md) <br/> |Indica si un usuario envió un elemento a sí mismo.  <br/> |
|[IsResend](isresend.md) <br/> |Indica si el elemento se envió anteriormente.  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |Indica si el elemento se ha modificado.  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Representa la colección de todos los encabezados de mensajes de Internet contenidos en un elemento de un buzón.  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |Representa la fecha y hora en que se envió un elemento de un buzón.  <br/> |
|[DateTimeCreated](datetimecreated.md) <br/> |Representa la fecha y hora en que se creó un elemento determinado en el buzón.  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Contiene una colección de todos los objetos de respuesta asociados con un elemento del Exchange almacén.  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |Representa la fecha y hora en que se produce el evento. El elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) lo usa para determinar cuándo se muestra el aviso.  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |Indica si se ha establecido un aviso para un elemento en el Exchange almacén.  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |Representa el número de minutos antes de un evento cuando se muestra un aviso.  <br/> |
|[DisplayCc](displaycc.md) <br/> |Representa la cadena de presentación que se usa para el contenido del cuadro Cc. Esta es la cadena concatenada de todos los nombres para mostrar de destinatarios cc.  <br/> |
|[DisplayTo](displayto.md) <br/> |Representa la cadena para mostrar que se usa para el contenido del cuadro Para. Esta es la cadena concatenada de todos los nombres para mostrar de destinatarios To.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Representa una propiedad que se establece en **true** si un elemento tiene datos adjuntos al menos un dato adjunto visible. Esta propiedad es de sólo lectura.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Identifica propiedades extendidas en carpetas y elementos.  <br/> |
|[Culture](culture.md) <br/> |Representa la referencia cultural de un elemento determinado en un buzón.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Contiene los derechos del cliente en función de la configuración de permisos del elemento o carpeta. Este elemento es de solo lectura.  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |Contiene el nombre para mostrar del último usuario que modifica un elemento.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Indica cuándo se modificó por última vez un elemento.  <br/> |
|[IsAssociated](isassociated.md) <br/> |Indica si el elemento está asociado a una carpeta.  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |Representa una dirección URL para concatenar al punto de conexión Microsoft Office Outlook Web App para leer un elemento en Outlook Web App.  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |Representa una dirección URL para concatenar al punto Outlook Web App para editar un elemento en Outlook Web App.  <br/> |
|[ConversationId](conversationid.md) <br/> |Contiene el identificador de un elemento o conversación.  <br/> |
|[UniqueBody](uniquebody.md) <br/> |Representa un fragmento HTML o texto sin formato que representa el cuerpo único de esta conversación.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Describe todos los elementos de calendario adyacentes a una hora de reunión.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifica los datos que se anexarán a una sola propiedad de un elemento o carpeta durante una [operación UpdateItem](updateitem-operation.md).  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifica todos los elementos que entren en conflicto con una hora de reunión.  <br/> |
|[Create (ItemSync)](create-itemsync.md) <br/> |Identifica un solo elemento para crear en el almacén de cliente local.  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Representa un Exchange que se adjunta a otro Exchange elemento.  <br/> |
|[Items](items.md) <br/> |Contiene una matriz de elementos.  <br/> |
|[Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Contiene una matriz de elementos para crear en la carpeta identificada por el [elemento ParentFolderId (TargetFolderIdType).](parentfolderid-targetfolderidtype.md)  <br/> |
|[SetItemField](setitemfield.md) <br/> |Representa una actualización de una sola propiedad de un elemento en una [operación UpdateItem](updateitem-operation.md).  <br/> |
|[Update (ItemSync)](update-itemsync.md) <br/> |Identifica un solo elemento para actualizar en el almacén de cliente local.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Es importante tener en cuenta que **ItemType** es el tipo base de [Task](task.md), [CalendarItem](calendaritem.md), [Contact](contact.md), [DistributionList](distributionlist.md)y [Message](message-ex15websvcsotherref.md).
  
[Los](message-ex15websvcsotherref.md) elementos message representan mensajes de correo electrónico y todos los demás elementos que no están fuertemente especificados por el esquema Exchange Web Services (EWS). Elementos como IPM. El uso compartido y IPM.InfoPath se devuelven como **elementos Message.** Microsoft Exchange Server 2010 no devuelve el **elemento Item** base en las respuestas. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)
  
[Referencia EWS para Exchange](ews-reference-for-exchange.md)

