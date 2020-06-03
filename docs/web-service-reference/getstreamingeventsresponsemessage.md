---
title: GetStreamingEventsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetStreamingEventsResponseMessage
api_type:
- schema
ms.assetid: 655e4e78-af74-48b0-a988-7d86ab368feb
description: El elemento GetStreamingEventsResponseMessage contiene el estado y el resultado de una única solicitud de operación GetStreamingEvents.
ms.openlocfilehash: 055fb7eeb12e241739eb860cecbe398b8a322bd2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459149"
---
# <a name="getstreamingeventsresponsemessage"></a><span data-ttu-id="95125-103">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="95125-103">GetStreamingEventsResponseMessage</span></span>

<span data-ttu-id="95125-104">El elemento **GetStreamingEventsResponseMessage** contiene el estado y el resultado de una única solicitud de [operación GetStreamingEvents](getstreamingevents-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="95125-104">The **GetStreamingEventsResponseMessage** element contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.</span></span> 
  
```xml
<GetStreamingEventsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Notifications/>
   <ErrorSubscriptionIds/>
   <ConnectionStatus/>
</GetStreamingEventsResponseMessage>
```

 <span data-ttu-id="95125-105">**GetStreamingEventsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="95125-105">**GetStreamingEventsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="95125-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="95125-106">Attributes and elements</span></span>

<span data-ttu-id="95125-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="95125-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95125-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="95125-108">Attributes</span></span>

|<span data-ttu-id="95125-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="95125-109">**Attribute**</span></span>|<span data-ttu-id="95125-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="95125-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="95125-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="95125-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="95125-112">Describe el estado de una respuesta de [operación de GetStreamingEvents](getstreamingevents-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="95125-112">Describes the status of a [GetStreamingEvents operation](getstreamingevents-operation.md) response.</span></span> <br/><br/><span data-ttu-id="95125-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="95125-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="95125-114">-Correcto</span><span class="sxs-lookup"><span data-stu-id="95125-114">-  Success</span></span>  <br/><span data-ttu-id="95125-115">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="95125-115">-  Warning</span></span>  <br/><span data-ttu-id="95125-116">-Error</span><span class="sxs-lookup"><span data-stu-id="95125-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="95125-117">Atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="95125-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="95125-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="95125-118">**Value**</span></span>|<span data-ttu-id="95125-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="95125-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="95125-120">Correcto</span><span class="sxs-lookup"><span data-stu-id="95125-120">Success</span></span>  <br/> |<span data-ttu-id="95125-121">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="95125-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="95125-122">Advertencia</span><span class="sxs-lookup"><span data-stu-id="95125-122">Warning</span></span>  <br/> | <span data-ttu-id="95125-123">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="95125-123">Describes a request that was not processed.</span></span> <span data-ttu-id="95125-124">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="95125-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="95125-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="95125-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="95125-126">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="95125-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="95125-127">-Los servicios de dominio de Active Directory (AD DS) están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="95125-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="95125-128">-Se movieron los buzones.</span><span class="sxs-lookup"><span data-stu-id="95125-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="95125-129">-La base de datos de buzones (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="95125-129">-  The mailbox database (MDB) is offline.</span></span>  <br/><span data-ttu-id="95125-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="95125-130">-  A password has expired.</span></span>  <br/><span data-ttu-id="95125-131">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="95125-131">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="95125-132">Error</span><span class="sxs-lookup"><span data-stu-id="95125-132">Error</span></span>  <br/> | <span data-ttu-id="95125-133">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="95125-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="95125-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="95125-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="95125-135">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="95125-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="95125-136">-Atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="95125-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="95125-137">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="95125-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="95125-138">-Un atributo o elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="95125-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="95125-139">-Un intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="95125-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="95125-140">-Un error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="95125-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="95125-141">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="95125-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="95125-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="95125-142">Child elements</span></span>

|<span data-ttu-id="95125-143">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="95125-143">**Element**</span></span>|<span data-ttu-id="95125-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="95125-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95125-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="95125-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="95125-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="95125-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="95125-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="95125-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="95125-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="95125-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="95125-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="95125-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="95125-150">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="95125-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="95125-151">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="95125-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="95125-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="95125-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="95125-153">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="95125-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="95125-154">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="95125-154">Notifications</span></span>](notifications.md) <br/> |<span data-ttu-id="95125-155">Contiene una lista de información sobre la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="95125-155">Contains a list of information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
|[<span data-ttu-id="95125-156">ErrorSubscriptionIds</span><span class="sxs-lookup"><span data-stu-id="95125-156">ErrorSubscriptionIds</span></span>](errorsubscriptionids.md) <br/> |<span data-ttu-id="95125-157">Contiene una lista de identificadores de suscripción que no son válidos.</span><span class="sxs-lookup"><span data-stu-id="95125-157">Contains a list of subscription IDs that are invalid.</span></span>  <br/> |
|[<span data-ttu-id="95125-158">ConnectionStatus</span><span class="sxs-lookup"><span data-stu-id="95125-158">ConnectionStatus</span></span>](connectionstatus.md) <br/> |<span data-ttu-id="95125-159">Proporciona una descripción textual del estado de una suscripción de transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="95125-159">Provides a text description of the status of a streaming subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="95125-160">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="95125-160">Parent elements</span></span>

|<span data-ttu-id="95125-161">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="95125-161">**Element**</span></span>|<span data-ttu-id="95125-162">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="95125-162">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95125-163">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="95125-163">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="95125-164">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="95125-164">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="95125-165">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="95125-165">Text value</span></span>

<span data-ttu-id="95125-166">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="95125-166">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="95125-167">Comentarios</span><span class="sxs-lookup"><span data-stu-id="95125-167">Remarks</span></span>

<span data-ttu-id="95125-168">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="95125-168">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="95125-169">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="95125-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95125-170">Namespace</span><span class="sxs-lookup"><span data-stu-id="95125-170">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="95125-171">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="95125-171">Schema Name</span></span>  <br/> |<span data-ttu-id="95125-172">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="95125-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="95125-173">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="95125-173">Validation File</span></span>  <br/> |<span data-ttu-id="95125-174">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="95125-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="95125-175">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="95125-175">Can be Empty</span></span>  <br/> |<span data-ttu-id="95125-176">Falso</span><span class="sxs-lookup"><span data-stu-id="95125-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="95125-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="95125-177">See also</span></span>

- [<span data-ttu-id="95125-178">GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="95125-178">GetStreamingEvents</span></span>](getstreamingevents.md) 
- [<span data-ttu-id="95125-179">GetStreamingEventsResponse</span><span class="sxs-lookup"><span data-stu-id="95125-179">GetStreamingEventsResponse</span></span>](getstreamingeventsresponse.md)
- [<span data-ttu-id="95125-180">Operación GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="95125-180">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)

