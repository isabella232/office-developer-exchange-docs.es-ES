---
title: Operación CreateItem (convocatoria de reunión)
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
ms.assetid: fe136881-a804-456a-8552-8a1bea5eb9c8
description: La operación CreateItem se usa para responder a las convocatorias de reunión.
ms.openlocfilehash: f9e6bd1742e6a30d08736ea67c0ff80b7a18e88a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457112"
---
# <a name="createitem-operation-meeting-request"></a><span data-ttu-id="c1ffc-103">Operación CreateItem (convocatoria de reunión)</span><span class="sxs-lookup"><span data-stu-id="c1ffc-103">CreateItem operation (meeting request)</span></span>

<span data-ttu-id="c1ffc-104">La operación CreateItem se usa para responder a las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="c1ffc-104">The CreateItem operation is used to respond to meeting requests.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c1ffc-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c1ffc-105">Remarks</span></span>

<span data-ttu-id="c1ffc-106">La operación CreateItem proporciona tres opciones para responder a una convocatoria de reunión: aceptar, aceptar provisionalmente o rechazar.</span><span class="sxs-lookup"><span data-stu-id="c1ffc-106">The CreateItem operation provides three options for responding to a meeting request: accept, tentatively accept, or decline.</span></span> 
  
## <a name="accept-meeting-request-example"></a><span data-ttu-id="c1ffc-107">Ejemplo de convocatoria de reunión aceptada</span><span class="sxs-lookup"><span data-stu-id="c1ffc-107">Accept Meeting request example</span></span>

### <a name="description"></a><span data-ttu-id="c1ffc-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1ffc-108">Description</span></span>

<span data-ttu-id="c1ffc-109">En el siguiente ejemplo, se muestra cómo aceptar una invitación a convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="c1ffc-109">The following example shows how to accept a meeting request invitation.</span></span>
  
### <a name="code"></a><span data-ttu-id="c1ffc-110">Código</span><span class="sxs-lookup"><span data-stu-id="c1ffc-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                MessageDisposition="SendAndSaveCopy">
      <Items>
        <AcceptItem xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <ReferenceItemId Id="AAAlAFVzZ"
                           ChangeKey="CwAAABYAA"/>
        </AcceptItem>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="c1ffc-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c1ffc-111">Comments</span></span>

<span data-ttu-id="c1ffc-112">Para aceptar provisionalmente o para rechazar la convocatoria de reunión, use los elementos [TentativelyAcceptItem](tentativelyacceptitem.md) o [DeclineItem](declineitem.md) en vez del elemento [AcceptItem](acceptitem.md) .</span><span class="sxs-lookup"><span data-stu-id="c1ffc-112">To tentatively accept or to decline the meeting request, use the [TentativelyAcceptItem](tentativelyacceptitem.md) or [DeclineItem](declineitem.md) elements in place of the [AcceptItem](acceptitem.md) element.</span></span> 
  
<span data-ttu-id="c1ffc-113">El identificador de elemento y la clave de cambio se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="c1ffc-113">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="accepting-meeting-request-elements"></a><span data-ttu-id="c1ffc-114">Aceptar elementos de convocatoria de reunión</span><span class="sxs-lookup"><span data-stu-id="c1ffc-114">Accepting Meeting Request Elements</span></span>

<span data-ttu-id="c1ffc-115">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="c1ffc-115">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="c1ffc-116">CreateItem</span><span class="sxs-lookup"><span data-stu-id="c1ffc-116">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="c1ffc-117">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="c1ffc-117">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="c1ffc-118">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="c1ffc-118">AcceptItem</span></span>](acceptitem.md)
    
- [<span data-ttu-id="c1ffc-119">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="c1ffc-119">ReferenceItemId</span></span>](referenceitemid.md)
    
## <a name="successful-accept-meeting-response-example"></a><span data-ttu-id="c1ffc-120">Ejemplo de respuesta de aceptación de reunión correcta</span><span class="sxs-lookup"><span data-stu-id="c1ffc-120">Successful Accept Meeting response example</span></span>

### <a name="description"></a><span data-ttu-id="c1ffc-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1ffc-121">Description</span></span>

<span data-ttu-id="c1ffc-122">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud CreateItem.</span><span class="sxs-lookup"><span data-stu-id="c1ffc-122">The following example shows a successful response to the CreateItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="c1ffc-123">Código</span><span class="sxs-lookup"><span data-stu-id="c1ffc-123">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="successful-response-elements"></a><span data-ttu-id="c1ffc-124">Elementos Response correcto</span><span class="sxs-lookup"><span data-stu-id="c1ffc-124">Successful response elements</span></span>

<span data-ttu-id="c1ffc-125">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="c1ffc-125">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="c1ffc-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c1ffc-126">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="c1ffc-127">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="c1ffc-127">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="c1ffc-128">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c1ffc-128">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c1ffc-129">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c1ffc-129">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="c1ffc-130">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c1ffc-130">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c1ffc-131">Items</span><span class="sxs-lookup"><span data-stu-id="c1ffc-131">Items</span></span>](items.md)
    
## <a name="accept-meeting-error-response-example"></a><span data-ttu-id="c1ffc-132">Ejemplo de respuesta de error de aceptación de reunión</span><span class="sxs-lookup"><span data-stu-id="c1ffc-132">Accept Meeting Error response example</span></span>

### <a name="description"></a><span data-ttu-id="c1ffc-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1ffc-133">Description</span></span>

<span data-ttu-id="c1ffc-134">El ejemplo siguiente muestra una respuesta de error a la solicitud CreateItem.</span><span class="sxs-lookup"><span data-stu-id="c1ffc-134">The following example shows an error response to CreateItem request.</span></span> <span data-ttu-id="c1ffc-135">El error se debe a un intento de aceptar una convocatoria de reunión que no se encuentra en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c1ffc-135">The error is caused by an attempt to accept a meeting request that cannot be found in the Exchange store.</span></span>
  
### <a name="code"></a><span data-ttu-id="c1ffc-136">Código</span><span class="sxs-lookup"><span data-stu-id="c1ffc-136">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
  xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="c1ffc-137">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="c1ffc-137">Error response elements</span></span>

<span data-ttu-id="c1ffc-138">Los siguientes elementos se usan en la respuesta de error:</span><span class="sxs-lookup"><span data-stu-id="c1ffc-138">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="c1ffc-139">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c1ffc-139">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="c1ffc-140">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="c1ffc-140">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="c1ffc-141">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c1ffc-141">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c1ffc-142">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c1ffc-142">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="c1ffc-143">MessageText</span><span class="sxs-lookup"><span data-stu-id="c1ffc-143">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="c1ffc-144">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c1ffc-144">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c1ffc-145">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c1ffc-145">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="c1ffc-146">Items</span><span class="sxs-lookup"><span data-stu-id="c1ffc-146">Items</span></span>](items.md)
    
## <a name="see-also"></a><span data-ttu-id="c1ffc-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1ffc-147">See also</span></span>



[<span data-ttu-id="c1ffc-148">Operación CreateItem</span><span class="sxs-lookup"><span data-stu-id="c1ffc-148">CreateItem operation</span></span>](createitem-operation.md)
  
[<span data-ttu-id="c1ffc-149">Operación CreateItem (elemento de calendario)</span><span class="sxs-lookup"><span data-stu-id="c1ffc-149">CreateItem operation (calendar item)</span></span>](createitem-operation-calendar-item.md)

