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
ms.lasthandoff: 06/21/2018
ms.locfileid: "19837348"
---
# <a name="sendnotificationresponsemessage"></a><span data-ttu-id="700ee-103">SendNotificationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="700ee-103">SendNotificationResponseMessage</span></span>

<span data-ttu-id="700ee-104">El elemento **SendNotificationResponseMessage** contiene el estado y el resultado de una única solicitud de operación **SendNotification** .</span><span class="sxs-lookup"><span data-stu-id="700ee-104">The **SendNotificationResponseMessage** element contains the status and result of a single **SendNotification** operation request.</span></span> 
  
```xml
<SendNotificationResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Notification/>
</SendNotificationResponseMessage>
```

 <span data-ttu-id="700ee-105">**SendNotificationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="700ee-105">**SendNotificationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="700ee-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="700ee-106">Attributes and elements</span></span>

<span data-ttu-id="700ee-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="700ee-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="700ee-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="700ee-108">Attributes</span></span>

|<span data-ttu-id="700ee-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="700ee-109">**Attribute**</span></span>|<span data-ttu-id="700ee-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="700ee-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="700ee-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="700ee-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="700ee-112">Describe el estado de una respuesta de la operación de **SendNotification** .</span><span class="sxs-lookup"><span data-stu-id="700ee-112">Describes the status of a **SendNotification** operation response.</span></span> <br/><br/><span data-ttu-id="700ee-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="700ee-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="700ee-114">-Éxito</span><span class="sxs-lookup"><span data-stu-id="700ee-114">-  Success</span></span>  <br/><span data-ttu-id="700ee-115">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="700ee-115">-  Warning</span></span>  <br/><span data-ttu-id="700ee-116">-Error</span><span class="sxs-lookup"><span data-stu-id="700ee-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="700ee-117">Atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="700ee-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="700ee-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="700ee-118">**Value**</span></span>|<span data-ttu-id="700ee-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="700ee-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="700ee-120">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="700ee-120">**Success**</span></span> <br/> |<span data-ttu-id="700ee-121">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="700ee-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="700ee-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="700ee-122">**Warning**</span></span> <br/> | <span data-ttu-id="700ee-123">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="700ee-123">Describes a request that was not processed.</span></span> <span data-ttu-id="700ee-124">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="700ee-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="700ee-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="700ee-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="700ee-126">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="700ee-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="700ee-127">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="700ee-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="700ee-128">-Se mueven los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="700ee-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="700ee-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="700ee-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="700ee-130">-Una contraseña ha caducado.</span><span class="sxs-lookup"><span data-stu-id="700ee-130">-  A password has expired.</span></span>  <br/><span data-ttu-id="700ee-131">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="700ee-131">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="700ee-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="700ee-132">**Error**</span></span> <br/> | <span data-ttu-id="700ee-133">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="700ee-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="700ee-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="700ee-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="700ee-135">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="700ee-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="700ee-136">-Los atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="700ee-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="700ee-137">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="700ee-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="700ee-138">-De atributo o elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="700ee-138">-  Attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="700ee-139">-Un intento de acceso no autorizado por cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="700ee-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="700ee-140">-Un error del lado del servidor en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="700ee-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="700ee-141">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="700ee-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="700ee-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="700ee-142">Child elements</span></span>

|<span data-ttu-id="700ee-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="700ee-143">**Element**</span></span>|<span data-ttu-id="700ee-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="700ee-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="700ee-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="700ee-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="700ee-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="700ee-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="700ee-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="700ee-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="700ee-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="700ee-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="700ee-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="700ee-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="700ee-150">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="700ee-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="700ee-151">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="700ee-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="700ee-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="700ee-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="700ee-153">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="700ee-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="700ee-154">Notificación</span><span class="sxs-lookup"><span data-stu-id="700ee-154">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="700ee-155">Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="700ee-155">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="700ee-156">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="700ee-156">Parent elements</span></span>

|<span data-ttu-id="700ee-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="700ee-157">**Element**</span></span>|<span data-ttu-id="700ee-158">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="700ee-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="700ee-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="700ee-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="700ee-160">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="700ee-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="700ee-161">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="700ee-161">Text value</span></span>

<span data-ttu-id="700ee-162">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="700ee-162">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="700ee-163">Comentarios</span><span class="sxs-lookup"><span data-stu-id="700ee-163">Remarks</span></span>

<span data-ttu-id="700ee-164">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="700ee-164">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="700ee-165">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="700ee-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="700ee-166">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="700ee-166">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="700ee-167">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="700ee-167">Schema Name</span></span>  <br/> |<span data-ttu-id="700ee-168">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="700ee-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="700ee-169">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="700ee-169">Validation File</span></span>  <br/> |<span data-ttu-id="700ee-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="700ee-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="700ee-171">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="700ee-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="700ee-172">False</span><span class="sxs-lookup"><span data-stu-id="700ee-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="700ee-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="700ee-173">See also</span></span>

- [<span data-ttu-id="700ee-174">SendNotification</span><span class="sxs-lookup"><span data-stu-id="700ee-174">SendNotification</span></span>](sendnotification.md)
- [<span data-ttu-id="700ee-175">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="700ee-175">Subscribe operation</span></span>](subscribe-operation.md)
- [<span data-ttu-id="700ee-176">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="700ee-176">Unsubscribe operation</span></span>](unsubscribe-operation.md)

