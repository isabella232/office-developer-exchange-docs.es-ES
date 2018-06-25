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
ms.openlocfilehash: 90e79194182f61ba7298ef67b1070b1aa239073d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764831"
---
# <a name="geteventsresponsemessage"></a><span data-ttu-id="39c2b-103">GetEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="39c2b-103">GetEventsResponseMessage</span></span>

<span data-ttu-id="39c2b-104">El elemento **GetEventsResponseMessage** contiene el estado y el resultado de una única solicitud de [operación GetEvents](getevents-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="39c2b-104">The **GetEventsResponseMessage** element contains the status and result of a single [GetEvents operation](getevents-operation.md) request.</span></span> 
  
```xml
<GetEventsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Notification/>
</GetEventsResponseMessage>
```

 <span data-ttu-id="39c2b-105">**GetEventsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="39c2b-105">**GetEventsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="39c2b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="39c2b-106">Attributes and elements</span></span>

<span data-ttu-id="39c2b-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="39c2b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="39c2b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="39c2b-108">Attributes</span></span>

|<span data-ttu-id="39c2b-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="39c2b-109">**Attribute**</span></span>|<span data-ttu-id="39c2b-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="39c2b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="39c2b-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="39c2b-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="39c2b-112">Describe el estado de una respuesta de [la operación GetEvents](getevents-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="39c2b-112">Describes the status of a [GetEvents operation](getevents-operation.md) response.</span></span> <br/><br/><span data-ttu-id="39c2b-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="39c2b-113">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="39c2b-114">-Éxito</span><span class="sxs-lookup"><span data-stu-id="39c2b-114">-  Success</span></span>  <br/><span data-ttu-id="39c2b-115">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="39c2b-115">-  Warning</span></span>  <br/><span data-ttu-id="39c2b-116">-Error</span><span class="sxs-lookup"><span data-stu-id="39c2b-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="39c2b-117">Atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="39c2b-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="39c2b-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="39c2b-118">**Value**</span></span>|<span data-ttu-id="39c2b-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="39c2b-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="39c2b-120">Correcto</span><span class="sxs-lookup"><span data-stu-id="39c2b-120">Success</span></span>  <br/> |<span data-ttu-id="39c2b-121">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="39c2b-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="39c2b-122">Advertencia</span><span class="sxs-lookup"><span data-stu-id="39c2b-122">Warning</span></span>  <br/> | <span data-ttu-id="39c2b-123">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="39c2b-123">Describes a request that was not processed.</span></span> <span data-ttu-id="39c2b-124">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="39c2b-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="39c2b-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="39c2b-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="39c2b-126">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="39c2b-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="39c2b-127">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="39c2b-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="39c2b-128">-Buzones se han movido.</span><span class="sxs-lookup"><span data-stu-id="39c2b-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="39c2b-129">-La base de datos de buzón (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="39c2b-129">-  The mailbox database (MDB) is offline.</span></span>  <br/><span data-ttu-id="39c2b-130">-Una contraseña ha caducado.</span><span class="sxs-lookup"><span data-stu-id="39c2b-130">-  A password has expired.</span></span>  <br/><span data-ttu-id="39c2b-131">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="39c2b-131">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="39c2b-132">Error</span><span class="sxs-lookup"><span data-stu-id="39c2b-132">Error</span></span>  <br/> | <span data-ttu-id="39c2b-133">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="39c2b-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="39c2b-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="39c2b-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="39c2b-135">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="39c2b-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="39c2b-136">-Los atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="39c2b-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="39c2b-137">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="39c2b-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="39c2b-138">-Un atributo o un elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="39c2b-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="39c2b-139">-Un intento de acceso no autorizado por cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="39c2b-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="39c2b-140">-Un error del lado del servidor en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="39c2b-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="39c2b-141">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="39c2b-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="39c2b-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="39c2b-142">Child elements</span></span>

|<span data-ttu-id="39c2b-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="39c2b-143">**Element**</span></span>|<span data-ttu-id="39c2b-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="39c2b-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39c2b-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="39c2b-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="39c2b-146">Proporciona la descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="39c2b-146">Provides text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="39c2b-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="39c2b-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="39c2b-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="39c2b-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="39c2b-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="39c2b-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="39c2b-150">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="39c2b-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="39c2b-151">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="39c2b-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="39c2b-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="39c2b-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="39c2b-153">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="39c2b-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="39c2b-154">Notificación</span><span class="sxs-lookup"><span data-stu-id="39c2b-154">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="39c2b-155">Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="39c2b-155">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="39c2b-156">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="39c2b-156">Parent elements</span></span>

|<span data-ttu-id="39c2b-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="39c2b-157">**Element**</span></span>|<span data-ttu-id="39c2b-158">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="39c2b-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39c2b-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="39c2b-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="39c2b-160">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="39c2b-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39c2b-161">Comentarios</span><span class="sxs-lookup"><span data-stu-id="39c2b-161">Remarks</span></span>

<span data-ttu-id="39c2b-162">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="39c2b-162">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="39c2b-163">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="39c2b-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39c2b-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="39c2b-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="39c2b-165">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="39c2b-165">Schema Name</span></span>  <br/> |<span data-ttu-id="39c2b-166">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="39c2b-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="39c2b-167">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="39c2b-167">Validation File</span></span>  <br/> |<span data-ttu-id="39c2b-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="39c2b-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="39c2b-169">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="39c2b-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="39c2b-170">False</span><span class="sxs-lookup"><span data-stu-id="39c2b-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="39c2b-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="39c2b-171">See also</span></span>

- [<span data-ttu-id="39c2b-172">GetEvents</span><span class="sxs-lookup"><span data-stu-id="39c2b-172">GetEvents</span></span>](getevents.md) 
- [<span data-ttu-id="39c2b-173">GetEventsResponse</span><span class="sxs-lookup"><span data-stu-id="39c2b-173">GetEventsResponse</span></span>](geteventsresponse.md)
- [<span data-ttu-id="39c2b-174">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="39c2b-174">GetEvents operation</span></span>](getevents-operation.md)

