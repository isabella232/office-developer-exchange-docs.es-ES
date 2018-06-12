---
title: SetItemField
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetItemField
api_type:
- schema
ms.assetid: 85284fcb-bd1e-4fda-9dab-cb4cd637cd5b
description: El elemento SetItemField representa una actualización para una única propiedad de un elemento en una operación UpdateItem.
ms.openlocfilehash: 012e6ae21af653b4bf12588e5a97334a62884059
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837439"
---
# <a name="setitemfield"></a>SetItemField

El elemento **SetItemField** representa una actualización para una única propiedad de un elemento en una [operación de UpdateItem](updateitem-operation.md).
  
```xml
<SetItemField>
   <FieldURI/>
   <Item/>
</SetItemField>
```

 **SetItemFieldType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifica a los miembros individuales de un diccionario.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifica las propiedades extendidas de MAPI para establecer.  <br/> |
|[Item](item.md) <br/> |Representa un elemento en el almacén de Exchange.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico de Exchange para actualizar.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange para actualizar.  <br/> |
|[Contact](contact.md) <br/> |Representa un elemento de contacto de Exchange para actualizar.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución que se debe actualizar.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa un mensaje de reunión que se debe actualizar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión que se debe actualizar.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta a la reunión que se debe actualizar.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión que se debe actualizar.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea que se debe actualizar.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Actualizaciones (elemento)](updates-item.md) <br/> |Contiene un conjunto de elementos que definen append, establecer y eliminar los cambios realizados en las propiedades de elementos.  <br/> |
   
## <a name="remarks"></a>Notas

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación UpdateItem](updateitem-operation.md)

