---
title: ItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- ItemId
api_type:
- schema
ms.assetid: 3350b597-57a0-4961-8f44-8624946719b4
description: El elemento ItemId contiene el identificador único y la clave de cambio de un elemento en el almacén de Exchange.
localization_priority: Priority
ms.openlocfilehash: d5931702225c6864b1ca60a6f0753b65f65aca30
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44441565"
---
# <a name="itemid"></a>ItemId

El elemento **Itemid** contiene el identificador único y la clave de cambio de un elemento en el almacén de Exchange. 
  
```XML
<ItemId Id="" ChangeKey="" />
```

 **ItemIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Id** <br/> |Identifica un elemento específico en el almacén de Exchange. **ID** distingue mayúsculas de minúsculas; por lo tanto, las comparaciones entre **identificadores** deben distinguir mayúsculas de minúsculas o binarias.  <br/> |
|**ChangeKey** <br/> | Identifica una versión específica de un elemento. <br/><br/>Se necesita un **changekey** para los siguientes escenarios: <br/> <br/>-El elemento [UpdateItem](updateitem.md) requiere un **changekey** si el atributo **ConflictResolution** está establecido en autoresolve. Autoresolve es un valor predeterminado. Si no se incluye el atributo **changekey** , la respuesta devolverá un valor de [ResponseCode](responsecode.md) igual a **ErrorChangeKeyRequired**.  <br/><br/>-El elemento [SendItem](senditem.md) requiere un **changekey** para comprobar si la operación que se ha intentado actuar? a en la versión más reciente de un elemento. Si el atributo **changekey** no se incluye en **Itemid** o si **changekey** está vacío, la respuesta devolverá un valor [ResponseCode](responsecode.md) igual a **ErrorStaleObject**.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange.  <br/> |
|[Contacto](contact.md) <br/> |Representa un elemento de contacto de Exchange.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Representa un evento cuando se copia un elemento o una carpeta.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Representa un evento cuando se crea un elemento o una carpeta.  <br/> |
|[Eliminar (ItemSync)](delete-itemsync.md) <br/> |Identifica un solo elemento que se va a eliminar en el almacén de cliente local.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Representa un evento cuando se elimina un elemento o una carpeta.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[ExportItemsResponseMessage](exportitemsresponsemessage.md) <br/> |Contiene el estado y los resultados de una solicitud para exportar un solo elemento de buzón.  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |Representa la primera aparición de un elemento de calendario periódico.  <br/> |
|[GlobalItemIds](globalitemids.md) <br/> |Contiene la colección de identificadores de elemento para todos los elementos de conversación en un buzón.  <br/> |
|[Ignore](ignore.md) <br/> |Identifica los elementos que se deben omitir durante la sincronización.  <br/> |
|[Elemento](item.md) <br/> |Representa un elemento de Exchange genérico.  <br/> |
|[Item (UploadItemType)](item-uploaditemtype.md) <br/> |Representa un solo elemento que se va a cargar en un buzón.  <br/> |
|[ItemChange](itemchange.md) <br/> |Contiene un identificador de elemento y las actualizaciones que se aplican al elemento.  <br/><br/> La siguiente es la expresión XPath a este elemento: <br/> <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
|[ItemIds](itemids.md) <br/> | Contiene las identidades únicas de los elementos, los elementos de ocurrencia y los elementos maestros periódicos usados para eliminar, enviar, obtener, mover o copiar elementos en el almacén de Exchange. <br/> <br/>  Las siguientes son las expresiones XPath de este elemento: <br/> <br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/>  `/MoveItem/ItemIds` <br/>  `/CopyItem//ItemIds` <br/> |
|[ItemIds (NonEmptyArrayOfItemIdsType)](itemids-nonemptyarrayofitemidstype.md) <br/> |Contiene una matriz de identificadores de elementos que identifican los elementos que se exportarán de un buzón.  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |Representa la última repetición de un elemento de calendario periódico.  <br/> |
|[Buzón](mailbox.md) <br/> |Identifica un objeto de servicio de directorio de Active Directory habilitado para correo.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en el almacén de Exchange.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el almacén de Exchange.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta a una reunión en el almacén de Exchange.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico de Exchange.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Representa un evento que se produce cuando se modifica un elemento.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Representa un evento que se produce cuando un elemento se mueve de una carpeta principal a otra carpeta principal.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Representa un evento desencadenado por un nuevo elemento de correo en un buzón.  <br/> |
|[Suceda](occurrence.md) <br/> |Representa una ocurrencia única modificada de un elemento de calendario periódico.  <br/> |
|[Reproducir (servicios web Exchange)](playonphone-exchange-web-services.md) <br/> |Representa una solicitud para leer un elemento en un teléfono.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Quita un elemento del almacén de Exchange.  <br/> |
|[RoomList](roomlist.md) <br/> |Representa una dirección de correo electrónico que identifica una lista de salas de reuniones.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea del almacén de Exchange.  <br/> |
|[UploadItemsResponseMessage](uploaditemsresponsemessage.md) <br/> |Contiene el estado y los resultados de una solicitud para cargar un solo elemento de buzón.  <br/> |
|[UserConfiguration](userconfiguration.md) <br/> |Define un objeto de configuración de usuario único.  <br/> |
   
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

- [Operación ExportItems](exportitems-operation.md)
- [Operación UploadItems](uploaditems-operation.md) 
- [Operación FindConversation](findconversation-operation.md)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

