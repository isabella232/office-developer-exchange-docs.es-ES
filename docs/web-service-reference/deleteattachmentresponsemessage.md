---
title: DeleteAttachmentResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteAttachmentResponseMessage
api_type:
- schema
ms.assetid: 1edb085f-1674-48e5-8ec3-42351adeac7d
description: El elemento DeleteAttachmentResponseMessage contiene el estado y el resultado de una única solicitud de operación DeleteAttachment.
ms.openlocfilehash: 3ff253a5c2b6cbd69b7b976f7f41ca8b83814a74
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464262"
---
# <a name="deleteattachmentresponsemessage"></a><span data-ttu-id="838d0-103">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="838d0-103">DeleteAttachmentResponseMessage</span></span>

<span data-ttu-id="838d0-104">El elemento **DeleteAttachmentResponseMessage** contiene el estado y el resultado de una única solicitud de [operación DeleteAttachment](deleteattachment-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="838d0-104">The **DeleteAttachmentResponseMessage** element contains the status and result of a single [DeleteAttachment operation](deleteattachment-operation.md) request.</span></span> 
  
- [<span data-ttu-id="838d0-105">DeleteAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="838d0-105">DeleteAttachmentResponse</span></span>](deleteattachmentresponse.md)  
- [<span data-ttu-id="838d0-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="838d0-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="838d0-107">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="838d0-107">DeleteAttachmentResponseMessage</span></span>](deleteattachmentresponsemessage.md)
  
```xml
<DeleteAttachmentResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RootItemId/>
</DeleteAttachmentResponseMessage>
```

<span data-ttu-id="838d0-108">**DeleteAttachmentResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="838d0-108">**DeleteAttachmentResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="838d0-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="838d0-109">Attributes and elements</span></span>

<span data-ttu-id="838d0-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="838d0-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="838d0-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="838d0-111">Attributes</span></span>

|<span data-ttu-id="838d0-112">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="838d0-112">**Attribute**</span></span>|<span data-ttu-id="838d0-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="838d0-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="838d0-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="838d0-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="838d0-115">Describe el estado de una respuesta de [operación de DeleteAttachment](deleteattachment-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="838d0-115">Describes the status of a [DeleteAttachment operation](deleteattachment-operation.md) response.</span></span><br/><br/><span data-ttu-id="838d0-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="838d0-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="838d0-117">-Correcto</span><span class="sxs-lookup"><span data-stu-id="838d0-117">-  Success</span></span>  <br/><span data-ttu-id="838d0-118">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="838d0-118">-  Warning</span></span>  <br/><span data-ttu-id="838d0-119">-Error</span><span class="sxs-lookup"><span data-stu-id="838d0-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="838d0-120">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="838d0-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="838d0-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="838d0-121">**Value**</span></span>|<span data-ttu-id="838d0-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="838d0-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="838d0-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="838d0-123">**Success**</span></span> <br/> |<span data-ttu-id="838d0-124">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="838d0-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="838d0-125">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="838d0-125">**Warning**</span></span> <br/> | <span data-ttu-id="838d0-126">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="838d0-126">Describes a request that was not processed.</span></span> <span data-ttu-id="838d0-127">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="838d0-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="838d0-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="838d0-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="838d0-129">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="838d0-129">- The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="838d0-130">-Los servicios de dominio de Active Directory (AD DS) están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="838d0-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="838d0-131">-Se mueven los buzones.</span><span class="sxs-lookup"><span data-stu-id="838d0-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="838d0-132">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="838d0-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="838d0-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="838d0-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="838d0-134">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="838d0-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="838d0-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="838d0-135">**Error**</span></span> <br/> | <span data-ttu-id="838d0-136">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="838d0-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="838d0-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="838d0-137">The following are examples of sources of errors:</span></span><br/><br/><span data-ttu-id="838d0-138">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="838d0-138">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="838d0-139">-Atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="838d0-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="838d0-140">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="838d0-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="838d0-141">-Atributo o elemento no válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="838d0-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="838d0-142">-Intento de acceso no autorizado por parte de un cliente</span><span class="sxs-lookup"><span data-stu-id="838d0-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="838d0-143">-Error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="838d0-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="838d0-144">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="838d0-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="838d0-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="838d0-145">Child elements</span></span>

|<span data-ttu-id="838d0-146">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="838d0-146">**Element**</span></span>|<span data-ttu-id="838d0-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="838d0-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="838d0-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="838d0-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="838d0-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="838d0-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="838d0-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="838d0-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="838d0-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="838d0-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="838d0-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="838d0-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="838d0-153">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="838d0-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="838d0-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="838d0-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="838d0-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="838d0-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="838d0-156">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="838d0-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="838d0-157">RootItemId</span><span class="sxs-lookup"><span data-stu-id="838d0-157">RootItemId</span></span>](rootitemid.md) <br/> |<span data-ttu-id="838d0-158">Identifica el elemento primario de un dato adjunto eliminado.</span><span class="sxs-lookup"><span data-stu-id="838d0-158">Identifies the parent item of a deleted attachment.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="838d0-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="838d0-159">Parent elements</span></span>

|<span data-ttu-id="838d0-160">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="838d0-160">**Element**</span></span>|<span data-ttu-id="838d0-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="838d0-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="838d0-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="838d0-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="838d0-163">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="838d0-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="838d0-164">Comentarios</span><span class="sxs-lookup"><span data-stu-id="838d0-164">Remarks</span></span>

<span data-ttu-id="838d0-165">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con el rol de servidor acceso de clientes instalado.</span><span class="sxs-lookup"><span data-stu-id="838d0-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="838d0-166">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="838d0-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="838d0-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="838d0-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="838d0-168">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="838d0-168">Schema Name</span></span>  <br/> |<span data-ttu-id="838d0-169">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="838d0-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="838d0-170">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="838d0-170">Validation File</span></span>  <br/> |<span data-ttu-id="838d0-171">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="838d0-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="838d0-172">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="838d0-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="838d0-173">Falso</span><span class="sxs-lookup"><span data-stu-id="838d0-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="838d0-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="838d0-174">See also</span></span>

- [<span data-ttu-id="838d0-175">DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="838d0-175">DeleteAttachment</span></span>](deleteattachment.md) 
- [<span data-ttu-id="838d0-176">Operación DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="838d0-176">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
- [<span data-ttu-id="838d0-177">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="838d0-177">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="838d0-178">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="838d0-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

