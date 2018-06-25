---
title: Operación CreateItem (tarea)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateItem
api_type:
- schema
ms.assetid: 12c5da4d-290c-4a8a-a965-0bf5d55c7978
description: La operación CreateItem crea los elementos de tarea en el almacén de Exchange.
ms.openlocfilehash: 5a5203202071ae9391faa9348902424317ee96d1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763954"
---
# <a name="createitem-operation-task"></a>Operación CreateItem (tarea)

La operación CreateItem crea los elementos de tarea en el almacén de Exchange.
  
## <a name="task-createitem-request"></a>Solicitud de tarea CreateItem

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud CreateItem muestra cómo crear un elemento de tarea en un buzón de correo.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                MessageDisposition="SaveOnly">
      <Items>
        <t:Task>
          <t:Subject>My task</t:Subject>
          <t:DueDate>2006-10-26T21:32:52</t:DueDate>
          <t:Status>NotStarted</t:Status>
        </t:Task>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

Las solicitudes para las tareas repetitivas se modificarán cuando se reciben por el equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente. Se producen los siguientes cambios:
  
- Se guarda sólo la fecha para la propiedad [StartDate (periodicidad)](startdate-recurrence.md) del intervalo de periodicidad de la tarea. El elemento de tiempo se trunca. 
    
- Se pueden ajustar la propiedad [StartDate (periodicidad)](startdate-recurrence.md) , según el patrón de periodicidad. Por ejemplo, si se especifica el patrón de periodicidad como todos los lunes y StartDate está establecida en 26 de octubre de 2006, que es un jueves, StartDate se ajusta a 30 de octubre de 2006, que es el próximo lunes. 
    
- Si se establece la propiedad [StartDate](startdate.md) de la tarea, se actualiza para que coincida con la [StartDate (periodicidad)](startdate-recurrence.md) del intervalo de periodicidad. La propiedad [DueDate](duedate.md) de la tarea también se actualiza según el nuevo [StartDate](startdate.md).
    
- Si no está establecido el [StartDate](startdate.md) , sólo la propiedad [DueDate](duedate.md) se actualiza para que coincida con la [StartDate (periodicidad)](startdate-recurrence.md) del intervalo de periodicidad. 
    
La siguiente tabla muestran los cambios que realiza el servidor de acceso de cliente a una tarea periódica que tiene un Task.Recurrence.Pattern de todos los lunes.
  
**Cambios realizados en una tarea periódica**

|**Propiedad**|**Valor original**|**Valor actualizado**|
|:-----|:-----|:-----|
|Task.StartDate  <br/> |1 de enero de 2006  <br/> |30 de octubre de 2006  <br/> |
|Task.DueDate  <br/> |3 de enero de 2006  <br/> |1 de noviembre de 2006  <br/> |
|Task.Recurrence.Range.StartDate  <br/> |26 de octubre de 2006  <br/> |30 de octubre de 2006  <br/> |
   
De forma predeterminada, si no se especifica una carpeta de destino, se crean elementos de tarea en la carpeta tareas.
  
### <a name="request-elements"></a>Elementos de solicitud

En la solicitud se usan los siguientes elementos:
  
- [CreateItem](createitem.md)
    
- [Elementos (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md)
    
- [Tarea](task.md)
    
- [Subject](subject.md)
    
- [DueDate](duedate.md)
    
- [Status](status.md)
    
## <a name="successful-task-createitem-response"></a>Respuesta de CreateItem correcta de la tarea

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta correcta a la solicitud CreateItem.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Task>
              <t:ItemId Id="AAAtAE=" ChangeKey="EwAAABYA"/>
            </t:Task>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a>Elementos de respuesta correcta

En la respuesta se incluyen los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CreateItemResponse](createitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateItemResponseMessage](createitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Elementos (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md)
    
- [Tarea](task.md)
    
- [ItemId](itemid.md)
    
## <a name="see-also"></a>Vea también



[Operación CreateItem](createitem-operation.md)


[Creación de tareas](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[Actualización de tareas](http://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)
  
[Eliminación de tareas](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

