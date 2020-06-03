---
title: Operación SendItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendItem
api_type:
- schema
ms.assetid: 337b89ef-e1b7-45ed-92f3-8abe4200e4c7
description: La operación SendItem se usa para enviar mensajes de correo electrónico que se encuentran en el almacén de Exchange.
ms.openlocfilehash: 9136379e50723211fe5a483c7f113da4fa125fc1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530341"
---
# <a name="senditem-operation"></a><span data-ttu-id="dc513-103">Operación SendItem</span><span class="sxs-lookup"><span data-stu-id="dc513-103">SendItem operation</span></span>

<span data-ttu-id="dc513-104">La operación SendItem se usa para enviar mensajes de correo electrónico que se encuentran en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="dc513-104">The SendItem operation is used to send e-mail messages that are located in the Exchange store.</span></span>
  
## <a name="senditem-e-mail-message-request-example"></a><span data-ttu-id="dc513-105">Ejemplo de solicitud de SendItem (mensaje de correo electrónico)</span><span class="sxs-lookup"><span data-stu-id="dc513-105">SendItem (E-mail Message) request example</span></span>

### <a name="description"></a><span data-ttu-id="dc513-106">Description</span><span class="sxs-lookup"><span data-stu-id="dc513-106">Description</span></span>

<span data-ttu-id="dc513-107">En el siguiente ejemplo, se muestra cómo enviar un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="dc513-107">The following example shows how to send an e-mail message.</span></span>
  
### <a name="code"></a><span data-ttu-id="dc513-108">Código</span><span class="sxs-lookup"><span data-stu-id="dc513-108">Code</span></span>

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SendItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
              SaveItemToFolder="true">
      <ItemIds>
        <t:ItemId Id="AAAtAEF=" ChangeKey="CQAAABY+T" />
      </ItemIds>
    </SendItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="dc513-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dc513-109">Comments</span></span>

<span data-ttu-id="dc513-110">El identificador de elemento se ha abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="dc513-110">The item identifier has been shortened to preserve readability.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="dc513-111">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="dc513-111">Request elements</span></span>

<span data-ttu-id="dc513-112">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="dc513-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="dc513-113">SendItem</span><span class="sxs-lookup"><span data-stu-id="dc513-113">SendItem</span></span>](senditem.md)
    
- [<span data-ttu-id="dc513-114">ItemIds</span><span class="sxs-lookup"><span data-stu-id="dc513-114">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="dc513-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="dc513-115">ItemId</span></span>](itemid.md)
    
## <a name="successful-senditem-e-mail-message-response"></a><span data-ttu-id="dc513-116">Respuesta SendItem (mensaje de correo electrónico) correcta</span><span class="sxs-lookup"><span data-stu-id="dc513-116">Successful SendItem (E-mail Message) Response</span></span>

### <a name="description"></a><span data-ttu-id="dc513-117">Description</span><span class="sxs-lookup"><span data-stu-id="dc513-117">Description</span></span>

<span data-ttu-id="dc513-118">En el ejemplo siguiente se muestra una respuesta SendItem correcta.</span><span class="sxs-lookup"><span data-stu-id="dc513-118">The following example shows a successful SendItem response.</span></span>
  
### <a name="code"></a><span data-ttu-id="dc513-119">Código</span><span class="sxs-lookup"><span data-stu-id="dc513-119">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SendItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SendItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:SendItemResponseMessage>
      </m:ResponseMessages>
    </SendItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="dc513-120">Elementos Response correcto</span><span class="sxs-lookup"><span data-stu-id="dc513-120">Successful response elements</span></span>

<span data-ttu-id="dc513-121">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="dc513-121">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="dc513-122">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="dc513-122">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="dc513-123">SendItemResponse</span><span class="sxs-lookup"><span data-stu-id="dc513-123">SendItemResponse</span></span>](senditemresponse.md)
    
- [<span data-ttu-id="dc513-124">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="dc513-124">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="dc513-125">SendItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="dc513-125">SendItemResponseMessage</span></span>](senditemresponsemessage.md)
    
- [<span data-ttu-id="dc513-126">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="dc513-126">ResponseCode</span></span>](responsecode.md)
    
### <a name="comments"></a><span data-ttu-id="dc513-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dc513-127">Comments</span></span>

<span data-ttu-id="dc513-128">Un delegado que intenta enviar un mensaje de correo electrónico que se encuentra en la carpeta de borradores de la entidad de identidad con la opción SendAndSaveCopy establecida para guardar una copia en la carpeta completa de elementos enviados no podrá mover una copia del elemento enviado a la carpeta de elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="dc513-128">A delegate who tries to send an e-mail message that is located in the principal's Drafts folder with the SendAndSaveCopy option set to save a copy in the Sent Items distinguished folder will silently fail to move a copy of the sent item to the Sent Items distinguished folder.</span></span> <span data-ttu-id="dc513-129">El elemento permanecerá en la carpeta Borradores de la entidad de identidad.</span><span class="sxs-lookup"><span data-stu-id="dc513-129">The item will remain in the principal's Drafts folder.</span></span> <span data-ttu-id="dc513-130">La solución para este problema es especificar el buzón de la entidad de identidad en el elemento [DistinguishedFolderId](distinguishedfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="dc513-130">The workaround for this issue is to specify the principal's mailbox in the [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span> 
  
<span data-ttu-id="dc513-131">Un escenario adicional que se debe considerar es cuando un delegado crea un mensaje de correo electrónico y lo guarda en la carpeta Borradores del buzón de correo del delegado.</span><span class="sxs-lookup"><span data-stu-id="dc513-131">An additional scenario to consider is when a delegate creates an e-mail message and saves it to the Drafts folder of the delegate's mailbox.</span></span> <span data-ttu-id="dc513-132">Si el delegado intenta enviar el elemento y guardar una copia en la carpeta de elementos enviados de la entidad de la identidad, el mensaje se envía correctamente, el borrador permanece en la carpeta Borradores del delegado, el mensaje enviado no aparece en la carpeta elementos enviados del delegado o del principal, y la respuesta es un éxito.</span><span class="sxs-lookup"><span data-stu-id="dc513-132">If the delegate tries to send the item and save a copy to the principal's Sent Items distinguished folder, the message is sent correctly, the draft message remains in the delegate's Drafts folder, the sent message does not appear in either the delegate's or principal's Sent Items folder, and the response is a success.</span></span>
  
## <a name="invalid-senditem-e-mail-message-request-example"></a><span data-ttu-id="dc513-133">Ejemplo de solicitud de SendItem (mensaje de correo electrónico) no válido</span><span class="sxs-lookup"><span data-stu-id="dc513-133">Invalid SendItem (E-mail Message) request example</span></span>

### <a name="description"></a><span data-ttu-id="dc513-134">Description</span><span class="sxs-lookup"><span data-stu-id="dc513-134">Description</span></span>

<span data-ttu-id="dc513-135">En el ejemplo de código siguiente se muestra un ejemplo de una solicitud con un identificador no válido.</span><span class="sxs-lookup"><span data-stu-id="dc513-135">The following code sample shows an example of a request with an invalid identifier.</span></span>
  
### <a name="code"></a><span data-ttu-id="dc513-136">Código</span><span class="sxs-lookup"><span data-stu-id="dc513-136">Code</span></span>

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SendItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
              SaveItemToFolder="true">
      <ItemIds>
        <t:ItemId Id="%BadItemId%" ChangeKey="CQAAABYAAA" />
      </ItemIds>
    </SendItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="senditem-e-mail-message-error-response"></a><span data-ttu-id="dc513-137">Respuesta de error de SendItem (mensaje de correo electrónico)</span><span class="sxs-lookup"><span data-stu-id="dc513-137">SendItem (E-mail Message) error response</span></span>

### <a name="description"></a><span data-ttu-id="dc513-138">Description</span><span class="sxs-lookup"><span data-stu-id="dc513-138">Description</span></span>

<span data-ttu-id="dc513-139">En el ejemplo siguiente se muestra una respuesta de error a una solicitud SendItem que contiene un identificador no válido.</span><span class="sxs-lookup"><span data-stu-id="dc513-139">The following example shows an error response to a SendItem request that contains an invalid identifier.</span></span>
  
### <a name="code"></a><span data-ttu-id="dc513-140">Código</span><span class="sxs-lookup"><span data-stu-id="dc513-140">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SendItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SendItemResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:SendItemResponseMessage>
      </m:ResponseMessages>
    </SendItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="dc513-141">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="dc513-141">Error response elements</span></span>

<span data-ttu-id="dc513-142">Los siguientes elementos se usan en la respuesta de error:</span><span class="sxs-lookup"><span data-stu-id="dc513-142">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="dc513-143">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="dc513-143">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="dc513-144">SendItemResponse</span><span class="sxs-lookup"><span data-stu-id="dc513-144">SendItemResponse</span></span>](senditemresponse.md)
    
- [<span data-ttu-id="dc513-145">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="dc513-145">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="dc513-146">SendItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="dc513-146">SendItemResponseMessage</span></span>](senditemresponsemessage.md)
    
- [<span data-ttu-id="dc513-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="dc513-147">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="dc513-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="dc513-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="dc513-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="dc513-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="dc513-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc513-150">See also</span></span>



[<span data-ttu-id="dc513-151">Operación SendItem</span><span class="sxs-lookup"><span data-stu-id="dc513-151">SendItem operation</span></span>](senditem-operation.md)
  
 <span data-ttu-id="dc513-152">**SendItemType**</span><span class="sxs-lookup"><span data-stu-id="dc513-152">**SendItemType**</span></span>


- [<span data-ttu-id="dc513-153">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="dc513-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

