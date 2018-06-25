---
title: Elementos
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Items
api_type:
- schema
ms.assetid: 0811a73e-bf1f-4889-9219-73902dd47639
description: El elemento de elementos contiene una matriz de elementos.
ms.openlocfilehash: 241a56ee23e87d6a4320b93cc65b1f5aa1f60120
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836163"
---
# <a name="items"></a>Elementos

El elemento de **elementos** contiene una matriz de elementos. 
  
```xml
<Items>
   <Item/>
   <Message/>
   <CalendarItem/>
   <Contact/>
   <DistributionList/>
   <MeetingMessage/>
   <MeetingRequest/>
   <MeetingResponse/>
   <MeetingCancellation/>
   <Task/>
   <PostItem/>
</Items>
```

 **ArrayOfRealItemsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Item](item.md) <br/> |Representa un elemento en el almacén de Exchange.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico de Exchange.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange.  <br/> |
|[Contact](contact.md) <br/> |Representa un elemento de contacto de Exchange.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa un mensaje de reunión en el almacén de Exchange.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta a la reunión en el almacén de Exchange.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa la cancelación de la reunión en el almacén de Exchange.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea en el almacén de Exchange.  <br/> |
|[Objeto postItem](postitem.md) <br/> |Representa un elemento para exponer en el almacén de Exchange.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[CopyItemResponseMessage](copyitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación CopyItem](copyitem-operation.md) .  <br/> |
|[CreateItemResponseMessage](createitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud [CreateItem operation](createitem-operation.md) .  <br/> |
|[GetItemResponseMessage](getitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [GetItem operation](getitem-operation.md) .  <br/> |
|[GroupedItems](groupeditems.md) <br/> |Representa una colección de elementos que son el resultado de una [operación FindItem](finditem-operation.md) de agrupada de llamadas.  <br/> |
|[MoveItemResponseMessage](moveitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación MoveItem](moveitem-operation.md) .  <br/> |
|[RootFolder (FindItemResponseMessage)](rootfolder-finditemresponsemessage.md) <br/> |Contiene los resultados de una búsqueda de una sola carpeta raíz durante una [operación de FindItem](finditem-operation.md).  <br/> |
|[UpdateItemResponseMessage](updateitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación UpdateItem](updateitem-operation.md) .  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener información sobre el conjunto de elementos en una solicitud de [operación CreateItem](createitem-operation.md) , vea [elementos (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md).
  
Elementos del [mensaje](message-ex15websvcsotherref.md) representan los mensajes de correo electrónico y todos los otros elementos que no están fuertemente tipados por el esquema de Exchange Web Services (EWS). Elementos como IPM. Uso compartido y IPM.InfoPath se devuelven como elementos del **mensaje** . Las versiones de Exchange a partir de Exchange Server 2010 no devuelven el elemento base del [elemento](item.md) en las respuestas. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Referencia EWS para Exchange](ews-reference-for-exchange.md)
  
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

