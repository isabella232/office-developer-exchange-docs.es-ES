---
title: CreateAttachmentResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateAttachmentResponseMessage
api_type:
- schema
ms.assetid: b326e616-3ce0-4dcb-ba75-4ce4b9867211
description: El elemento CreateAttachmentResponseMessage contiene el estado y el resultado de una única solicitud de operación CreateAttachment.
ms.openlocfilehash: a6d3adde07dedb7a2533d6e9c7fc6ff0497792bf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763924"
---
# <a name="createattachmentresponsemessage"></a><span data-ttu-id="de480-103">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="de480-103">CreateAttachmentResponseMessage</span></span>

<span data-ttu-id="de480-104">El elemento **CreateAttachmentResponseMessage** contiene el estado y el resultado de una única solicitud de [operación CreateAttachment](createattachment-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="de480-104">The **CreateAttachmentResponseMessage** element contains the status and result of a single [CreateAttachment operation](createattachment-operation.md) request.</span></span> 
  
- [<span data-ttu-id="de480-105">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="de480-105">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
- [<span data-ttu-id="de480-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="de480-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="de480-107">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="de480-107">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
  
```xml
<CreateAttachmentResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Attachments/>
</CreateAttachmentResponseMessage>
```

<span data-ttu-id="de480-108">**AttachmentInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="de480-108">**AttachmentInfoResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="de480-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="de480-109">Attributes and elements</span></span>

<span data-ttu-id="de480-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="de480-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="de480-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="de480-111">Attributes</span></span>

|<span data-ttu-id="de480-112">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="de480-112">**Attribute**</span></span>|<span data-ttu-id="de480-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de480-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="de480-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="de480-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="de480-115">Describe el estado de una respuesta de [la operación CreateAttachment](createattachment-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="de480-115">Describes the status of a [CreateAttachment operation](createattachment-operation.md) response.</span></span> <br/><br/><span data-ttu-id="de480-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="de480-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="de480-117">-Éxito</span><span class="sxs-lookup"><span data-stu-id="de480-117">-  Success</span></span>  <br/><span data-ttu-id="de480-118">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="de480-118">-  Warning</span></span>  <br/><span data-ttu-id="de480-119">-Error</span><span class="sxs-lookup"><span data-stu-id="de480-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="de480-120">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="de480-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="de480-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="de480-121">**Value**</span></span>|<span data-ttu-id="de480-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de480-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="de480-123">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="de480-123">**Success**</span></span> <br/> |<span data-ttu-id="de480-124">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="de480-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="de480-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="de480-125">**Warning**</span></span> <br/> | <span data-ttu-id="de480-126">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="de480-126">Describes a request that was not processed.</span></span> <span data-ttu-id="de480-127">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="de480-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="de480-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="de480-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="de480-129">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="de480-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="de480-130">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="de480-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="de480-131">-Se mueven los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="de480-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="de480-132">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="de480-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="de480-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="de480-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="de480-134">-Se ha excedido una cuota.</span><span class="sxs-lookup"><span data-stu-id="de480-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="de480-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="de480-135">**Error**</span></span> <br/> | <span data-ttu-id="de480-136">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="de480-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="de480-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="de480-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="de480-138">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="de480-138">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="de480-139">-Los atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="de480-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="de480-140">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="de480-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="de480-141">-De atributo o elemento no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="de480-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="de480-142">-Intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="de480-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="de480-143">-Error server-side en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="de480-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="de480-144">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="de480-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="de480-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="de480-145">Child elements</span></span>

|<span data-ttu-id="de480-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="de480-146">**Element**</span></span>|<span data-ttu-id="de480-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de480-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de480-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="de480-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="de480-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="de480-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="de480-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="de480-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="de480-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="de480-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="de480-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="de480-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="de480-153">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="de480-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="de480-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="de480-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="de480-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="de480-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="de480-156">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="de480-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="de480-157">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="de480-157">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="de480-158">Contiene los elementos o archivos que se adjuntan a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="de480-158">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="de480-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="de480-159">Parent elements</span></span>

|<span data-ttu-id="de480-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="de480-160">**Element**</span></span>|<span data-ttu-id="de480-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de480-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de480-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="de480-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="de480-163">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="de480-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de480-164">Comentarios</span><span class="sxs-lookup"><span data-stu-id="de480-164">Remarks</span></span>

<span data-ttu-id="de480-165">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="de480-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="de480-166">Si varios datos adjuntos se adjuntan a un elemento en un solo viaje de ida y vuelta, el atributo **RootItemChangeKey** en el último mensaje de respuesta es la que representa la nueva clave de cambio del elemento que tiene los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="de480-166">If multiple attachments are attached to an item in a single round trip, the **RootItemChangeKey** attribute in the last response message is the one that represents the new change key of the item that has the attachments.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="de480-167">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="de480-167">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de480-168">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="de480-168">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="de480-169">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="de480-169">Schema Name</span></span>  <br/> |<span data-ttu-id="de480-170">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="de480-170">Messages schema</span></span>  <br/> |
|<span data-ttu-id="de480-171">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="de480-171">Validation File</span></span>  <br/> |<span data-ttu-id="de480-172">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="de480-172">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="de480-173">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="de480-173">Can be Empty</span></span>  <br/> |<span data-ttu-id="de480-174">False</span><span class="sxs-lookup"><span data-stu-id="de480-174">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="de480-175">Vea también</span><span class="sxs-lookup"><span data-stu-id="de480-175">See also</span></span>

- [<span data-ttu-id="de480-176">Operación CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="de480-176">CreateAttachment operation</span></span>](createattachment-operation.md) 
- [<span data-ttu-id="de480-177">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="de480-177">CreateAttachment</span></span>](createattachment.md)
- [<span data-ttu-id="de480-178">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="de480-178">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="de480-179">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="de480-179">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

