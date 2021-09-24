---
title: Operación CreateItem (tarea)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CreateItem
api_type:
- schema
ms.assetid: 12c5da4d-290c-4a8a-a965-0bf5d55c7978
description: La operación CreateItem crea elementos de tarea en Exchange almacén.
ms.openlocfilehash: 814a32e82cd5c1c95be252d1b53387741898dd40
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510262"
---
# <a name="createitem-operation-task"></a>Operación CreateItem (tarea)

La operación CreateItem crea elementos de tarea en Exchange almacén.
  
## <a name="task-createitem-request"></a>Solicitud CreateItem de tarea

### <a name="description"></a>Descripción

En el siguiente ejemplo de una solicitud CreateItem se muestra cómo crear un elemento de tarea en un buzón.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
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

Las solicitudes de tareas periódicas se modifican cuando las recibe el equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalada la función de servidor Acceso de cliente. Se producen los siguientes cambios:
  
- Solo se guarda la fecha para la [propiedad StartDate (Recurrence)](startdate-recurrence.md) del intervalo de periodicidad de la tarea. La parte de tiempo se trunca. 
    
- La [propiedad StartDate (Recurrence)](startdate-recurrence.md) puede ajustarse, según el patrón de periodicidad. Por ejemplo, si el patrón de periodicidad se especifica como todos los lunes y StartDate se establece en 26 de octubre de 2006, que es un jueves, StartDate se ajusta al 30 de octubre de 2006, que es el lunes siguiente. 
    
- Si se establece la propiedad [StartDate](startdate.md) de la tarea, se actualiza para que coincida con [el StartDate (Recurrence)](startdate-recurrence.md) del intervalo de periodicidad. La [propiedad DueDate](duedate.md) de la tarea también se actualiza en función del [nuevo StartDate](startdate.md).
    
- Si no [se establece StartDate,](startdate.md) solo se actualiza la propiedad [DueDate](duedate.md) para que coincida con [el StartDate (Recurrence)](startdate-recurrence.md) del intervalo de periodicidad. 
    
En la tabla siguiente se muestran los cambios que realiza el servidor de acceso de cliente en una tarea periódica que tiene un objeto Task.Recurrence.Pattern de cada lunes.
  
**Cambios en una tarea periódica**

|**Property**|**Valor original**|**Valor actualizado**|
|:-----|:-----|:-----|
|Task.StartDate  <br/> |1 de enero de 2006  <br/> |30 de octubre de 2006  <br/> |
|Task.DueDate  <br/> |3 de enero de 2006  <br/> |1 de noviembre de 2006  <br/> |
|Task.Recurrence.Range.StartDate  <br/> |26 de octubre de 2006  <br/> |30 de octubre de 2006  <br/> |
   
De forma predeterminada, si no se especifica una carpeta de destino, los elementos de tarea se crean en la carpeta Tareas.
  
### <a name="request-elements"></a>Elementos Request

En la solicitud se usan los siguientes elementos:
  
- [CreateItem](createitem.md)
    
- [Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md)
    
- [Tarea](task.md)
    
- [Asunto](subject.md)
    
- [DueDate](duedate.md)
    
- [Estado](status.md)
    
## <a name="successful-task-createitem-response"></a>Respuesta de CreateItem de tarea correcta

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
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="successful-response-elements"></a>Elementos de respuesta correctos

En la respuesta se incluyen los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CreateItemResponse](createitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateItemResponseMessage](createitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md)
    
- [Tarea](task.md)
    
- [ItemId](itemid.md)
    
## <a name="see-also"></a>Ver también



[Operación CreateItem](createitem-operation.md)


[Creación de tareas](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[Actualizar tareas](https://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)
  
[Eliminación de tareas](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

