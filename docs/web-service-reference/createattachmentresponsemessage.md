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
ms.openlocfilehash: 14d8d1936b3cfd52bdb816343c86606cb8ccf76f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458925"
---
# <a name="createattachmentresponsemessage"></a><span data-ttu-id="a8383-103">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a8383-103">CreateAttachmentResponseMessage</span></span>

<span data-ttu-id="a8383-104">El elemento **CreateAttachmentResponseMessage** contiene el estado y el resultado de una única solicitud de [operación CreateAttachment](createattachment-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="a8383-104">The **CreateAttachmentResponseMessage** element contains the status and result of a single [CreateAttachment operation](createattachment-operation.md) request.</span></span> 
  
- [<span data-ttu-id="a8383-105">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="a8383-105">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
- [<span data-ttu-id="a8383-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a8383-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="a8383-107">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a8383-107">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
  
```xml
<CreateAttachmentResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Attachments/>
</CreateAttachmentResponseMessage>
```

<span data-ttu-id="a8383-108">**AttachmentInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="a8383-108">**AttachmentInfoResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a8383-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a8383-109">Attributes and elements</span></span>

<span data-ttu-id="a8383-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a8383-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a8383-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="a8383-111">Attributes</span></span>

|<span data-ttu-id="a8383-112">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a8383-112">**Attribute**</span></span>|<span data-ttu-id="a8383-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a8383-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a8383-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="a8383-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="a8383-115">Describe el estado de una respuesta de [operación de CreateAttachment](createattachment-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="a8383-115">Describes the status of a [CreateAttachment operation](createattachment-operation.md) response.</span></span> <br/><br/><span data-ttu-id="a8383-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="a8383-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="a8383-117">-Correcto</span><span class="sxs-lookup"><span data-stu-id="a8383-117">-  Success</span></span>  <br/><span data-ttu-id="a8383-118">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="a8383-118">-  Warning</span></span>  <br/><span data-ttu-id="a8383-119">-Error</span><span class="sxs-lookup"><span data-stu-id="a8383-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="a8383-120">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="a8383-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="a8383-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a8383-121">**Value**</span></span>|<span data-ttu-id="a8383-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a8383-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a8383-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="a8383-123">**Success**</span></span> <br/> |<span data-ttu-id="a8383-124">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="a8383-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="a8383-125">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="a8383-125">**Warning**</span></span> <br/> | <span data-ttu-id="a8383-126">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="a8383-126">Describes a request that was not processed.</span></span> <span data-ttu-id="a8383-127">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="a8383-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="a8383-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="a8383-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="a8383-129">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="a8383-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="a8383-130">-Los servicios de dominio de Active Directory (AD DS) están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="a8383-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="a8383-131">-Se mueven los buzones.</span><span class="sxs-lookup"><span data-stu-id="a8383-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="a8383-132">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="a8383-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="a8383-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="a8383-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="a8383-134">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="a8383-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="a8383-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="a8383-135">**Error**</span></span> <br/> | <span data-ttu-id="a8383-136">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="a8383-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="a8383-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="a8383-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="a8383-138">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="a8383-138">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="a8383-139">-Atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="a8383-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="a8383-140">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="a8383-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="a8383-141">-Atributo o elemento no válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="a8383-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="a8383-142">-Intento de acceso no autorizado por parte de un cliente</span><span class="sxs-lookup"><span data-stu-id="a8383-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="a8383-143">-Error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="a8383-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="a8383-144">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="a8383-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a8383-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a8383-145">Child elements</span></span>

|<span data-ttu-id="a8383-146">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a8383-146">**Element**</span></span>|<span data-ttu-id="a8383-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a8383-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a8383-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="a8383-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="a8383-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a8383-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="a8383-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a8383-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="a8383-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a8383-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="a8383-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="a8383-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="a8383-153">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="a8383-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="a8383-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="a8383-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="a8383-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="a8383-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="a8383-156">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="a8383-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="a8383-157">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="a8383-157">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="a8383-158">Contiene los elementos o archivos adjuntos a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a8383-158">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a8383-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a8383-159">Parent elements</span></span>

|<span data-ttu-id="a8383-160">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a8383-160">**Element**</span></span>|<span data-ttu-id="a8383-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a8383-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a8383-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a8383-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="a8383-163">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a8383-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8383-164">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a8383-164">Remarks</span></span>

<span data-ttu-id="a8383-165">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="a8383-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a8383-166">Si se adjuntan varios datos adjuntos a un elemento en una sola acción de ida y vuelta, el atributo **RootItemChangeKey** del último mensaje de respuesta es el que representa la nueva clave de cambio del elemento que tiene los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="a8383-166">If multiple attachments are attached to an item in a single round trip, the **RootItemChangeKey** attribute in the last response message is the one that represents the new change key of the item that has the attachments.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="a8383-167">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a8383-167">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8383-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8383-168">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a8383-169">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a8383-169">Schema Name</span></span>  <br/> |<span data-ttu-id="a8383-170">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="a8383-170">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a8383-171">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a8383-171">Validation File</span></span>  <br/> |<span data-ttu-id="a8383-172">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a8383-172">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a8383-173">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a8383-173">Can be Empty</span></span>  <br/> |<span data-ttu-id="a8383-174">Falso</span><span class="sxs-lookup"><span data-stu-id="a8383-174">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a8383-175">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8383-175">See also</span></span>

- [<span data-ttu-id="a8383-176">Operación CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="a8383-176">CreateAttachment operation</span></span>](createattachment-operation.md) 
- [<span data-ttu-id="a8383-177">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="a8383-177">CreateAttachment</span></span>](createattachment.md)
- [<span data-ttu-id="a8383-178">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="a8383-178">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="a8383-179">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a8383-179">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

