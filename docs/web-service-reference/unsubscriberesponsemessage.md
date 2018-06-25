---
title: UnsubscribeResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnsubscribeResponseMessage
api_type:
- schema
ms.assetid: 92c53b13-0ca1-4b44-b925-b23682e9417c
description: El elemento UnsubscribeResponseMessage contiene el estado y el resultado de una única solicitud de la operación de cancelación de suscripción.
ms.openlocfilehash: 09475b8c858ddcd0e404819b6b9a281cbf7cfcbb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840802"
---
# <a name="unsubscriberesponsemessage"></a><span data-ttu-id="f0c33-103">UnsubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f0c33-103">UnsubscribeResponseMessage</span></span>

<span data-ttu-id="f0c33-104">El elemento **UnsubscribeResponseMessage** contiene el estado y el resultado de una única solicitud de [operación de cancelación de suscripción](unsubscribe-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="f0c33-104">The **UnsubscribeResponseMessage** element contains the status and result of a single [Unsubscribe operation](unsubscribe-operation.md) request.</span></span> 
  
- [<span data-ttu-id="f0c33-105">UnsubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="f0c33-105">UnsubscribeResponse</span></span>](unsubscriberesponse.md)
- [<span data-ttu-id="f0c33-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f0c33-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="f0c33-107">UnsubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f0c33-107">UnsubscribeResponseMessage</span></span>](unsubscriberesponsemessage.md)
  
```xml
<UnsubscribeResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</UnsubscribeResponseMessage>
```

 <span data-ttu-id="f0c33-108">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f0c33-108">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f0c33-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f0c33-109">Attributes and elements</span></span>

<span data-ttu-id="f0c33-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f0c33-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f0c33-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="f0c33-111">Attributes</span></span>

|<span data-ttu-id="f0c33-112">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="f0c33-112">**Attribute**</span></span>|<span data-ttu-id="f0c33-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f0c33-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f0c33-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="f0c33-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="f0c33-115">Describe el estado de una respuesta de la [operación de cancelación de suscripción](unsubscribe-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="f0c33-115">Describes the status of an [Unsubscribe operation](unsubscribe-operation.md) response.</span></span> <br/><br/><span data-ttu-id="f0c33-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="f0c33-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="f0c33-117">-Éxito</span><span class="sxs-lookup"><span data-stu-id="f0c33-117">-  Success</span></span>  <br/><span data-ttu-id="f0c33-118">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="f0c33-118">-  Warning</span></span>  <br/><span data-ttu-id="f0c33-119">-Error</span><span class="sxs-lookup"><span data-stu-id="f0c33-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="f0c33-120">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="f0c33-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="f0c33-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f0c33-121">**Value**</span></span>|<span data-ttu-id="f0c33-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f0c33-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f0c33-123">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="f0c33-123">**Success**</span></span> <br/> |<span data-ttu-id="f0c33-124">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="f0c33-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="f0c33-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="f0c33-125">**Warning**</span></span> <br/> | <span data-ttu-id="f0c33-126">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="f0c33-126">Describes a request that was not processed.</span></span> <span data-ttu-id="f0c33-127">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="f0c33-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="f0c33-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="f0c33-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="f0c33-129">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="f0c33-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="f0c33-130">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="f0c33-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="f0c33-131">-Se mueven los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="f0c33-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="f0c33-132">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="f0c33-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="f0c33-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="f0c33-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="f0c33-134">-Se ha excedido una cuota.</span><span class="sxs-lookup"><span data-stu-id="f0c33-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="f0c33-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="f0c33-135">**Error**</span></span> <br/> | <span data-ttu-id="f0c33-136">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="f0c33-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="f0c33-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="f0c33-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="f0c33-138">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="f0c33-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="f0c33-139">-Los atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="f0c33-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="f0c33-140">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="f0c33-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="f0c33-141">-De atributo o elemento no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="f0c33-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="f0c33-142">-Intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="f0c33-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="f0c33-143">-Error server-side en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="f0c33-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="f0c33-144">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="f0c33-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f0c33-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f0c33-145">Child elements</span></span>

|<span data-ttu-id="f0c33-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="f0c33-146">**Element**</span></span>|<span data-ttu-id="f0c33-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f0c33-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f0c33-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="f0c33-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="f0c33-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f0c33-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="f0c33-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f0c33-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="f0c33-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f0c33-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="f0c33-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f0c33-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="f0c33-153">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="f0c33-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="f0c33-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="f0c33-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="f0c33-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="f0c33-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="f0c33-156">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="f0c33-156">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f0c33-157">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f0c33-157">Parent elements</span></span>

|<span data-ttu-id="f0c33-158">**Element**</span><span class="sxs-lookup"><span data-stu-id="f0c33-158">**Element**</span></span>|<span data-ttu-id="f0c33-159">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f0c33-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f0c33-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f0c33-160">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="f0c33-161">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f0c33-161">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0c33-162">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f0c33-162">Remarks</span></span>

<span data-ttu-id="f0c33-163">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="f0c33-163">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f0c33-164">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f0c33-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f0c33-165">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f0c33-165">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f0c33-166">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f0c33-166">Schema Name</span></span>  <br/> |<span data-ttu-id="f0c33-167">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="f0c33-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f0c33-168">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f0c33-168">Validation File</span></span>  <br/> |<span data-ttu-id="f0c33-169">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f0c33-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f0c33-170">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f0c33-170">Can be Empty</span></span>  <br/> |<span data-ttu-id="f0c33-171">False</span><span class="sxs-lookup"><span data-stu-id="f0c33-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f0c33-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0c33-172">See also</span></span>

- [<span data-ttu-id="f0c33-173">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="f0c33-173">Unsubscribe operation</span></span>](unsubscribe-operation.md)
- [<span data-ttu-id="f0c33-174">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f0c33-174">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

