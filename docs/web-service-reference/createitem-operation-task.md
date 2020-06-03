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
description: La operación CreateItem crea elementos de tarea en el almacén de Exchange.
ms.openlocfilehash: 502108843193e7ed8377b0fade9e106ef3d1976c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457105"
---
# <a name="createitem-operation-task"></a>Operación CreateItem (tarea)

La operación CreateItem crea elementos de tarea en el almacén de Exchange.
  
## <a name="task-createitem-request"></a>Solicitud CreateItem de tarea

### <a name="description"></a>Description

El siguiente ejemplo de una solicitud CreateItem muestra cómo crear un elemento de tarea en un buzón.
  
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

Las solicitudes de tareas periódicas se modifican cuando las recibe el equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes. Se producen los siguientes cambios:
  
- Solo se guarda la fecha de la propiedad [startDate (periodicidad)](startdate-recurrence.md) del intervalo de periodicidad de la tarea. La parte Time se trunca. 
    
- La propiedad [startDate (recurrence)](startdate-recurrence.md) se puede ajustar según el patrón de periodicidad. Por ejemplo, si el patrón de periodicidad se especifica como cada lunes y el StartDate está establecido en el 26 de octubre de 2006, que es un jueves, StartDate se ajusta al 30 de octubre de 2006, que es el próximo lunes. 
    
- Si se establece la propiedad [startDate](startdate.md) de la tarea, ésta se actualiza para coincidir con la [startDate (periodicidad)](startdate-recurrence.md) del intervalo de periodicidad. La propiedad [DueDate](duedate.md) de la tarea también se actualiza en función del nuevo [startDate](startdate.md).
    
- Si no se ha establecido [startDate](startdate.md) , sólo la propiedad [DueDate](duedate.md) se actualiza para coincidir con la [startDate (periodicidad)](startdate-recurrence.md) del intervalo de periodicidad. 
    
En la siguiente tabla se muestran los cambios que realiza el servidor de acceso de cliente en una tarea recurrente que tiene una tarea. recurrence. Pattern de cada lunes.
  
**Cambios en una tarea recurrente**

|**Propiedad**|**Valor original**|**Valor actualizado**|
|:-----|:-----|:-----|
|Task. StartDate  <br/> |1 de enero de 2006  <br/> |30 de octubre de 2006  <br/> |
|Task. DueDate  <br/> |3 de enero de 2006  <br/> |1 de noviembre de 2006  <br/> |
|Task. recurrence. Range. StartDate  <br/> |26 de octubre de 2006  <br/> |30 de octubre de 2006  <br/> |
   
De forma predeterminada, si no se especifica una carpeta de destino, se crean elementos de tarea en la carpeta tareas.
  
### <a name="request-elements"></a>Elementos de solicitud

Los siguientes elementos se usan en la solicitud:
  
- [CreateItem](createitem.md)
    
- [Elementos (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md)
    
- [Tarea](task.md)
    
- [Asunto](subject.md)
    
- [DueDate](duedate.md)
    
- [Estado](status.md)
    
## <a name="successful-task-createitem-response"></a>Respuesta de tarea CreateItem correcta

### <a name="description"></a>Description

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

### <a name="successful-response-elements"></a>Elementos Response correcto

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


[Creación de tareas](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[Actualización de tareas](https://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)
  
[Eliminación de tareas](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

