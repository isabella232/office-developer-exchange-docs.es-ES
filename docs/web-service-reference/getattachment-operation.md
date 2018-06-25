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
description: La operación GetAttachment se usa para recuperar los datos adjuntos de existentes en los elementos en el almacén de Exchange.
ms.openlocfilehash: c260033208bf49c60463c09041d8ffcc52a8f5c2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764759"
---
# <a name="getattachment-operation"></a><span data-ttu-id="2367b-103">Operación GetAttachment</span><span class="sxs-lookup"><span data-stu-id="2367b-103">GetAttachment operation</span></span>

<span data-ttu-id="2367b-104">La operación GetAttachment se usa para recuperar los datos adjuntos de existentes en los elementos en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2367b-104">The GetAttachment operation is used to retrieve existing attachments on items in the Exchange store.</span></span>
  
## <a name="getattachment-request-example"></a><span data-ttu-id="2367b-105">Ejemplo de solicitud de GetAttachment</span><span class="sxs-lookup"><span data-stu-id="2367b-105">GetAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="2367b-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="2367b-106">Description</span></span>

<span data-ttu-id="2367b-107">El siguiente ejemplo de solicitud de GetAttachment muestra cómo obtener datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="2367b-107">The following example of GetAttachment request shows how to get an attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="2367b-108">Código</span><span class="sxs-lookup"><span data-stu-id="2367b-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape/>
      <AttachmentIds>
        <t:AttachmentId Id="AAAtAEFkbWluaX..."/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="2367b-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2367b-109">Comments</span></span>

<span data-ttu-id="2367b-110">El elemento [AttachmentShape](attachmentshape.md) permite especificar qué información de datos adjuntos que se debe devolver.</span><span class="sxs-lookup"><span data-stu-id="2367b-110">The [AttachmentShape](attachmentshape.md) element allows you to specify which attachment information should be returned.</span></span> <span data-ttu-id="2367b-111">Un elemento [AttachmentShape](attachmentshape.md) vacío es válido y representará los datos adjuntos sin contenido MIME para los datos adjuntos de elemento, con un tipo de cuerpo de texto y sin las propiedades adicionales.</span><span class="sxs-lookup"><span data-stu-id="2367b-111">An empty [AttachmentShape](attachmentshape.md) element is valid and will render your attachments without MIME content for item attachments, with a text body type, and without any additional properties.</span></span> 
  
<span data-ttu-id="2367b-112">La colección de [AttachmentIds](attachmentids.md) permite especificar uno o varios identificadores de datos adjuntos para devolver.</span><span class="sxs-lookup"><span data-stu-id="2367b-112">The [AttachmentIds](attachmentids.md) collection allows you to specify one or more attachment identifiers to return.</span></span> <span data-ttu-id="2367b-113">Tenga en cuenta que estos son de tipo RequestAttachmentIdType, por lo que cualquier AttachmentIds que reciba de **CreateAttachment** debe tener los atributos **RootItemId** y **RootItemChangeKey** se quita antes de pasarlas a **GetAttachment**.</span><span class="sxs-lookup"><span data-stu-id="2367b-113">Note that these are of type RequestAttachmentIdType, so any AttachmentIds that you receive from **CreateAttachment** must have the **RootItemId** and **RootItemChangeKey** attributes removed before passing them to **GetAttachment**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2367b-114">El identificador de datos adjuntos y la clave de cambio se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="2367b-114">The attachment identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="2367b-115">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="2367b-115">Request elements</span></span>

<span data-ttu-id="2367b-116">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="2367b-116">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="2367b-117">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="2367b-117">GetAttachment</span></span>](getattachment.md)
    
- [<span data-ttu-id="2367b-118">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="2367b-118">AttachmentShape</span></span>](attachmentshape.md)
    
- [<span data-ttu-id="2367b-119">AttachmentIds</span><span class="sxs-lookup"><span data-stu-id="2367b-119">AttachmentIds</span></span>](attachmentids.md)
    
- [<span data-ttu-id="2367b-120">AttachmentId (GetAttachment y DeleteAttachment)</span><span class="sxs-lookup"><span data-stu-id="2367b-120">AttachmentId (GetAttachment and DeleteAttachment)</span></span>](attachmentid-getattachment-and-deleteattachment.md)
    
## <a name="getattachment-response-example"></a><span data-ttu-id="2367b-121">Ejemplo de respuesta de GetAttachment</span><span class="sxs-lookup"><span data-stu-id="2367b-121">GetAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="2367b-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="2367b-122">Description</span></span>

<span data-ttu-id="2367b-123">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de GetAttachment.</span><span class="sxs-lookup"><span data-stu-id="2367b-123">The following example shows a successful response to a GetAttachment request.</span></span> <span data-ttu-id="2367b-124">En este ejemplo se devuelve un archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="2367b-124">This example returns a file attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="2367b-125">Código</span><span class="sxs-lookup"><span data-stu-id="2367b-125">Code</span></span>

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
    <GetAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                           xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="2367b-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2367b-126">Comments</span></span>

<span data-ttu-id="2367b-127">Los mensajes de respuesta para GetAttachment siempre va a contener los datos adjuntos completo; es decir, todas las propiedades siempre se incluirán.</span><span class="sxs-lookup"><span data-stu-id="2367b-127">The response messages for GetAttachment will always contain the full attachment; that is, all properties will always be included.</span></span> <span data-ttu-id="2367b-128">Los archivos adjuntos, esas propiedades son [nombre (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [ContentId](contentid.md), [ContentLocation](contentlocation.md)y [contenido](content.md).</span><span class="sxs-lookup"><span data-stu-id="2367b-128">For file attachments, those properties are [Name (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [ContentId](contentid.md), [ContentLocation](contentlocation.md), and [Content](content.md).</span></span> <span data-ttu-id="2367b-129">Los datos adjuntos de elemento, esas propiedades son [nombre (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [ContentId](contentid.md), [ContentLocation](contentlocation.md) y todas las propiedades del elemento, tal y como si se hubiera utilizado la forma de **AllProperties** en una llamada GetItem.</span><span class="sxs-lookup"><span data-stu-id="2367b-129">For item attachments, those properties are [Name (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [ContentId](contentid.md), [ContentLocation](contentlocation.md) and all of the item's properties, as if the **AllProperties** shape had been used in a GetItem call.</span></span> <span data-ttu-id="2367b-130">El elemento [AttachmentShape](attachmentshape.md) , si está presente, le permitirá que una aplicación de consumidor solicitar propiedades extendidas adicionales para los datos adjuntos del elemento.</span><span class="sxs-lookup"><span data-stu-id="2367b-130">The [AttachmentShape](attachmentshape.md) element, if present, will allow a consumer application to request additional extended properties for item attachments.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="2367b-131">Elementos de respuesta correcta</span><span class="sxs-lookup"><span data-stu-id="2367b-131">Successful response elements</span></span>

<span data-ttu-id="2367b-132">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="2367b-132">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="2367b-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2367b-133">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="2367b-134">GetAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="2367b-134">GetAttachmentResponse</span></span>](getattachmentresponse.md)
    
- [<span data-ttu-id="2367b-135">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2367b-135">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="2367b-136">GetAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2367b-136">GetAttachmentResponseMessage</span></span>](getattachmentresponsemessage.md)
    
- [<span data-ttu-id="2367b-137">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2367b-137">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="2367b-138">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="2367b-138">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="2367b-139">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="2367b-139">FileAttachment</span></span>](fileattachment.md)
    
- [<span data-ttu-id="2367b-140">AttachmentId (GetAttachment y DeleteAttachment)</span><span class="sxs-lookup"><span data-stu-id="2367b-140">AttachmentId (GetAttachment and DeleteAttachment)</span></span>](attachmentid-getattachment-and-deleteattachment.md)
    
- [<span data-ttu-id="2367b-141">Nombre (AttachmentType)</span><span class="sxs-lookup"><span data-stu-id="2367b-141">Name (AttachmentType)</span></span>](name-attachmenttype.md)
    
- [<span data-ttu-id="2367b-142">Contenido</span><span class="sxs-lookup"><span data-stu-id="2367b-142">Content</span></span>](content.md)
    
## <a name="see-also"></a><span data-ttu-id="2367b-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="2367b-143">See also</span></span>



[<span data-ttu-id="2367b-144">Operación CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="2367b-144">CreateAttachment operation</span></span>](createattachment-operation.md)
  
[<span data-ttu-id="2367b-145">Operación DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="2367b-145">DeleteAttachment operation</span></span>](deleteattachment-operation.md)

