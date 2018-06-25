---
title: CopyItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyItem
api_type:
- schema
ms.assetid: bcc68f9e-d511-4c29-bba6-ed535524624a
description: La operación CopyItem copia elementos y coloca los elementos en una carpeta diferente.
ms.openlocfilehash: 95d2371e9185aa25f40eaec37dda54276a54d321
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763899"
---
# <a name="copyitem-operation"></a><span data-ttu-id="0b2ec-103">CopyItem Operation</span><span class="sxs-lookup"><span data-stu-id="0b2ec-103">CopyItem operation</span></span>

<span data-ttu-id="0b2ec-104">La operación **CopyItem** copia elementos y coloca los elementos en una carpeta diferente.</span><span class="sxs-lookup"><span data-stu-id="0b2ec-104">The **CopyItem** operation copies items and puts the items in a different folder.</span></span> 
  
## <a name="copyitem-request-example"></a><span data-ttu-id="0b2ec-105">Ejemplo de solicitud de CopyItem</span><span class="sxs-lookup"><span data-stu-id="0b2ec-105">CopyItem request example</span></span>

### <a name="description"></a><span data-ttu-id="0b2ec-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b2ec-106">Description</span></span>

<span data-ttu-id="0b2ec-107">El siguiente ejemplo de una solicitud de **CopyItem** muestra cómo formar una solicitud para copiar un elemento a la Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="0b2ec-107">The following example of a **CopyItem** request shows how to form a request to copy an item to the Inbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="0b2ec-108">Código</span><span class="sxs-lookup"><span data-stu-id="0b2ec-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CopyItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ToFolderId>
        <t:DistinguishedFolderId Id="inbox"/>
      </ToFolderId>
      <ItemIds>
        <t:ItemId Id="AS4AUnV="/>
      </ItemIds>
    </CopyItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="0b2ec-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0b2ec-109">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="0b2ec-110">El identificador de la carpeta y la clave de cambio se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="0b2ec-110">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="0b2ec-111">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="0b2ec-111">Request elements</span></span>

<span data-ttu-id="0b2ec-112">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0b2ec-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="0b2ec-113">CopyItem</span><span class="sxs-lookup"><span data-stu-id="0b2ec-113">CopyItem</span></span>](copyitem.md)
    
- [<span data-ttu-id="0b2ec-114">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="0b2ec-114">ToFolderId</span></span>](tofolderid.md)
    
- [<span data-ttu-id="0b2ec-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="0b2ec-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="0b2ec-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="0b2ec-116">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="0b2ec-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="0b2ec-117">ItemId</span></span>](itemid.md)
    
> [!NOTE]
> <span data-ttu-id="0b2ec-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="0b2ec-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="0b2ec-119">Para buscar otras opciones para el mensaje de solicitud de la operación **CopyItem** , explore la jerarquía de esquema.</span><span class="sxs-lookup"><span data-stu-id="0b2ec-119">To find other options for the request message of the **CopyItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="0b2ec-120">Comenzar en el elemento de [CopyItem](copyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="0b2ec-120">Start at the [CopyItem](copyitem.md) element.</span></span> 
  
## <a name="successful-copyitem-response"></a><span data-ttu-id="0b2ec-121">Respuesta CopyItem es correcta</span><span class="sxs-lookup"><span data-stu-id="0b2ec-121">Successful CopyItem Response</span></span>

### <a name="description"></a><span data-ttu-id="0b2ec-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b2ec-122">Description</span></span>

<span data-ttu-id="0b2ec-123">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud de **CopyItem** .</span><span class="sxs-lookup"><span data-stu-id="0b2ec-123">The following example shows a successful response to the **CopyItem** request.</span></span> 
  
<span data-ttu-id="0b2ec-124">Se devuelve el identificador de elemento del nuevo elemento en el mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="0b2ec-124">The item identifier of the new item is returned in the response message.</span></span> <span data-ttu-id="0b2ec-125">Identificadores de elemento no se devuelven en las respuestas para entre buzones de correo o buzón de correo a las operaciones de **CopyItem** de carpeta pública.</span><span class="sxs-lookup"><span data-stu-id="0b2ec-125">Item identifiers are not returned in responses for cross-mailbox or mailbox to public folder **CopyItem** operations.</span></span> 
  
### <a name="code"></a><span data-ttu-id="0b2ec-126">Código</span><span class="sxs-lookup"><span data-stu-id="0b2ec-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CopyItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CopyItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemID Id="AAMkAd" ChangeKey="FwAAABY" />
            </t:Message>
          </m:Items>
        </m:CopyItemResponseMessage>
      </m:ResponseMessages>
    </CopyItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="0b2ec-127">Elementos de respuesta correcta</span><span class="sxs-lookup"><span data-stu-id="0b2ec-127">Successful response elements</span></span>

<span data-ttu-id="0b2ec-128">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0b2ec-128">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="0b2ec-129">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0b2ec-129">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="0b2ec-130">CopyItemResponse</span><span class="sxs-lookup"><span data-stu-id="0b2ec-130">CopyItemResponse</span></span>](copyitemresponse.md)
    
- [<span data-ttu-id="0b2ec-131">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0b2ec-131">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="0b2ec-132">CopyItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0b2ec-132">CopyItemResponseMessage</span></span>](copyitemresponsemessage.md)
    
- [<span data-ttu-id="0b2ec-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0b2ec-133">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0b2ec-134">Items</span><span class="sxs-lookup"><span data-stu-id="0b2ec-134">Items</span></span>](items.md)
    
<span data-ttu-id="0b2ec-135">Para buscar otras opciones para el mensaje de respuesta de la operación **CopyItem** , explore la jerarquía de esquema.</span><span class="sxs-lookup"><span data-stu-id="0b2ec-135">To find other options for the response message of the **CopyItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="0b2ec-136">Comenzar en el elemento de [CopyItemResponse](copyitemresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="0b2ec-136">Start at the [CopyItemResponse](copyitemresponse.md) element.</span></span> 
  
## <a name="copyitem-error-response"></a><span data-ttu-id="0b2ec-137">Respuesta de error CopyItem</span><span class="sxs-lookup"><span data-stu-id="0b2ec-137">CopyItem error response</span></span>

### <a name="description"></a><span data-ttu-id="0b2ec-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b2ec-138">Description</span></span>

<span data-ttu-id="0b2ec-139">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de **CopyItem** .</span><span class="sxs-lookup"><span data-stu-id="0b2ec-139">The following example shows an error response to a **CopyItem** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="0b2ec-140">Código</span><span class="sxs-lookup"><span data-stu-id="0b2ec-140">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CopyItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CopyItemResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Items />
        </m:CopyItemResponseMessage>
      </m:ResponseMessages>
    </CopyItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="0b2ec-141">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="0b2ec-141">Error response elements</span></span>

<span data-ttu-id="0b2ec-142">En la respuesta de error, se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0b2ec-142">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="0b2ec-143">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0b2ec-143">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="0b2ec-144">CopyItemResponse</span><span class="sxs-lookup"><span data-stu-id="0b2ec-144">CopyItemResponse</span></span>](copyitemresponse.md)
    
- [<span data-ttu-id="0b2ec-145">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0b2ec-145">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="0b2ec-146">CopyItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0b2ec-146">CopyItemResponseMessage</span></span>](copyitemresponsemessage.md)
    
- [<span data-ttu-id="0b2ec-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="0b2ec-147">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="0b2ec-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0b2ec-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0b2ec-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0b2ec-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="0b2ec-150">Items</span><span class="sxs-lookup"><span data-stu-id="0b2ec-150">Items</span></span>](items.md)
    
<span data-ttu-id="0b2ec-151">Para buscar otras opciones para el mensaje de respuesta de error de la operación **CopyItem** , explore la jerarquía de esquema.</span><span class="sxs-lookup"><span data-stu-id="0b2ec-151">To find other options for the error response message of the **CopyItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="0b2ec-152">Comenzar en el elemento de [CopyItemResponse](copyitemresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="0b2ec-152">Start at the [CopyItemResponse](copyitemresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0b2ec-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b2ec-153">See also</span></span>



- [<span data-ttu-id="0b2ec-154">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0b2ec-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

