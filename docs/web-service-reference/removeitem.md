---
title: RemoveItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RemoveItem
api_type:
- schema
ms.assetid: 766878e3-9007-454f-8501-45139bc5c0e2
description: El elemento RemoveItem representa un objeto de respuesta que se usa para quitar un elemento de reunión cuando se recibe un mensaje MeetingCancellation.
ms.openlocfilehash: c0cd5c1f9894287ee78c2f7a65b8f4d3b943414e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467693"
---
# <a name="removeitem"></a>RemoveItem

El elemento **RemoveItem** representa un objeto de respuesta que se usa para quitar un elemento de reunión cuando se recibe un mensaje MeetingCancellation. 
  
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
|**ObjectName** <br/> |Representa el nombre de la clase de objeto de respuesta de RemoveItem como una cadena en inglés.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ReferenceItemId](referenceitemid.md) <br/> |Identifica el elemento al que hace referencia el objeto de respuesta RemoveItem.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Elementos (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Contiene una matriz de elementos que se van a crear en la carpeta identificada por el elemento [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Contiene una colección de todos los objetos de respuesta que están asociados a un elemento en el almacén de Exchange.  <br/> |
   
## <a name="remarks"></a>Comentarios

 **RemoveItem** solo es válido para [MeetingCancellation](meetingcancellation.md). De lo contrario, se produce un error.
  
> [!NOTE]
> El [ItemClass](itemclass.md) de una cancelación de reunión es IPM. Program. Meeting. Canceled. 
  
Para quitar la propiedad [MeetingRequest](meetingrequest.md) y la [CalendarItem](calendaritem.md)asociada, use el objeto de respuesta [DeclineItem](declineitem.md) en lugar de **RemoveItem**.
  
 No se admite **RemoveItem** para el acceso de delegado. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

