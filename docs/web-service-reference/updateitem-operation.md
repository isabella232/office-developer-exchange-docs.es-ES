---
title: Operación UpdateItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: 5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4
description: La operación UpdateItem se usa para modificar las propiedades de un elemento existente en el Exchange almacén.
ms.openlocfilehash: 6ac09c24c13efff8053fc605ec2c0e6cf2957429
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514063"
---
# <a name="updateitem-operation"></a>Operación UpdateItem

La **operación UpdateItem** se usa para modificar las propiedades de un elemento existente en el Exchange almacén. 
  
## <a name="remarks"></a>Comentarios

Puede realizar tres acciones básicas de actualización en un elemento. En la tabla siguiente se enumeran las acciones que puede realizar.
  
|**Action**|**Descripción**|
|:-----|:-----|
|Anexar  <br/> |Agrega datos a una propiedad existente. Esta acción conserva los datos actuales. Append no se aplica a todas las propiedades.  <br/> |
|Set  <br/> |Reemplaza los datos de una propiedad si la propiedad contiene datos o crea la propiedad y establece su valor si la propiedad no existe. La acción set solo se aplica a las propiedades que se pueden escribir.  <br/> |
|Eliminar  <br/> |Quita una propiedad de un elemento. Esto difiere de establecer una propiedad en un valor vacío. Una vez finalizada esta acción, la propiedad no existe para el elemento. Eliminar solo se aplica a las propiedades que se pueden escribir.  <br/> |
   
Se puede usar una llamada **UpdateItem** para modificar uno o varios elementos y una o más propiedades en cada elemento. El [elemento ItemChanges](itemchanges.md) contiene todas las modificaciones que se van a realizar como parte de esta llamada. El [elemento ItemChange,](itemchange.md) un elemento secundario del [elemento ItemChanges,](itemchanges.md) representa las modificaciones que se deben realizar en un solo elemento. El [elemento ItemChange](itemchange.md) contiene un conjunto de acciones de actualización que se pueden realizar en un solo elemento. Estos cambios se incluyen en el [elemento Updates (Item).](updates-item.md) El [elemento ItemId](itemid.md) identifica el elemento que se debe actualizar. Para actualizar más de una propiedad en un elemento, se debe proporcionar un [SetItemField](setitemfield.md), [AppendToItemField](appendtoitemfield.md)o [DeleteItemField](deleteitemfield.md) para cada propiedad que requiera la actualización. 
  
> [!NOTE]
> Las acciones de actualización se aplican en el orden en que se especifican. 
  
Para cada cambio, debe especificar la ruta de acceso de la propiedad que se va a cambiar y una representación de ese elemento con su nuevo valor. La acción eliminar es ligeramente diferente, ya que solo se requiere la ruta de acceso de la propiedad que se debe eliminar. Para establecer y anexar acciones, la ruta de acceso especificada debe hacer referencia a la misma propiedad que se establece en la representación del elemento. Si difieren, se devolverá un error.
  
La **operación UpdateItem** puede establecer [la](start.md) hora [de](end-ex15websvcsotherref.md) inicio y finalización de un Exchange de almacenamiento. En una **solicitud UpdateItem,** la [hora de](start.md) inicio se puede establecer sin establecer también la hora [de](end-ex15websvcsotherref.md) finalización. Esto puede provocar un error si la [hora de](start.md) inicio es posterior a la [hora de ](end-ex15websvcsotherref.md) finalización. Tenga en cuenta que las aplicaciones cliente deben ajustar la [hora ](end-ex15websvcsotherref.md) de finalización cuando se cambia la [hora](start.md) de inicio para conservar la duración. 
  
Cuando se actualiza un único elemento de calendario para convertirse en un elemento de calendario maestro periódico, la operación **UpdateItem** debe establecer la propiedad [MeetingTimeZone](meetingtimezone.md) para conservar la zona horaria original del elemento de calendario. 
  
## <a name="setitemfield-request-example"></a>Ejemplo de solicitud SetItemField

### <a name="description"></a>Descripción

En el siguiente ejemplo de una **solicitud UpdateItem** se muestra cómo establecer la propiedad sensitivity en un elemento. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

El identificador del elemento y la clave de cambio se han acortado para conservar la legibilidad.
  
### <a name="setitemfield-request-elements"></a>Elementos de solicitud SetItemField

En la solicitud se usan los siguientes elementos:
  
- [UpdateItem](updateitem.md)
    
- [ItemChanges](itemchanges.md)
    
- [ItemChange](itemchange.md)
    
- [ItemId](itemid.md)
    
- [Updates (Elemento)](updates-item.md)
    
- [SetItemField](setitemfield.md)
    
- [FieldURI](fielduri.md)
    
- [Mensaje](message-ex15websvcsotherref.md)
    
- [Sensitivity](sensitivity.md)
    
## <a name="appendtoitemfield-request-example"></a>Ejemplo de solicitud AppendToItemField

### <a name="description"></a>Descripción

En el siguiente ejemplo de una **solicitud UpdateItem** se muestra cómo anexar texto a la propiedad body de un elemento. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

Las siguientes propiedades admiten la acción anexar:
  
- **message:ReplyTo**
    
- **item:Body**
    
- Todas las propiedades de la colección de destinatarios y asistentes
    
El identificador del elemento y la clave de cambio se han acortado para conservar la legibilidad.
  
### <a name="appendtoitemfield-request-elements"></a>Elementos de solicitud AppendToItemField

En la solicitud se usan los siguientes elementos:
  
- [UpdateItem](updateitem.md)
    
- [ItemChanges](itemchanges.md)
    
- [ItemChange](itemchange.md)
    
- [ItemId](itemid.md)
    
- [Updates (Elemento)](updates-item.md)
    
- [AppendToItemField](appendtoitemfield.md)
    
- [FieldURI](fielduri.md)
    
- [Mensaje](message-ex15websvcsotherref.md)
    
- [Cuerpo](body.md)
    
## <a name="deleteitemfield-request-example"></a>Ejemplo de solicitud DeleteItemField

### <a name="description"></a>Descripción

En el siguiente ejemplo de una **solicitud UpdateItem** se muestra cómo eliminar una propiedad en un elemento. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

El identificador del elemento y la clave de cambio se han acortado para conservar la legibilidad.
  
### <a name="deleteitemfield-request-elements"></a>Elementos de solicitud DeleteItemField

En la solicitud se usan los siguientes elementos:
  
- [UpdateItem](updateitem.md)
    
- [ItemChanges](itemchanges.md)
    
- [ItemChange](itemchange.md)
    
- [ItemId](itemid.md)
    
- [Updates (Elemento)](updates-item.md)
    
- [DeleteItemField](deleteitemfield.md)
    
- [FieldURI](fielduri.md)
    
## <a name="successful-response-example"></a>Ejemplo de respuesta correcta

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta correcta a una **solicitud UpdateItem.** 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
  xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="664" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <UpdateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

El identificador del elemento y la clave de cambio se han acortado para conservar la legibilidad.
  
### <a name="successful-response-elements"></a>Elementos de respuesta correctos

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateItemResponse](updateitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [UpdateItemResponseMessage](updateitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Items](items.md)
    
- [Mensaje](message-ex15websvcsotherref.md)
    
- [ItemId](itemid.md)
    
## <a name="see-also"></a>Ver también



[Operación UpdateItem (tarea)](updateitem-operation-task.md)
  
[Operación UpdateItem (contacto)](updateitem-operation-contact.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


[Actualizar contactos](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[Actualizar tareas](https://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)

