---
title: Operación SyncFolderItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderItems
api_type:
- schema
ms.assetid: 7f0de089-8876-47ec-a871-df118ceae75d
description: La operación SyncFolderItems sincroniza los elementos entre el servidor de Exchange y el cliente.
ms.openlocfilehash: 6b2e4694ac793e17a2b7cb2edb2cb9e6a4a105ea
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840616"
---
# <a name="syncfolderitems-operation"></a>Operación SyncFolderItems

La operación SyncFolderItems sincroniza los elementos entre el servidor de Exchange y el cliente.
  
## <a name="remarks"></a>Comentarios

La operación SyncFolderItems devolverá un máximo de 512 cambios. Solicitudes SyncFolderItems subsiguientes se deben realizar para obtener los cambios adicionales. 
  
SyncFolderItems es similar a la operación FindItem en que no se devolverá propiedades como cuerpo o datos adjuntos. Si la operación SyncFolderItems no devuelve las propiedades que necesita, puede usar la [operación GetItem](getitem-operation.md) para obtener un conjunto específico de propiedades para cada elemento que devuelve por SyncFolderItems. 
  
## <a name="syncfolderitems-request-example"></a>Ejemplo de solicitud SyncFolderItems

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de SyncFolderItems muestra cómo sincronizar elementos en una carpeta. En este ejemplo se muestra la sincronización del elemento de una carpeta que no es la primera sincronización para que se han producido para la carpeta Elementos enviados. El elemento de [estado de sincronización](syncstate-ex15websvcsotherref.md) no está incluido en la solicitud para el primer intento sincronizar a un cliente con el servidor de Exchange. El primer intento de sincronizar los elementos de una jerarquía de carpetas devolverá todos los elementos en el buzón de correo, excepto los elementos que se identifican en el elemento de [Omitir](ignore.md) . Esta solicitud SyncFolderItems intentará sincronizar todos los cambios a los elementos de la carpeta desde la última sincronización. Esta solicitud pasará por alto el intento de sincronizar el único elemento que se identifica en el elemento de [Omitir](ignore.md) . 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SyncFolderItems xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>Default</t:BaseShape>
      </ItemShape>
      <SyncFolderId>
        <t:DistinguishedFolderId Id="sentitems"/>
      </SyncFolderId>
      <SyncState>AEbJ94eMOAAA=</SyncState>
      <Ignore>
        <t:ItemId Id="AQApAHRAA==" ChangeKey="CQAAABY"/>
      </Ignore>
      <MaxChangesReturned>100</MaxChangesReturned>
    </SyncFolderItems>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

Los datos del [estado de sincronización](syncstate-ex15websvcsotherref.md) elemento codificado en base64 y el atributo de **identificador** de elemento [ItemId](itemid.md) se han abreviado para conservar la legibilidad. 
  
### <a name="request-elements"></a>Elementos de solicitud

En la solicitud se usan los siguientes elementos:
  
- [SyncFolderItems](syncfolderitems.md)
    
- [ItemShape](itemshape.md)
    
- [BaseShape](baseshape.md)
    
- [SyncFolderId](syncfolderid.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [Estado de sincronización](syncstate-ex15websvcsotherref.md)
    
- [Ignorar](ignore.md)
    
- [ItemId](itemid.md)
    
- [MaxChangesReturned](maxchangesreturned.md)
    
## <a name="successful-syncfolderitems-response"></a>Respuesta SyncFolderItems es correcta

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta correcta a la solicitud de SyncFolderItems. En este ejemplo, una convocatoria de reunión se sincroniza desde la carpeta Elementos enviados.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SyncFolderItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                             xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SyncFolderItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAAAAA=</m:SyncState>
          <m:IncludesLastItemInRange>true</m:IncludesLastItemInRange>
          <m:Changes>
            <t:Create>
              <t:MeetingRequest>
                <t:ItemId Id="AQApAHRwA==" ChangeKey="CwAAABYA" />
                <t:Subject>Budget Q3</t:Subject>
                <t:Sensitivity>Normal</t:Sensitivity>
                <t:IsOutOfDate>false</t:IsOutOfDate>
                <t:HasBeenProcessed>true</t:HasBeenProcessed>
                <t:ResponseType>NoResponseReceived</t:ResponseType>
                <t:IntendedFreeBusyStatus>Busy</t:IntendedFreeBusyStatus>
                <t:Start>2006-08-02T17:30:00Z</t:Start>
                <t:End>2006-08-02T19:30:00Z</t:End>
                <t:Location>Conference Room 2</t:Location>
                <t:Organizer>
                  <t:Mailbox>
                    <t:Name>Dan Park</t:Name>
                    <t:EmailAddress>dpark@example.com</t:EmailAddress>
                    <t:RoutingType>SMTP</t:RoutingType>
                  </t:Mailbox>
                </t:Organizer>
              </t:MeetingRequest>
            </t:Create>
          </m:Changes>
        </m:SyncFolderItemsResponseMessage>
      </m:ResponseMessages>
    </SyncFolderItemsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

Los datos del [estado de sincronización](syncstate-ex15websvcsotherref.md) elemento codificado en base64 y el atributo de **identificador** de elemento [ItemId](itemid.md) se han abreviado para conservar la legibilidad. 
  
### <a name="successful-response-elements"></a>Elementos de respuesta correcta

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SyncFolderItemsResponse](syncfolderitemsresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Estado de sincronización](syncstate-ex15websvcsotherref.md)
    
- [IncludesLastItemInRange](includeslastiteminrange.md)
    
- [Cambios (elementos)](changes-items.md)
    
- [Crear (ItemSync)](create-itemsync.md)
    
- [MeetingRequest](meetingrequest.md)
    
- [ItemId](itemid.md)
    
- [Subject](subject.md)
    
- [Sensibilidad](sensitivity.md)
    
- [IsOutOfDate](isoutofdate.md)
    
- [HasBeenProcessed](hasbeenprocessed.md)
    
- [ResponseType](responsetype.md)
    
- [IntendedFreeBusyStatus](intendedfreebusystatus.md)
    
- [Start](start.md)
    
- [End](end-ex15websvcsotherref.md)
    
- [Location](location.md)
    
- [Organizer](organizer.md)
    
- [Buzón de correo](mailbox.md)
    
- [Nombre (EmailAddressType)](name-emailaddresstype.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)
    
- [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md)
    
## <a name="syncfolderitems-error-response"></a>Respuesta de error SyncFolderItems

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de SyncFolderItems. Este error se produjo por un estado de sincronización no válido.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SyncFolderItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                             xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SyncFolderItemsResponseMessage ResponseClass="Error">
          <m:MessageText>Synchronization state data is corrupt or otherwise invalid.</m:MessageText>
          <m:ResponseCode>ErrorInvalidSyncStateData</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:SyncState />
          <m:IncludesLastItemInRange>true</m:IncludesLastItemInRange>
        </m:SyncFolderItemsResponseMessage>
      </m:ResponseMessages>
    </SyncFolderItemsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Elementos de respuesta de error

En la respuesta de error, se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SyncFolderItemsResponse](syncfolderitemsresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Estado de sincronización](syncstate-ex15websvcsotherref.md)
    
- [IncludesLastItemInRange](includeslastiteminrange.md)
    
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

