---
title: SubscribeResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SubscribeResponseMessage
api_type:
- schema
ms.assetid: d121d38a-a61a-4f9c-a477-fc6d7f9af77e
description: El elemento SubscribeResponseMessage contiene el estado y el resultado de una única solicitud de operación de suscripción.
ms.openlocfilehash: 97c7bd9f12511ff226e75f53278c13481679c8a0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837621"
---
# <a name="subscriberesponsemessage"></a><span data-ttu-id="3bc16-103">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3bc16-103">SubscribeResponseMessage</span></span>

<span data-ttu-id="3bc16-104">El elemento **SubscribeResponseMessage** contiene el estado y el resultado de una única solicitud [Subscribe operación](subscribe-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="3bc16-104">The **SubscribeResponseMessage** element contains the status and result of a single [Subscribe operation](subscribe-operation.md) request.</span></span> 
  
- [<span data-ttu-id="3bc16-105">SubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="3bc16-105">SubscribeResponse</span></span>](subscriberesponse.md)
- [<span data-ttu-id="3bc16-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3bc16-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="3bc16-107">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3bc16-107">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md)
  
```xml
<SubscribeResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <SubscriptionId/>
   <Watermark/>
</SubscribeResponseMessage>
```

 <span data-ttu-id="3bc16-108">**SubscribeResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="3bc16-108">**SubscribeResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3bc16-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3bc16-109">Attributes and elements</span></span>

<span data-ttu-id="3bc16-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3bc16-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3bc16-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="3bc16-111">Attributes</span></span>

|<span data-ttu-id="3bc16-112">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="3bc16-112">**Attribute**</span></span>|<span data-ttu-id="3bc16-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3bc16-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3bc16-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="3bc16-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="3bc16-115">Describe el estado de una respuesta de [la operación Suscribir](subscribe-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="3bc16-115">Describes the status of a [Subscribe operation](subscribe-operation.md) response.</span></span> <br/><br/><span data-ttu-id="3bc16-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="3bc16-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="3bc16-117">-Éxito</span><span class="sxs-lookup"><span data-stu-id="3bc16-117">-  Success</span></span>  <br/><span data-ttu-id="3bc16-118">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="3bc16-118">-  Warning</span></span>  <br/><span data-ttu-id="3bc16-119">-Error</span><span class="sxs-lookup"><span data-stu-id="3bc16-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="3bc16-120">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="3bc16-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="3bc16-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3bc16-121">**Value**</span></span>|<span data-ttu-id="3bc16-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3bc16-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3bc16-123">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="3bc16-123">**Success**</span></span> <br/> |<span data-ttu-id="3bc16-124">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="3bc16-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="3bc16-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="3bc16-125">**Warning**</span></span> <br/> | <span data-ttu-id="3bc16-126">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="3bc16-126">Describes a request that was not processed.</span></span> <span data-ttu-id="3bc16-127">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="3bc16-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="3bc16-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="3bc16-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="3bc16-129">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="3bc16-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="3bc16-130">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="3bc16-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="3bc16-131">-Buzones se han movido.</span><span class="sxs-lookup"><span data-stu-id="3bc16-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="3bc16-132">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="3bc16-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="3bc16-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="3bc16-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="3bc16-134">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="3bc16-134">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="3bc16-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="3bc16-135">**Error**</span></span> <br/> | <span data-ttu-id="3bc16-136">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="3bc16-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="3bc16-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="3bc16-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="3bc16-138">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="3bc16-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="3bc16-139">-Los atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="3bc16-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="3bc16-140">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="3bc16-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="3bc16-141">-Un atributo o un elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="3bc16-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="3bc16-142">-Un intento de acceso no autorizado por cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="3bc16-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="3bc16-143">-Un error del lado del servidor en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="3bc16-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="3bc16-144">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="3bc16-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3bc16-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3bc16-145">Child elements</span></span>

|<span data-ttu-id="3bc16-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="3bc16-146">**Element**</span></span>|<span data-ttu-id="3bc16-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3bc16-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3bc16-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="3bc16-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="3bc16-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3bc16-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="3bc16-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="3bc16-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="3bc16-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3bc16-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="3bc16-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="3bc16-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="3bc16-153">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="3bc16-153">Currently unused and reserved for future use.</span></span> <span data-ttu-id="3bc16-154">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="3bc16-154">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="3bc16-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="3bc16-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="3bc16-156">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="3bc16-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="3bc16-157">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="3bc16-157">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="3bc16-158">Representa el identificador para una suscripción a.</span><span class="sxs-lookup"><span data-stu-id="3bc16-158">Represents the identifier for a subscription.</span></span>  <br/> |
|[<span data-ttu-id="3bc16-159">Marca de agua</span><span class="sxs-lookup"><span data-stu-id="3bc16-159">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="3bc16-160">Representa un marcador de evento en la cola de eventos de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="3bc16-160">Represents an event bookmark in the mailbox event queue.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3bc16-161">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3bc16-161">Parent elements</span></span>

|<span data-ttu-id="3bc16-162">**Element**</span><span class="sxs-lookup"><span data-stu-id="3bc16-162">**Element**</span></span>|<span data-ttu-id="3bc16-163">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3bc16-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3bc16-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3bc16-164">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="3bc16-165">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3bc16-165">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3bc16-166">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3bc16-166">Remarks</span></span>

<span data-ttu-id="3bc16-167">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="3bc16-167">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3bc16-168">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3bc16-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3bc16-169">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3bc16-169">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3bc16-170">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3bc16-170">Schema Name</span></span>  <br/> |<span data-ttu-id="3bc16-171">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3bc16-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3bc16-172">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3bc16-172">Validation File</span></span>  <br/> |<span data-ttu-id="3bc16-173">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3bc16-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3bc16-174">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3bc16-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="3bc16-175">False</span><span class="sxs-lookup"><span data-stu-id="3bc16-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3bc16-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="3bc16-176">See also</span></span>

- [<span data-ttu-id="3bc16-177">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="3bc16-177">Subscribe operation</span></span>](subscribe-operation.md)
- [<span data-ttu-id="3bc16-178">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="3bc16-178">GetEvents operation</span></span>](getevents-operation.md)
- [<span data-ttu-id="3bc16-179">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="3bc16-179">Unsubscribe operation</span></span>](unsubscribe-operation.md)

