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
ms.openlocfilehash: cfe36364431a8fe81c3f62e68356b634f00bee78
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457798"
---
# <a name="getattachmentresponsemessage"></a><span data-ttu-id="6ba49-103">GetAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6ba49-103">GetAttachmentResponseMessage</span></span>

<span data-ttu-id="6ba49-104">El elemento **GetAttachmentResponseMessage** contiene el estado y el resultado de una única solicitud de [operación GetAttachment](getattachment-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="6ba49-104">The **GetAttachmentResponseMessage** element contains the status and result of a single [GetAttachment operation](getattachment-operation.md) request.</span></span> 
  
- [<span data-ttu-id="6ba49-105">GetAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="6ba49-105">GetAttachmentResponse</span></span>](getattachmentresponse.md) 
- [<span data-ttu-id="6ba49-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="6ba49-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="6ba49-107">GetAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6ba49-107">GetAttachmentResponseMessage</span></span>](getattachmentresponsemessage.md)
  
```xml
<GetAttachmentResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Attachments/>
</GetAttachmentResponseMessage>
```

 <span data-ttu-id="6ba49-108">**AttachmentInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="6ba49-108">**AttachmentInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6ba49-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6ba49-109">Attributes and elements</span></span>

<span data-ttu-id="6ba49-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6ba49-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6ba49-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="6ba49-111">Attributes</span></span>

|<span data-ttu-id="6ba49-112">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="6ba49-112">**Attribute**</span></span>|<span data-ttu-id="6ba49-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6ba49-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6ba49-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="6ba49-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="6ba49-115">Describe el estado de una respuesta de la [operación GetAttachment](getattachment-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="6ba49-115">Describes the status of a [GetAttachment operation](getattachment-operation.md) response.</span></span><br/><br/> <span data-ttu-id="6ba49-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="6ba49-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="6ba49-117">-Correcto</span><span class="sxs-lookup"><span data-stu-id="6ba49-117">-  Success</span></span>  <br/><span data-ttu-id="6ba49-118">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="6ba49-118">-  Warning</span></span>  <br/><span data-ttu-id="6ba49-119">-Error</span><span class="sxs-lookup"><span data-stu-id="6ba49-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="6ba49-120">Atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="6ba49-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="6ba49-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6ba49-121">**Value**</span></span>|<span data-ttu-id="6ba49-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6ba49-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6ba49-123">Correcto</span><span class="sxs-lookup"><span data-stu-id="6ba49-123">Success</span></span>  <br/> |<span data-ttu-id="6ba49-124">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="6ba49-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="6ba49-125">Advertencia</span><span class="sxs-lookup"><span data-stu-id="6ba49-125">Warning</span></span>  <br/> | <span data-ttu-id="6ba49-126">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="6ba49-126">Describes a request that was not processed.</span></span> <span data-ttu-id="6ba49-127">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="6ba49-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="6ba49-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="6ba49-128">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="6ba49-129">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="6ba49-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="6ba49-130">-Los servicios de dominio de Active Directory (AD DS) están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="6ba49-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="6ba49-131">-Se mueven los buzones.</span><span class="sxs-lookup"><span data-stu-id="6ba49-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="6ba49-132">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="6ba49-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="6ba49-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="6ba49-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="6ba49-134">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="6ba49-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="6ba49-135">Error</span><span class="sxs-lookup"><span data-stu-id="6ba49-135">Error</span></span>  <br/> | <span data-ttu-id="6ba49-136">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="6ba49-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="6ba49-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="6ba49-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="6ba49-138">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="6ba49-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="6ba49-139">-Atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="6ba49-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="6ba49-140">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="6ba49-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="6ba49-141">-Atributo o elemento no válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="6ba49-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="6ba49-142">-Intento de acceso no autorizado por parte de un cliente</span><span class="sxs-lookup"><span data-stu-id="6ba49-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="6ba49-143">-Error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="6ba49-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="6ba49-144">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="6ba49-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6ba49-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6ba49-145">Child elements</span></span>

|<span data-ttu-id="6ba49-146">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6ba49-146">**Element**</span></span>|<span data-ttu-id="6ba49-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6ba49-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ba49-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="6ba49-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="6ba49-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ba49-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="6ba49-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="6ba49-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="6ba49-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6ba49-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="6ba49-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="6ba49-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="6ba49-153">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="6ba49-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="6ba49-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="6ba49-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="6ba49-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="6ba49-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="6ba49-156">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="6ba49-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="6ba49-157">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="6ba49-157">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="6ba49-158">Contiene los elementos o archivos que se ttached a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6ba49-158">Contains the items or files that are ttached to an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6ba49-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6ba49-159">Parent elements</span></span>

|<span data-ttu-id="6ba49-160">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6ba49-160">**Element**</span></span>|<span data-ttu-id="6ba49-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6ba49-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ba49-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="6ba49-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="6ba49-163">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6ba49-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ba49-164">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6ba49-164">Remarks</span></span>

<span data-ttu-id="6ba49-165">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="6ba49-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6ba49-166">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6ba49-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ba49-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ba49-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6ba49-168">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6ba49-168">Schema Name</span></span>  <br/> |<span data-ttu-id="6ba49-169">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="6ba49-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6ba49-170">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6ba49-170">Validation File</span></span>  <br/> |<span data-ttu-id="6ba49-171">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6ba49-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6ba49-172">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6ba49-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="6ba49-173">Falso</span><span class="sxs-lookup"><span data-stu-id="6ba49-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6ba49-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ba49-174">See also</span></span>

- [<span data-ttu-id="6ba49-175">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="6ba49-175">GetAttachment</span></span>](getattachment.md) 
- [<span data-ttu-id="6ba49-176">Operación GetAttachment</span><span class="sxs-lookup"><span data-stu-id="6ba49-176">GetAttachment operation</span></span>](getattachment-operation.md)

