---
title: Operación CreateItem (mensaje de correo electrónico)
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
ms.assetid: fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1
description: La operación CreateItem se usa para crear mensajes de correo electrónico.
ms.openlocfilehash: 384ed8ff653029c2b7db0b36986d85842b0a06cf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457119"
---
# <a name="createitem-operation-email-message"></a><span data-ttu-id="b806a-103">Operación CreateItem (mensaje de correo electrónico)</span><span class="sxs-lookup"><span data-stu-id="b806a-103">CreateItem operation (email message)</span></span>

<span data-ttu-id="b806a-104">La operación CreateItem se usa para crear mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="b806a-104">The CreateItem operation is used to create e-mail messages.</span></span>
  
## <a name="createitem-request-example"></a><span data-ttu-id="b806a-105">Ejemplo de solicitud CreateItem</span><span class="sxs-lookup"><span data-stu-id="b806a-105">CreateItem request example</span></span>

### <a name="description"></a><span data-ttu-id="b806a-106">Description</span><span class="sxs-lookup"><span data-stu-id="b806a-106">Description</span></span>

<span data-ttu-id="b806a-107">El siguiente ejemplo de una solicitud CreateItem muestra cómo crear un nuevo mensaje de correo electrónico, enviar el mensaje y guardar una copia en la carpeta Borradores.</span><span class="sxs-lookup"><span data-stu-id="b806a-107">The following example of a CreateItem request shows how to create a new e-mail message, send the message, and save a copy of it in the drafts folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="b806a-108">Código</span><span class="sxs-lookup"><span data-stu-id="b806a-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem MessageDisposition="SendAndSaveCopy" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <SavedItemFolderId>
        <t:DistinguishedFolderId Id="drafts" />
      </SavedItemFolderId>
      <Items>
        <t:Message>
          <t:ItemClass>IPM.Note</t:ItemClass>
          <t:Subject>Project Action</t:Subject>
          <t:Body BodyType="Text">Priority - Update specification</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sschmidt@example.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
          <t:IsRead>false</t:IsRead>
        </t:Message>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="b806a-109">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="b806a-109">Request elements</span></span>

<span data-ttu-id="b806a-110">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="b806a-110">The following elements are used in the request:</span></span> 
  
- [<span data-ttu-id="b806a-111">CreateItem</span><span class="sxs-lookup"><span data-stu-id="b806a-111">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="b806a-112">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="b806a-112">SavedItemFolderId</span></span>](saveditemfolderid.md)
    
- [<span data-ttu-id="b806a-113">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="b806a-113">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="b806a-114">Message</span><span class="sxs-lookup"><span data-stu-id="b806a-114">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="b806a-115">ItemClass</span><span class="sxs-lookup"><span data-stu-id="b806a-115">ItemClass</span></span>](itemclass.md)
    
- [<span data-ttu-id="b806a-116">Asunto</span><span class="sxs-lookup"><span data-stu-id="b806a-116">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="b806a-117">Body</span><span class="sxs-lookup"><span data-stu-id="b806a-117">Body</span></span>](body.md)
    
- [<span data-ttu-id="b806a-118">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="b806a-118">ToRecipients</span></span>](torecipients.md)
    
- [<span data-ttu-id="b806a-119">Buzón</span><span class="sxs-lookup"><span data-stu-id="b806a-119">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="b806a-120">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="b806a-120">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="b806a-121">IsRead</span><span class="sxs-lookup"><span data-stu-id="b806a-121">IsRead</span></span>](isread.md)
    
<span data-ttu-id="b806a-122">Para buscar otras opciones para el mensaje de solicitud de la operación CreateItem, explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="b806a-122">To find other options for the request message of the CreateItem operation, explore the schema hierarchy.</span></span> <span data-ttu-id="b806a-123">Comience en el elemento [CreateItem](createitem.md) .</span><span class="sxs-lookup"><span data-stu-id="b806a-123">Start at the [CreateItem](createitem.md) element.</span></span> 
  
## <a name="successful-createitem-response"></a><span data-ttu-id="b806a-124">Respuesta de CreateItem correcta</span><span class="sxs-lookup"><span data-stu-id="b806a-124">Successful CreateItem Response</span></span>

### <a name="description"></a><span data-ttu-id="b806a-125">Description</span><span class="sxs-lookup"><span data-stu-id="b806a-125">Description</span></span>

<span data-ttu-id="b806a-126">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud CreateItem.</span><span class="sxs-lookup"><span data-stu-id="b806a-126">The following example shows a successful response to the CreateItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="b806a-127">Código</span><span class="sxs-lookup"><span data-stu-id="b806a-127">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
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

### <a name="successful-response-elements"></a><span data-ttu-id="b806a-128">Elementos Response correcto</span><span class="sxs-lookup"><span data-stu-id="b806a-128">Successful response elements</span></span>

<span data-ttu-id="b806a-129">En la respuesta se incluyen los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="b806a-129">The following elements are included in the response:</span></span> 
  
- [<span data-ttu-id="b806a-130">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="b806a-130">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="b806a-131">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b806a-131">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="b806a-132">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b806a-132">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="b806a-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b806a-133">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="b806a-134">Items</span><span class="sxs-lookup"><span data-stu-id="b806a-134">Items</span></span>](items.md)
    
<span data-ttu-id="b806a-135">Para buscar otras opciones para el mensaje de respuesta de la operación CreateItem, explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="b806a-135">To find other options for the response message of the CreateItem operation, explore the schema hierarchy.</span></span> <span data-ttu-id="b806a-136">Empiece en el elemento [CreateItemResponse](createitemresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="b806a-136">Start at the [CreateItemResponse](createitemresponse.md) element.</span></span> 
  
## <a name="error-createitem-response"></a><span data-ttu-id="b806a-137">Error CreateItem Response</span><span class="sxs-lookup"><span data-stu-id="b806a-137">Error CreateItem Response</span></span>

### <a name="description"></a><span data-ttu-id="b806a-138">Description</span><span class="sxs-lookup"><span data-stu-id="b806a-138">Description</span></span>

<span data-ttu-id="b806a-139">En el ejemplo siguiente se muestra una respuesta de error a una solicitud CreateItem.</span><span class="sxs-lookup"><span data-stu-id="b806a-139">The following example shows an error response to a CreateItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="b806a-140">Código</span><span class="sxs-lookup"><span data-stu-id="b806a-140">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Error">
          <m:MessageText>The user account which was used to submit this request does not have the right to send mail on behalf of the specified sending account.</m:MessageText>
          <m:ResponseCode>ErrorSendAsDenied</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Items />
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="b806a-141">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="b806a-141">Error response elements</span></span>

<span data-ttu-id="b806a-142">Los siguientes elementos se usan en la respuesta de error:</span><span class="sxs-lookup"><span data-stu-id="b806a-142">The following elements are used in the error response:</span></span> 
  
- [<span data-ttu-id="b806a-143">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="b806a-143">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="b806a-144">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b806a-144">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="b806a-145">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b806a-145">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="b806a-146">MessageText</span><span class="sxs-lookup"><span data-stu-id="b806a-146">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="b806a-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b806a-147">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="b806a-148">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="b806a-148">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="b806a-149">Items</span><span class="sxs-lookup"><span data-stu-id="b806a-149">Items</span></span>](items.md)
    
<span data-ttu-id="b806a-150">Para buscar otras opciones para el mensaje de respuesta de error de la operación CreateItem, explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="b806a-150">To find other options for the error response message of the CreateItem operation, explore the schema hierarchy.</span></span> <span data-ttu-id="b806a-151">Empiece en el elemento [CreateItemResponse](createitemresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="b806a-151">Start at the [CreateItemResponse](createitemresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b806a-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="b806a-152">See also</span></span>



[<span data-ttu-id="b806a-153">Operación CreateItem</span><span class="sxs-lookup"><span data-stu-id="b806a-153">CreateItem operation</span></span>](createitem-operation.md)

