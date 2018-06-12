---
title: ItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemId
api_type:
- schema
ms.assetid: 3350b597-57a0-4961-8f44-8624946719b4
description: El elemento de ItemId contiene el único identificador y cambiar la clave de un elemento en el almacén de Exchange.
ms.openlocfilehash: 9c5d71a23e1e4b77d2a50016aa4d765d872d04cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836157"
---
# <a name="itemid"></a>ItemId

El elemento de **ItemId** contiene el único identificador y cambiar la clave de un elemento en el almacén de Exchange. 
  
```XML
<ItemId Id="" ChangeKey="" />
```

 **ItemIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**Id** <br/> |Identifica un elemento específico en el almacén de Exchange. **Identificador** distingue mayúsculas de minúsculas; por lo tanto, las comparaciones entre **los identificadores de** deben ser entre mayúsculas y minúsculas o binario.  <br/> |
|**ChangeKey** <br/> | Identifica una versión específica de un elemento. <br/><br/>Un **ChangeKey** es necesario para los siguientes escenarios: <br/> <br/>-El elemento [UpdateItem](updateitem.md) requiere un **ChangeKey** si se establece el atributo **ConflictResolution** para resolver automáticamente. Resolución automática es un valor predeterminado. Si no se incluye el atributo **ChangeKey** , la respuesta devolverá un valor [ResponseCode](responsecode.md) igual a **ErrorChangeKeyRequired**.  <br/><br/>-El elemento [SendItem](senditem.md) requiere un **ChangeKey** comprobar si la operación intentada actuará de la versión más reciente de un elemento. Si el atributo **ChangeKey** no está incluido en la **ItemId** o si el **ChangeKey** está vacío, la respuesta devolverá un valor [ResponseCode](responsecode.md) igual a **ErrorStaleObject**.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange.  <br/> |
|[Contact](contact.md) <br/> |Representa un elemento de contacto de Exchange.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Representa un evento cuando se copia un elemento o carpeta.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Representa un evento cuando se crea un elemento o carpeta.  <br/> |
|[Eliminar (ItemSync)](delete-itemsync.md) <br/> |Identifica un solo elemento para eliminar en el almacén de cliente local.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Representa un evento cuando se elimina un elemento o carpeta.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[ExportItemsResponseMessage](exportitemsresponsemessage.md) <br/> |Contiene el estado y los resultados de una solicitud para exportar un elemento de un solo buzón de correo.  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |Representa la primera aparición de un elemento periódico del calendario.  <br/> |
|[GlobalItemIds](globalitemids.md) <br/> |Contiene la colección de identificadores de elemento para todos los elementos de la conversación en un buzón de correo.  <br/> |
|[Ignorar](ignore.md) <br/> |Identifica a los elementos que se debe omitir durante la sincronización.  <br/> |
|[Item](item.md) <br/> |Representa un elemento genérico de Exchange.  <br/> |
|[Elemento (UploadItemType)](item-uploaditemtype.md) <br/> |Representa un solo elemento va a cargar en un buzón de correo.  <br/> |
|[ItemChange](itemchange.md) <br/> |Contiene un identificador de elemento y las actualizaciones que se debe aplicar al elemento.  <br/><br/> La siguiente es la expresión de XPath para este elemento: <br/> <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
|[ItemId](itemids.md) <br/> | Contiene las identidades únicas de los elementos, elementos de aparición y periódicos elementos maestros que se usa para eliminar, enviar, obtener, mover o copiar elementos en el almacén de Exchange. <br/> <br/>  Los siguientes son las expresiones de XPath para este elemento: <br/> <br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/>  `/MoveItem/ItemIds` <br/>  `/CopyItem//ItemIds` <br/> |
|[ItemId (NonEmptyArrayOfItemIdsType)](itemids-nonemptyarrayofitemidstype.md) <br/> |Contiene una matriz de identificadores de elemento que identifican los elementos que desee exportar desde un buzón de correo.  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |Representa la última aparición de un elemento periódico del calendario.  <br/> |
|[Buzón de correo](mailbox.md) <br/> |Identifica un objeto de servicio de directorio de Active Directory habilitados para correo.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa la cancelación de la reunión en el almacén de Exchange.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el almacén de Exchange.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta a la reunión en el almacén de Exchange.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico de Exchange.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Representa un evento que se produce cuando se modifica un elemento.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Representa un evento que se produce cuando un elemento se mueve desde la carpeta principal de una a otra carpeta primaria.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Representa un evento que se desencadena por un nuevo elemento de correo en un buzón de correo.  <br/> |
|[Repetición](occurrence.md) <br/> |Representa una sola aparición de modificación de un elemento periódico del calendario.  <br/> |
|[PlayOnPhone (servicios Web de Exchange)](playonphone-exchange-web-services.md) <br/> |Representa una solicitud para leer un elemento en un teléfono.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Quita un elemento desde el almacén de Exchange.  <br/> |
|[RoomList](roomlist.md) <br/> |Representa una dirección de correo electrónico que identifica una lista de las salas de reuniones.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea en el almacén de Exchange.  <br/> |
|[UploadItemsResponseMessage](uploaditemsresponsemessage.md) <br/> |Contiene el estado y los resultados de una solicitud para cargar un elemento de un solo buzón de correo.  <br/> |
|[UserConfiguration](userconfiguration.md) <br/> |Define un objeto de configuración de usuario único.  <br/> |
   
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

- [Operación ExportItems](exportitems-operation.md)
- [Operación UploadItems](uploaditems-operation.md) 
- [Operación de FindConversation](findconversation-operation.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

