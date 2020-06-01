---
title: Operación DeleteAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteAttachment
api_type:
- schema
ms.assetid: 4d48e595-b98c-48e7-bbeb-cacf91d12a78
description: La operación DeleteAttachment se usa para eliminar archivos y datos adjuntos de un elemento existente en el almacén de Exchange.
ms.openlocfilehash: 1d34ce4c5ba1d955989a35dafb8ab3c5d229d505
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457336"
---
# <a name="deleteattachment-operation"></a><span data-ttu-id="aafc4-103">Operación DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="aafc4-103">DeleteAttachment operation</span></span>

<span data-ttu-id="aafc4-104">La operación DeleteAttachment se usa para eliminar archivos y datos adjuntos de un elemento existente en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="aafc4-104">The DeleteAttachment operation is used to delete file and item attachments from an existing item in the Exchange store.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aafc4-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aafc4-105">Remarks</span></span>

<span data-ttu-id="aafc4-106">Esta operación permite eliminar uno o más datos adjuntos por identificador.</span><span class="sxs-lookup"><span data-stu-id="aafc4-106">This operation allows you to delete one or more attachments by ID.</span></span>
  
## <a name="deleteattachment-request-example"></a><span data-ttu-id="aafc4-107">Ejemplo de solicitud DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="aafc4-107">DeleteAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="aafc4-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="aafc4-108">Description</span></span>

<span data-ttu-id="aafc4-109">El siguiente ejemplo de una solicitud DeleteAttachment muestra cómo eliminar un elemento adjunto.</span><span class="sxs-lookup"><span data-stu-id="aafc4-109">The following example of a DeleteAttachment request shows how to delete an item attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="aafc4-110">Código</span><span class="sxs-lookup"><span data-stu-id="aafc4-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <DeleteAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentIds>
        <t:AttachmentId Id="AAAtAEFkbWluaX"/>
      </AttachmentIds>
    </DeleteAttachment>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="aafc4-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aafc4-111">Comments</span></span>

<span data-ttu-id="aafc4-112">El identificador de datos adjuntos se ha abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="aafc4-112">The attachment identifier has been shortened to preserve readability.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="aafc4-113">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="aafc4-113">Request elements</span></span>

<span data-ttu-id="aafc4-114">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="aafc4-114">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="aafc4-115">DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="aafc4-115">DeleteAttachment</span></span>](deleteattachment.md)
    
- [<span data-ttu-id="aafc4-116">Identificadores</span><span class="sxs-lookup"><span data-stu-id="aafc4-116">AttachmentIds</span></span>](attachmentids.md)
    
- [<span data-ttu-id="aafc4-117">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="aafc4-117">AttachmentId</span></span>](attachmentid.md)
    
## <a name="deleteattachment-response-example"></a><span data-ttu-id="aafc4-118">Ejemplo de respuesta DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="aafc4-118">DeleteAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="aafc4-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="aafc4-119">Description</span></span>

<span data-ttu-id="aafc4-120">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud DeleteAttachment.</span><span class="sxs-lookup"><span data-stu-id="aafc4-120">The following example shows a successful response to a DeleteAttachment request.</span></span>
  
### <a name="code"></a><span data-ttu-id="aafc4-121">Código</span><span class="sxs-lookup"><span data-stu-id="aafc4-121">Code</span></span>

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
    <DeleteAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteAttachmentResponseMessage xsi:type="m:DeleteAttachmentResponseMessageType" ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="AAAtAEFkbWluaXN..." RootItemChangeKey="CQAAABYAA..."/>
        </m:DeleteAttachmentResponseMessage>
      </m:ResponseMessages>
    </DeleteAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="aafc4-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aafc4-122">Comments</span></span>

<span data-ttu-id="aafc4-123">La operación CreateAttachment devuelve un elemento de tipo AttachmentIdType que incluye un **RootItemId** y **RootItemChangeKey**.</span><span class="sxs-lookup"><span data-stu-id="aafc4-123">The CreateAttachment operation returns an element of AttachmentIdType type that includes a **RootItemId** and **RootItemChangeKey**.</span></span> <span data-ttu-id="aafc4-124">Estos atributos no se permiten para los identificadores dentro de una solicitud DeleteAttachment.</span><span class="sxs-lookup"><span data-stu-id="aafc4-124">These attributes are not permitted for identifiers within a DeleteAttachment request.</span></span> <span data-ttu-id="aafc4-125">DeleteAttachment usa elementos de tipo RequestAttachmentIdType, que no incluyen estos atributos.</span><span class="sxs-lookup"><span data-stu-id="aafc4-125">DeleteAttachment uses elements of type RequestAttachmentIdType, which does not include these attributes.</span></span>
  
<span data-ttu-id="aafc4-126">La respuesta DeleteAttachment incluye el identificador del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="aafc4-126">The DeleteAttachment response includes the ID of the parent item.</span></span> <span data-ttu-id="aafc4-127">Cuando se quitan datos adjuntos de un elemento, se modifica la clave de cambio del elemento.</span><span class="sxs-lookup"><span data-stu-id="aafc4-127">When attachments are removed from an item, the item's change key is modified.</span></span> <span data-ttu-id="aafc4-128">La nueva clave de cambio de elemento se puede obtener de la respuesta DeleteAttachment.</span><span class="sxs-lookup"><span data-stu-id="aafc4-128">The new item change key can be obtained from the DeleteAttachment response.</span></span>
  
> [!NOTE]
> <span data-ttu-id="aafc4-129">El identificador [RootItemId](rootitemid.md) y changekey se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="aafc4-129">The [RootItemId](rootitemid.md) identifier and ChangeKey have been shortened to preserve readability.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="aafc4-130">Elementos Response correcto</span><span class="sxs-lookup"><span data-stu-id="aafc4-130">Successful response elements</span></span>

<span data-ttu-id="aafc4-131">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="aafc4-131">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="aafc4-132">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="aafc4-132">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="aafc4-133">DeleteAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="aafc4-133">DeleteAttachmentResponse</span></span>](deleteattachmentresponse.md)
    
- [<span data-ttu-id="aafc4-134">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="aafc4-134">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="aafc4-135">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="aafc4-135">DeleteAttachmentResponseMessage</span></span>](deleteattachmentresponsemessage.md)
    
- [<span data-ttu-id="aafc4-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="aafc4-136">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="aafc4-137">RootItemId</span><span class="sxs-lookup"><span data-stu-id="aafc4-137">RootItemId</span></span>](rootitemid.md)
    
## <a name="see-also"></a><span data-ttu-id="aafc4-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="aafc4-138">See also</span></span>

- [<span data-ttu-id="aafc4-139">Operación CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="aafc4-139">CreateAttachment operation</span></span>](createattachment-operation.md) 
- [<span data-ttu-id="aafc4-140">Operación GetAttachment</span><span class="sxs-lookup"><span data-stu-id="aafc4-140">GetAttachment operation</span></span>](getattachment-operation.md)

