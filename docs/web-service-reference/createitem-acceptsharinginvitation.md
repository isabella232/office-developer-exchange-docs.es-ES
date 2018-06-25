---
title: CreateItem (AcceptSharingInvitation)
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
ms.assetid: 710c893a-3037-4f04-b336-aefedd36c406
description: La operación CreateItem se usa para aceptar una invitación para compartir calendario de otro usuario o datos de los contactos.
ms.openlocfilehash: 993ef0402e624af69f632af5bdce4c02bd9d41f3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763944"
---
# <a name="createitem-acceptsharinginvitation"></a><span data-ttu-id="17420-103">CreateItem (AcceptSharingInvitation)</span><span class="sxs-lookup"><span data-stu-id="17420-103">CreateItem (AcceptSharingInvitation)</span></span>

<span data-ttu-id="17420-104">La operación **CreateItem** se usa para aceptar una invitación para compartir calendario de otro usuario o datos de los contactos.</span><span class="sxs-lookup"><span data-stu-id="17420-104">The **CreateItem** operation is used to accept an invitation to share another user's calendar or contacts data.</span></span> 
  
## <a name="accept-sharing-invitation-request-example"></a><span data-ttu-id="17420-105">Acepte el ejemplo de solicitud de invitación de uso compartido</span><span class="sxs-lookup"><span data-stu-id="17420-105">Accept Sharing Invitation request example</span></span>

### <a name="description"></a><span data-ttu-id="17420-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="17420-106">Description</span></span>

<span data-ttu-id="17420-107">En el ejemplo siguiente se muestra cómo aceptar una invitación para compartir.</span><span class="sxs-lookup"><span data-stu-id="17420-107">The following example shows how to accept a sharing invitation.</span></span>
  
### <a name="code"></a><span data-ttu-id="17420-108">Código</span><span class="sxs-lookup"><span data-stu-id="17420-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <Items xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
        <AcceptSharingInvitation xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <ReferenceItemId Id="AAAlAFVzZ" ChangeKey="CwAAABYAA" />
        </AcceptSharingInvitation>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="17420-109">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="17420-109">Request elements</span></span>

<span data-ttu-id="17420-110">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="17420-110">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="17420-111">CreateItem</span><span class="sxs-lookup"><span data-stu-id="17420-111">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="17420-112">Items</span><span class="sxs-lookup"><span data-stu-id="17420-112">Items</span></span>](items.md)
    
- [<span data-ttu-id="17420-113">AcceptSharingInvitation</span><span class="sxs-lookup"><span data-stu-id="17420-113">AcceptSharingInvitation</span></span>](acceptsharinginvitation.md)
    
- [<span data-ttu-id="17420-114">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="17420-114">ReferenceItemId</span></span>](referenceitemid.md)
    
### <a name="comments"></a><span data-ttu-id="17420-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="17420-115">Comments</span></span>

<span data-ttu-id="17420-116">El identificador de elemento y la clave de cambio se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="17420-116">The item identifier and change key have been shortened to preserve readability.</span></span>
  
## <a name="successful-accept-sharing-invitation-response-example"></a><span data-ttu-id="17420-117">Ejemplo de respuesta correcta de aceptar la invitación de uso compartido</span><span class="sxs-lookup"><span data-stu-id="17420-117">Successful Accept Sharing Invitation response example</span></span>

### <a name="description"></a><span data-ttu-id="17420-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="17420-118">Description</span></span>

<span data-ttu-id="17420-119">En el ejemplo siguiente se muestra una respuesta a una solicitud **CreateItem** correcta.</span><span class="sxs-lookup"><span data-stu-id="17420-119">The following example shows a successful response to a **CreateItem** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="17420-120">Código</span><span class="sxs-lookup"><span data-stu-id="17420-120">Code</span></span>

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
    <CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items />
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="17420-121">Elementos de respuesta correcta</span><span class="sxs-lookup"><span data-stu-id="17420-121">Successful response elements</span></span>

<span data-ttu-id="17420-122">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="17420-122">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="17420-123">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="17420-123">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="17420-124">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="17420-124">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="17420-125">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="17420-125">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="17420-126">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="17420-126">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="17420-127">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="17420-127">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="17420-128">Items</span><span class="sxs-lookup"><span data-stu-id="17420-128">Items</span></span>](items.md)
    
## <a name="accept-sharing-invitation-error-response-example"></a><span data-ttu-id="17420-129">Acepte el ejemplo de respuesta de Error de la invitación de uso compartido</span><span class="sxs-lookup"><span data-stu-id="17420-129">Accept Sharing Invitation Error response example</span></span>

### <a name="description"></a><span data-ttu-id="17420-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="17420-130">Description</span></span>

<span data-ttu-id="17420-131">En el ejemplo siguiente se muestra una respuesta de error a una solicitud **CreateItem** .</span><span class="sxs-lookup"><span data-stu-id="17420-131">The following example shows an error response to a **CreateItem** request.</span></span> <span data-ttu-id="17420-132">El error se debe a un intento de aceptar una invitación para compartir que no se encuentra en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="17420-132">The error is caused by an attempt to accept a sharing invitation that cannot be found in the Exchange store.</span></span> 
  
### <a name="code"></a><span data-ttu-id="17420-133">Código</span><span class="sxs-lookup"><span data-stu-id="17420-133">Code</span></span>

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
    <CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Items />
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="17420-134">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="17420-134">Error response elements</span></span>

<span data-ttu-id="17420-135">En la respuesta de error, se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="17420-135">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="17420-136">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="17420-136">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="17420-137">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="17420-137">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="17420-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="17420-138">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="17420-139">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="17420-139">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="17420-140">MessageText</span><span class="sxs-lookup"><span data-stu-id="17420-140">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="17420-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="17420-141">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="17420-142">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="17420-142">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="17420-143">Items</span><span class="sxs-lookup"><span data-stu-id="17420-143">Items</span></span>](items.md)
    
## <a name="see-also"></a><span data-ttu-id="17420-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="17420-144">See also</span></span>



[<span data-ttu-id="17420-145">Operación CreateItem</span><span class="sxs-lookup"><span data-stu-id="17420-145">CreateItem operation</span></span>](createitem-operation.md)

