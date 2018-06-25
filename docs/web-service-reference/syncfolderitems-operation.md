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
# <a name="syncfolderitems-operation"></a><span data-ttu-id="e9c5d-103">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="e9c5d-103">SyncFolderItems operation</span></span>

<span data-ttu-id="e9c5d-104">La operación SyncFolderItems sincroniza los elementos entre el servidor de Exchange y el cliente.</span><span class="sxs-lookup"><span data-stu-id="e9c5d-104">The SyncFolderItems operation synchronizes items between the Exchange server and the client.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e9c5d-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e9c5d-105">Remarks</span></span>

<span data-ttu-id="e9c5d-106">La operación SyncFolderItems devolverá un máximo de 512 cambios.</span><span class="sxs-lookup"><span data-stu-id="e9c5d-106">The SyncFolderItems operation will return a maximum of 512 changes.</span></span> <span data-ttu-id="e9c5d-107">Solicitudes SyncFolderItems subsiguientes se deben realizar para obtener los cambios adicionales.</span><span class="sxs-lookup"><span data-stu-id="e9c5d-107">Subsequent SyncFolderItems requests must be performed to get additional changes.</span></span> 
  
<span data-ttu-id="e9c5d-108">SyncFolderItems es similar a la operación FindItem en que no se devolverá propiedades como cuerpo o datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="e9c5d-108">SyncFolderItems is similar to the FindItem operation in that it cannot return properties like Body or Attachments.</span></span> <span data-ttu-id="e9c5d-109">Si la operación SyncFolderItems no devuelve las propiedades que necesita, puede usar la [operación GetItem](getitem-operation.md) para obtener un conjunto específico de propiedades para cada elemento que devuelve por SyncFolderItems.</span><span class="sxs-lookup"><span data-stu-id="e9c5d-109">If the SyncFolderItems operation does not return the properties that you need, you can use the [GetItem operation](getitem-operation.md) to get a specific set of properties for each item that it returned by SyncFolderItems.</span></span> 
  
## <a name="syncfolderitems-request-example"></a><span data-ttu-id="e9c5d-110">Ejemplo de solicitud SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="e9c5d-110">SyncFolderItems request example</span></span>

### <a name="description"></a><span data-ttu-id="e9c5d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9c5d-111">Description</span></span>

<span data-ttu-id="e9c5d-112">El siguiente ejemplo de una solicitud de SyncFolderItems muestra cómo sincronizar elementos en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="e9c5d-112">The following example of a SyncFolderItems request shows how to synchronize items in a folder.</span></span> <span data-ttu-id="e9c5d-113">En este ejemplo se muestra la sincronización del elemento de una carpeta que no es la primera sincronización para que se han producido para la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="e9c5d-113">This example shows a folder item's synchronization that is not the first synchronization to have occurred for the Sent Items folder.</span></span> <span data-ttu-id="e9c5d-114">El elemento de [estado de sincronización](syncstate-ex15websvcsotherref.md) no está incluido en la solicitud para el primer intento sincronizar a un cliente con el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e9c5d-114">The [SyncState](syncstate-ex15websvcsotherref.md) element is not included in the request for the first attempt to synchronize a client with the Exchange server.</span></span> <span data-ttu-id="e9c5d-115">El primer intento de sincronizar los elementos de una jerarquía de carpetas devolverá todos los elementos en el buzón de correo, excepto los elementos que se identifican en el elemento de [Omitir](ignore.md) .</span><span class="sxs-lookup"><span data-stu-id="e9c5d-115">The first attempt to synchronize the items in a folder hierarchy will return all the items in the mailbox, excluding items that are identified in the [Ignore](ignore.md) element.</span></span> <span data-ttu-id="e9c5d-116">Esta solicitud SyncFolderItems intentará sincronizar todos los cambios a los elementos de la carpeta desde la última sincronización.</span><span class="sxs-lookup"><span data-stu-id="e9c5d-116">This SyncFolderItems request will try to synchronize all changes to the folder items since the last synchronization.</span></span> <span data-ttu-id="e9c5d-117">Esta solicitud pasará por alto el intento de sincronizar el único elemento que se identifica en el elemento de [Omitir](ignore.md) .</span><span class="sxs-lookup"><span data-stu-id="e9c5d-117">This request will ignore the attempt to synchronize the one item that is identified in the [Ignore](ignore.md) element.</span></span> 
  
### <a name="code"></a><span data-ttu-id="e9c5d-118">Código</span><span class="sxs-lookup"><span data-stu-id="e9c5d-118">Code</span></span>

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

### <a name="comments"></a><span data-ttu-id="e9c5d-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e9c5d-119">Comments</span></span>

<span data-ttu-id="e9c5d-120">Los datos del [estado de sincronización](syncstate-ex15websvcsotherref.md) elemento codificado en base64 y el atributo de **identificador** de elemento [ItemId](itemid.md) se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="e9c5d-120">The [SyncState](syncstate-ex15websvcsotherref.md) element base64-encoded data and the [ItemId](itemid.md) element **Id** attribute have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="e9c5d-121">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="e9c5d-121">Request elements</span></span>

<span data-ttu-id="e9c5d-122">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="e9c5d-122">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="e9c5d-123">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="e9c5d-123">SyncFolderItems</span></span>](syncfolderitems.md)
    
- [<span data-ttu-id="e9c5d-124">ItemShape</span><span class="sxs-lookup"><span data-stu-id="e9c5d-124">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="e9c5d-125">BaseShape</span><span class="sxs-lookup"><span data-stu-id="e9c5d-125">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="e9c5d-126">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="e9c5d-126">SyncFolderId</span></span>](syncfolderid.md)
    
- [<span data-ttu-id="e9c5d-127">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="e9c5d-127">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="e9c5d-128">Estado de sincronización</span><span class="sxs-lookup"><span data-stu-id="e9c5d-128">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
- [<span data-ttu-id="e9c5d-129">Ignorar</span><span class="sxs-lookup"><span data-stu-id="e9c5d-129">Ignore</span></span>](ignore.md)
    
- [<span data-ttu-id="e9c5d-130">ItemId</span><span class="sxs-lookup"><span data-stu-id="e9c5d-130">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="e9c5d-131">MaxChangesReturned</span><span class="sxs-lookup"><span data-stu-id="e9c5d-131">MaxChangesReturned</span></span>](maxchangesreturned.md)
    
## <a name="successful-syncfolderitems-response"></a><span data-ttu-id="e9c5d-132">Respuesta SyncFolderItems es correcta</span><span class="sxs-lookup"><span data-stu-id="e9c5d-132">Successful SyncFolderItems Response</span></span>

### <a name="description"></a><span data-ttu-id="e9c5d-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9c5d-133">Description</span></span>

<span data-ttu-id="e9c5d-134">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud de SyncFolderItems.</span><span class="sxs-lookup"><span data-stu-id="e9c5d-134">The following example shows a successful response to the SyncFolderItems request.</span></span> <span data-ttu-id="e9c5d-135">En este ejemplo, una convocatoria de reunión se sincroniza desde la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="e9c5d-135">In this example, a meeting request is synchronized from the Sent Items folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="e9c5d-136">Código</span><span class="sxs-lookup"><span data-stu-id="e9c5d-136">Code</span></span>

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

### <a name="comments"></a><span data-ttu-id="e9c5d-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e9c5d-137">Comments</span></span>

<span data-ttu-id="e9c5d-138">Los datos del [estado de sincronización](syncstate-ex15websvcsotherref.md) elemento codificado en base64 y el atributo de **identificador** de elemento [ItemId](itemid.md) se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="e9c5d-138">The [SyncState](syncstate-ex15websvcsotherref.md) element base64-encoded data and the [ItemId](itemid.md) element **Id** attribute have been shortened to preserve readability.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="e9c5d-139">Elementos de respuesta correcta</span><span class="sxs-lookup"><span data-stu-id="e9c5d-139">Successful response elements</span></span>

<span data-ttu-id="e9c5d-140">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="e9c5d-140">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="e9c5d-141">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e9c5d-141">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="e9c5d-142">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="e9c5d-142">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)
    
- [<span data-ttu-id="e9c5d-143">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e9c5d-143">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="e9c5d-144">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e9c5d-144">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)
    
- [<span data-ttu-id="e9c5d-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e9c5d-145">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e9c5d-146">Estado de sincronización</span><span class="sxs-lookup"><span data-stu-id="e9c5d-146">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
- [<span data-ttu-id="e9c5d-147">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="e9c5d-147">IncludesLastItemInRange</span></span>](includeslastiteminrange.md)
    
- [<span data-ttu-id="e9c5d-148">Cambios (elementos)</span><span class="sxs-lookup"><span data-stu-id="e9c5d-148">Changes (Items)</span></span>](changes-items.md)
    
- [<span data-ttu-id="e9c5d-149">Crear (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="e9c5d-149">Create (ItemSync)</span></span>](create-itemsync.md)
    
- [<span data-ttu-id="e9c5d-150">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="e9c5d-150">MeetingRequest</span></span>](meetingrequest.md)
    
- [<span data-ttu-id="e9c5d-151">ItemId</span><span class="sxs-lookup"><span data-stu-id="e9c5d-151">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="e9c5d-152">Subject</span><span class="sxs-lookup"><span data-stu-id="e9c5d-152">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="e9c5d-153">Sensibilidad</span><span class="sxs-lookup"><span data-stu-id="e9c5d-153">Sensitivity</span></span>](sensitivity.md)
    
- [<span data-ttu-id="e9c5d-154">IsOutOfDate</span><span class="sxs-lookup"><span data-stu-id="e9c5d-154">IsOutOfDate</span></span>](isoutofdate.md)
    
- [<span data-ttu-id="e9c5d-155">HasBeenProcessed</span><span class="sxs-lookup"><span data-stu-id="e9c5d-155">HasBeenProcessed</span></span>](hasbeenprocessed.md)
    
- [<span data-ttu-id="e9c5d-156">ResponseType</span><span class="sxs-lookup"><span data-stu-id="e9c5d-156">ResponseType</span></span>](responsetype.md)
    
- [<span data-ttu-id="e9c5d-157">IntendedFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="e9c5d-157">IntendedFreeBusyStatus</span></span>](intendedfreebusystatus.md)
    
- [<span data-ttu-id="e9c5d-158">Start</span><span class="sxs-lookup"><span data-stu-id="e9c5d-158">Start</span></span>](start.md)
    
- [<span data-ttu-id="e9c5d-159">End</span><span class="sxs-lookup"><span data-stu-id="e9c5d-159">End </span></span>](end-ex15websvcsotherref.md)
    
- [<span data-ttu-id="e9c5d-160">Location</span><span class="sxs-lookup"><span data-stu-id="e9c5d-160">Location</span></span>](location.md)
    
- [<span data-ttu-id="e9c5d-161">Organizer</span><span class="sxs-lookup"><span data-stu-id="e9c5d-161">Organizer</span></span>](organizer.md)
    
- [<span data-ttu-id="e9c5d-162">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="e9c5d-162">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="e9c5d-163">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="e9c5d-163">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="e9c5d-164">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="e9c5d-164">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="e9c5d-165">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="e9c5d-165">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
## <a name="syncfolderitems-error-response"></a><span data-ttu-id="e9c5d-166">Respuesta de error SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="e9c5d-166">SyncFolderItems error response</span></span>

### <a name="description"></a><span data-ttu-id="e9c5d-167">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9c5d-167">Description</span></span>

<span data-ttu-id="e9c5d-168">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de SyncFolderItems.</span><span class="sxs-lookup"><span data-stu-id="e9c5d-168">The following example shows an error response to a SyncFolderItems request.</span></span> <span data-ttu-id="e9c5d-169">Este error se produjo por un estado de sincronización no válido.</span><span class="sxs-lookup"><span data-stu-id="e9c5d-169">This error was caused by an invalid SyncState.</span></span>
  
### <a name="code"></a><span data-ttu-id="e9c5d-170">Código</span><span class="sxs-lookup"><span data-stu-id="e9c5d-170">Code</span></span>

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

### <a name="error-response-elements"></a><span data-ttu-id="e9c5d-171">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="e9c5d-171">Error response elements</span></span>

<span data-ttu-id="e9c5d-172">En la respuesta de error, se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="e9c5d-172">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="e9c5d-173">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e9c5d-173">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="e9c5d-174">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="e9c5d-174">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)
    
- [<span data-ttu-id="e9c5d-175">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e9c5d-175">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="e9c5d-176">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e9c5d-176">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)
    
- [<span data-ttu-id="e9c5d-177">MessageText</span><span class="sxs-lookup"><span data-stu-id="e9c5d-177">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="e9c5d-178">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e9c5d-178">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e9c5d-179">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e9c5d-179">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="e9c5d-180">Estado de sincronización</span><span class="sxs-lookup"><span data-stu-id="e9c5d-180">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
- [<span data-ttu-id="e9c5d-181">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="e9c5d-181">IncludesLastItemInRange</span></span>](includeslastiteminrange.md)
    
## <a name="see-also"></a><span data-ttu-id="e9c5d-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9c5d-182">See also</span></span>



- [<span data-ttu-id="e9c5d-183">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e9c5d-183">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

