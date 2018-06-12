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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837621"
---
# <a name="subscriberesponsemessage"></a><span data-ttu-id="2dbf6-103">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2dbf6-103">SubscribeResponseMessage</span></span>

<span data-ttu-id="2dbf6-104">El elemento **SubscribeResponseMessage** contiene el estado y el resultado de una única solicitud [Subscribe operación](subscribe-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="2dbf6-104">The **SubscribeResponseMessage** element contains the status and result of a single [Subscribe operation](subscribe-operation.md) request.</span></span> 
  
- [<span data-ttu-id="2dbf6-105">SubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="2dbf6-105">SubscribeResponse</span></span>](subscriberesponse.md)
- [<span data-ttu-id="2dbf6-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2dbf6-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="2dbf6-107">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2dbf6-107">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md)
  
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

 <span data-ttu-id="2dbf6-108">**SubscribeResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2dbf6-108">**SubscribeResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2dbf6-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2dbf6-109">Attributes and elements</span></span>

<span data-ttu-id="2dbf6-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2dbf6-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2dbf6-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="2dbf6-111">Attributes</span></span>

|<span data-ttu-id="2dbf6-112">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="2dbf6-112">**Attribute**</span></span>|<span data-ttu-id="2dbf6-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2dbf6-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2dbf6-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="2dbf6-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="2dbf6-115">Describe el estado de una respuesta de [la operación Suscribir](subscribe-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="2dbf6-115">Describes the status of a [Subscribe operation](subscribe-operation.md) response.</span></span> <br/><br/><span data-ttu-id="2dbf6-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="2dbf6-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="2dbf6-117">-Éxito</span><span class="sxs-lookup"><span data-stu-id="2dbf6-117">-  Success</span></span>  <br/><span data-ttu-id="2dbf6-118">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="2dbf6-118">-  Warning</span></span>  <br/><span data-ttu-id="2dbf6-119">-Error</span><span class="sxs-lookup"><span data-stu-id="2dbf6-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="2dbf6-120">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="2dbf6-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="2dbf6-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2dbf6-121">**Value**</span></span>|<span data-ttu-id="2dbf6-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2dbf6-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2dbf6-123">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="2dbf6-123">**Success**</span></span> <br/> |<span data-ttu-id="2dbf6-124">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="2dbf6-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="2dbf6-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="2dbf6-125">**Warning**</span></span> <br/> | <span data-ttu-id="2dbf6-126">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="2dbf6-126">Describes a request that was not processed.</span></span> <span data-ttu-id="2dbf6-127">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="2dbf6-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="2dbf6-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="2dbf6-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="2dbf6-129">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="2dbf6-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="2dbf6-130">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="2dbf6-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="2dbf6-131">-Buzones se han movido.</span><span class="sxs-lookup"><span data-stu-id="2dbf6-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="2dbf6-132">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="2dbf6-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="2dbf6-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="2dbf6-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="2dbf6-134">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="2dbf6-134">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="2dbf6-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="2dbf6-135">**Error**</span></span> <br/> | <span data-ttu-id="2dbf6-136">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="2dbf6-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="2dbf6-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="2dbf6-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="2dbf6-138">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="2dbf6-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="2dbf6-139">-Los atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="2dbf6-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="2dbf6-140">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="2dbf6-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="2dbf6-141">-Un atributo o un elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="2dbf6-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="2dbf6-142">-Un intento de acceso no autorizado por cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="2dbf6-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="2dbf6-143">-Un error del lado del servidor en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="2dbf6-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="2dbf6-144">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="2dbf6-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2dbf6-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2dbf6-145">Child elements</span></span>

|<span data-ttu-id="2dbf6-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="2dbf6-146">**Element**</span></span>|<span data-ttu-id="2dbf6-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2dbf6-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2dbf6-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="2dbf6-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="2dbf6-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2dbf6-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="2dbf6-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2dbf6-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="2dbf6-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2dbf6-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="2dbf6-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2dbf6-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="2dbf6-153">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="2dbf6-153">Currently unused and reserved for future use.</span></span> <span data-ttu-id="2dbf6-154">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="2dbf6-154">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="2dbf6-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="2dbf6-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="2dbf6-156">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="2dbf6-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="2dbf6-157">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="2dbf6-157">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="2dbf6-158">Representa el identificador para una suscripción a.</span><span class="sxs-lookup"><span data-stu-id="2dbf6-158">Represents the identifier for a subscription.</span></span>  <br/> |
|[<span data-ttu-id="2dbf6-159">Marca de agua</span><span class="sxs-lookup"><span data-stu-id="2dbf6-159">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="2dbf6-160">Representa un marcador de evento en la cola de eventos de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="2dbf6-160">Represents an event bookmark in the mailbox event queue.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2dbf6-161">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2dbf6-161">Parent elements</span></span>

|<span data-ttu-id="2dbf6-162">**Element**</span><span class="sxs-lookup"><span data-stu-id="2dbf6-162">**Element**</span></span>|<span data-ttu-id="2dbf6-163">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2dbf6-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2dbf6-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2dbf6-164">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="2dbf6-165">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2dbf6-165">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2dbf6-166">Notas</span><span class="sxs-lookup"><span data-stu-id="2dbf6-166">Remarks</span></span>

<span data-ttu-id="2dbf6-167">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="2dbf6-167">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2dbf6-168">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2dbf6-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2dbf6-169">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2dbf6-169">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2dbf6-170">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2dbf6-170">Schema Name</span></span>  <br/> |<span data-ttu-id="2dbf6-171">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="2dbf6-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2dbf6-172">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2dbf6-172">Validation File</span></span>  <br/> |<span data-ttu-id="2dbf6-173">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2dbf6-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2dbf6-174">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2dbf6-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="2dbf6-175">False</span><span class="sxs-lookup"><span data-stu-id="2dbf6-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2dbf6-176">Ver también</span><span class="sxs-lookup"><span data-stu-id="2dbf6-176">See also</span></span>

- [<span data-ttu-id="2dbf6-177">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="2dbf6-177">Subscribe operation</span></span>](subscribe-operation.md)
- [<span data-ttu-id="2dbf6-178">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="2dbf6-178">GetEvents operation</span></span>](getevents-operation.md)
- [<span data-ttu-id="2dbf6-179">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="2dbf6-179">Unsubscribe operation</span></span>](unsubscribe-operation.md)

