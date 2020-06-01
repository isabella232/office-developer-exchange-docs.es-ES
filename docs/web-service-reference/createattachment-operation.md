---
title: Operación CreateAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateAttachment
api_type:
- schema
ms.assetid: e066db95-6963-4507-a8d0-8efad287f550
description: La operación CreateAttachment crea un elemento o datos adjuntos de archivo y lo adjunta al elemento especificado.
ms.openlocfilehash: 8028c56aa306774b54b39e5ee1ac0382b9113fa0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456573"
---
# <a name="createattachment-operation"></a><span data-ttu-id="136ef-103">Operación CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="136ef-103">CreateAttachment operation</span></span>

<span data-ttu-id="136ef-104">La operación CreateAttachment crea un elemento o datos adjuntos de archivo y lo adjunta al elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="136ef-104">The CreateAttachment operation creates either an item or file attachment and attaches it to the specified item.</span></span>
  
## <a name="file-createattachment-request-example"></a><span data-ttu-id="136ef-105">Ejemplo de solicitud de CreateAttachment de archivo</span><span class="sxs-lookup"><span data-stu-id="136ef-105">File CreateAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="136ef-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="136ef-106">Description</span></span>

<span data-ttu-id="136ef-107">El siguiente ejemplo de una solicitud CreateAttachment muestra cómo crear un archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="136ef-107">The following example of a CreateAttachment request shows how to create a file attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="136ef-108">Código</span><span class="sxs-lookup"><span data-stu-id="136ef-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
<soap:Body>
  <CreateAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
    <ParentItemId Id="AAAtAE..." ChangeKey="CQAAABYA..."/>
    <Attachments>
      <t:FileAttachment>
        <t:Name>SomeFile</t:Name>
        <t:Content>AQIDBAU=</t:Content>
      </t:FileAttachment>
    </Attachments>
  </CreateAttachment>
</soap:Body>
</soap:Envelope>
```

### <a name="comment"></a><span data-ttu-id="136ef-109">Comentario</span><span class="sxs-lookup"><span data-stu-id="136ef-109">Comment</span></span>

<span data-ttu-id="136ef-110">Se debe proporcionar un nombre para los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="136ef-110">A name for the attachment must be provided.</span></span>
  
> [!NOTE]
> <span data-ttu-id="136ef-111">El identificador de elemento primario y la clave de cambio se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="136ef-111">The parent item identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="136ef-112">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="136ef-112">Request elements</span></span>

<span data-ttu-id="136ef-113">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="136ef-113">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="136ef-114">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="136ef-114">CreateAttachment</span></span>](createattachment.md)
    
- [<span data-ttu-id="136ef-115">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="136ef-115">ParentItemId</span></span>](parentitemid.md)
    
- [<span data-ttu-id="136ef-116">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="136ef-116">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="136ef-117">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="136ef-117">FileAttachment</span></span>](fileattachment.md)
    
- [<span data-ttu-id="136ef-118">Nombre (AttachmentType)</span><span class="sxs-lookup"><span data-stu-id="136ef-118">Name (AttachmentType)</span></span>](name-attachmenttype.md)
    
- [<span data-ttu-id="136ef-119">Content</span><span class="sxs-lookup"><span data-stu-id="136ef-119">Content</span></span>](content.md)
    
## <a name="successful-file-createattachment-response-example"></a><span data-ttu-id="136ef-120">Ejemplo de archivo con éxito CreateAttachment Response</span><span class="sxs-lookup"><span data-stu-id="136ef-120">Successful File CreateAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="136ef-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="136ef-121">Description</span></span>

<span data-ttu-id="136ef-122">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud CreateAttachment.</span><span class="sxs-lookup"><span data-stu-id="136ef-122">The following example shows a successful response to the CreateAttachment request.</span></span>
  
### <a name="code"></a><span data-ttu-id="136ef-123">Código</span><span class="sxs-lookup"><span data-stu-id="136ef-123">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:FileAttachment>
              <t:AttachmentId Id="AAAtAE=" RootItemId="AAAtAEFk=" RootItemChangeKey="CQAAAB"/>
            </t:FileAttachment>
          </m:Attachments>
        </m:CreateAttachmentResponseMessage>
      </m:ResponseMessages>
    </CreateAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a><span data-ttu-id="136ef-124">Comentario</span><span class="sxs-lookup"><span data-stu-id="136ef-124">Comment</span></span>

<span data-ttu-id="136ef-125">La respuesta contiene el identificador del archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="136ef-125">The response contains the identifier of the attached file.</span></span> <span data-ttu-id="136ef-126">También contiene el identificador y la clave de cambio del elemento raíz.</span><span class="sxs-lookup"><span data-stu-id="136ef-126">It also contains the identifier and change key of the root item.</span></span> <span data-ttu-id="136ef-127">Los identificadores de elemento y la clave de cambio se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="136ef-127">The item identifiers and change key have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="136ef-128">Elementos Response correcto</span><span class="sxs-lookup"><span data-stu-id="136ef-128">Successful response elements</span></span>

<span data-ttu-id="136ef-129">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="136ef-129">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="136ef-130">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="136ef-130">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="136ef-131">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="136ef-131">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
    
- [<span data-ttu-id="136ef-132">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="136ef-132">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="136ef-133">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="136ef-133">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
    
- [<span data-ttu-id="136ef-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="136ef-134">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="136ef-135">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="136ef-135">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="136ef-136">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="136ef-136">FileAttachment</span></span>](fileattachment.md)
    
- [<span data-ttu-id="136ef-137">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="136ef-137">AttachmentId</span></span>](attachmentid.md)
    
## <a name="item-createattachment-request-example"></a><span data-ttu-id="136ef-138">Ejemplo de solicitud de CreateAttachment de elemento</span><span class="sxs-lookup"><span data-stu-id="136ef-138">Item CreateAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="136ef-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="136ef-139">Description</span></span>

<span data-ttu-id="136ef-140">El siguiente ejemplo de una solicitud CreateAttachment muestra cómo crear un elemento adjunto.</span><span class="sxs-lookup"><span data-stu-id="136ef-140">The following example of a CreateAttachment request shows how to create an item attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="136ef-141">Código</span><span class="sxs-lookup"><span data-stu-id="136ef-141">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <ParentItemId Id="AAAtAE=" ChangeKey="CQAAABYA"/>
      <Attachments>
        <t:ItemAttachment>
          <t:Name>An item attachment</t:Name>
          <t:Message>
            <t:Subject>A message to attach</t:Subject>
          </t:Message>
        </t:ItemAttachment>
      </Attachments>
    </CreateAttachment>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a><span data-ttu-id="136ef-142">Comentario</span><span class="sxs-lookup"><span data-stu-id="136ef-142">Comment</span></span>

<span data-ttu-id="136ef-143">Se debe proporcionar un nombre para los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="136ef-143">A name for the attachment must be provided.</span></span>
  
 <span data-ttu-id="136ef-144">**Nota:** El identificador de elemento primario y la clave de cambio se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="136ef-144">**Note** The parent item identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="136ef-145">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="136ef-145">Request elements</span></span>

<span data-ttu-id="136ef-146">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="136ef-146">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="136ef-147">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="136ef-147">CreateAttachment</span></span>](createattachment.md)
    
- [<span data-ttu-id="136ef-148">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="136ef-148">ParentItemId</span></span>](parentitemid.md)
    
- [<span data-ttu-id="136ef-149">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="136ef-149">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="136ef-150">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="136ef-150">ItemAttachment</span></span>](itemattachment.md)
    
- [<span data-ttu-id="136ef-151">Nombre (AttachmentType)</span><span class="sxs-lookup"><span data-stu-id="136ef-151">Name (AttachmentType)</span></span>](name-attachmenttype.md)
    
- [<span data-ttu-id="136ef-152">Mensaje</span><span class="sxs-lookup"><span data-stu-id="136ef-152">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="136ef-153">Asunto</span><span class="sxs-lookup"><span data-stu-id="136ef-153">Subject</span></span>](subject.md)
    
## <a name="successful-item-createattachment-response-example"></a><span data-ttu-id="136ef-154">Ejemplo de respuesta de CreateAttachment de elemento correcta</span><span class="sxs-lookup"><span data-stu-id="136ef-154">Successful Item CreateAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="136ef-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="136ef-155">Description</span></span>

<span data-ttu-id="136ef-156">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud CreateAttachment.</span><span class="sxs-lookup"><span data-stu-id="136ef-156">The following example shows a successful response to the CreateAttachment request.</span></span>
  
### <a name="code"></a><span data-ttu-id="136ef-157">Código</span><span class="sxs-lookup"><span data-stu-id="136ef-157">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:ItemAttachment>
              <t:AttachmentId Id="AAAtAEFk=" RootItemId="AAAtAEFkb=" RootItemChangeKey="CQAAABYA"/>
            </t:ItemAttachment>
          </m:Attachments>
        </m:CreateAttachmentResponseMessage>
      </m:ResponseMessages>
    </CreateAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a><span data-ttu-id="136ef-158">Comentario</span><span class="sxs-lookup"><span data-stu-id="136ef-158">Comment</span></span>

<span data-ttu-id="136ef-159">La respuesta contiene el identificador de los datos adjuntos nuevos.</span><span class="sxs-lookup"><span data-stu-id="136ef-159">The response contains the identifier of the new attachment.</span></span> <span data-ttu-id="136ef-160">También contiene el identificador y la clave de cambio del elemento raíz.</span><span class="sxs-lookup"><span data-stu-id="136ef-160">It also contains the identifier and change key of the root item.</span></span> <span data-ttu-id="136ef-161">El elemento raíz es el elemento que contiene los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="136ef-161">The root item is the item that contains the attachment.</span></span> <span data-ttu-id="136ef-162">Los identificadores de elemento y la clave de cambio se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="136ef-162">The item identifiers and change key have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="136ef-163">Elementos Response correcto</span><span class="sxs-lookup"><span data-stu-id="136ef-163">Successful response elements</span></span>

<span data-ttu-id="136ef-164">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="136ef-164">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="136ef-165">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="136ef-165">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="136ef-166">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="136ef-166">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
    
- [<span data-ttu-id="136ef-167">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="136ef-167">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="136ef-168">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="136ef-168">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
    
- [<span data-ttu-id="136ef-169">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="136ef-169">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="136ef-170">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="136ef-170">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="136ef-171">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="136ef-171">ItemAttachment</span></span>](itemattachment.md)
    
- [<span data-ttu-id="136ef-172">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="136ef-172">AttachmentId</span></span>](attachmentid.md)
    
## <a name="createattachment-error-response-example"></a><span data-ttu-id="136ef-173">Ejemplo de respuesta de error CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="136ef-173">CreateAttachment Error response example</span></span>

### <a name="description"></a><span data-ttu-id="136ef-174">Descripción</span><span class="sxs-lookup"><span data-stu-id="136ef-174">Description</span></span>

<span data-ttu-id="136ef-175">En el ejemplo siguiente se muestra una respuesta de error a la solicitud CreateAttachment.</span><span class="sxs-lookup"><span data-stu-id="136ef-175">The following example shows an error response to the CreateAttachment request.</span></span> <span data-ttu-id="136ef-176">El error se debe a que no se ha especificado el nombre de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="136ef-176">The error is due to the fact that the name of the attachment was not specified.</span></span>
  
### <a name="code"></a><span data-ttu-id="136ef-177">Código</span><span class="sxs-lookup"><span data-stu-id="136ef-177">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateAttachmentResponseMessage ResponseClass="Error">
          <m:MessageText>Required property is missing.</m:MessageText>
          <m:ResponseCode>ErrorRequiredPropertyMissing</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:MessageXml>
            <t:ExceptionFieldURI FieldURI="attachment:Name"/>
          </m:MessageXml>
          <m:Attachments/>
        </m:CreateAttachmentResponseMessage>
      </m:ResponseMessages>
    </CreateAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="136ef-178">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="136ef-178">Error response elements</span></span>

<span data-ttu-id="136ef-179">Los siguientes elementos se usan en la respuesta de error:</span><span class="sxs-lookup"><span data-stu-id="136ef-179">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="136ef-180">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="136ef-180">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="136ef-181">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="136ef-181">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
    
- [<span data-ttu-id="136ef-182">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="136ef-182">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="136ef-183">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="136ef-183">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
    
- [<span data-ttu-id="136ef-184">MessageText</span><span class="sxs-lookup"><span data-stu-id="136ef-184">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="136ef-185">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="136ef-185">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="136ef-186">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="136ef-186">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="136ef-187">MessageXml</span><span class="sxs-lookup"><span data-stu-id="136ef-187">MessageXml</span></span>](messagexml.md)
    
- [<span data-ttu-id="136ef-188">ExceptionFieldURI</span><span class="sxs-lookup"><span data-stu-id="136ef-188">ExceptionFieldURI</span></span>](exceptionfielduri.md)
    
- [<span data-ttu-id="136ef-189">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="136ef-189">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
## <a name="remarks"></a><span data-ttu-id="136ef-190">Comentarios</span><span class="sxs-lookup"><span data-stu-id="136ef-190">Remarks</span></span>

<span data-ttu-id="136ef-191">Si se adjuntan varios datos adjuntos a un elemento en una sola acción de ida y vuelta, el RootItemChangeKey del último mensaje de respuesta es el que representa la nueva clave de cambio del elemento que tiene los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="136ef-191">If multiple attachments are attached to an item in a single round trip, the RootItemChangeKey in the last response message is the one that represents the new change key of the item that has the attachments.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="136ef-192">Vea también</span><span class="sxs-lookup"><span data-stu-id="136ef-192">See also</span></span>



[<span data-ttu-id="136ef-193">Operación DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="136ef-193">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
  
[<span data-ttu-id="136ef-194">Operación GetAttachment</span><span class="sxs-lookup"><span data-stu-id="136ef-194">GetAttachment operation</span></span>](getattachment-operation.md)

