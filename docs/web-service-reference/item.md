---
title: Elemento
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Item
api_type:
- schema
ms.assetid: 4dfe8f48-e7b4-444d-bdf9-a34e180f598b
description: El elemento Item representa un elemento genérico del almacén de Exchange.
ms.openlocfilehash: 72d8b1344bea3bcd105a0e293365b17f37193ac3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460319"
---
# <a name="item"></a>Elemento

El elemento **Item** representa un elemento genérico del almacén de Exchange. 
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |Contiene la secuencia nativa de extensiones de correo de Internet multipropósito (MIME) de un objeto representado en formato base64Binary.  <br/> |
|[ItemId](itemid.md) <br/> |Contiene el identificador único y la clave de cambio de un elemento en el almacén de Exchange. Esta propiedad es de sólo lectura.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Representa el identificador de la carpeta principal que contiene el elemento o carpeta. Esta propiedad es de sólo lectura.  <br/> |
|[ItemClass](itemclass.md) <br/> |Representa la clase de mensaje de un elemento.  <br/> |
|[Asunto](subject.md) <br/> |Representa el asunto de los elementos de almacén de Exchange y los objetos de respuesta. El asunto está limitado a 255 caracteres.  <br/> |
|[Sensitivity](sensitivity.md) <br/> |Indica el nivel de confidencialidad de un elemento.  <br/> |
|[Body](body.md) <br/> |Representa el contenido del cuerpo real de un mensaje.  <br/> |
|[Datos adjuntos](attachments-ex15websvcsotherref.md) <br/> |Contiene los elementos o archivos adjuntos a un elemento en el almacén de Exchange.  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |Representa la fecha y la hora en que se recibió un elemento en un buzón.  <br/> |
|[Tamaño](size.md) <br/> |Representa el tamaño en bytes de un elemento. Esta propiedad es de sólo lectura.  <br/> |
|[Categorías](categories-ex15websvcsotherref.md) <br/> |Representa una colección de cadenas que identifican a qué categorías pertenece un elemento del buzón.  <br/> |
|[Importance](importance.md) <br/> |Describe la importancia de un elemento.  <br/> |
|[Inreplyto](inreplyto.md) <br/> |Representa el identificador del elemento al que se reenviará este elemento.  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |Indica si un elemento se ha enviado a la carpeta predeterminada de la bandeja de salida.  <br/> |
|[IsDraft](isdraft.md) <br/> |Representa si un elemento todavía no se ha enviado.  <br/> |
|[IsFromMe](isfromme.md) <br/> |Indica si un usuario envió un elemento a sí mismo.  <br/> |
|[IsResend](isresend.md) <br/> |Indica si el elemento se ha enviado previamente.  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |Indica si se ha modificado el elemento.  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Representa la colección de todos los encabezados de mensajes de Internet que se encuentran dentro de un elemento en un buzón.  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |Representa la fecha y la hora en que se envió un elemento en un buzón.  <br/> |
|[DateTimeCreated](datetimecreated.md) <br/> |Representa la fecha y la hora en que se creó un elemento determinado en el buzón.  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Contiene una colección de todos los objetos de respuesta que están asociados a un elemento en el almacén de Exchange.  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |Representa la fecha y la hora en que se produce el evento. El elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) lo usa para determinar cuándo se muestra el aviso.  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |Indica si se ha establecido un aviso para un elemento en el almacén de Exchange.  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |Representa el número de minutos antes de un evento cuando se muestra un aviso.  <br/> |
|[DisplayCc](displaycc.md) <br/> |Representa la cadena para mostrar que se usa para el contenido del cuadro CC. Esta es la cadena concatenada de todos los nombres para mostrar de los destinatarios en CC.  <br/> |
|[DisplayTo](displayto.md) <br/> |Representa la cadena para mostrar que se usa para el contenido del cuadro para. Esta es la cadena concatenada de todos los nombres para mostrar de destinatarios.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Representa una propiedad que se establece en **true** si un elemento tiene datos adjuntos al menos un archivo de datos adjuntos visible. Esta propiedad es de sólo lectura.  <br/> |
|[Las extendedproperty](extendedproperty.md) <br/> |Identifica las propiedades extendidas de las carpetas y los elementos.  <br/> |
|[Culture](culture.md) <br/> |Representa la referencia cultural de un elemento determinado en un buzón.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta. Este elemento es de sólo lectura.  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |Contiene el nombre para mostrar del último usuario que modificó un elemento.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Indica cuándo se modificó por última vez un elemento.  <br/> |
|[IsAssociated](isassociated.md) <br/> |Indica si el elemento está asociado a una carpeta.  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |Representa una dirección URL que se va a concatenar con el punto de conexión de Microsoft Office Outlook Web App para leer un elemento en Outlook Web App.  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |Representa una dirección URL que se va a concatenar con el punto de conexión de Outlook Web App para editar un elemento en Outlook Web App.  <br/> |
|[ConversationId](conversationid.md) <br/> |Contiene el identificador de un elemento o una conversación.  <br/> |
|[UniqueBody](uniquebody.md) <br/> |Representa un fragmento HTML o texto sin formato que representa el único cuerpo de esta conversación.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Describe todos los elementos de calendario adyacentes a una hora de reunión.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifica los datos que se van a anexar a una sola propiedad de un elemento o carpeta durante una [operación UpdateItem](updateitem-operation.md).  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifica todos los elementos que entran en conflicto con una hora de reunión.  <br/> |
|[Crear (ItemSync)](create-itemsync.md) <br/> |Identifica un solo elemento que se va a crear en el almacén de cliente local.  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Representa un elemento de Exchange que está adjunto a otro elemento de Exchange.  <br/> |
|[Items](items.md) <br/> |Contiene una matriz de elementos.  <br/> |
|[Elementos (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Contiene una matriz de elementos que se van a crear en la carpeta identificada por el elemento [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .  <br/> |
|[SetItemField](setitemfield.md) <br/> |Representa una actualización de una propiedad única de un elemento en una [operación UpdateItem](updateitem-operation.md).  <br/> |
|[Actualización (ItemSync)](update-itemsync.md) <br/> |Identifica un elemento único para actualizar en el almacén de cliente local.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Es importante tener en cuenta que **itemType** es el tipo base para [Task](task.md), [CalendarItem](calendaritem.md), [Contact](contact.md), [DistributionList](distributionlist.md)y [Message](message-ex15websvcsotherref.md).
  
Los elementos de [mensaje](message-ex15websvcsotherref.md) representan mensajes de correo electrónico y todos los demás elementos que no son fuertemente tipados por el esquema de servicios web Exchange (EWS). Elementos como IPM. Uso compartido e IPM. InfoPath se devuelven como elementos del **mensaje** . Microsoft Exchange Server 2010 no devuelve el elemento de **elemento** base en las respuestas. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)
  
[Referencia EWS para Exchange](ews-reference-for-exchange.md)

