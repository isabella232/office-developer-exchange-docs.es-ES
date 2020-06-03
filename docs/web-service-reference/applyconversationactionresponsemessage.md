---
title: ApplyConversationActionResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ApplyConversationActionResponseMessage
api_type:
- schema
ms.assetid: a09edc89-7f2f-4846-a3a5-06694c97b9f6
description: El elemento ApplyConversationActionResponseMessage contiene el estado y los resultados de una solicitud de operación ApplyConversationAction.
ms.openlocfilehash: 377aee12d8cc7d6b4aff8d6fc2a6cb67b3bcd10b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464696"
---
# <a name="applyconversationactionresponsemessage"></a><span data-ttu-id="94a44-103">ApplyConversationActionResponseMessage</span><span class="sxs-lookup"><span data-stu-id="94a44-103">ApplyConversationActionResponseMessage</span></span>

<span data-ttu-id="94a44-104">El elemento **ApplyConversationActionResponseMessage** contiene el estado y los resultados de una solicitud de [operación ApplyConversationAction](applyconversationaction-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="94a44-104">The **ApplyConversationActionResponseMessage** element contains the status and results of an [ApplyConversationAction operation](applyconversationaction-operation.md) request.</span></span>  
  
- [<span data-ttu-id="94a44-105">ApplyConversationActionResponse</span><span class="sxs-lookup"><span data-stu-id="94a44-105">ApplyConversationActionResponse</span></span>](applyconversationactionresponse.md)
- [<span data-ttu-id="94a44-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="94a44-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="94a44-107">ApplyConversationActionResponseMessage</span><span class="sxs-lookup"><span data-stu-id="94a44-107">ApplyConversationActionResponseMessage</span></span>](applyconversationactionresponsemessage.md)
  
```XML
<ApplyConversationActionResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</ApplyConversationActionResponseMessage>
```

 <span data-ttu-id="94a44-108">**ApplyConversationActionResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="94a44-108">**ApplyConversationActionResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="94a44-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="94a44-109">Attributes and elements</span></span>

<span data-ttu-id="94a44-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="94a44-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="94a44-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="94a44-111">Attributes</span></span>

|<span data-ttu-id="94a44-112">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="94a44-112">**Attribute**</span></span>|<span data-ttu-id="94a44-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="94a44-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="94a44-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="94a44-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="94a44-115">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="94a44-115">Describes the status of the response.</span></span><br/><br/><span data-ttu-id="94a44-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="94a44-116">The following values are valid for this attribute:</span></span><ul><li><span data-ttu-id="94a44-117">Correcto</span><span class="sxs-lookup"><span data-stu-id="94a44-117">Success</span></span></li><li><span data-ttu-id="94a44-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="94a44-118">Warning</span></span></li><li><span data-ttu-id="94a44-119">Error</span><span class="sxs-lookup"><span data-stu-id="94a44-119">Error</span></span></li></ul> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="94a44-120">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="94a44-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="94a44-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="94a44-121">**Value**</span></span>|<span data-ttu-id="94a44-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="94a44-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="94a44-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="94a44-123">**Success**</span></span> <br/> |<span data-ttu-id="94a44-124">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="94a44-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="94a44-125">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="94a44-125">**Warning**</span></span> <br/> | <span data-ttu-id="94a44-126">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="94a44-126">Describes a request that was not processed.</span></span> <span data-ttu-id="94a44-127">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="94a44-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="94a44-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="94a44-128">The following are examples of sources of warnings:</span></span><ul><li><span data-ttu-id="94a44-129">El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="94a44-129">The Exchange store is offline during the batch.</span></span></li><li><span data-ttu-id="94a44-130">Los servicios de dominio de Active Directory (AD DS) están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="94a44-130">Active Directory Domain Services (AD DS) is offline.</span></span></li><li><span data-ttu-id="94a44-131">Buzones de correo que se movieron.</span><span class="sxs-lookup"><span data-stu-id="94a44-131">Mailboxes were moved.</span></span></li><li><span data-ttu-id="94a44-132">La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="94a44-132">The message database (MDB) is offline.</span></span></li><li><span data-ttu-id="94a44-133">Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="94a44-133">A password is expired.</span></span></li><li><span data-ttu-id="94a44-134">Se ha superado una cuota.</span><span class="sxs-lookup"><span data-stu-id="94a44-134">A quota has been exceeded.</span></span></li></ul> |
|<span data-ttu-id="94a44-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="94a44-135">**Error**</span></span> <br/> | <span data-ttu-id="94a44-136">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="94a44-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="94a44-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="94a44-137">The following are examples of sources of errors:</span></span>  <ul><li><span data-ttu-id="94a44-138">Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="94a44-138">Invalid attributes or elements</span></span></li><li><span data-ttu-id="94a44-139">Atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="94a44-139">Attributes or elements that are out of range</span></span></li><li><span data-ttu-id="94a44-140">Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="94a44-140">An unknown tag</span></span>  </li><li><span data-ttu-id="94a44-141">Un atributo o elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="94a44-141">An attribute or element that is not valid in the context</span></span></li><li><span data-ttu-id="94a44-142">Un intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="94a44-142">An unauthorized access attempt by any client</span></span></li><li><span data-ttu-id="94a44-143">Un error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="94a44-143">A server-side failure in response to a valid client-side call</span></span></li></ul><span data-ttu-id="94a44-144">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="94a44-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="94a44-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="94a44-145">Child elements</span></span>

|<span data-ttu-id="94a44-146">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="94a44-146">**Element**</span></span>|<span data-ttu-id="94a44-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="94a44-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="94a44-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="94a44-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="94a44-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="94a44-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="94a44-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="94a44-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="94a44-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="94a44-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="94a44-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="94a44-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="94a44-153">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="94a44-153">Currently unused and reserved for future use.</span></span> <span data-ttu-id="94a44-154">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="94a44-154">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="94a44-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="94a44-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="94a44-156">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="94a44-156">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="94a44-157">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="94a44-157">Parent elements</span></span>

|<span data-ttu-id="94a44-158">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="94a44-158">**Element**</span></span>|<span data-ttu-id="94a44-159">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="94a44-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="94a44-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="94a44-160">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="94a44-161">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="94a44-161">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="94a44-162">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="94a44-162">Text value</span></span>

<span data-ttu-id="94a44-163">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="94a44-163">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="94a44-164">Comentarios</span><span class="sxs-lookup"><span data-stu-id="94a44-164">Remarks</span></span>

<span data-ttu-id="94a44-165">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="94a44-165">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="94a44-166">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="94a44-166">Version differences</span></span>

<span data-ttu-id="94a44-167">En las versiones de Exchange que comienzan con la compilación 15.00.0986.00, el elemento **ApplyConversationActionResponseMessage** es del tipo **ApplyConversationActionResponseMessageType**.</span><span class="sxs-lookup"><span data-stu-id="94a44-167">In versions of Exchange starting with build 15.00.0986.00, the **ApplyConversationActionResponseMessage** element is of type **ApplyConversationActionResponseMessageType**.</span></span> <span data-ttu-id="94a44-168">En versiones anteriores, el elemento es del tipo **ResponseMessageType**.</span><span class="sxs-lookup"><span data-stu-id="94a44-168">In previous versions, the element is of type **ResponseMessageType**.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="94a44-169">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="94a44-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="94a44-170">Namespace</span><span class="sxs-lookup"><span data-stu-id="94a44-170">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="94a44-171">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="94a44-171">Schema Name</span></span>  <br/> |<span data-ttu-id="94a44-172">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="94a44-172">Message schema</span></span>  <br/> |
|<span data-ttu-id="94a44-173">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="94a44-173">Validation File</span></span>  <br/> |<span data-ttu-id="94a44-174">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="94a44-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="94a44-175">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="94a44-175">Can be Empty</span></span>  <br/> |<span data-ttu-id="94a44-176">Falso</span><span class="sxs-lookup"><span data-stu-id="94a44-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="94a44-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="94a44-177">See also</span></span>

- [<span data-ttu-id="94a44-178">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="94a44-178">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="94a44-179">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="94a44-179">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

