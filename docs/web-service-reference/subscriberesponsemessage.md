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
description: El elemento SubscribeResponseMessage contiene el estado y el resultado de una única solicitud de operación subscribe.
ms.openlocfilehash: eea7356dbcf1887383d56e40a4f6dcd091535fa3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465376"
---
# <a name="subscriberesponsemessage"></a><span data-ttu-id="7da15-103">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7da15-103">SubscribeResponseMessage</span></span>

<span data-ttu-id="7da15-104">El elemento **SubscribeResponseMessage** contiene el estado y el resultado de una única solicitud de [operación subscribe](subscribe-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="7da15-104">The **SubscribeResponseMessage** element contains the status and result of a single [Subscribe operation](subscribe-operation.md) request.</span></span> 
  
- [<span data-ttu-id="7da15-105">SubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="7da15-105">SubscribeResponse</span></span>](subscriberesponse.md)
- [<span data-ttu-id="7da15-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7da15-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="7da15-107">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7da15-107">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md)
  
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

 <span data-ttu-id="7da15-108">**SubscribeResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="7da15-108">**SubscribeResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7da15-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7da15-109">Attributes and elements</span></span>

<span data-ttu-id="7da15-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7da15-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7da15-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="7da15-111">Attributes</span></span>

|<span data-ttu-id="7da15-112">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="7da15-112">**Attribute**</span></span>|<span data-ttu-id="7da15-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7da15-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7da15-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="7da15-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="7da15-115">Describe el estado de una respuesta de [operación de suscripción](subscribe-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="7da15-115">Describes the status of a [Subscribe operation](subscribe-operation.md) response.</span></span> <br/><br/><span data-ttu-id="7da15-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="7da15-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="7da15-117">-Correcto</span><span class="sxs-lookup"><span data-stu-id="7da15-117">-  Success</span></span>  <br/><span data-ttu-id="7da15-118">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="7da15-118">-  Warning</span></span>  <br/><span data-ttu-id="7da15-119">-Error</span><span class="sxs-lookup"><span data-stu-id="7da15-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="7da15-120">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="7da15-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="7da15-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7da15-121">**Value**</span></span>|<span data-ttu-id="7da15-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7da15-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7da15-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="7da15-123">**Success**</span></span> <br/> |<span data-ttu-id="7da15-124">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="7da15-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="7da15-125">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="7da15-125">**Warning**</span></span> <br/> | <span data-ttu-id="7da15-126">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="7da15-126">Describes a request that was not processed.</span></span> <span data-ttu-id="7da15-127">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="7da15-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="7da15-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="7da15-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="7da15-129">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="7da15-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="7da15-130">-Los servicios de dominio de Active Directory (AD DS) están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="7da15-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="7da15-131">-Se movieron los buzones.</span><span class="sxs-lookup"><span data-stu-id="7da15-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="7da15-132">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="7da15-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="7da15-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="7da15-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="7da15-134">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="7da15-134">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="7da15-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="7da15-135">**Error**</span></span> <br/> | <span data-ttu-id="7da15-136">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="7da15-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="7da15-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="7da15-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="7da15-138">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="7da15-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="7da15-139">-Atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="7da15-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="7da15-140">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="7da15-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="7da15-141">-Un atributo o elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="7da15-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="7da15-142">-Un intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="7da15-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="7da15-143">-Un error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="7da15-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="7da15-144">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="7da15-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7da15-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7da15-145">Child elements</span></span>

|<span data-ttu-id="7da15-146">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7da15-146">**Element**</span></span>|<span data-ttu-id="7da15-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7da15-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7da15-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="7da15-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="7da15-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7da15-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="7da15-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7da15-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="7da15-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7da15-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="7da15-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="7da15-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="7da15-153">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="7da15-153">Currently unused and reserved for future use.</span></span> <span data-ttu-id="7da15-154">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="7da15-154">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="7da15-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="7da15-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="7da15-156">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="7da15-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="7da15-157">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="7da15-157">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="7da15-158">Representa el identificador de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="7da15-158">Represents the identifier for a subscription.</span></span>  <br/> |
|[<span data-ttu-id="7da15-159">Watermark</span><span class="sxs-lookup"><span data-stu-id="7da15-159">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="7da15-160">Representa un marcador de evento en la cola de eventos del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="7da15-160">Represents an event bookmark in the mailbox event queue.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7da15-161">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7da15-161">Parent elements</span></span>

|<span data-ttu-id="7da15-162">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7da15-162">**Element**</span></span>|<span data-ttu-id="7da15-163">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7da15-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7da15-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7da15-164">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="7da15-165">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7da15-165">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7da15-166">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7da15-166">Remarks</span></span>

<span data-ttu-id="7da15-167">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="7da15-167">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7da15-168">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7da15-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7da15-169">Namespace</span><span class="sxs-lookup"><span data-stu-id="7da15-169">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7da15-170">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7da15-170">Schema Name</span></span>  <br/> |<span data-ttu-id="7da15-171">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="7da15-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7da15-172">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7da15-172">Validation File</span></span>  <br/> |<span data-ttu-id="7da15-173">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="7da15-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7da15-174">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7da15-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="7da15-175">Falso</span><span class="sxs-lookup"><span data-stu-id="7da15-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7da15-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="7da15-176">See also</span></span>

- [<span data-ttu-id="7da15-177">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="7da15-177">Subscribe operation</span></span>](subscribe-operation.md)
- [<span data-ttu-id="7da15-178">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="7da15-178">GetEvents operation</span></span>](getevents-operation.md)
- [<span data-ttu-id="7da15-179">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="7da15-179">Unsubscribe operation</span></span>](unsubscribe-operation.md)

