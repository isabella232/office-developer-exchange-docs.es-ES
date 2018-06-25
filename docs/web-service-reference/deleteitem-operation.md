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
description: La operación DeleteItem elimina los elementos en el almacén de Exchange.
ms.openlocfilehash: 87d7853daa5db0cd87b3f6469c228a584b4d9caf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764101"
---
# <a name="deleteitem-operation"></a><span data-ttu-id="33c40-103">Operación DeleteItem</span><span class="sxs-lookup"><span data-stu-id="33c40-103">DeleteItem operation</span></span>

<span data-ttu-id="33c40-104">La operación **DeleteItem** elimina los elementos en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="33c40-104">The **DeleteItem** operation deletes items in the Exchange store.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="33c40-105">Se devuelve una respuesta de error que incluye el código de error de ErrorCannotDeleteObject para una operación de **DeleteItem** cuando un delegado intenta eliminar un elemento en el buzón de la entidad de seguridad mediante la configuración de la DisposalType a MoveToDeletedItems.</span><span class="sxs-lookup"><span data-stu-id="33c40-105">An error response that includes the ErrorCannotDeleteObject error code will be returned for a **DeleteItem** operation when a delegate tries to delete an item in the principal's mailbox by setting the DisposalType to MoveToDeletedItems.</span></span> <span data-ttu-id="33c40-106">Para eliminar un elemento moviendo a la carpeta Elementos eliminados, un delegado debe usar la [operación MoveItem](moveitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="33c40-106">To delete an item by moving it to the Deleted Items folder, a delegate must use the [MoveItem operation](moveitem-operation.md).</span></span> 
  
## <a name="deleteitem-request-example"></a><span data-ttu-id="33c40-107">Ejemplo de solicitud DeleteItem</span><span class="sxs-lookup"><span data-stu-id="33c40-107">DeleteItem request example</span></span>

### <a name="description"></a><span data-ttu-id="33c40-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="33c40-108">Description</span></span>

<span data-ttu-id="33c40-109">El siguiente ejemplo de una solicitud de **DeleteItem** muestra cómo realizar una eliminación de disco duro de un elemento de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="33c40-109">The following example of a **DeleteItem** request shows how to perform a hard delete of an item from a mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="33c40-110">El identificador de elemento se ha acortado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="33c40-110">The item ID has been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="33c40-111">Código</span><span class="sxs-lookup"><span data-stu-id="33c40-111">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <DeleteItem DeleteType="HardDelete" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemIds>
        <t:ItemId Id="AS4AUn=="/>
      </ItemIds>
    </DeleteItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="33c40-112">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="33c40-112">Request elements</span></span>

<span data-ttu-id="33c40-113">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="33c40-113">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="33c40-114">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="33c40-114">DeleteItem</span></span>](deleteitem.md)
    
- [<span data-ttu-id="33c40-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="33c40-115">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="33c40-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="33c40-116">ItemId</span></span>](itemid.md)
    
<span data-ttu-id="33c40-117">Para buscar otras opciones para el mensaje de solicitud de la operación **DeleteItem** , explore la jerarquía de esquema.</span><span class="sxs-lookup"><span data-stu-id="33c40-117">To find other options for the request message of the **DeleteItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="33c40-118">Comenzar en el elemento de [DeleteItem](deleteitem.md) .</span><span class="sxs-lookup"><span data-stu-id="33c40-118">Start at the [DeleteItem](deleteitem.md) element.</span></span> 
  
## <a name="successful-deleteitem-response"></a><span data-ttu-id="33c40-119">Respuesta DeleteItem es correcta</span><span class="sxs-lookup"><span data-stu-id="33c40-119">Successful DeleteItem response</span></span>

### <a name="description"></a><span data-ttu-id="33c40-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="33c40-120">Description</span></span>

<span data-ttu-id="33c40-121">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud de **DeleteItem** .</span><span class="sxs-lookup"><span data-stu-id="33c40-121">The following example shows a successful response to the **DeleteItem** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="33c40-122">Código</span><span class="sxs-lookup"><span data-stu-id="33c40-122">Code</span></span>

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
    <DeleteItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DeleteItemResponseMessage>
      </m:ResponseMessages>
    </DeleteItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="33c40-123">Elementos de respuesta correcta</span><span class="sxs-lookup"><span data-stu-id="33c40-123">Successful response elements</span></span>

<span data-ttu-id="33c40-124">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="33c40-124">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="33c40-125">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="33c40-125">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="33c40-126">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="33c40-126">DeleteItemResponse</span></span>](deleteitemresponse.md)
    
- [<span data-ttu-id="33c40-127">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="33c40-127">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="33c40-128">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="33c40-128">DeleteItemResponseMessage</span></span>](deleteitemresponsemessage.md)
    
- [<span data-ttu-id="33c40-129">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="33c40-129">ResponseCode</span></span>](responsecode.md)
    
<span data-ttu-id="33c40-130">Para buscar otras opciones para el mensaje de respuesta de la operación **DeleteItem** , explore la jerarquía de esquema.</span><span class="sxs-lookup"><span data-stu-id="33c40-130">To find other options for the response message of the **DeleteItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="33c40-131">Comenzar en el elemento de [DeleteItemResponse](deleteitemresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="33c40-131">Start at the [DeleteItemResponse](deleteitemresponse.md) element.</span></span> 
  
## <a name="deleteitem-error-response"></a><span data-ttu-id="33c40-132">Respuesta de error DeleteItem</span><span class="sxs-lookup"><span data-stu-id="33c40-132">DeleteItem error response</span></span>

### <a name="description"></a><span data-ttu-id="33c40-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="33c40-133">Description</span></span>

<span data-ttu-id="33c40-134">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de **DeleteItem** .</span><span class="sxs-lookup"><span data-stu-id="33c40-134">The following example shows an error response to a **DeleteItem** request.</span></span> <span data-ttu-id="33c40-135">Se creó el error debido a que la operación intentó eliminar un elemento que no se encontró en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="33c40-135">The error was created because the operation tried to delete an item that was not found in the Exchange store.</span></span> 
  
### <a name="code"></a><span data-ttu-id="33c40-136">Código</span><span class="sxs-lookup"><span data-stu-id="33c40-136">Code</span></span>

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
    <DeleteItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="33c40-137">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="33c40-137">Error response elements</span></span>

<span data-ttu-id="33c40-138">En la respuesta de error, se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="33c40-138">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="33c40-139">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="33c40-139">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="33c40-140">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="33c40-140">DeleteItemResponse</span></span>](deleteitemresponse.md)
    
- [<span data-ttu-id="33c40-141">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="33c40-141">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="33c40-142">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="33c40-142">DeleteItemResponseMessage</span></span>](deleteitemresponsemessage.md)
    
- [<span data-ttu-id="33c40-143">MessageText</span><span class="sxs-lookup"><span data-stu-id="33c40-143">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="33c40-144">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="33c40-144">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="33c40-145">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="33c40-145">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="33c40-146">Para buscar otras opciones para el mensaje de respuesta de error de la operación **DeleteItem** , explore la jerarquía de esquema.</span><span class="sxs-lookup"><span data-stu-id="33c40-146">To find other options for the error response message of the **DeleteItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="33c40-147">Comenzar en el elemento de [DeleteItemResponse](deleteitemresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="33c40-147">Start at the [DeleteItemResponse](deleteitemresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="33c40-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="33c40-148">See also</span></span>

- [<span data-ttu-id="33c40-149">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="33c40-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="33c40-150">Eliminación de contactos</span><span class="sxs-lookup"><span data-stu-id="33c40-150">Deleting Contacts</span></span>](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)  
- [<span data-ttu-id="33c40-151">Eliminación de mensajes de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="33c40-151">Deleting E-mail Messages</span></span>](http://msdn.microsoft.com/library/c40f2f0b-dae0-412f-b716-727e8c0949b4%28Office.15%29.aspx) 
- [<span data-ttu-id="33c40-152">Eliminación de tareas</span><span class="sxs-lookup"><span data-stu-id="33c40-152">Deleting Tasks</span></span>](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

