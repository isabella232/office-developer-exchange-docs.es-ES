---
title: UpdateItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: 5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4
description: La operación UpdateItem se usa para modificar las propiedades de un elemento existente en el almacén de Exchange.
ms.openlocfilehash: 009ba16315017c4418fbd71d49744015c4d6d1b1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840841"
---
# <a name="updateitem-operation"></a>UpdateItem Operation

La operación **UpdateItem** se usa para modificar las propiedades de un elemento existente en el almacén de Exchange. 
  
## <a name="remarks"></a>Comentarios

Se pueden realizar tres acciones de actualización básica en un elemento. En la siguiente tabla se enumera las acciones que puede realizar.
  
|**Acción**|**Descripción**|
|:-----|:-----|
|Anexar  <br/> |Agrega datos a una propiedad existente. Esta acción conserva los datos actuales. Append no se aplica a todas las propiedades.  <br/> |
|Activado  <br/> |Reemplaza los datos de una propiedad si la propiedad contiene datos, o crea la propiedad y establece su valor si la propiedad no existe. La acción de conjunto sólo es aplicable a propiedades modificables.  <br/> |
|Eliminar  <br/> |Quita una propiedad de un elemento. Esto difiere de la configuración de una propiedad en un valor vacío. Cuando finalice esta acción, la propiedad no existe para el elemento. Eliminar solo es aplicable a las propiedades de escritura.  <br/> |
   
Una llamada **UpdateItem** puede utilizarse para modificar uno o varios elementos y una o varias propiedades de cada elemento. El elemento [ItemChanges](itemchanges.md) contiene todas las modificaciones que se van a realizar como parte de esta llamada. El elemento [ItemChange](itemchange.md) , un elemento secundario del elemento [ItemChanges](itemchanges.md) , representa las modificaciones que se debe realizar en un solo elemento. El elemento [ItemChange](itemchange.md) contiene un conjunto de acciones de actualización que se pueden realizar en un solo elemento. Estos cambios se encuentran en el elemento de [actualizaciones (elemento)](updates-item.md) . El elemento [ItemId](itemid.md) identifica el elemento que se debe actualizar. Para actualizar más de una propiedad en un elemento, se debe proporcionar un [SetItemField](setitemfield.md), [AppendToItemField](appendtoitemfield.md)o [DeleteItemField](deleteitemfield.md) para cada propiedad que requiere la actualización. 
  
> [!NOTE]
> Acciones de actualización se aplican en el orden en que se especifican. 
  
Para cada cambio, es necesario especificar la ruta de acceso de la propiedad que se va a cambiar y una representación de ese elemento con su nuevo valor. La acción de eliminar es ligeramente diferente en que se requiere sólo la ruta de acceso de la propiedad que se debe eliminar. Para establecer y anexar acciones, la ruta de acceso especificada debe hacer referencia a la misma propiedad que se va a establecer en la representación del artículo. Si estos difieren, se devolverá un error.
  
La operación **UpdateItem** puede establecer la hora de [Inicio](start.md) y [final](end-ex15websvcsotherref.md) de un elemento del almacén de Exchange. En una solicitud **UpdateItem** , se puede establecer la hora de [Inicio](start.md) sin establecer también la hora de [finalización](end-ex15websvcsotherref.md) . Esto puede producir un error si la hora de [Inicio](start.md) es posterior a la hora de [finalización](end-ex15websvcsotherref.md) . Tenga en cuenta que las aplicaciones cliente deben ajustar la hora de [finalización](end-ex15websvcsotherref.md) cuando se cambia la hora de [Inicio](start.md) con el fin de conservar la duración. 
  
Cuando se actualiza un elemento de calendario único se convierta en un elemento periódico del calendario principal, se debe establecer la propiedad [MeetingTimeZone](meetingtimezone.md) por la operación **UpdateItem** con el fin de conservar la zona horaria de original del elemento de calendario. 
  
## <a name="setitemfield-request-example"></a>Ejemplo de solicitud de SetItemField

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de **UpdateItem** muestra cómo establecer la propiedad sensitivity de un elemento. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEFkb..." ChangeKey="CQAAABYAAAB..."/>
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Sensitivity"/>
              <t:Message>
                <t:Sensitivity>Normal</t:Sensitivity>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

El identificador de elemento y la clave de cambio se han abreviado para conservar la legibilidad.
  
### <a name="setitemfield-request-elements"></a>Elementos de solicitud de SetItemField

En la solicitud se usan los siguientes elementos:
  
- [UpdateItem](updateitem.md)
    
- [ItemChanges](itemchanges.md)
    
- [ItemChange](itemchange.md)
    
- [ItemId](itemid.md)
    
- [Actualizaciones (elemento)](updates-item.md)
    
- [SetItemField](setitemfield.md)
    
- [FieldURI](fielduri.md)
    
- [Message](message-ex15websvcsotherref.md)
    
- [Sensibilidad](sensitivity.md)
    
## <a name="appendtoitemfield-request-example"></a>Ejemplo de solicitud de AppendToItemField

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de **UpdateItem** muestra cómo anexar texto a la propiedad body en un elemento. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEFkbW..." ChangeKey="CQAAABYA..."/>
          <t:Updates>
            <t:AppendToItemField>
              <t:FieldURI FieldURI="item:Body"/>
              <t:Message>
                <t:Body BodyType="Text">Some additional text to append</t:Body>
              </t:Message>
            </t:AppendToItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

Las siguientes propiedades admiten la acción de datos anexados:
  
- **mensaje: ReplyTo**
    
- **Cuerpo del elemento:**
    
- Todos los del destinatario y attendee propiedades de la colección
    
El identificador de elemento y la clave de cambio se han abreviado para conservar la legibilidad.
  
### <a name="appendtoitemfield-request-elements"></a>Elementos de solicitud de AppendToItemField

En la solicitud se usan los siguientes elementos:
  
- [UpdateItem](updateitem.md)
    
- [ItemChanges](itemchanges.md)
    
- [ItemChange](itemchange.md)
    
- [ItemId](itemid.md)
    
- [Actualizaciones (elemento)](updates-item.md)
    
- [AppendToItemField](appendtoitemfield.md)
    
- [FieldURI](fielduri.md)
    
- [Message](message-ex15websvcsotherref.md)
    
- [Body](body.md)
    
## <a name="deleteitemfield-request-example"></a>Ejemplo de solicitud de DeleteItemField

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de **UpdateItem** muestra cómo eliminar una propiedad en un elemento. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEFkbWluaXN0cm..." ChangeKey="CQAAABYAA..."/>
          <t:Updates>
            <t:DeleteItemField>
              <t:FieldURI FieldURI="item:Body"/>
            </t:DeleteItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

El identificador de elemento y la clave de cambio se han abreviado para conservar la legibilidad.
  
### <a name="deleteitemfield-request-elements"></a>Elementos de solicitud de DeleteItemField

En la solicitud se usan los siguientes elementos:
  
- [UpdateItem](updateitem.md)
    
- [ItemChanges](itemchanges.md)
    
- [ItemChange](itemchange.md)
    
- [ItemId](itemid.md)
    
- [Actualizaciones (elemento)](updates-item.md)
    
- [DeleteItemField](deleteitemfield.md)
    
- [FieldURI](fielduri.md)
    
## <a name="successful-response-example"></a>Ejemplo de la respuesta es correcta

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta a una solicitud de **UpdateItem** correcta. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
  xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="664" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <UpdateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UpdateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="AAAtAEFkbW..." ChangeKey="CQAAABYAAA..."/>
            </t:Message>
          </m:Items>
        </m:UpdateItemResponseMessage>
      </m:ResponseMessages>
    </UpdateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

El identificador de elemento y la clave de cambio se han abreviado para conservar la legibilidad.
  
### <a name="successful-response-elements"></a>Elementos de respuesta correcta

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateItemResponse](updateitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [UpdateItemResponseMessage](updateitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Items](items.md)
    
- [Message](message-ex15websvcsotherref.md)
    
- [ItemId](itemid.md)
    
## <a name="see-also"></a>Vea también



[Operación UpdateItem (tarea)](updateitem-operation-task.md)
  
[Operación UpdateItem (contacto)](updateitem-operation-contact.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


[Actualizar contactos](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[Actualización de tareas](http://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)

