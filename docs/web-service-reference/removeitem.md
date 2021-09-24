---
title: RemoveItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RemoveItem
api_type:
- schema
ms.assetid: 766878e3-9007-454f-8501-45139bc5c0e2
description: El elemento RemoveItem representa un objeto de respuesta que se usa para quitar un elemento de reunión cuando se recibe un mensaje MeetingCancellation.
ms.openlocfilehash: 4dbe9ede36bf6e3c008a2186cfe617519ecfae1f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517962"
---
# <a name="removeitem"></a>RemoveItem

El **elemento RemoveItem** representa un objeto de respuesta que se usa para quitar un elemento de reunión cuando se recibe un mensaje MeetingCancellation. 
  
```xml
<RemoveItem ObjectName="">
   <ReferenceItemId/>
</RemoveItem>
```

 **RemoveItemType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**ObjectName** <br/> |Representa el nombre de la clase de objeto de respuesta RemoveItem como una cadena en inglés.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ReferenceItemId](referenceitemid.md) <br/> |Identifica el elemento al que hace referencia el objeto de respuesta RemoveItem.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Contiene una matriz de elementos para crear en la carpeta identificada por el [elemento ParentFolderId (TargetFolderIdType).](parentfolderid-targetfolderidtype.md)  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Contiene una colección de todos los objetos de respuesta asociados con un elemento del Exchange almacén.  <br/> |
   
## <a name="remarks"></a>Comentarios

 **RemoveItem** solo es válido para [un objeto MeetingCancellation](meetingcancellation.md). De lo contrario, se produce un error.
  
> [!NOTE]
> ItemClass [para](itemclass.md) una cancelación de reunión es IPM. Schedule.Meeting.Canceled. 
  
Para quitar un [Objeto MeetingRequest](meetingrequest.md) y el [objeto CalendarItem](calendaritem.md)asociado, use el objeto de respuesta [DeclineItem](declineitem.md) en lugar de **RemoveItem**.
  
 **RemoveItem** no se admite para el acceso delegado. 
  
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

