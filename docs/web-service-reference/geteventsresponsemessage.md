---
title: GetEventsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetEventsResponseMessage
api_type:
- schema
ms.assetid: d433977f-b86a-499e-b9c3-f405ac229358
description: El elemento GetEventsResponseMessage contiene el estado y el resultado de una única solicitud de operación GetEvents.
ms.openlocfilehash: d307aa1f5234ab5a7a2527c55f5e48814ea2687b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462860"
---
# <a name="geteventsresponsemessage"></a><span data-ttu-id="26e87-103">GetEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="26e87-103">GetEventsResponseMessage</span></span>

<span data-ttu-id="26e87-104">El elemento **GetEventsResponseMessage** contiene el estado y el resultado de una única solicitud de [operación GetEvents](getevents-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="26e87-104">The **GetEventsResponseMessage** element contains the status and result of a single [GetEvents operation](getevents-operation.md) request.</span></span> 
  
```xml
<GetEventsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Notification/>
</GetEventsResponseMessage>
```

 <span data-ttu-id="26e87-105">**GetEventsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="26e87-105">**GetEventsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="26e87-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="26e87-106">Attributes and elements</span></span>

<span data-ttu-id="26e87-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="26e87-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="26e87-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="26e87-108">Attributes</span></span>

|<span data-ttu-id="26e87-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="26e87-109">**Attribute**</span></span>|<span data-ttu-id="26e87-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26e87-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="26e87-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="26e87-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="26e87-112">Describe el estado de una respuesta de la [operación GetEvents](getevents-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="26e87-112">Describes the status of a [GetEvents operation](getevents-operation.md) response.</span></span> <br/><br/><span data-ttu-id="26e87-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="26e87-113">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="26e87-114">-Correcto</span><span class="sxs-lookup"><span data-stu-id="26e87-114">-  Success</span></span>  <br/><span data-ttu-id="26e87-115">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="26e87-115">-  Warning</span></span>  <br/><span data-ttu-id="26e87-116">-Error</span><span class="sxs-lookup"><span data-stu-id="26e87-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="26e87-117">Atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="26e87-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="26e87-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="26e87-118">**Value**</span></span>|<span data-ttu-id="26e87-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26e87-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="26e87-120">Correcto</span><span class="sxs-lookup"><span data-stu-id="26e87-120">Success</span></span>  <br/> |<span data-ttu-id="26e87-121">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="26e87-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="26e87-122">Advertencia</span><span class="sxs-lookup"><span data-stu-id="26e87-122">Warning</span></span>  <br/> | <span data-ttu-id="26e87-123">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="26e87-123">Describes a request that was not processed.</span></span> <span data-ttu-id="26e87-124">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="26e87-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="26e87-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="26e87-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="26e87-126">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="26e87-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="26e87-127">-Los servicios de dominio de Active Directory (AD DS) están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="26e87-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="26e87-128">-Se movieron los buzones.</span><span class="sxs-lookup"><span data-stu-id="26e87-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="26e87-129">-La base de datos de buzones (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="26e87-129">-  The mailbox database (MDB) is offline.</span></span>  <br/><span data-ttu-id="26e87-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="26e87-130">-  A password has expired.</span></span>  <br/><span data-ttu-id="26e87-131">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="26e87-131">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="26e87-132">Error</span><span class="sxs-lookup"><span data-stu-id="26e87-132">Error</span></span>  <br/> | <span data-ttu-id="26e87-133">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="26e87-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="26e87-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="26e87-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="26e87-135">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="26e87-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="26e87-136">-Atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="26e87-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="26e87-137">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="26e87-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="26e87-138">-Un atributo o elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="26e87-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="26e87-139">-Un intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="26e87-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="26e87-140">-Un error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="26e87-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="26e87-141">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="26e87-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="26e87-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="26e87-142">Child elements</span></span>

|<span data-ttu-id="26e87-143">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="26e87-143">**Element**</span></span>|<span data-ttu-id="26e87-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26e87-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26e87-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="26e87-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="26e87-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="26e87-146">Provides text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="26e87-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="26e87-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="26e87-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="26e87-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="26e87-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="26e87-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="26e87-150">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="26e87-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="26e87-151">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="26e87-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="26e87-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="26e87-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="26e87-153">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="26e87-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="26e87-154">Notificación</span><span class="sxs-lookup"><span data-stu-id="26e87-154">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="26e87-155">Contiene información sobre la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="26e87-155">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="26e87-156">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="26e87-156">Parent elements</span></span>

|<span data-ttu-id="26e87-157">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="26e87-157">**Element**</span></span>|<span data-ttu-id="26e87-158">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26e87-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26e87-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="26e87-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="26e87-160">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="26e87-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26e87-161">Comentarios</span><span class="sxs-lookup"><span data-stu-id="26e87-161">Remarks</span></span>

<span data-ttu-id="26e87-162">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="26e87-162">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="26e87-163">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="26e87-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26e87-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="26e87-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="26e87-165">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="26e87-165">Schema Name</span></span>  <br/> |<span data-ttu-id="26e87-166">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="26e87-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="26e87-167">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="26e87-167">Validation File</span></span>  <br/> |<span data-ttu-id="26e87-168">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="26e87-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="26e87-169">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="26e87-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="26e87-170">Falso</span><span class="sxs-lookup"><span data-stu-id="26e87-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="26e87-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="26e87-171">See also</span></span>

- [<span data-ttu-id="26e87-172">GetEvents</span><span class="sxs-lookup"><span data-stu-id="26e87-172">GetEvents</span></span>](getevents.md) 
- [<span data-ttu-id="26e87-173">GetEventsResponse</span><span class="sxs-lookup"><span data-stu-id="26e87-173">GetEventsResponse</span></span>](geteventsresponse.md)
- [<span data-ttu-id="26e87-174">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="26e87-174">GetEvents operation</span></span>](getevents-operation.md)

