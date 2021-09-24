---
title: Elementos
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Items
api_type:
- schema
ms.assetid: 0811a73e-bf1f-4889-9219-73902dd47639
description: El elemento Items contiene una matriz de elementos.
ms.openlocfilehash: b6e9db6524640098a902f431393fccd6bd4e8868
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540890"
---
# <a name="items"></a>Elementos

El **elemento Items** contiene una matriz de elementos. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Item](item.md) <br/> |Representa un elemento en el Exchange almacén.  <br/> |
|[Mensaje](message-ex15websvcsotherref.md) <br/> |Representa un Exchange de correo electrónico.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un Exchange de calendario.  <br/> |
|[Contact](contact.md) <br/> |Representa un Exchange de contacto.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa un mensaje de reunión en el Exchange almacén.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una solicitud de reunión en Exchange almacén.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta de reunión en Exchange almacén.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en el Exchange local.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea en el Exchange almacén.  <br/> |
|[PostItem](postitem.md) <br/> |Representa un elemento de publicación en el Exchange almacén.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CopyItemResponseMessage](copyitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación CopyItem.](copyitem-operation.md)  <br/> |
|[CreateItemResponseMessage](createitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una única [solicitud de operación CreateItem.](createitem-operation.md)  <br/> |
|[GetItemResponseMessage](getitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación GetItem.](getitem-operation.md)  <br/> |
|[GroupedItems](groupeditems.md) <br/> |Representa una colección de elementos que son el resultado de una llamada de operación [FindItem](finditem-operation.md) agrupada.  <br/> |
|[MoveItemResponseMessage](moveitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación MoveItem.](moveitem-operation.md)  <br/> |
|[RootFolder (FindItemResponseMessage)](rootfolder-finditemresponsemessage.md) <br/> |Contiene los resultados de una búsqueda de una sola carpeta raíz durante una [operación FindItem](finditem-operation.md).  <br/> |
|[UpdateItemResponseMessage](updateitemresponsemessage.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación UpdateItem.](updateitem-operation.md)  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener información sobre el conjunto de elementos de una solicitud de operación [CreateItem,](createitem-operation.md) vea [Items (NonEmptyArrayOfAllItemsType).](items-nonemptyarrayofallitemstype.md)
  
[Los](message-ex15websvcsotherref.md) elementos message representan mensajes de correo electrónico y todos los demás elementos que no están fuertemente especificados por el esquema Exchange Web Services (EWS). Elementos como IPM. El uso compartido y IPM.InfoPath se devuelven como **elementos Message.** Las versiones Exchange a partir de Exchange Server 2010 no devuelven el [elemento Item](item.md) base en las respuestas. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Exchange que tiene instalado el rol de servidor acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Referencia EWS para Exchange](ews-reference-for-exchange.md)
  
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

