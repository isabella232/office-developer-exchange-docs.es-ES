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
ms.openlocfilehash: 387e998a393c23f416cc5ad8d6c4a7ad4c92ebc7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764087"
---
# <a name="deleteattachmentresponsemessage"></a><span data-ttu-id="18ab3-103">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="18ab3-103">DeleteAttachmentResponseMessage</span></span>

<span data-ttu-id="18ab3-104">El elemento **DeleteAttachmentResponseMessage** contiene el estado y el resultado de una única solicitud de [operación DeleteAttachment](deleteattachment-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="18ab3-104">The **DeleteAttachmentResponseMessage** element contains the status and result of a single [DeleteAttachment operation](deleteattachment-operation.md) request.</span></span> 
  
- [<span data-ttu-id="18ab3-105">DeleteAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="18ab3-105">DeleteAttachmentResponse</span></span>](deleteattachmentresponse.md)  
- [<span data-ttu-id="18ab3-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="18ab3-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="18ab3-107">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="18ab3-107">DeleteAttachmentResponseMessage</span></span>](deleteattachmentresponsemessage.md)
  
```xml
<DeleteAttachmentResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RootItemId/>
</DeleteAttachmentResponseMessage>
```

<span data-ttu-id="18ab3-108">**DeleteAttachmentResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="18ab3-108">**DeleteAttachmentResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="18ab3-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="18ab3-109">Attributes and elements</span></span>

<span data-ttu-id="18ab3-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="18ab3-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="18ab3-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="18ab3-111">Attributes</span></span>

|<span data-ttu-id="18ab3-112">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="18ab3-112">**Attribute**</span></span>|<span data-ttu-id="18ab3-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="18ab3-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="18ab3-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="18ab3-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="18ab3-115">Describe el estado de una respuesta de [la operación DeleteAttachment](deleteattachment-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="18ab3-115">Describes the status of a [DeleteAttachment operation](deleteattachment-operation.md) response.</span></span><br/><br/><span data-ttu-id="18ab3-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="18ab3-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="18ab3-117">-Éxito</span><span class="sxs-lookup"><span data-stu-id="18ab3-117">-  Success</span></span>  <br/><span data-ttu-id="18ab3-118">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="18ab3-118">-  Warning</span></span>  <br/><span data-ttu-id="18ab3-119">-Error</span><span class="sxs-lookup"><span data-stu-id="18ab3-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="18ab3-120">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="18ab3-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="18ab3-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="18ab3-121">**Value**</span></span>|<span data-ttu-id="18ab3-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="18ab3-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="18ab3-123">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="18ab3-123">**Success**</span></span> <br/> |<span data-ttu-id="18ab3-124">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="18ab3-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="18ab3-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="18ab3-125">**Warning**</span></span> <br/> | <span data-ttu-id="18ab3-126">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="18ab3-126">Describes a request that was not processed.</span></span> <span data-ttu-id="18ab3-127">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="18ab3-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="18ab3-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="18ab3-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="18ab3-129">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="18ab3-129">- The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="18ab3-130">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="18ab3-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="18ab3-131">-Se mueven los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="18ab3-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="18ab3-132">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="18ab3-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="18ab3-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="18ab3-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="18ab3-134">-Se ha excedido una cuota.</span><span class="sxs-lookup"><span data-stu-id="18ab3-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="18ab3-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="18ab3-135">**Error**</span></span> <br/> | <span data-ttu-id="18ab3-136">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="18ab3-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="18ab3-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="18ab3-137">The following are examples of sources of errors:</span></span><br/><br/><span data-ttu-id="18ab3-138">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="18ab3-138">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="18ab3-139">-Los atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="18ab3-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="18ab3-140">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="18ab3-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="18ab3-141">-De atributo o elemento no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="18ab3-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="18ab3-142">-Intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="18ab3-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="18ab3-143">-Error server-side en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="18ab3-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="18ab3-144">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="18ab3-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="18ab3-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="18ab3-145">Child elements</span></span>

|<span data-ttu-id="18ab3-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="18ab3-146">**Element**</span></span>|<span data-ttu-id="18ab3-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="18ab3-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="18ab3-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="18ab3-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="18ab3-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18ab3-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="18ab3-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="18ab3-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="18ab3-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="18ab3-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="18ab3-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="18ab3-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="18ab3-153">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="18ab3-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="18ab3-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="18ab3-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="18ab3-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="18ab3-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="18ab3-156">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="18ab3-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="18ab3-157">RootItemId</span><span class="sxs-lookup"><span data-stu-id="18ab3-157">RootItemId</span></span>](rootitemid.md) <br/> |<span data-ttu-id="18ab3-158">Identifica el elemento primario de un archivo adjunto eliminado.</span><span class="sxs-lookup"><span data-stu-id="18ab3-158">Identifies the parent item of a deleted attachment.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="18ab3-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="18ab3-159">Parent elements</span></span>

|<span data-ttu-id="18ab3-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="18ab3-160">**Element**</span></span>|<span data-ttu-id="18ab3-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="18ab3-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="18ab3-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="18ab3-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="18ab3-163">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="18ab3-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18ab3-164">Comentarios</span><span class="sxs-lookup"><span data-stu-id="18ab3-164">Remarks</span></span>

<span data-ttu-id="18ab3-165">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con la función de servidor de acceso de cliente instalada.</span><span class="sxs-lookup"><span data-stu-id="18ab3-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="18ab3-166">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="18ab3-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18ab3-167">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="18ab3-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="18ab3-168">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="18ab3-168">Schema Name</span></span>  <br/> |<span data-ttu-id="18ab3-169">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="18ab3-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="18ab3-170">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="18ab3-170">Validation File</span></span>  <br/> |<span data-ttu-id="18ab3-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="18ab3-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="18ab3-172">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="18ab3-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="18ab3-173">False</span><span class="sxs-lookup"><span data-stu-id="18ab3-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18ab3-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="18ab3-174">See also</span></span>

- [<span data-ttu-id="18ab3-175">DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="18ab3-175">DeleteAttachment</span></span>](deleteattachment.md) 
- [<span data-ttu-id="18ab3-176">Operación DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="18ab3-176">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
- [<span data-ttu-id="18ab3-177">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="18ab3-177">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="18ab3-178">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="18ab3-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

