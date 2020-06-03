---
title: AppendToItemField
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AppendToItemField
api_type:
- schema
ms.assetid: 66dbcb4a-ae6d-4648-8610-67187bdb105c
description: El elemento AppendToItemField identifica los datos que se van a anexar a una única propiedad de un elemento durante una operación de UpdateItem.
ms.openlocfilehash: 902239155bff45d6f81989de954c9459cf012288
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466048"
---
# <a name="appendtoitemfield"></a>AppendToItemField

El elemento **AppendToItemField** identifica los datos que se van a anexar a una única propiedad de un elemento durante una [operación de UpdateItem](updateitem-operation.md).
  
- [UpdateItem](updateitem.md)
  
- [ItemChanges](itemchanges.md)
  
- [ItemChange](itemchange.md)
  
- [Actualizaciones (elemento)](updates-item.md)
  
- [AppendToItemField](appendtoitemfield.md)
  
```xml
<AppendToItemField>
   <FieldURI/>
   <Item/>
</AppendToItemField>
```

 **AppendToItemFieldType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifica las propiedades a las que se hace referencia con frecuencia mediante el URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifica a los miembros individuales de un diccionario.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifica las propiedades MAPI extendidas que se van a anexar.  <br/> |
|[Elemento](item.md) <br/> |Representa un elemento en el almacén de Exchange.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico de Exchange.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange.  <br/> |
|[Contacto](contact.md) <br/> |Representa un elemento de contacto de Exchange.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el almacén de Exchange.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta a una reunión en el almacén de Exchange.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en el almacén de Exchange.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea del almacén de Exchange.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Actualizaciones (elemento)](updates-item.md) <br/> |Contiene una matriz que define los cambios de anexión, establecimiento y eliminación en las propiedades de elemento.  <br/> La siguiente es la expresión XPath a este elemento:`/UpdateItem/ItemChanges/ItemChange[i]/Updates` <br/> |
   
## <a name="remarks"></a>Comentarios

Solo algunas propiedades admiten operaciones de anexión. Si se intenta anexar a una propiedad que no admite la anexión, se producirá un error.
  
Para las operaciones de actualización, solo se puede modificar una propiedad en una sola solicitud. Se debe hacer referencia a esa propiedad única en el elemento [path](path.md) . El elemento **Item** de las clases derivadas solo puede contener una única propiedad que esté dentro del acuerdo con el elemento **path** único. 
  
> [!NOTE]
> El elemento [path](path.md) es abstracto. Debe sustituirse por el elemento [FieldURI](fielduri.md), [IndexedFieldURI](indexedfielduri.md)o [ExtendedFieldURI](extendedfielduri.md) . 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación UpdateItem](updateitem-operation.md)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

