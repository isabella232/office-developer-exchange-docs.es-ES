---
title: Operación GetAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetAttachment
api_type:
- schema
ms.assetid: 24d10a15-b942-415e-9024-a6375708f326
description: La operación GetAttachment se usa para recuperar datos adjuntos existentes en los elementos del almacén de Exchange.
ms.openlocfilehash: ac7eafd61c62b077a8d20e5fd8d004924bf06cf1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461292"
---
# <a name="getattachment-operation"></a><span data-ttu-id="6b32e-103">Operación GetAttachment</span><span class="sxs-lookup"><span data-stu-id="6b32e-103">GetAttachment operation</span></span>

<span data-ttu-id="6b32e-104">La operación GetAttachment se usa para recuperar datos adjuntos existentes en los elementos del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6b32e-104">The GetAttachment operation is used to retrieve existing attachments on items in the Exchange store.</span></span>
  
## <a name="getattachment-request-example"></a><span data-ttu-id="6b32e-105">Ejemplo de solicitud GetAttachment</span><span class="sxs-lookup"><span data-stu-id="6b32e-105">GetAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="6b32e-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b32e-106">Description</span></span>

<span data-ttu-id="6b32e-107">El siguiente ejemplo de solicitud GetAttachment muestra cómo obtener datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="6b32e-107">The following example of GetAttachment request shows how to get an attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="6b32e-108">Código</span><span class="sxs-lookup"><span data-stu-id="6b32e-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape/>
      <AttachmentIds>
        <t:AttachmentId Id="AAAtAEFkbWluaX..."/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="6b32e-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b32e-109">Comments</span></span>

<span data-ttu-id="6b32e-110">El elemento [AttachmentShape](attachmentshape.md) permite especificar qué información de archivos adjuntos se debe devolver.</span><span class="sxs-lookup"><span data-stu-id="6b32e-110">The [AttachmentShape](attachmentshape.md) element allows you to specify which attachment information should be returned.</span></span> <span data-ttu-id="6b32e-111">Un elemento [AttachmentShape](attachmentshape.md) vacío es válido y representará los datos adjuntos sin contenido MIME para los datos adjuntos de elemento, con un tipo de cuerpo de texto y sin propiedades adicionales.</span><span class="sxs-lookup"><span data-stu-id="6b32e-111">An empty [AttachmentShape](attachmentshape.md) element is valid and will render your attachments without MIME content for item attachments, with a text body type, and without any additional properties.</span></span> 
  
<span data-ttu-id="6b32e-112">La colección [identificadores](attachmentids.md) permite especificar uno o más identificadores de datos adjuntos que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="6b32e-112">The [AttachmentIds](attachmentids.md) collection allows you to specify one or more attachment identifiers to return.</span></span> <span data-ttu-id="6b32e-113">Tenga en cuenta que son de tipo RequestAttachmentIdType, por lo que cualquier identificadores que reciba de **CreateAttachment** debe tener los atributos **RootItemId** y **RootItemChangeKey** antes de pasarlos a **GetAttachment**.</span><span class="sxs-lookup"><span data-stu-id="6b32e-113">Note that these are of type RequestAttachmentIdType, so any AttachmentIds that you receive from **CreateAttachment** must have the **RootItemId** and **RootItemChangeKey** attributes removed before passing them to **GetAttachment**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6b32e-114">El identificador de los datos adjuntos y la clave de cambio se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="6b32e-114">The attachment identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="6b32e-115">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="6b32e-115">Request elements</span></span>

<span data-ttu-id="6b32e-116">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="6b32e-116">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="6b32e-117">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="6b32e-117">GetAttachment</span></span>](getattachment.md)
    
- [<span data-ttu-id="6b32e-118">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="6b32e-118">AttachmentShape</span></span>](attachmentshape.md)
    
- [<span data-ttu-id="6b32e-119">Identificadores</span><span class="sxs-lookup"><span data-stu-id="6b32e-119">AttachmentIds</span></span>](attachmentids.md)
    
- [<span data-ttu-id="6b32e-120">AttachmentId (GetAttachment y DeleteAttachment)</span><span class="sxs-lookup"><span data-stu-id="6b32e-120">AttachmentId (GetAttachment and DeleteAttachment)</span></span>](attachmentid-getattachment-and-deleteattachment.md)
    
## <a name="getattachment-response-example"></a><span data-ttu-id="6b32e-121">Ejemplo de respuesta GetAttachment</span><span class="sxs-lookup"><span data-stu-id="6b32e-121">GetAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="6b32e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b32e-122">Description</span></span>

<span data-ttu-id="6b32e-123">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud GetAttachment.</span><span class="sxs-lookup"><span data-stu-id="6b32e-123">The following example shows a successful response to a GetAttachment request.</span></span> <span data-ttu-id="6b32e-124">En este ejemplo se devuelven datos adjuntos de archivo.</span><span class="sxs-lookup"><span data-stu-id="6b32e-124">This example returns a file attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="6b32e-125">Código</span><span class="sxs-lookup"><span data-stu-id="6b32e-125">Code</span></span>

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
    <GetAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                           xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:FileAttachment>
              <t:AttachmentId Id="AAAtAEFkbWluaX..."/>
              <t:Name>SomeFile</t:Name>
              <t:Content>AQIDBAU=</t:Content>
            </t:FileAttachment>
          </m:Attachments>
        </m:GetAttachmentResponseMessage>
      </m:ResponseMessages>
    </GetAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="6b32e-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b32e-126">Comments</span></span>

<span data-ttu-id="6b32e-127">Los mensajes de respuesta para GetAttachment siempre contendrán los datos adjuntos completos; es decir, siempre se incluirán todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="6b32e-127">The response messages for GetAttachment will always contain the full attachment; that is, all properties will always be included.</span></span> <span data-ttu-id="6b32e-128">Para los datos adjuntos, esas propiedades son [Name (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [contentid](contentid.md), [ContentLocation](contentlocation.md)y [Content](content.md).</span><span class="sxs-lookup"><span data-stu-id="6b32e-128">For file attachments, those properties are [Name (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [ContentId](contentid.md), [ContentLocation](contentlocation.md), and [Content](content.md).</span></span> <span data-ttu-id="6b32e-129">Para los datos adjuntos de elementos, esas propiedades son [nombre (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [contentid](contentid.md), [ContentLocation](contentlocation.md) y todas las propiedades del elemento, como si la forma **AllProperties** se hubiera usado en una llamada GetItem.</span><span class="sxs-lookup"><span data-stu-id="6b32e-129">For item attachments, those properties are [Name (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [ContentId](contentid.md), [ContentLocation](contentlocation.md) and all of the item's properties, as if the **AllProperties** shape had been used in a GetItem call.</span></span> <span data-ttu-id="6b32e-130">El elemento [AttachmentShape](attachmentshape.md) , si está presente, permitirá que una aplicación de consumidor solicite propiedades extendidas adicionales para los datos adjuntos de elementos.</span><span class="sxs-lookup"><span data-stu-id="6b32e-130">The [AttachmentShape](attachmentshape.md) element, if present, will allow a consumer application to request additional extended properties for item attachments.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="6b32e-131">Elementos Response correcto</span><span class="sxs-lookup"><span data-stu-id="6b32e-131">Successful response elements</span></span>

<span data-ttu-id="6b32e-132">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="6b32e-132">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="6b32e-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="6b32e-133">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="6b32e-134">GetAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="6b32e-134">GetAttachmentResponse</span></span>](getattachmentresponse.md)
    
- [<span data-ttu-id="6b32e-135">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="6b32e-135">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="6b32e-136">GetAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6b32e-136">GetAttachmentResponseMessage</span></span>](getattachmentresponsemessage.md)
    
- [<span data-ttu-id="6b32e-137">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="6b32e-137">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="6b32e-138">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="6b32e-138">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="6b32e-139">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="6b32e-139">FileAttachment</span></span>](fileattachment.md)
    
- [<span data-ttu-id="6b32e-140">AttachmentId (GetAttachment y DeleteAttachment)</span><span class="sxs-lookup"><span data-stu-id="6b32e-140">AttachmentId (GetAttachment and DeleteAttachment)</span></span>](attachmentid-getattachment-and-deleteattachment.md)
    
- [<span data-ttu-id="6b32e-141">Nombre (AttachmentType)</span><span class="sxs-lookup"><span data-stu-id="6b32e-141">Name (AttachmentType)</span></span>](name-attachmenttype.md)
    
- [<span data-ttu-id="6b32e-142">Content</span><span class="sxs-lookup"><span data-stu-id="6b32e-142">Content</span></span>](content.md)
    
## <a name="see-also"></a><span data-ttu-id="6b32e-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b32e-143">See also</span></span>



[<span data-ttu-id="6b32e-144">Operación CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="6b32e-144">CreateAttachment operation</span></span>](createattachment-operation.md)
  
[<span data-ttu-id="6b32e-145">Operación DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="6b32e-145">DeleteAttachment operation</span></span>](deleteattachment-operation.md)

