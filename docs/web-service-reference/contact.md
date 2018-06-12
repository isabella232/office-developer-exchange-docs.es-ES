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
description: El elemento de contacto representa un elemento de contacto en el almacén de Exchange.
ms.openlocfilehash: 7b2e7c0197914c2a0a0ba3815dd05fca52a5f872
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763789"
---
# <a name="contact"></a>Contacto

El elemento **de contacto** representa un elemento de contacto en el almacén de Exchange. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Nombre del elemento**|**Descripción**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |Contiene la secuencia de extensiones multipropósito de correo Internet (MIME) nativo de un objeto que se representa en formato base64Binary.  <br/> |
|[ItemId](itemid.md) <br/> |Contiene el único identificador y cambiar la clave de un elemento en el almacén de Exchange.  <br/> |
|[Id](parentfolderid.md) <br/> |Representa el identificador de la carpeta primaria que contiene el elemento o la carpeta.  <br/> |
|[ItemClass](itemclass.md) <br/> |Representa la clase de mensaje de un elemento.  <br/> |
|[Subject](subject.md) <br/> |Representa al asunto de los elementos del almacén de Exchange y objetos de respuesta.  <br/> |
|[Sensibilidad](sensitivity.md) <br/> |Indica el nivel de confidencialidad de un elemento.  <br/> |
|[Body](body.md) <br/> |Representa el contenido real del cuerpo de un mensaje.  <br/> |
|[Datos adjuntos](attachments-ex15websvcsotherref.md) <br/> |Contiene los elementos o archivos que se adjuntan a un elemento en el almacén de Exchange.  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |Representa la fecha y hora en que se recibió un elemento en un buzón de correo.  <br/> |
|[Size](size.md) <br/> |Representa el tamaño en bytes de un elemento. Esta propiedad es de sólo lectura.  <br/> |
|[Categories](categories-ex15websvcsotherref.md) <br/> |Representa una colección de cadenas que identifican a qué categorías pertenece un elemento en el buzón de correo.  <br/> |
|[Importancia](importance.md) <br/> |Describe la importancia de un elemento.  <br/> |
|[InReplyTo](inreplyto.md) <br/> |Representa el identificador del elemento al que este elemento es una respuesta.  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |Indica si un elemento se ha enviado a la carpeta predeterminada Bandeja de salida.  <br/> |
|[IsDraft](isdraft.md) <br/> |Representa si un elemento aún no se ha enviado.  <br/> |
|[IsFromMe](isfromme.md) <br/> |Indica si un usuario envía un elemento a sí mismo o a sí mismo.  <br/> |
|[IsResend](isresend.md) <br/> |Indica si el elemento se había enviado anteriormente.  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |Indica si el elemento se ha modificado.  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Representa la colección de todos los encabezados de mensaje de Internet que están contenidos en un elemento en un buzón de correo.  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |Representa la fecha y hora en que se envió un elemento en un buzón de correo.  <br/> |
|[DateTimeCreated](datetimecreated.md) <br/> |Representa la fecha y hora en que se creó un elemento determinado en el buzón de correo.  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Contiene una colección de todos los objetos de respuesta que están asociados con un elemento en el almacén de Exchange.  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |Representa la fecha y hora cuando se produce el evento. Esto se usa en el elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) para determinar cuándo se muestra el aviso.  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |Indica si se ha establecido un aviso para un elemento en el almacén de Exchange.  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |Representa el número de minutos antes de un evento cuando se muestra un aviso.  <br/> |
|[DisplayCc](displaycc.md) <br/> |Representa la cadena para mostrar que se usa para el contenido de la línea Cc. Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios de Cc.  <br/> |
|[DisplayTo](displayto.md) <br/> |Representa la cadena para mostrar que se usa para el contenido de la línea para. Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Representa una propiedad que se establece en **true** si un elemento tiene al menos un dato adjunto visible. Esta propiedad es de sólo lectura.  <br/> |
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
|[Archivar como](fileas.md) <br/> |Representa cómo se archiva un contacto en la carpeta Contactos.  <br/> |
|[FileAsMapping](fileasmapping.md) <br/> |Define cómo se construye lo que se muestra para un contacto.  <br/> |
|[DisplayName (cadena)](displayname-string.md) <br/> |Define el nombre para mostrar de un contacto.  <br/> |
|[GivenName](givenname.md) <br/> |Contiene el nombre de un contacto determinado.  <br/> |
|[Iniciales](initials.md) <br/> |Representa las iniciales del contacto.  <br/> |
|[MiddleName](middlename.md) <br/> |Representa el segundo nombre de un contacto.  <br/> |
|[Alias](nickname.md) <br/> |Representa el alias de un contacto.  <br/> |
|[CompleteName](completename.md) <br/> |Representa el nombre completo de un contacto.  <br/> |
|[CompanyName](companyname.md) <br/> |Representa el nombre de la empresa que está asociado con un contacto.  <br/> |
|[EmailAddresses](emailaddresses.md) <br/> |Representa una colección de direcciones de correo electrónico de un contacto.  <br/> |
|[PhysicalAddresses](physicaladdresses.md) <br/> |Contiene una colección de direcciones físicas que están asociados con un contacto.  <br/> |
|[PhoneNumbers](phonenumbers.md) <br/> |Representa una colección de números de teléfono de un contacto.  <br/> |
|[AssistantName](assistantname.md) <br/> |Representa a un asistente a un contacto.  <br/> |
|[Cumpleaños](birthday.md) <br/> |Representa la fecha de nacimiento de un contacto.  <br/> |
|[BusinessHomePage](businesshomepage.md) <br/> |Representa la página principal (dirección Web) para el contacto.  <br/> |
|[Niños](children.md) <br/> |Contiene los nombres de los elementos secundarios de un contacto.  <br/> |
|[Empresas](companies.md) <br/> |Representa la colección de las empresas que están asociados con un contacto.  <br/> |
|[ContactSource](contactsource.md) <br/> |Describe si el contacto se encuentra en el almacén de Exchange o el servicio de directorio de Active Directory.  <br/> |
|[Departamento](department.md) <br/> |Representa el departamento del contacto en el trabajo.  <br/> |
|[Generación](generation.md) <br/> |Representa una abreviatura de generaciones que sigue el nombre completo de un contacto.  <br/> |
|[ImAddresses](imaddresses.md) <br/> |Representa una colección de direcciones de mensajería instantáneas para un contacto.  <br/> |
|[JobTitle](jobtitle.md) <br/> |Representa el título del trabajo de un contacto.  <br/> |
|[Manager](manager.md) <br/> |Representa el Administrador de un contacto.  <br/> |
|[Kilometraje](mileage.md) <br/> |Representa mileage para un elemento de contacto.  <br/> |
|[OfficeLocation](officelocation.md) <br/> |Representa la ubicación de la oficina de un contacto.  <br/> |
|[PostalAddressIndex](postaladdressindex.md) <br/> |Representa los tipos de presentación para direcciones físicas.  <br/> |
|[Profession](profession.md) <br/> |Representa el ámbito de un contacto.  <br/> |
|[NombreCónyuge](spousename.md) <br/> |Representa el nombre del cónyuge o pareja de un contacto.  <br/> |
|[Apellido](surname.md) <br/> |Representa el apellido de un contacto.  <br/> |
|[WeddingAnniversary](weddinganniversary.md) <br/> |Contiene el aniversario despedida de un contacto.  <br/> |
|[HasPicture](haspicture.md) <br/> |Indica si el elemento de contacto tiene un archivo adjunto que representa la imagen del contacto.  <br/> |
|[PhoneticFullName](phoneticfullname.md) <br/> |Contiene el nombre completo de un contacto, incluido el nombre y el apellido, escrito fonéticamente.  <br/> |
|[PhoneticFirstName](phoneticfirstname.md) <br/> |Contiene el nombre de un contacto, escrito fonéticamente.  <br/> |
|[PhoneticLastName](phoneticlastname.md) <br/> |Contiene el último nombre de un contacto, escrito fonéticamente.  <br/> |
|[Alias](alias.md) <br/> |Contiene el alias de correo electrónico de un contacto.  <br/> |
|[Notas (contacto)](notes-contact.md) <br/> |Contiene información de contacto adicional.  <br/> |
|[Photo](photo.md) <br/> |Contiene un valor que se codifica la foto de un contacto.  <br/> |
|[UserSMIMECertificate](usersmimecertificate.md) <br/> |Contiene un valor que se codifica el certificado SMIME de un contacto.  <br/> |
|[MSExchangeCertificate](msexchangecertificate.md) <br/> |Contiene un valor que se codifica el certificado de Microsoft Exchange de un contacto.  <br/> |
|[DirectoryId](directoryid.md) <br/> |Contiene el identificador de directorio de un contacto.  <br/> |
|[ManagerMailbox](managermailbox.md) <br/> |Contiene información de SMTP que identifica el buzón de correo del administrador del contacto.  <br/> |
|[DirectReports](directreports.md) <br/> |Contiene información de SMTP que identifica los informes directos del contacto.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Nombre del elemento**|**Descripción**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Describe todos los elementos de calendario que están junto a una hora de reunión.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifica los datos que se anexará a una propiedad única de una carpeta o elemento durante una [operación de UpdateItem](updateitem-operation.md).  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifica todos los elementos que entran en conflicto con un tiempo de la reunión  <br/> |
|[Crear (ItemSync)](create-itemsync.md) <br/> |Identifica una sola carpeta para crear en el almacén de cliente local.  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Representa un elemento de Exchange que está vinculado a otro elemento de Exchange.  <br/> |
|[Items](items.md) <br/> |Contiene una matriz de elementos.  <br/> |
|[Elementos (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Contiene una matriz de elementos que desea crear en la carpeta que se identifica con el elemento [ID (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .  <br/> |
|[Resoluci?n](resolution.md) <br/> |Contiene una única entidad resuelta.  <br/> |
|[SetItemField](setitemfield.md) <br/> |Representa una actualización para una única propiedad de un elemento en una [operación de UpdateItem](updateitem-operation.md).  <br/> |
|[Actualización (ItemSync)](update-itemsync.md) <br/> |Identifica un solo elemento que se debe actualizar en el almacén de cliente local.  <br/> |
   
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


[Creación de contactos (servicios Web de Exchange)](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[Actualizar contactos](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[Eliminación de contactos](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

