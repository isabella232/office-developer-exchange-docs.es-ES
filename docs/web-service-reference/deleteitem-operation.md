---
title: Operación DeleteItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItem
api_type:
- schema
ms.assetid: 3e26c416-fa12-476e-bfd2-5c1f4bb7b348
description: La operación DeleteItem elimina elementos en el almacén de Exchange.
ms.openlocfilehash: f068e08ef0d0f590c9ed8274f77d4dae9f942995
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526938"
---
# <a name="deleteitem-operation"></a><span data-ttu-id="a9bf1-103">Operación DeleteItem</span><span class="sxs-lookup"><span data-stu-id="a9bf1-103">DeleteItem operation</span></span>

<span data-ttu-id="a9bf1-104">La operación **DeleteItem** elimina elementos en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a9bf1-104">The **DeleteItem** operation deletes items in the Exchange store.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a9bf1-105">Se devolverá una respuesta de error que incluye el código de error ErrorCannotDeleteObject para una operación **DeleteItem** cuando un delegado intenta eliminar un elemento en el buzón de la entidad de identidad al configurar DisposalType en MoveToDeletedItems.</span><span class="sxs-lookup"><span data-stu-id="a9bf1-105">An error response that includes the ErrorCannotDeleteObject error code will be returned for a **DeleteItem** operation when a delegate tries to delete an item in the principal's mailbox by setting the DisposalType to MoveToDeletedItems.</span></span> <span data-ttu-id="a9bf1-106">Para eliminar un elemento moviéndolo a la carpeta elementos eliminados, un delegado debe usar la [operación MoveItem](moveitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="a9bf1-106">To delete an item by moving it to the Deleted Items folder, a delegate must use the [MoveItem operation](moveitem-operation.md).</span></span> 
  
## <a name="deleteitem-request-example"></a><span data-ttu-id="a9bf1-107">Ejemplo de solicitud DeleteItem</span><span class="sxs-lookup"><span data-stu-id="a9bf1-107">DeleteItem request example</span></span>

### <a name="description"></a><span data-ttu-id="a9bf1-108">Description</span><span class="sxs-lookup"><span data-stu-id="a9bf1-108">Description</span></span>

<span data-ttu-id="a9bf1-109">El siguiente ejemplo de una solicitud **DeleteItem** muestra cómo realizar una eliminación de un elemento de un buzón.</span><span class="sxs-lookup"><span data-stu-id="a9bf1-109">The following example of a **DeleteItem** request shows how to perform a hard delete of an item from a mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a9bf1-110">El identificador de elemento se ha abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="a9bf1-110">The item ID has been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="a9bf1-111">Código</span><span class="sxs-lookup"><span data-stu-id="a9bf1-111">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <DeleteItem DeleteType="HardDelete" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemIds>
        <t:ItemId Id="AS4AUn=="/>
      </ItemIds>
    </DeleteItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="a9bf1-112">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="a9bf1-112">Request elements</span></span>

<span data-ttu-id="a9bf1-113">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="a9bf1-113">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="a9bf1-114">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="a9bf1-114">DeleteItem</span></span>](deleteitem.md)
    
- [<span data-ttu-id="a9bf1-115">ItemIds</span><span class="sxs-lookup"><span data-stu-id="a9bf1-115">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="a9bf1-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="a9bf1-116">ItemId</span></span>](itemid.md)
    
<span data-ttu-id="a9bf1-117">Para buscar otras opciones para el mensaje de solicitud de la operación **DeleteItem** , explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="a9bf1-117">To find other options for the request message of the **DeleteItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="a9bf1-118">Comienza en el elemento [DeleteItem](deleteitem.md) .</span><span class="sxs-lookup"><span data-stu-id="a9bf1-118">Start at the [DeleteItem](deleteitem.md) element.</span></span> 
  
## <a name="successful-deleteitem-response"></a><span data-ttu-id="a9bf1-119">Respuesta DeleteItem correcta</span><span class="sxs-lookup"><span data-stu-id="a9bf1-119">Successful DeleteItem response</span></span>

### <a name="description"></a><span data-ttu-id="a9bf1-120">Description</span><span class="sxs-lookup"><span data-stu-id="a9bf1-120">Description</span></span>

<span data-ttu-id="a9bf1-121">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud **DeleteItem** .</span><span class="sxs-lookup"><span data-stu-id="a9bf1-121">The following example shows a successful response to the **DeleteItem** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="a9bf1-122">Código</span><span class="sxs-lookup"><span data-stu-id="a9bf1-122">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <DeleteItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DeleteItemResponseMessage>
      </m:ResponseMessages>
    </DeleteItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="a9bf1-123">Elementos Response correcto</span><span class="sxs-lookup"><span data-stu-id="a9bf1-123">Successful response elements</span></span>

<span data-ttu-id="a9bf1-124">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="a9bf1-124">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="a9bf1-125">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a9bf1-125">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="a9bf1-126">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="a9bf1-126">DeleteItemResponse</span></span>](deleteitemresponse.md)
    
- [<span data-ttu-id="a9bf1-127">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a9bf1-127">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="a9bf1-128">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a9bf1-128">DeleteItemResponseMessage</span></span>](deleteitemresponsemessage.md)
    
- [<span data-ttu-id="a9bf1-129">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a9bf1-129">ResponseCode</span></span>](responsecode.md)
    
<span data-ttu-id="a9bf1-130">Para buscar otras opciones para el mensaje de respuesta de la operación **DeleteItem** , explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="a9bf1-130">To find other options for the response message of the **DeleteItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="a9bf1-131">Empiece en el elemento [DeleteItemResponse](deleteitemresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="a9bf1-131">Start at the [DeleteItemResponse](deleteitemresponse.md) element.</span></span> 
  
## <a name="deleteitem-error-response"></a><span data-ttu-id="a9bf1-132">Respuesta de error DeleteItem</span><span class="sxs-lookup"><span data-stu-id="a9bf1-132">DeleteItem error response</span></span>

### <a name="description"></a><span data-ttu-id="a9bf1-133">Description</span><span class="sxs-lookup"><span data-stu-id="a9bf1-133">Description</span></span>

<span data-ttu-id="a9bf1-134">En el ejemplo siguiente se muestra una respuesta de error a una solicitud **DeleteItem** .</span><span class="sxs-lookup"><span data-stu-id="a9bf1-134">The following example shows an error response to a **DeleteItem** request.</span></span> <span data-ttu-id="a9bf1-135">El error se creó porque la operación intentó eliminar un elemento que no se encontró en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a9bf1-135">The error was created because the operation tried to delete an item that was not found in the Exchange store.</span></span> 
  
### <a name="code"></a><span data-ttu-id="a9bf1-136">Código</span><span class="sxs-lookup"><span data-stu-id="a9bf1-136">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <DeleteItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteItemResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:DeleteItemResponseMessage>
      </m:ResponseMessages>
    </DeleteItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="a9bf1-137">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="a9bf1-137">Error response elements</span></span>

<span data-ttu-id="a9bf1-138">Los siguientes elementos se usan en la respuesta de error:</span><span class="sxs-lookup"><span data-stu-id="a9bf1-138">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="a9bf1-139">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a9bf1-139">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="a9bf1-140">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="a9bf1-140">DeleteItemResponse</span></span>](deleteitemresponse.md)
    
- [<span data-ttu-id="a9bf1-141">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a9bf1-141">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="a9bf1-142">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a9bf1-142">DeleteItemResponseMessage</span></span>](deleteitemresponsemessage.md)
    
- [<span data-ttu-id="a9bf1-143">MessageText</span><span class="sxs-lookup"><span data-stu-id="a9bf1-143">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="a9bf1-144">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a9bf1-144">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="a9bf1-145">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="a9bf1-145">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="a9bf1-146">Para buscar otras opciones para el mensaje de respuesta de error de la operación **DeleteItem** , explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="a9bf1-146">To find other options for the error response message of the **DeleteItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="a9bf1-147">Empiece en el elemento [DeleteItemResponse](deleteitemresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="a9bf1-147">Start at the [DeleteItemResponse](deleteitemresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a9bf1-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9bf1-148">See also</span></span>

- [<span data-ttu-id="a9bf1-149">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a9bf1-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="a9bf1-150">Eliminación de contactos</span><span class="sxs-lookup"><span data-stu-id="a9bf1-150">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)  
- [<span data-ttu-id="a9bf1-151">Eliminación de mensajes de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="a9bf1-151">Deleting E-mail Messages</span></span>](https://msdn.microsoft.com/library/c40f2f0b-dae0-412f-b716-727e8c0949b4%28Office.15%29.aspx) 
- [<span data-ttu-id="a9bf1-152">Eliminación de tareas</span><span class="sxs-lookup"><span data-stu-id="a9bf1-152">Deleting Tasks</span></span>](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

