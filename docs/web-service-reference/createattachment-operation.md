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
description: La operación CreateAttachment crea un elemento o un archivo de datos adjuntos y lo adjunta al elemento especificado.
ms.openlocfilehash: fed60275a007f2796c60d936def7a937e4982f29
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763913"
---
# <a name="createattachment-operation"></a><span data-ttu-id="59898-103">Operación CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="59898-103">CreateAttachment operation</span></span>

<span data-ttu-id="59898-104">La operación CreateAttachment crea un elemento o un archivo de datos adjuntos y lo adjunta al elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="59898-104">The CreateAttachment operation creates either an item or file attachment and attaches it to the specified item.</span></span>
  
## <a name="file-createattachment-request-example"></a><span data-ttu-id="59898-105">Ejemplo de solicitud de archivo CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="59898-105">File CreateAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="59898-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="59898-106">Description</span></span>

<span data-ttu-id="59898-107">El siguiente ejemplo de una solicitud de CreateAttachment muestra cómo crear un archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="59898-107">The following example of a CreateAttachment request shows how to create a file attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="59898-108">Código</span><span class="sxs-lookup"><span data-stu-id="59898-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
<soap:Body>
  <CreateAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comment"></a><span data-ttu-id="59898-109">Comment</span><span class="sxs-lookup"><span data-stu-id="59898-109">Comment</span></span>

<span data-ttu-id="59898-110">Debe proporcionar un nombre para los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="59898-110">A name for the attachment must be provided.</span></span>
  
> [!NOTE]
> <span data-ttu-id="59898-111">El identificador del elemento primario y la clave de cambio se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="59898-111">The parent item identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="59898-112">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="59898-112">Request elements</span></span>

<span data-ttu-id="59898-113">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="59898-113">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="59898-114">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="59898-114">CreateAttachment</span></span>](createattachment.md)
    
- [<span data-ttu-id="59898-115">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="59898-115">ParentItemId</span></span>](parentitemid.md)
    
- [<span data-ttu-id="59898-116">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="59898-116">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="59898-117">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="59898-117">FileAttachment</span></span>](fileattachment.md)
    
- [<span data-ttu-id="59898-118">Nombre (AttachmentType)</span><span class="sxs-lookup"><span data-stu-id="59898-118">Name (AttachmentType)</span></span>](name-attachmenttype.md)
    
- [<span data-ttu-id="59898-119">Contenido</span><span class="sxs-lookup"><span data-stu-id="59898-119">Content</span></span>](content.md)
    
## <a name="successful-file-createattachment-response-example"></a><span data-ttu-id="59898-120">Ejemplo de respuesta correcta de archivo CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="59898-120">Successful File CreateAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="59898-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="59898-121">Description</span></span>

<span data-ttu-id="59898-122">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud de CreateAttachment.</span><span class="sxs-lookup"><span data-stu-id="59898-122">The following example shows a successful response to the CreateAttachment request.</span></span>
  
### <a name="code"></a><span data-ttu-id="59898-123">Código</span><span class="sxs-lookup"><span data-stu-id="59898-123">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comment"></a><span data-ttu-id="59898-124">Comment</span><span class="sxs-lookup"><span data-stu-id="59898-124">Comment</span></span>

<span data-ttu-id="59898-125">La respuesta contiene el identificador del archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="59898-125">The response contains the identifier of the attached file.</span></span> <span data-ttu-id="59898-126">También contiene el identificador y cambiar la clave del elemento raíz.</span><span class="sxs-lookup"><span data-stu-id="59898-126">It also contains the identifier and change key of the root item.</span></span> <span data-ttu-id="59898-127">Los identificadores de elemento y cambiar la clave se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="59898-127">The item identifiers and change key have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="59898-128">Elementos de respuesta correcta</span><span class="sxs-lookup"><span data-stu-id="59898-128">Successful response elements</span></span>

<span data-ttu-id="59898-129">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="59898-129">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="59898-130">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="59898-130">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="59898-131">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="59898-131">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
    
- [<span data-ttu-id="59898-132">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="59898-132">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="59898-133">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="59898-133">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
    
- [<span data-ttu-id="59898-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="59898-134">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="59898-135">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="59898-135">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="59898-136">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="59898-136">FileAttachment</span></span>](fileattachment.md)
    
- [<span data-ttu-id="59898-137">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="59898-137">AttachmentId</span></span>](attachmentid.md)
    
## <a name="item-createattachment-request-example"></a><span data-ttu-id="59898-138">Ejemplo de solicitud de elemento CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="59898-138">Item CreateAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="59898-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="59898-139">Description</span></span>

<span data-ttu-id="59898-140">El siguiente ejemplo de una solicitud de CreateAttachment muestra cómo crear un elemento de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="59898-140">The following example of a CreateAttachment request shows how to create an item attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="59898-141">Código</span><span class="sxs-lookup"><span data-stu-id="59898-141">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comment"></a><span data-ttu-id="59898-142">Comment</span><span class="sxs-lookup"><span data-stu-id="59898-142">Comment</span></span>

<span data-ttu-id="59898-143">Debe proporcionar un nombre para los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="59898-143">A name for the attachment must be provided.</span></span>
  
 <span data-ttu-id="59898-144">**Nota** El identificador del elemento primario y la clave de cambio se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="59898-144">**Note** The parent item identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="59898-145">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="59898-145">Request elements</span></span>

<span data-ttu-id="59898-146">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="59898-146">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="59898-147">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="59898-147">CreateAttachment</span></span>](createattachment.md)
    
- [<span data-ttu-id="59898-148">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="59898-148">ParentItemId</span></span>](parentitemid.md)
    
- [<span data-ttu-id="59898-149">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="59898-149">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="59898-150">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="59898-150">ItemAttachment</span></span>](itemattachment.md)
    
- [<span data-ttu-id="59898-151">Nombre (AttachmentType)</span><span class="sxs-lookup"><span data-stu-id="59898-151">Name (AttachmentType)</span></span>](name-attachmenttype.md)
    
- [<span data-ttu-id="59898-152">Message</span><span class="sxs-lookup"><span data-stu-id="59898-152">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="59898-153">Subject</span><span class="sxs-lookup"><span data-stu-id="59898-153">Subject</span></span>](subject.md)
    
## <a name="successful-item-createattachment-response-example"></a><span data-ttu-id="59898-154">Ejemplo de respuesta correcta de elemento CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="59898-154">Successful Item CreateAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="59898-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="59898-155">Description</span></span>

<span data-ttu-id="59898-156">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud de CreateAttachment.</span><span class="sxs-lookup"><span data-stu-id="59898-156">The following example shows a successful response to the CreateAttachment request.</span></span>
  
### <a name="code"></a><span data-ttu-id="59898-157">Código</span><span class="sxs-lookup"><span data-stu-id="59898-157">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comment"></a><span data-ttu-id="59898-158">Comment</span><span class="sxs-lookup"><span data-stu-id="59898-158">Comment</span></span>

<span data-ttu-id="59898-159">La respuesta contiene el identificador de los nuevos datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="59898-159">The response contains the identifier of the new attachment.</span></span> <span data-ttu-id="59898-160">También contiene el identificador y cambiar la clave del elemento raíz.</span><span class="sxs-lookup"><span data-stu-id="59898-160">It also contains the identifier and change key of the root item.</span></span> <span data-ttu-id="59898-161">El elemento raíz es el elemento que contiene los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="59898-161">The root item is the item that contains the attachment.</span></span> <span data-ttu-id="59898-162">Los identificadores de elemento y cambiar la clave se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="59898-162">The item identifiers and change key have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="59898-163">Elementos de respuesta correcta</span><span class="sxs-lookup"><span data-stu-id="59898-163">Successful response elements</span></span>

<span data-ttu-id="59898-164">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="59898-164">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="59898-165">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="59898-165">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="59898-166">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="59898-166">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
    
- [<span data-ttu-id="59898-167">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="59898-167">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="59898-168">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="59898-168">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
    
- [<span data-ttu-id="59898-169">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="59898-169">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="59898-170">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="59898-170">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="59898-171">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="59898-171">ItemAttachment</span></span>](itemattachment.md)
    
- [<span data-ttu-id="59898-172">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="59898-172">AttachmentId</span></span>](attachmentid.md)
    
## <a name="createattachment-error-response-example"></a><span data-ttu-id="59898-173">Ejemplo de respuesta de CreateAttachment Error</span><span class="sxs-lookup"><span data-stu-id="59898-173">CreateAttachment Error response example</span></span>

### <a name="description"></a><span data-ttu-id="59898-174">Descripción</span><span class="sxs-lookup"><span data-stu-id="59898-174">Description</span></span>

<span data-ttu-id="59898-175">En el ejemplo siguiente se muestra una respuesta de error a la solicitud de CreateAttachment.</span><span class="sxs-lookup"><span data-stu-id="59898-175">The following example shows an error response to the CreateAttachment request.</span></span> <span data-ttu-id="59898-176">El error es debido a que no se especificó el nombre de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="59898-176">The error is due to the fact that the name of the attachment was not specified.</span></span>
  
### <a name="code"></a><span data-ttu-id="59898-177">Código</span><span class="sxs-lookup"><span data-stu-id="59898-177">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="59898-178">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="59898-178">Error response elements</span></span>

<span data-ttu-id="59898-179">En la respuesta de error, se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="59898-179">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="59898-180">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="59898-180">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="59898-181">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="59898-181">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
    
- [<span data-ttu-id="59898-182">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="59898-182">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="59898-183">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="59898-183">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
    
- [<span data-ttu-id="59898-184">MessageText</span><span class="sxs-lookup"><span data-stu-id="59898-184">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="59898-185">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="59898-185">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="59898-186">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="59898-186">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="59898-187">MessageXml</span><span class="sxs-lookup"><span data-stu-id="59898-187">MessageXml</span></span>](messagexml.md)
    
- [<span data-ttu-id="59898-188">ExceptionFieldURI</span><span class="sxs-lookup"><span data-stu-id="59898-188">ExceptionFieldURI</span></span>](exceptionfielduri.md)
    
- [<span data-ttu-id="59898-189">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="59898-189">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
## <a name="remarks"></a><span data-ttu-id="59898-190">Notas</span><span class="sxs-lookup"><span data-stu-id="59898-190">Remarks</span></span>

<span data-ttu-id="59898-191">Si varios datos adjuntos se adjuntan a un elemento en un solo viaje de ida, el RootItemChangeKey en el último mensaje de respuesta es la única que representa la nueva clave de cambio del elemento que tiene los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="59898-191">If multiple attachments are attached to an item in a single round trip, the RootItemChangeKey in the last response message is the one that represents the new change key of the item that has the attachments.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="59898-192">Ver también</span><span class="sxs-lookup"><span data-stu-id="59898-192">See also</span></span>



[<span data-ttu-id="59898-193">Operación DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="59898-193">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
  
[<span data-ttu-id="59898-194">Operación GetAttachment</span><span class="sxs-lookup"><span data-stu-id="59898-194">GetAttachment operation</span></span>](getattachment-operation.md)

