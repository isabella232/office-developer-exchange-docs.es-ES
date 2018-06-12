---
title: SendNotificationResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendNotificationResponseMessage
api_type:
- schema
ms.assetid: 2c6d681b-67ac-4331-bc6b-a2e709b638e3
description: El elemento SendNotificationResponseMessage contiene el estado y el resultado de una única solicitud de operación SendNotification.
ms.openlocfilehash: 49677b6d61f525b469679ec3fdcb8aadcca7239d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837348"
---
# <a name="sendnotificationresponsemessage"></a><span data-ttu-id="9a54a-103">SendNotificationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9a54a-103">SendNotificationResponseMessage</span></span>

<span data-ttu-id="9a54a-104">El elemento **SendNotificationResponseMessage** contiene el estado y el resultado de una única solicitud de operación **SendNotification** .</span><span class="sxs-lookup"><span data-stu-id="9a54a-104">The **SendNotificationResponseMessage** element contains the status and result of a single **SendNotification** operation request.</span></span> 
  
```xml
<SendNotificationResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Notification/>
</SendNotificationResponseMessage>
```

 <span data-ttu-id="9a54a-105">**SendNotificationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="9a54a-105">**SendNotificationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9a54a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9a54a-106">Attributes and elements</span></span>

<span data-ttu-id="9a54a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9a54a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9a54a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9a54a-108">Attributes</span></span>

|<span data-ttu-id="9a54a-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="9a54a-109">**Attribute**</span></span>|<span data-ttu-id="9a54a-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9a54a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9a54a-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="9a54a-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="9a54a-112">Describe el estado de una respuesta de la operación de **SendNotification** .</span><span class="sxs-lookup"><span data-stu-id="9a54a-112">Describes the status of a **SendNotification** operation response.</span></span> <br/><br/><span data-ttu-id="9a54a-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="9a54a-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="9a54a-114">-Éxito</span><span class="sxs-lookup"><span data-stu-id="9a54a-114">-  Success</span></span>  <br/><span data-ttu-id="9a54a-115">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="9a54a-115">-  Warning</span></span>  <br/><span data-ttu-id="9a54a-116">-Error</span><span class="sxs-lookup"><span data-stu-id="9a54a-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="9a54a-117">Atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="9a54a-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="9a54a-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9a54a-118">**Value**</span></span>|<span data-ttu-id="9a54a-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9a54a-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9a54a-120">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="9a54a-120">**Success**</span></span> <br/> |<span data-ttu-id="9a54a-121">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="9a54a-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="9a54a-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="9a54a-122">**Warning**</span></span> <br/> | <span data-ttu-id="9a54a-123">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="9a54a-123">Describes a request that was not processed.</span></span> <span data-ttu-id="9a54a-124">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="9a54a-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="9a54a-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="9a54a-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="9a54a-126">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="9a54a-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="9a54a-127">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="9a54a-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="9a54a-128">-Se mueven los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="9a54a-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="9a54a-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="9a54a-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="9a54a-130">-Una contraseña ha caducado.</span><span class="sxs-lookup"><span data-stu-id="9a54a-130">-  A password has expired.</span></span>  <br/><span data-ttu-id="9a54a-131">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="9a54a-131">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="9a54a-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="9a54a-132">**Error**</span></span> <br/> | <span data-ttu-id="9a54a-133">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="9a54a-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="9a54a-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="9a54a-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="9a54a-135">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="9a54a-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="9a54a-136">-Los atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="9a54a-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="9a54a-137">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="9a54a-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="9a54a-138">-De atributo o elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="9a54a-138">-  Attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="9a54a-139">-Un intento de acceso no autorizado por cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="9a54a-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="9a54a-140">-Un error del lado del servidor en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="9a54a-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="9a54a-141">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="9a54a-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9a54a-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9a54a-142">Child elements</span></span>

|<span data-ttu-id="9a54a-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="9a54a-143">**Element**</span></span>|<span data-ttu-id="9a54a-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9a54a-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9a54a-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="9a54a-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="9a54a-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9a54a-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="9a54a-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9a54a-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="9a54a-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9a54a-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="9a54a-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="9a54a-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="9a54a-150">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="9a54a-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="9a54a-151">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="9a54a-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="9a54a-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="9a54a-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="9a54a-153">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="9a54a-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="9a54a-154">Notificación</span><span class="sxs-lookup"><span data-stu-id="9a54a-154">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="9a54a-155">Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="9a54a-155">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9a54a-156">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9a54a-156">Parent elements</span></span>

|<span data-ttu-id="9a54a-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="9a54a-157">**Element**</span></span>|<span data-ttu-id="9a54a-158">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9a54a-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9a54a-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9a54a-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="9a54a-160">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9a54a-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9a54a-161">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="9a54a-161">Text value</span></span>

<span data-ttu-id="9a54a-162">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9a54a-162">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9a54a-163">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a54a-163">Remarks</span></span>

<span data-ttu-id="9a54a-164">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="9a54a-164">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9a54a-165">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9a54a-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a54a-166">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9a54a-166">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9a54a-167">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9a54a-167">Schema Name</span></span>  <br/> |<span data-ttu-id="9a54a-168">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="9a54a-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9a54a-169">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9a54a-169">Validation File</span></span>  <br/> |<span data-ttu-id="9a54a-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9a54a-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9a54a-171">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9a54a-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="9a54a-172">False</span><span class="sxs-lookup"><span data-stu-id="9a54a-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9a54a-173">Ver también</span><span class="sxs-lookup"><span data-stu-id="9a54a-173">See also</span></span>

- [<span data-ttu-id="9a54a-174">SendNotification</span><span class="sxs-lookup"><span data-stu-id="9a54a-174">SendNotification</span></span>](sendnotification.md)
- [<span data-ttu-id="9a54a-175">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="9a54a-175">Subscribe operation</span></span>](subscribe-operation.md)
- [<span data-ttu-id="9a54a-176">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="9a54a-176">Unsubscribe operation</span></span>](unsubscribe-operation.md)

