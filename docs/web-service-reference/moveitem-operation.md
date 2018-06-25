---
title: MoveItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveItem
api_type:
- schema
ms.assetid: dcf40fa7-7796-4a5c-bf5b-7a509a18d208
description: La operación MoveItem se usa para mover uno o varios elementos a una sola carpeta de destino.
ms.openlocfilehash: c5619befb02ec20ef0911992484dcc00cc2c5e92
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836492"
---
# <a name="moveitem-operation"></a><span data-ttu-id="7e825-103">MoveItem Operation</span><span class="sxs-lookup"><span data-stu-id="7e825-103">MoveItem operation</span></span>

<span data-ttu-id="7e825-104">La operación **MoveItem** se usa para mover uno o varios elementos a una sola carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="7e825-104">The **MoveItem** operation is used to move one or more items to a single destination folder.</span></span> 
  
## <a name="moveitem-request-example"></a><span data-ttu-id="7e825-105">Ejemplo de solicitud MoveItem</span><span class="sxs-lookup"><span data-stu-id="7e825-105">MoveItem request example</span></span>

### <a name="description"></a><span data-ttu-id="7e825-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e825-106">Description</span></span>

<span data-ttu-id="7e825-107">El siguiente ejemplo de una solicitud de **MoveItem** muestra cómo mover un elemento a la carpeta Borradores.</span><span class="sxs-lookup"><span data-stu-id="7e825-107">The following example of a **MoveItem** request shows how to move an item to the Drafts folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="7e825-108">Código</span><span class="sxs-lookup"><span data-stu-id="7e825-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <MoveItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <ToFolderId>
        <t:DistinguishedFolderId Id="drafts"/>
      </ToFolderId>
      <ItemIds>
        <t:ItemId Id="AAAtAEF/swbAAA=" ChangeKey="EwAAABYA/s4b"/>
      </ItemIds>
    </MoveItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="7e825-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7e825-109">Comments</span></span>

<span data-ttu-id="7e825-110">El elemento [ToFolderId](tofolderid.md) especifica la carpeta a la que se moverán los elementos.</span><span class="sxs-lookup"><span data-stu-id="7e825-110">The [ToFolderId](tofolderid.md) element specifies the folder to which the items will be moved.</span></span> <span data-ttu-id="7e825-111">Tenga en cuenta que todos los elementos que aparecen en la colección [ItemID](itemids.md) acabará en la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="7e825-111">Note that all items listed in the [ItemIds](itemids.md) collection will end up in the destination folder.</span></span> <span data-ttu-id="7e825-112">Debe realizar llamadas de **MoveItem** independientes para colocar los elementos en las carpetas de destino diferente.</span><span class="sxs-lookup"><span data-stu-id="7e825-112">You must make separate **MoveItem** calls to place items in different destination folders.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7e825-113">El identificador de elemento y la clave de cambio se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="7e825-113">The item identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="7e825-114">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="7e825-114">Request elements</span></span>

<span data-ttu-id="7e825-115">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="7e825-115">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="7e825-116">MoveItem</span><span class="sxs-lookup"><span data-stu-id="7e825-116">MoveItem</span></span>](moveitem.md)
    
- [<span data-ttu-id="7e825-117">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="7e825-117">ToFolderId</span></span>](tofolderid.md)
    
- [<span data-ttu-id="7e825-118">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="7e825-118">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="7e825-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="7e825-119">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="7e825-120">ItemId</span><span class="sxs-lookup"><span data-stu-id="7e825-120">ItemId</span></span>](itemid.md)
    
## <a name="moveitem-response-example"></a><span data-ttu-id="7e825-121">Ejemplo de respuesta MoveItem</span><span class="sxs-lookup"><span data-stu-id="7e825-121">MoveItem response example</span></span>

### <a name="description"></a><span data-ttu-id="7e825-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e825-122">Description</span></span>

<span data-ttu-id="7e825-123">En el ejemplo siguiente se muestra una respuesta a una solicitud de **MoveItem** correcta.</span><span class="sxs-lookup"><span data-stu-id="7e825-123">The following example shows a successful response to a **MoveItem** request.</span></span> 
  
<span data-ttu-id="7e825-124">Se devuelve el identificador de elemento del nuevo elemento en el mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="7e825-124">The item identifier of the new item is returned in the response message.</span></span> <span data-ttu-id="7e825-125">Identificadores de elemento no se devuelven en las respuestas para entre buzones de correo o buzón de correo a las operaciones de **MoveItem** de carpeta pública.</span><span class="sxs-lookup"><span data-stu-id="7e825-125">Item identifiers are not returned in responses for cross-mailbox or mailbox to public folder **MoveItem** operations.</span></span> 
  
### <a name="code"></a><span data-ttu-id="7e825-126">Código</span><span class="sxs-lookup"><span data-stu-id="7e825-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="662" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <MoveItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:MoveItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemID Id="AAMkAd" ChangeKey="FwAAABY" />
            </t:Message>
          </m:Items>
        </m:MoveItemResponseMessage>
      </m:ResponseMessages>
    </MoveItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="7e825-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7e825-127">Comments</span></span>

<span data-ttu-id="7e825-128">La operación **MoveItem** indicará éxito si el movimiento se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="7e825-128">The **MoveItem** operation will indicate success if the move was successful.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="7e825-129">Elementos de respuesta correcta</span><span class="sxs-lookup"><span data-stu-id="7e825-129">Successful response elements</span></span>

<span data-ttu-id="7e825-130">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="7e825-130">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="7e825-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="7e825-131">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="7e825-132">MoveItemResponse</span><span class="sxs-lookup"><span data-stu-id="7e825-132">MoveItemResponse</span></span>](moveitemresponse.md)
    
- [<span data-ttu-id="7e825-133">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7e825-133">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="7e825-134">MoveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7e825-134">MoveItemResponseMessage</span></span>](moveitemresponsemessage.md)
    
- [<span data-ttu-id="7e825-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7e825-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="7e825-136">Items</span><span class="sxs-lookup"><span data-stu-id="7e825-136">Items</span></span>](items.md)
    
## <a name="see-also"></a><span data-ttu-id="7e825-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e825-137">See also</span></span>



- [<span data-ttu-id="7e825-138">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="7e825-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

