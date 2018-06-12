---
title: FindItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindItemResponseMessage
api_type:
- schema
ms.assetid: fb2cd399-8a04-4f26-9091-993134ed1d15
description: El elemento FindItemResponseMessage contiene el estado y el resultado de una única solicitud de operación FindItem.
ms.openlocfilehash: 0a4bfb3ba8d85b0bff0d03f043be865ce7276229
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764636"
---
# <a name="finditemresponsemessage"></a><span data-ttu-id="ef620-103">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ef620-103">FindItemResponseMessage</span></span>

<span data-ttu-id="ef620-104">El elemento **FindItemResponseMessage** contiene el estado y el resultado de una única solicitud de [operación FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="ef620-104">The **FindItemResponseMessage** element contains the status and result of a single [FindItem operation](finditem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="ef620-105">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="ef620-105">FindItemResponse</span></span>](finditemresponse.md) 
- [<span data-ttu-id="ef620-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ef620-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="ef620-107">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ef620-107">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
  
```xml
<FindItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RootFolder/>
</FindItemResponseMessage>
```

 <span data-ttu-id="ef620-108">**FindItemResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ef620-108">**FindItemResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ef620-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ef620-109">Attributes and elements</span></span>

<span data-ttu-id="ef620-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ef620-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef620-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="ef620-111">Attributes</span></span>

|<span data-ttu-id="ef620-112">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="ef620-112">**Attribute**</span></span>|<span data-ttu-id="ef620-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ef620-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ef620-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="ef620-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="ef620-115">Describe el estado de una respuesta de [la operación FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="ef620-115">Describes the status of a [FindItem operation](finditem-operation.md) response.</span></span><br/><br/> <span data-ttu-id="ef620-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="ef620-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="ef620-117">-Éxito</span><span class="sxs-lookup"><span data-stu-id="ef620-117">-  Success</span></span>  <br/><span data-ttu-id="ef620-118">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="ef620-118">-  Warning</span></span>  <br/><span data-ttu-id="ef620-119">-Error</span><span class="sxs-lookup"><span data-stu-id="ef620-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="ef620-120">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="ef620-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="ef620-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ef620-121">**Value**</span></span>|<span data-ttu-id="ef620-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ef620-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ef620-123">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="ef620-123">**Success**</span></span> <br/> |<span data-ttu-id="ef620-124">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="ef620-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="ef620-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="ef620-125">**Warning**</span></span> <br/> | <span data-ttu-id="ef620-126">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="ef620-126">Describes a request that was not processed.</span></span> <span data-ttu-id="ef620-127">Es posible que se devuelve una advertencia si se produjo un error mientras estaba procesando el procesamiento de un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="ef620-127">A warning may be returned if an error occurred while processing an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="ef620-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="ef620-128">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="ef620-129">-El almacén de Exchange se desconecta durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="ef620-129">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="ef620-130">-Los servicios de dominio de Active Directory (AD DS) se queda sin conexión.</span><span class="sxs-lookup"><span data-stu-id="ef620-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="ef620-131">-Se mueven los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="ef620-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="ef620-132">-La base de datos de mensajes (MDB) se queda sin conexión.</span><span class="sxs-lookup"><span data-stu-id="ef620-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="ef620-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="ef620-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="ef620-134">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="ef620-134">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="ef620-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="ef620-135">**Error**</span></span> <br/> | <span data-ttu-id="ef620-136">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="ef620-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="ef620-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="ef620-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="ef620-138">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="ef620-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="ef620-139">-Los atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="ef620-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="ef620-140">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="ef620-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="ef620-141">-Un atributo o un elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="ef620-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="ef620-142">-Un intento de acceso no autorizado por cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="ef620-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="ef620-143">-Un error del lado del servidor en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="ef620-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="ef620-144">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="ef620-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ef620-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ef620-145">Child elements</span></span>

|<span data-ttu-id="ef620-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="ef620-146">**Element**</span></span>|<span data-ttu-id="ef620-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ef620-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef620-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="ef620-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="ef620-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ef620-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="ef620-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ef620-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="ef620-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ef620-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="ef620-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ef620-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="ef620-153">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="ef620-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="ef620-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="ef620-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="ef620-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="ef620-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="ef620-156">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="ef620-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="ef620-157">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="ef620-157">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md) <br/> |<span data-ttu-id="ef620-158">Contiene los resultados de una búsqueda de una sola carpeta raíz durante una [operación de FindItem](finditem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="ef620-158">Contains the results from a search of a single root folder during a [FindItem operation](finditem-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ef620-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ef620-159">Parent elements</span></span>

|<span data-ttu-id="ef620-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="ef620-160">**Element**</span></span>|<span data-ttu-id="ef620-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ef620-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef620-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ef620-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="ef620-163">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ef620-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef620-164">Notas</span><span class="sxs-lookup"><span data-stu-id="ef620-164">Remarks</span></span>

<span data-ttu-id="ef620-165">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="ef620-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef620-166">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ef620-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef620-167">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ef620-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ef620-168">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ef620-168">Schema name</span></span>  <br/> |<span data-ttu-id="ef620-169">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ef620-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ef620-170">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ef620-170">Validation file</span></span>  <br/> |<span data-ttu-id="ef620-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ef620-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ef620-172">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ef620-172">Can be empty</span></span>  <br/> |<span data-ttu-id="ef620-173">False</span><span class="sxs-lookup"><span data-stu-id="ef620-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ef620-174">Ver también</span><span class="sxs-lookup"><span data-stu-id="ef620-174">See also</span></span>

- [<span data-ttu-id="ef620-175">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="ef620-175">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="ef620-176">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="ef620-176">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

