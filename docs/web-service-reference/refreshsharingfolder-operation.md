---
title: Operación RefreshSharingFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RefreshSharingFolder
api_type:
- schema
ms.assetid: 1b047e34-40f0-459f-ac9e-e9f8e7349479
description: La operación RefreshSharingFolder actualiza la carpeta local especificada con los datos más recientes de la carpeta que se está compartiendo.
ms.openlocfilehash: 0037de28f0720b97cd51c58a6ee7e3c06e84d642
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837041"
---
# <a name="refreshsharingfolder-operation"></a><span data-ttu-id="0b82e-103">Operación RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="0b82e-103">RefreshSharingFolder operation</span></span>

<span data-ttu-id="0b82e-104">La operación **RefreshSharingFolder** actualiza la carpeta local especificada con los datos más recientes de la carpeta que se está compartiendo.</span><span class="sxs-lookup"><span data-stu-id="0b82e-104">The **RefreshSharingFolder** operation refreshes the specified local folder with the latest data from the folder that is being shared.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="0b82e-105">Encabezados SOAP</span><span class="sxs-lookup"><span data-stu-id="0b82e-105">SOAP Headers</span></span>

<span data-ttu-id="0b82e-106">La operación de **RefreshSharingFolder** puede utilizar los encabezados SOAP que se enumeran y describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="0b82e-106">The **RefreshSharingFolder** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="0b82e-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="0b82e-107">**Header**</span></span>|<span data-ttu-id="0b82e-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="0b82e-108">**Element**</span></span>|<span data-ttu-id="0b82e-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0b82e-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0b82e-110">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="0b82e-110">RequestVersion</span></span>  <br/> |[<span data-ttu-id="0b82e-111">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="0b82e-111">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="0b82e-112">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="0b82e-112">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="0b82e-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="0b82e-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="0b82e-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0b82e-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="0b82e-115">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0b82e-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="refreshsharingfolder-request-example"></a><span data-ttu-id="0b82e-116">Ejemplo de solicitud de RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="0b82e-116">RefreshSharingFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="0b82e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b82e-117">Description</span></span>

<span data-ttu-id="0b82e-118">En el ejemplo siguiente se muestra cómo formar una solicitud para actualizar la carpeta local especificada con los datos más recientes de la carpeta que se está compartiendo.</span><span class="sxs-lookup"><span data-stu-id="0b82e-118">The following example shows how to form a request to refresh the specified local folder with the latest data from the folder that is being shared.</span></span> <span data-ttu-id="0b82e-119">El elemento [SharingFolderId](sharingfolderid.md) especifica el identificador de la carpeta local que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="0b82e-119">The [SharingFolderId](sharingfolderid.md) element specifies the identifier of the local folder to be refreshed.</span></span> 
  
### <a name="code"></a><span data-ttu-id="0b82e-120">Código</span><span class="sxs-lookup"><span data-stu-id="0b82e-120">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <RefreshSharingFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:SharingFolderId Id="AAMkAD=" ChangeKey="AwAAA=" />
    </RefreshSharingFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="0b82e-121">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="0b82e-121">Request elements</span></span>

<span data-ttu-id="0b82e-122">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0b82e-122">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="0b82e-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="0b82e-123">RequestServerVersion</span></span>](requestserverversion.md)
    
- [<span data-ttu-id="0b82e-124">RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="0b82e-124">RefreshSharingFolder</span></span>](refreshsharingfolder.md)
    
- [<span data-ttu-id="0b82e-125">SharingFolderId</span><span class="sxs-lookup"><span data-stu-id="0b82e-125">SharingFolderId</span></span>](sharingfolderid.md)
    
## <a name="successful-refreshsharingfolder-response"></a><span data-ttu-id="0b82e-126">RefreshSharingFolder la respuesta es correcta</span><span class="sxs-lookup"><span data-stu-id="0b82e-126">Successful RefreshSharingFolder Response</span></span>

### <a name="description"></a><span data-ttu-id="0b82e-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b82e-127">Description</span></span>

<span data-ttu-id="0b82e-128">En el ejemplo siguiente se muestra una respuesta a una solicitud **RefreshSharingFolder** correcta.</span><span class="sxs-lookup"><span data-stu-id="0b82e-128">The following example shows a successful response to a **RefreshSharingFolder** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="0b82e-129">Código</span><span class="sxs-lookup"><span data-stu-id="0b82e-129">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <RefreshSharingFolderResponseMessage ResponseClass="Success"
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
    </RefreshSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="0b82e-130">Elementos de respuesta correcta</span><span class="sxs-lookup"><span data-stu-id="0b82e-130">Successful response elements</span></span>

<span data-ttu-id="0b82e-131">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0b82e-131">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="0b82e-132">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0b82e-132">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="0b82e-133">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0b82e-133">RefreshSharingFolderResponseMessage</span></span>](refreshsharingfolderresponsemessage.md)
    
- [<span data-ttu-id="0b82e-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0b82e-134">ResponseCode</span></span>](responsecode.md)
    
## <a name="refreshsharingfolder-error-response"></a><span data-ttu-id="0b82e-135">Respuesta de error de RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="0b82e-135">RefreshSharingFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="0b82e-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b82e-136">Description</span></span>

<span data-ttu-id="0b82e-137">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de **RefreshSharingFolder** .</span><span class="sxs-lookup"><span data-stu-id="0b82e-137">The following example shows an error response to a **RefreshSharingFolder** request.</span></span> <span data-ttu-id="0b82e-138">En este ejemplo, la solicitud de **RefreshSharingFolder** error porque no se encontró una suscripción que corresponde a la carpeta local especificada.</span><span class="sxs-lookup"><span data-stu-id="0b82e-138">In this example, the **RefreshSharingFolder** request failed because a subscription that corresponds to the specified local folder was not found.</span></span> 
  
### <a name="code"></a><span data-ttu-id="0b82e-139">Código</span><span class="sxs-lookup"><span data-stu-id="0b82e-139">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <RefreshSharingFolderResponseMessage ResponseClass="Error"
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:MessageText>Failed to synchronize the sharing folder.</m:MessageText>
      <m:ResponseCode>ErrorSharingSynchronizationFailed</m:ResponseCode>
      <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
      <m:MessageXml>
        <t:Value Name="ErrorDetails">Microsoft.Exchange.InfoWorker.Common.Sharing.SubscriptionNotFoundException: The subscription wasn't found.;</t:Value>
      </m:MessageXml>
    </RefreshSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="0b82e-140">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="0b82e-140">Error response elements</span></span>

<span data-ttu-id="0b82e-141">En la respuesta de error, se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0b82e-141">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="0b82e-142">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0b82e-142">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="0b82e-143">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0b82e-143">RefreshSharingFolderResponseMessage</span></span>](refreshsharingfolderresponsemessage.md)
    
- [<span data-ttu-id="0b82e-144">MessageText</span><span class="sxs-lookup"><span data-stu-id="0b82e-144">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="0b82e-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0b82e-145">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0b82e-146">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0b82e-146">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="0b82e-147">MessageXml</span><span class="sxs-lookup"><span data-stu-id="0b82e-147">MessageXml</span></span>](messagexml.md)
    
## <a name="see-also"></a><span data-ttu-id="0b82e-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b82e-148">See also</span></span>



[<span data-ttu-id="0b82e-149">RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="0b82e-149">RefreshSharingFolder</span></span>](refreshsharingfolder.md)
  
[<span data-ttu-id="0b82e-150">RefreshSharingFolderType</span><span class="sxs-lookup"><span data-stu-id="0b82e-150">RefreshSharingFolderType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.RefreshSharingFolderType.aspx)
  
[<span data-ttu-id="0b82e-151">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0b82e-151">RefreshSharingFolderResponseMessage</span></span>](refreshsharingfolderresponsemessage.md)
  
[<span data-ttu-id="0b82e-152">RefreshSharingFolderResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="0b82e-152">RefreshSharingFolderResponseMessageType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.RefreshSharingFolderResponseMessageType.aspx)


[<span data-ttu-id="0b82e-153">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0b82e-153">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="0b82e-154">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0b82e-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

