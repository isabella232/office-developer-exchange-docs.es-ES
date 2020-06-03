---
title: Operación MoveItem
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
description: La operación MoveItem se usa para mover uno o más elementos a una única carpeta de destino.
ms.openlocfilehash: 6a455e483ad2e5c84b91cfaa7562f4f1ec46a112
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465684"
---
# <a name="moveitem-operation"></a><span data-ttu-id="ccfca-103">Operación MoveItem</span><span class="sxs-lookup"><span data-stu-id="ccfca-103">MoveItem operation</span></span>

<span data-ttu-id="ccfca-104">La operación **MoveItem** se usa para mover uno o más elementos a una única carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="ccfca-104">The **MoveItem** operation is used to move one or more items to a single destination folder.</span></span> 
  
## <a name="moveitem-request-example"></a><span data-ttu-id="ccfca-105">Ejemplo de solicitud MoveItem</span><span class="sxs-lookup"><span data-stu-id="ccfca-105">MoveItem request example</span></span>

### <a name="description"></a><span data-ttu-id="ccfca-106">Description</span><span class="sxs-lookup"><span data-stu-id="ccfca-106">Description</span></span>

<span data-ttu-id="ccfca-107">El siguiente ejemplo de una solicitud **MoveItem** muestra cómo mover un elemento a la carpeta Borradores.</span><span class="sxs-lookup"><span data-stu-id="ccfca-107">The following example of a **MoveItem** request shows how to move an item to the Drafts folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ccfca-108">Código</span><span class="sxs-lookup"><span data-stu-id="ccfca-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <MoveItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comments"></a><span data-ttu-id="ccfca-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ccfca-109">Comments</span></span>

<span data-ttu-id="ccfca-110">El elemento [ToFolderId](tofolderid.md) especifica la carpeta a la que se moverán los elementos.</span><span class="sxs-lookup"><span data-stu-id="ccfca-110">The [ToFolderId](tofolderid.md) element specifies the folder to which the items will be moved.</span></span> <span data-ttu-id="ccfca-111">Tenga en cuenta que todos los elementos que aparecen en la colección [ItemIds](itemids.md) terminarán en la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="ccfca-111">Note that all items listed in the [ItemIds](itemids.md) collection will end up in the destination folder.</span></span> <span data-ttu-id="ccfca-112">Debe realizar llamadas distintas de **MoveItem** para poner elementos en diferentes carpetas de destino.</span><span class="sxs-lookup"><span data-stu-id="ccfca-112">You must make separate **MoveItem** calls to place items in different destination folders.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ccfca-113">El identificador de elemento y la clave de cambio se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="ccfca-113">The item identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="ccfca-114">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="ccfca-114">Request elements</span></span>

<span data-ttu-id="ccfca-115">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="ccfca-115">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="ccfca-116">MoveItem</span><span class="sxs-lookup"><span data-stu-id="ccfca-116">MoveItem</span></span>](moveitem.md)
    
- [<span data-ttu-id="ccfca-117">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="ccfca-117">ToFolderId</span></span>](tofolderid.md)
    
- [<span data-ttu-id="ccfca-118">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="ccfca-118">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="ccfca-119">ItemIds</span><span class="sxs-lookup"><span data-stu-id="ccfca-119">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="ccfca-120">ItemId</span><span class="sxs-lookup"><span data-stu-id="ccfca-120">ItemId</span></span>](itemid.md)
    
## <a name="moveitem-response-example"></a><span data-ttu-id="ccfca-121">Ejemplo de respuesta MoveItem</span><span class="sxs-lookup"><span data-stu-id="ccfca-121">MoveItem response example</span></span>

### <a name="description"></a><span data-ttu-id="ccfca-122">Description</span><span class="sxs-lookup"><span data-stu-id="ccfca-122">Description</span></span>

<span data-ttu-id="ccfca-123">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud **MoveItem** .</span><span class="sxs-lookup"><span data-stu-id="ccfca-123">The following example shows a successful response to a **MoveItem** request.</span></span> 
  
<span data-ttu-id="ccfca-124">El identificador de elemento del nuevo elemento se devuelve en el mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="ccfca-124">The item identifier of the new item is returned in the response message.</span></span> <span data-ttu-id="ccfca-125">Los identificadores de elemento no se devuelven en las respuestas de las operaciones **MoveItem** de buzón o buzón entre buzones de correo y carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="ccfca-125">Item identifiers are not returned in responses for cross-mailbox or mailbox to public folder **MoveItem** operations.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ccfca-126">Código</span><span class="sxs-lookup"><span data-stu-id="ccfca-126">Code</span></span>

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
    <MoveItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="ccfca-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ccfca-127">Comments</span></span>

<span data-ttu-id="ccfca-128">La operación **MoveItem** indicará que se ha realizado correctamente si el movimiento se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ccfca-128">The **MoveItem** operation will indicate success if the move was successful.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="ccfca-129">Elementos Response correcto</span><span class="sxs-lookup"><span data-stu-id="ccfca-129">Successful response elements</span></span>

<span data-ttu-id="ccfca-130">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ccfca-130">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="ccfca-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ccfca-131">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="ccfca-132">MoveItemResponse</span><span class="sxs-lookup"><span data-stu-id="ccfca-132">MoveItemResponse</span></span>](moveitemresponse.md)
    
- [<span data-ttu-id="ccfca-133">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ccfca-133">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="ccfca-134">MoveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ccfca-134">MoveItemResponseMessage</span></span>](moveitemresponsemessage.md)
    
- [<span data-ttu-id="ccfca-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ccfca-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ccfca-136">Items</span><span class="sxs-lookup"><span data-stu-id="ccfca-136">Items</span></span>](items.md)
    
## <a name="see-also"></a><span data-ttu-id="ccfca-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="ccfca-137">See also</span></span>



- [<span data-ttu-id="ccfca-138">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ccfca-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

