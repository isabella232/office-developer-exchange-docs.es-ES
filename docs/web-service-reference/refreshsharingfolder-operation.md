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
description: La operación RefreshSharingFolder actualiza la carpeta local especificada con los datos más recientes de la carpeta que se comparte.
ms.openlocfilehash: dd7136ae82353841db09497d23eabe450c1c8b13
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456772"
---
# <a name="refreshsharingfolder-operation"></a><span data-ttu-id="293cf-103">Operación RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="293cf-103">RefreshSharingFolder operation</span></span>

<span data-ttu-id="293cf-104">La operación **RefreshSharingFolder** actualiza la carpeta local especificada con los datos más recientes de la carpeta que se comparte.</span><span class="sxs-lookup"><span data-stu-id="293cf-104">The **RefreshSharingFolder** operation refreshes the specified local folder with the latest data from the folder that is being shared.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="293cf-105">Encabezados SOAP</span><span class="sxs-lookup"><span data-stu-id="293cf-105">SOAP Headers</span></span>

<span data-ttu-id="293cf-106">La operación **RefreshSharingFolder** puede usar los encabezados SOAP que se enumeran y describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="293cf-106">The **RefreshSharingFolder** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="293cf-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="293cf-107">**Header**</span></span>|<span data-ttu-id="293cf-108">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="293cf-108">**Element**</span></span>|<span data-ttu-id="293cf-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="293cf-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="293cf-110">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="293cf-110">RequestVersion</span></span>  <br/> |[<span data-ttu-id="293cf-111">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="293cf-111">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="293cf-112">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="293cf-112">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="293cf-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="293cf-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="293cf-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="293cf-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="293cf-115">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="293cf-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="refreshsharingfolder-request-example"></a><span data-ttu-id="293cf-116">Ejemplo de solicitud RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="293cf-116">RefreshSharingFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="293cf-117">Description</span><span class="sxs-lookup"><span data-stu-id="293cf-117">Description</span></span>

<span data-ttu-id="293cf-118">En el siguiente ejemplo, se muestra cómo crear una solicitud para actualizar la carpeta local especificada con los datos más recientes de la carpeta que se está compartiendo.</span><span class="sxs-lookup"><span data-stu-id="293cf-118">The following example shows how to form a request to refresh the specified local folder with the latest data from the folder that is being shared.</span></span> <span data-ttu-id="293cf-119">El elemento [SharingFolderId](sharingfolderid.md) especifica el identificador de la carpeta local que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="293cf-119">The [SharingFolderId](sharingfolderid.md) element specifies the identifier of the local folder to be refreshed.</span></span> 
  
### <a name="code"></a><span data-ttu-id="293cf-120">Código</span><span class="sxs-lookup"><span data-stu-id="293cf-120">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <RefreshSharingFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:SharingFolderId Id="AAMkAD=" ChangeKey="AwAAA=" />
    </RefreshSharingFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="293cf-121">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="293cf-121">Request elements</span></span>

<span data-ttu-id="293cf-122">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="293cf-122">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="293cf-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="293cf-123">RequestServerVersion</span></span>](requestserverversion.md)
    
- [<span data-ttu-id="293cf-124">RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="293cf-124">RefreshSharingFolder</span></span>](refreshsharingfolder.md)
    
- [<span data-ttu-id="293cf-125">SharingFolderId</span><span class="sxs-lookup"><span data-stu-id="293cf-125">SharingFolderId</span></span>](sharingfolderid.md)
    
## <a name="successful-refreshsharingfolder-response"></a><span data-ttu-id="293cf-126">Respuesta RefreshSharingFolder correcta</span><span class="sxs-lookup"><span data-stu-id="293cf-126">Successful RefreshSharingFolder Response</span></span>

### <a name="description"></a><span data-ttu-id="293cf-127">Description</span><span class="sxs-lookup"><span data-stu-id="293cf-127">Description</span></span>

<span data-ttu-id="293cf-128">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud **RefreshSharingFolder** .</span><span class="sxs-lookup"><span data-stu-id="293cf-128">The following example shows a successful response to a **RefreshSharingFolder** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="293cf-129">Código</span><span class="sxs-lookup"><span data-stu-id="293cf-129">Code</span></span>

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
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <RefreshSharingFolderResponseMessage ResponseClass="Success"
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
    </RefreshSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="293cf-130">Elementos Response correcto</span><span class="sxs-lookup"><span data-stu-id="293cf-130">Successful response elements</span></span>

<span data-ttu-id="293cf-131">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="293cf-131">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="293cf-132">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="293cf-132">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="293cf-133">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="293cf-133">RefreshSharingFolderResponseMessage</span></span>](refreshsharingfolderresponsemessage.md)
    
- [<span data-ttu-id="293cf-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="293cf-134">ResponseCode</span></span>](responsecode.md)
    
## <a name="refreshsharingfolder-error-response"></a><span data-ttu-id="293cf-135">Respuesta de error de RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="293cf-135">RefreshSharingFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="293cf-136">Description</span><span class="sxs-lookup"><span data-stu-id="293cf-136">Description</span></span>

<span data-ttu-id="293cf-137">En el ejemplo siguiente se muestra una respuesta de error a una solicitud **RefreshSharingFolder** .</span><span class="sxs-lookup"><span data-stu-id="293cf-137">The following example shows an error response to a **RefreshSharingFolder** request.</span></span> <span data-ttu-id="293cf-138">En este ejemplo, se produjo un error en la solicitud **RefreshSharingFolder** porque no se encontró una suscripción que corresponde a la carpeta local especificada.</span><span class="sxs-lookup"><span data-stu-id="293cf-138">In this example, the **RefreshSharingFolder** request failed because a subscription that corresponds to the specified local folder was not found.</span></span> 
  
### <a name="code"></a><span data-ttu-id="293cf-139">Código</span><span class="sxs-lookup"><span data-stu-id="293cf-139">Code</span></span>

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
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <RefreshSharingFolderResponseMessage ResponseClass="Error"
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="293cf-140">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="293cf-140">Error response elements</span></span>

<span data-ttu-id="293cf-141">Los siguientes elementos se usan en la respuesta de error:</span><span class="sxs-lookup"><span data-stu-id="293cf-141">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="293cf-142">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="293cf-142">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="293cf-143">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="293cf-143">RefreshSharingFolderResponseMessage</span></span>](refreshsharingfolderresponsemessage.md)
    
- [<span data-ttu-id="293cf-144">MessageText</span><span class="sxs-lookup"><span data-stu-id="293cf-144">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="293cf-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="293cf-145">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="293cf-146">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="293cf-146">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="293cf-147">MessageXml</span><span class="sxs-lookup"><span data-stu-id="293cf-147">MessageXml</span></span>](messagexml.md)
    
## <a name="see-also"></a><span data-ttu-id="293cf-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="293cf-148">See also</span></span>



[<span data-ttu-id="293cf-149">RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="293cf-149">RefreshSharingFolder</span></span>](refreshsharingfolder.md)
  
[<span data-ttu-id="293cf-150">RefreshSharingFolderType</span><span class="sxs-lookup"><span data-stu-id="293cf-150">RefreshSharingFolderType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.RefreshSharingFolderType.aspx)
  
[<span data-ttu-id="293cf-151">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="293cf-151">RefreshSharingFolderResponseMessage</span></span>](refreshsharingfolderresponsemessage.md)
  
[<span data-ttu-id="293cf-152">RefreshSharingFolderResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="293cf-152">RefreshSharingFolderResponseMessageType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.RefreshSharingFolderResponseMessageType.aspx)


[<span data-ttu-id="293cf-153">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="293cf-153">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="293cf-154">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="293cf-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

