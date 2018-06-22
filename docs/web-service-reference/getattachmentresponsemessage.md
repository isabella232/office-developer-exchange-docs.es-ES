---
title: GetAttachmentResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetAttachmentResponseMessage
api_type:
- schema
ms.assetid: f0a841af-422d-4c82-b710-41e2038dbee4
description: El elemento GetAttachmentResponseMessage contiene el estado y el resultado de una única solicitud de operación GetAttachment.
ms.openlocfilehash: 3bf5aac8ba85675e2941acef6f06eb24f0667d17
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764761"
---
# <a name="getattachmentresponsemessage"></a><span data-ttu-id="5bca6-103">GetAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5bca6-103">GetAttachmentResponseMessage</span></span>

<span data-ttu-id="5bca6-104">El elemento **GetAttachmentResponseMessage** contiene el estado y el resultado de una única solicitud de [operación GetAttachment](getattachment-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="5bca6-104">The **GetAttachmentResponseMessage** element contains the status and result of a single [GetAttachment operation](getattachment-operation.md) request.</span></span> 
  
- [<span data-ttu-id="5bca6-105">GetAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="5bca6-105">GetAttachmentResponse</span></span>](getattachmentresponse.md) 
- [<span data-ttu-id="5bca6-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5bca6-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="5bca6-107">GetAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5bca6-107">GetAttachmentResponseMessage</span></span>](getattachmentresponsemessage.md)
  
```xml
<GetAttachmentResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Attachments/>
</GetAttachmentResponseMessage>
```

 <span data-ttu-id="5bca6-108">**AttachmentInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="5bca6-108">**AttachmentInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5bca6-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5bca6-109">Attributes and elements</span></span>

<span data-ttu-id="5bca6-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5bca6-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5bca6-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="5bca6-111">Attributes</span></span>

|<span data-ttu-id="5bca6-112">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="5bca6-112">**Attribute**</span></span>|<span data-ttu-id="5bca6-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5bca6-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5bca6-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="5bca6-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="5bca6-115">Describe el estado de una respuesta de [la operación GetAttachment](getattachment-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="5bca6-115">Describes the status of a [GetAttachment operation](getattachment-operation.md) response.</span></span><br/><br/> <span data-ttu-id="5bca6-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="5bca6-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="5bca6-117">-Éxito</span><span class="sxs-lookup"><span data-stu-id="5bca6-117">-  Success</span></span>  <br/><span data-ttu-id="5bca6-118">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="5bca6-118">-  Warning</span></span>  <br/><span data-ttu-id="5bca6-119">-Error</span><span class="sxs-lookup"><span data-stu-id="5bca6-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="5bca6-120">Atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="5bca6-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="5bca6-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5bca6-121">**Value**</span></span>|<span data-ttu-id="5bca6-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5bca6-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5bca6-123">Correcto</span><span class="sxs-lookup"><span data-stu-id="5bca6-123">Success</span></span>  <br/> |<span data-ttu-id="5bca6-124">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="5bca6-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="5bca6-125">Advertencia</span><span class="sxs-lookup"><span data-stu-id="5bca6-125">Warning</span></span>  <br/> | <span data-ttu-id="5bca6-126">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="5bca6-126">Describes a request that was not processed.</span></span> <span data-ttu-id="5bca6-127">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="5bca6-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="5bca6-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="5bca6-128">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="5bca6-129">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="5bca6-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="5bca6-130">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="5bca6-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="5bca6-131">-Se mueven los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="5bca6-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="5bca6-132">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="5bca6-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="5bca6-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="5bca6-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="5bca6-134">-Se ha excedido una cuota.</span><span class="sxs-lookup"><span data-stu-id="5bca6-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="5bca6-135">Error</span><span class="sxs-lookup"><span data-stu-id="5bca6-135">Error</span></span>  <br/> | <span data-ttu-id="5bca6-136">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="5bca6-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="5bca6-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="5bca6-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="5bca6-138">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="5bca6-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="5bca6-139">-Los atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="5bca6-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="5bca6-140">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="5bca6-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="5bca6-141">-De atributo o elemento no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="5bca6-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="5bca6-142">-Intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="5bca6-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="5bca6-143">-Error server-side en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="5bca6-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="5bca6-144">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="5bca6-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5bca6-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5bca6-145">Child elements</span></span>

|<span data-ttu-id="5bca6-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="5bca6-146">**Element**</span></span>|<span data-ttu-id="5bca6-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5bca6-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5bca6-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="5bca6-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="5bca6-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5bca6-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="5bca6-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5bca6-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="5bca6-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5bca6-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="5bca6-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="5bca6-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="5bca6-153">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="5bca6-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="5bca6-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="5bca6-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="5bca6-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="5bca6-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="5bca6-156">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="5bca6-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="5bca6-157">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="5bca6-157">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="5bca6-158">Contiene los elementos o archivos que están ttached a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5bca6-158">Contains the items or files that are ttached to an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5bca6-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5bca6-159">Parent elements</span></span>

|<span data-ttu-id="5bca6-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="5bca6-160">**Element**</span></span>|<span data-ttu-id="5bca6-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5bca6-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5bca6-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5bca6-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="5bca6-163">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5bca6-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5bca6-164">Notas</span><span class="sxs-lookup"><span data-stu-id="5bca6-164">Remarks</span></span>

<span data-ttu-id="5bca6-165">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="5bca6-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5bca6-166">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5bca6-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5bca6-167">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5bca6-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5bca6-168">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5bca6-168">Schema Name</span></span>  <br/> |<span data-ttu-id="5bca6-169">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="5bca6-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5bca6-170">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5bca6-170">Validation File</span></span>  <br/> |<span data-ttu-id="5bca6-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5bca6-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5bca6-172">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5bca6-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="5bca6-173">False</span><span class="sxs-lookup"><span data-stu-id="5bca6-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5bca6-174">Ver también</span><span class="sxs-lookup"><span data-stu-id="5bca6-174">See also</span></span>

- [<span data-ttu-id="5bca6-175">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="5bca6-175">GetAttachment</span></span>](getattachment.md) 
- [<span data-ttu-id="5bca6-176">Operación GetAttachment</span><span class="sxs-lookup"><span data-stu-id="5bca6-176">GetAttachment operation</span></span>](getattachment-operation.md)

