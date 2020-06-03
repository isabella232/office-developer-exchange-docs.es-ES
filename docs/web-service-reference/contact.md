---
title: Contacto
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Contact
api_type:
- schema
ms.assetid: 66bfff50-7a91-4d81-b6a0-610b9962f677
description: El elemento Contact representa un elemento de contacto en el almacén de Exchange.
ms.openlocfilehash: b5b4af211815dbbd09449ca2f3c6b6b2dfba6f93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44445653"
---
# <a name="contact"></a>Contacto

El elemento **Contact** representa un elemento de contacto en el almacén de Exchange. 
  
```XML
<Contact>
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
   <FileAs/>
   <FileAsMapping/>
   <DisplayName/>
   <GivenName/>
   <Initials/>
   <MiddleName/>
   <Nickname/>
   <CompleteName/>
   <CompanyName/>
   <EmailAddresses/>
   <PhysicalAddresses/>
   <PhoneNumbers/>
   <AssistantName/>
   <Birthday/>
   <BusinessHomePage/>
   <Children/>
   <Companies/>
   <ContactSource/>
   <Department/>
   <Generation/>
   <ImAddresses/>
   <JobTitle/>
   <Manager/>
   <Mileage/>
   <OfficeLocation/>
   <PostalAddressIndex/>
   <Profession/>
   <SpouseName/>
   <Surname/>
   <WeddingAnniversary/>
   <HasPicture/>
   <PhoneticFullName/>
   <PhoneticFirstName/>
   <PhoneticLastName/>
   <Alias/>
   <Notes/>
   <Photo/>
   <UserSMIMECertificate/>
   <MSExchangeCertificate/>
   <DirectoryId/>
   <ManagerMailbox/>
   <DirectReports/>
</Contact>
```

 **ContactItemType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Nombre del elemento**|**Descripción**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |Contiene la secuencia nativa de extensiones de correo de Internet multipropósito (MIME) de un objeto representado en formato base64Binary.  <br/> |
|[ItemId](itemid.md) <br/> |Contiene el identificador único y la clave de cambio de un elemento en el almacén de Exchange.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Representa el identificador de la carpeta principal que contiene el elemento o carpeta.  <br/> |
|[ItemClass](itemclass.md) <br/> |Representa la clase de mensaje de un elemento.  <br/> |
|[Asunto](subject.md) <br/> |Representa el asunto de los elementos de almacén de Exchange y los objetos de respuesta.  <br/> |
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
|[IsFromMe](isfromme.md) <br/> |Indica si un usuario ha enviado un elemento a sí mismo.  <br/> |
|[IsResend](isresend.md) <br/> |Indica si el elemento se ha enviado previamente.  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |Indica si se ha modificado el elemento.  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Representa la colección de todos los encabezados de mensajes de Internet que contiene un elemento en un buzón.  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |Representa la fecha y la hora en que se envió un elemento en un buzón.  <br/> |
|[DateTimeCreated](datetimecreated.md) <br/> |Representa la fecha y la hora en que se creó un elemento determinado en el buzón.  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Contiene una colección de todos los objetos de respuesta que están asociados a un elemento en el almacén de Exchange.  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |Representa la fecha y la hora en que se produce el evento. El elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) lo usa para determinar cuándo se muestra el aviso.  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |Indica si se ha establecido un aviso para un elemento en el almacén de Exchange.  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |Representa el número de minutos antes de un evento cuando se muestra un aviso.  <br/> |
|[DisplayCc](displaycc.md) <br/> |Representa la cadena para mostrar que se usa para el contenido de la línea CC. Esta es la cadena concatenada de todos los nombres para mostrar de los destinatarios en CC.  <br/> |
|[DisplayTo](displayto.md) <br/> |Representa la cadena para mostrar que se usa para el contenido de la línea para. Esta es la cadena concatenada de todos los nombres para mostrar de destinatarios.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Representa una propiedad que se establece en **true** si un elemento tiene al menos un archivo de datos adjuntos visible. Esta propiedad es de sólo lectura.  <br/> |
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
|[FileAs](fileas.md) <br/> |Representa cómo se archiva un contacto en la carpeta de contactos.  <br/> |
|[FileAsMapping](fileasmapping.md) <br/> |Define cómo crear lo que se muestra para un contacto.  <br/> |
|[DisplayName (cadena)](displayname-string.md) <br/> |Define el nombre para mostrar de un contacto.  <br/> |
|[GivenName](givenname.md) <br/> |Contiene el nombre especificado de un contacto.  <br/> |
|[Iniciales](initials.md) <br/> |Representa las iniciales de un contacto.  <br/> |
|[MiddleName](middlename.md) <br/> |Representa el segundo nombre de un contacto.  <br/> |
|[Llamamos](nickname.md) <br/> |Representa el alias de un contacto.  <br/> |
|[CompleteName](completename.md) <br/> |Representa el nombre completo de un contacto.  <br/> |
|[CompanyName](companyname.md) <br/> |Representa el nombre de la compañía que está asociado a un contacto.  <br/> |
|[EmailAddresses](emailaddresses.md) <br/> |Representa una colección de direcciones de correo electrónico de un contacto.  <br/> |
|[PhysicalAddresses](physicaladdresses.md) <br/> |Contiene una colección de direcciones físicas que están asociadas a un contacto.  <br/> |
|[PhoneNumbers](phonenumbers.md) <br/> |Representa una colección de números de teléfono de un contacto.  <br/> |
|[AssistantName](assistantname.md) <br/> |Representa un asistente para un contacto.  <br/> |
|[Cumpleaños](birthday.md) <br/> |Representa la fecha de nacimiento de un contacto.  <br/> |
|[BusinessHomePage](businesshomepage.md) <br/> |Representa la Página principal (dirección web) del contacto.  <br/> |
|[Niños](children.md) <br/> |Contiene los nombres de los elementos secundarios de un contacto.  <br/> |
|[Companies](companies.md) <br/> |Representa la colección de compañías que están asociadas a un contacto.  <br/> |
|[ContactSource](contactsource.md) <br/> |Describe si el contacto se encuentra en el almacén de Exchange o en el servicio de directorio de Active Directory.  <br/> |
|[Departamento](department.md) <br/> |Representa el Departamento del contacto en el trabajo.  <br/> |
|[Generación](generation.md) <br/> |Representa una abreviatura generacional que sigue el nombre completo de un contacto.  <br/> |
|[Indirecciones](imaddresses.md) <br/> |Representa una colección de direcciones de mensajería instantánea de un contacto.  <br/> |
|[JobTitle](jobtitle.md) <br/> |Representa el puesto de un contacto.  <br/> |
|[Manager](manager.md) <br/> |Representa el administrador de un contacto.  <br/> |
|[Mileage](mileage.md) <br/> |Representa el kilometraje de un elemento de contacto.  <br/> |
|[OfficeLocation](officelocation.md) <br/> |Representa la ubicación de la oficina de un contacto.  <br/> |
|[PostalAddressIndex](postaladdressindex.md) <br/> |Representa los tipos de presentación de direcciones físicas.  <br/> |
|[Profesión](profession.md) <br/> |Representa la profesión de un contacto.  <br/> |
|[SpouseName](spousename.md) <br/> |Representa el nombre del cónyuge o pareja de un contacto.  <br/> |
|[Apellido](surname.md) <br/> |Representa el apellido de un contacto.  <br/> |
|[WeddingAnniversary](weddinganniversary.md) <br/> |Contiene el aniversario de boda de un contacto.  <br/> |
|[HasPicture](haspicture.md) <br/> |Indica si el elemento de contacto tiene un archivo adjunto que representa la imagen del contacto.  <br/> |
|[PhoneticFullName](phoneticfullname.md) <br/> |Contiene el nombre completo de un contacto, incluidos el nombre y los apellidos, deletreados fonéticamente.  <br/> |
|[PhoneticFirstName](phoneticfirstname.md) <br/> |Contiene el nombre de un contacto, escrito en fonética.  <br/> |
|[PhoneticLastName](phoneticlastname.md) <br/> |Contiene el apellido de un contacto, escrito en fonética.  <br/> |
|[Alias](alias.md) <br/> |Contiene el alias de correo electrónico de un contacto.  <br/> |
|[Notas (contacto)](notes-contact.md) <br/> |Contiene información de contacto adicional.  <br/> |
|[Foto](photo.md) <br/> |Contiene un valor que codifica la foto de un contacto.  <br/> |
|[UserSMIMECertificate](usersmimecertificate.md) <br/> |Contiene un valor que codifica el certificado SMIME de un contacto.  <br/> |
|[MSExchangeCertificate](msexchangecertificate.md) <br/> |Contiene un valor que codifica el certificado de Microsoft Exchange de un contacto.  <br/> |
|[DirectoryId](directoryid.md) <br/> |Contiene el identificador de directorio de un contacto.  <br/> |
|[ManagerMailbox](managermailbox.md) <br/> |Contiene información SMTP que identifica el buzón de administrador del contacto.  <br/> |
|[DirectReports](directreports.md) <br/> |Contiene información SMTP que identifica los subordinados directos de un contacto.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Nombre del elemento**|**Descripción**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Describe todos los elementos de calendario adyacentes a una hora de reunión.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifica los datos que se van a anexar a una única propiedad de un elemento o carpeta durante una [operación UpdateItem](updateitem-operation.md).  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifica todos los elementos que entran en conflicto con una hora de reunión  <br/> |
|[Crear (ItemSync)](create-itemsync.md) <br/> |Identifica una única carpeta que se va a crear en el almacén de cliente local.  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Representa un elemento de Exchange que está adjunto a otro elemento de Exchange.  <br/> |
|[Items](items.md) <br/> |Contiene una matriz de elementos.  <br/> |
|[Elementos (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Contiene una matriz de elementos que se van a crear en la carpeta identificada por el elemento [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .  <br/> |
|[Resolución](resolution.md) <br/> |Contiene una única entidad resuelta.  <br/> |
|[SetItemField](setitemfield.md) <br/> |Representa una actualización de una propiedad única de un elemento en una [operación UpdateItem](updateitem-operation.md).  <br/> |
|[Actualización (ItemSync)](update-itemsync.md) <br/> |Identifica un elemento único para actualizar en el almacén de cliente local.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

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


[Creación de contactos (servicios Web de Exchange)](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[Actualizar contactos](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[Eliminación de contactos](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

