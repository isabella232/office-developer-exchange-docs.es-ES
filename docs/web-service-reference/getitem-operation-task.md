---
title: Operación GetItem (tarea)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItem
api_type:
- schema
ms.assetid: 8265dd06-1752-4470-8074-5f0e3e970f52
description: La operación GetItem se usa para obtener tareas del almacén de Exchange.
ms.openlocfilehash: 17a23d4c2a35761e831610f3514c980a5a67e12b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463338"
---
# <a name="getitem-operation-task"></a>Operación GetItem (tarea)

La operación GetItem se usa para obtener tareas del almacén de Exchange.
  
## <a name="remarks"></a>Comentarios

El formato de la solicitud GetItem para tareas es el mismo que GetItem para cualquier otro tipo de elemento. La única diferencia es que se pueden solicitar propiedades adicionales dentro de la forma de respuesta. Estas propiedades adicionales deben ser propiedades relacionadas con tareas o propiedades extendidas.
  
## <a name="task-getitem-request-example"></a>Ejemplo de solicitud GetItem de tarea

### <a name="description"></a>Description

El siguiente ejemplo de una solicitud GetItem muestra cómo obtener un elemento de tarea.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <ItemShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="AAAtAEFkb..."/>
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

> [!NOTE]
> El identificador de elemento y la clave de cambio se han abreviado para preservar la legibilidad. 
  
### <a name="request-elements"></a>Elementos de solicitud

Los siguientes elementos se usan en la solicitud:
  
- [GetItem](getitem.md)
    
- [ItemShape](itemshape.md)
    
- [BaseShape](baseshape.md)
    
- [ItemIds](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="task-getitem-response-example"></a>Ejemplo de respuesta GetItem de tarea

### <a name="description"></a>Description

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud GetItem.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="662" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Task>
              <t:ItemId Id="AAAtAEA=" ChangeKey="EwAAAB"/>
              <t:ParentFolderId Id="AAAtAEFkbWl=" ChangeKey="AQAAAA=="/>
              <t:ItemClass>IPM.Task</t:ItemClass>
              <t:Subject>Buy new shoes</t:Subject>
              <t:Sensitivity>Normal</t:Sensitivity>
              <t:Body BodyType="Text"/>
              <t:DateTimeReceived>2006-09-15T15:23:08Z</t:DateTimeReceived>
              <t:Size>153</t:Size>
              <t:Importance>Normal</t:Importance>
              <t:IsSubmitted>false</t:IsSubmitted>
              <t:IsDraft>true</t:IsDraft>
              <t:IsFromMe>false</t:IsFromMe>
              <t:IsResend>false</t:IsResend>
              <t:IsUnmodified>false</t:IsUnmodified>
              <t:DateTimeSent>2006-09-15T15:23:08Z</t:DateTimeSent>
              <t:DateTimeCreated>2006-09-15T15:23:08Z</t:DateTimeCreated>
              <t:HasAttachments>false</t:HasAttachments>
              <t:Culture>en-US</t:Culture>
              <t:ChangeCount>1</t:ChangeCount>
              <t:IsComplete>false</t:IsComplete>
              <t:IsRecurring>false</t:IsRecurring>
              <t:PercentComplete>0</t:PercentComplete>
              <t:Status>NotStarted</t:Status>
              <t:StatusDescription>Not Started</t:StatusDescription>
            </t:Task>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </GetItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

> [!NOTE]
> Los identificadores de elemento y carpeta y las claves de cambio se han abreviado para preservar la legibilidad. 
  
### <a name="successful-response-elements"></a>Elementos Response correcto

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetItemResponse](getitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetItemResponseMessage](getitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Items](items.md)
    
- [Tarea](task.md)
    
- [ItemId](itemid.md)
    
- [ParentFolderId](parentfolderid.md)
    
- [ItemClass](itemclass.md)
    
- [Asunto](subject.md)
    
- [Sensitivity](sensitivity.md)
    
- [Body](body.md)
    
- [DateTimeReceived](datetimereceived.md)
    
- [Tamaño](size.md)
    
- [Importance](importance.md)
    
- [IsSubmitted](issubmitted.md)
    
- [IsDraft](isdraft.md)
    
- [IsFromMe](isfromme.md)
    
- [IsResend](isresend.md)
    
- [IsUnmodified](isunmodified.md)
    
- [DateTimeSent](datetimesent.md)
    
- [DateTimeCreated](datetimecreated.md)
    
- [HasAttachments](hasattachments.md)
    
- [Culture](culture.md)
    
- [ChangeCount](changecount.md)
    
- [IsComplete](iscomplete.md)
    
- [IsRecurring](isrecurring.md)
    
- [PercentComplete](percentcomplete.md)
    
- [Estado](status.md)
    
- [StatusDescription](statusdescription.md)
    
## <a name="see-also"></a>Vea también



[Operación GetItem](getitem-operation.md)


[Creación de tareas](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[Actualización de tareas](https://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)
  
[Eliminación de tareas](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

