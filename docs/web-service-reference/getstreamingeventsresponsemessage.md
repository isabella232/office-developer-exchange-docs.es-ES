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
ms.openlocfilehash: 5fcc7ddde41b49a5d8b304da0732f4472c61a76a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835682"
---
# <a name="getstreamingeventsresponsemessage"></a><span data-ttu-id="1d4d7-103">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1d4d7-103">GetStreamingEventsResponseMessage</span></span>

<span data-ttu-id="1d4d7-104">El elemento **GetStreamingEventsResponseMessage** contiene el estado y el resultado de una única solicitud de [operación GetStreamingEvents](getstreamingevents-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="1d4d7-104">The **GetStreamingEventsResponseMessage** element contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.</span></span> 
  
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

 <span data-ttu-id="1d4d7-105">**GetStreamingEventsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="1d4d7-105">**GetStreamingEventsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1d4d7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1d4d7-106">Attributes and elements</span></span>

<span data-ttu-id="1d4d7-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1d4d7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1d4d7-108">Attributes</span></span>

|<span data-ttu-id="1d4d7-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="1d4d7-109">**Attribute**</span></span>|<span data-ttu-id="1d4d7-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d4d7-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1d4d7-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="1d4d7-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="1d4d7-112">Describe el estado de una respuesta de [la operación GetStreamingEvents](getstreamingevents-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="1d4d7-112">Describes the status of a [GetStreamingEvents operation](getstreamingevents-operation.md) response.</span></span> <br/><br/><span data-ttu-id="1d4d7-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="1d4d7-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="1d4d7-114">-Éxito</span><span class="sxs-lookup"><span data-stu-id="1d4d7-114">-  Success</span></span>  <br/><span data-ttu-id="1d4d7-115">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="1d4d7-115">-  Warning</span></span>  <br/><span data-ttu-id="1d4d7-116">-Error</span><span class="sxs-lookup"><span data-stu-id="1d4d7-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="1d4d7-117">Atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="1d4d7-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="1d4d7-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1d4d7-118">**Value**</span></span>|<span data-ttu-id="1d4d7-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d4d7-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1d4d7-120">Correcto</span><span class="sxs-lookup"><span data-stu-id="1d4d7-120">Success</span></span>  <br/> |<span data-ttu-id="1d4d7-121">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="1d4d7-122">Advertencia</span><span class="sxs-lookup"><span data-stu-id="1d4d7-122">Warning</span></span>  <br/> | <span data-ttu-id="1d4d7-123">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-123">Describes a request that was not processed.</span></span> <span data-ttu-id="1d4d7-124">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="1d4d7-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="1d4d7-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="1d4d7-126">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="1d4d7-127">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="1d4d7-128">-Buzones se han movido.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="1d4d7-129">-La base de datos de buzón (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-129">-  The mailbox database (MDB) is offline.</span></span>  <br/><span data-ttu-id="1d4d7-130">-Una contraseña ha caducado.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-130">-  A password has expired.</span></span>  <br/><span data-ttu-id="1d4d7-131">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-131">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="1d4d7-132">Error</span><span class="sxs-lookup"><span data-stu-id="1d4d7-132">Error</span></span>  <br/> | <span data-ttu-id="1d4d7-133">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="1d4d7-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="1d4d7-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="1d4d7-135">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="1d4d7-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="1d4d7-136">-Los atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="1d4d7-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="1d4d7-137">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="1d4d7-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="1d4d7-138">-Un atributo o un elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="1d4d7-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="1d4d7-139">-Un intento de acceso no autorizado por cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="1d4d7-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="1d4d7-140">-Un error del lado del servidor en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="1d4d7-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="1d4d7-141">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="1d4d7-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1d4d7-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1d4d7-142">Child elements</span></span>

|<span data-ttu-id="1d4d7-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="1d4d7-143">**Element**</span></span>|<span data-ttu-id="1d4d7-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d4d7-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d4d7-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="1d4d7-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="1d4d7-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="1d4d7-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1d4d7-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="1d4d7-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="1d4d7-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="1d4d7-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="1d4d7-150">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="1d4d7-151">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="1d4d7-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="1d4d7-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="1d4d7-153">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="1d4d7-154">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="1d4d7-154">Notifications</span></span>](notifications.md) <br/> |<span data-ttu-id="1d4d7-155">Contiene una lista de información acerca de la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-155">Contains a list of information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
|[<span data-ttu-id="1d4d7-156">ErrorSubscriptionIds</span><span class="sxs-lookup"><span data-stu-id="1d4d7-156">ErrorSubscriptionIds</span></span>](errorsubscriptionids.md) <br/> |<span data-ttu-id="1d4d7-157">Contiene una lista de suscripción de los identificadores que no son válidos.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-157">Contains a list of subscription IDs that are invalid.</span></span>  <br/> |
|[<span data-ttu-id="1d4d7-158">ConnectionStatus</span><span class="sxs-lookup"><span data-stu-id="1d4d7-158">ConnectionStatus</span></span>](connectionstatus.md) <br/> |<span data-ttu-id="1d4d7-159">Proporciona una descripción de texto del estado de una suscripción de transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-159">Provides a text description of the status of a streaming subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1d4d7-160">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1d4d7-160">Parent elements</span></span>

|<span data-ttu-id="1d4d7-161">**Element**</span><span class="sxs-lookup"><span data-stu-id="1d4d7-161">**Element**</span></span>|<span data-ttu-id="1d4d7-162">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d4d7-162">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d4d7-163">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="1d4d7-163">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="1d4d7-164">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-164">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1d4d7-165">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1d4d7-165">Text value</span></span>

<span data-ttu-id="1d4d7-166">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1d4d7-166">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1d4d7-167">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1d4d7-167">Remarks</span></span>

<span data-ttu-id="1d4d7-168">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="1d4d7-168">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1d4d7-169">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1d4d7-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d4d7-170">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1d4d7-170">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1d4d7-171">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1d4d7-171">Schema Name</span></span>  <br/> |<span data-ttu-id="1d4d7-172">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="1d4d7-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1d4d7-173">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1d4d7-173">Validation File</span></span>  <br/> |<span data-ttu-id="1d4d7-174">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1d4d7-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1d4d7-175">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1d4d7-175">Can be Empty</span></span>  <br/> |<span data-ttu-id="1d4d7-176">False</span><span class="sxs-lookup"><span data-stu-id="1d4d7-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d4d7-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d4d7-177">See also</span></span>

- [<span data-ttu-id="1d4d7-178">GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="1d4d7-178">GetStreamingEvents</span></span>](getstreamingevents.md) 
- [<span data-ttu-id="1d4d7-179">GetStreamingEventsResponse</span><span class="sxs-lookup"><span data-stu-id="1d4d7-179">GetStreamingEventsResponse</span></span>](getstreamingeventsresponse.md)
- [<span data-ttu-id="1d4d7-180">Operación GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="1d4d7-180">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)

