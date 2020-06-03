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
description: El elemento FindItemResponseMessage contiene el estado y el resultado de una sola solicitud de operación FindItem.
ms.openlocfilehash: ca941e0c7e5b9b08f6f495ccae0d634d72b8f429
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462538"
---
# <a name="finditemresponsemessage"></a><span data-ttu-id="bb60e-103">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bb60e-103">FindItemResponseMessage</span></span>

<span data-ttu-id="bb60e-104">El elemento **FindItemResponseMessage** contiene el estado y el resultado de una sola solicitud de [operación FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="bb60e-104">The **FindItemResponseMessage** element contains the status and result of a single [FindItem operation](finditem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="bb60e-105">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="bb60e-105">FindItemResponse</span></span>](finditemresponse.md) 
- [<span data-ttu-id="bb60e-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="bb60e-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="bb60e-107">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bb60e-107">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
  
```xml
<FindItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RootFolder/>
</FindItemResponseMessage>
```

 <span data-ttu-id="bb60e-108">**FindItemResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="bb60e-108">**FindItemResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bb60e-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bb60e-109">Attributes and elements</span></span>

<span data-ttu-id="bb60e-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bb60e-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bb60e-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="bb60e-111">Attributes</span></span>

|<span data-ttu-id="bb60e-112">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="bb60e-112">**Attribute**</span></span>|<span data-ttu-id="bb60e-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bb60e-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bb60e-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="bb60e-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="bb60e-115">Describe el estado de una respuesta de la [operación FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="bb60e-115">Describes the status of a [FindItem operation](finditem-operation.md) response.</span></span><br/><br/> <span data-ttu-id="bb60e-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="bb60e-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="bb60e-117">-Correcto</span><span class="sxs-lookup"><span data-stu-id="bb60e-117">-  Success</span></span>  <br/><span data-ttu-id="bb60e-118">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="bb60e-118">-  Warning</span></span>  <br/><span data-ttu-id="bb60e-119">-Error</span><span class="sxs-lookup"><span data-stu-id="bb60e-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="bb60e-120">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="bb60e-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="bb60e-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="bb60e-121">**Value**</span></span>|<span data-ttu-id="bb60e-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bb60e-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bb60e-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="bb60e-123">**Success**</span></span> <br/> |<span data-ttu-id="bb60e-124">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="bb60e-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="bb60e-125">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="bb60e-125">**Warning**</span></span> <br/> | <span data-ttu-id="bb60e-126">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="bb60e-126">Describes a request that was not processed.</span></span> <span data-ttu-id="bb60e-127">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud que se estaba procesando y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="bb60e-127">A warning may be returned if an error occurred while processing an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="bb60e-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="bb60e-128">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="bb60e-129">-El almacén de Exchange se desconecta durante el lote.</span><span class="sxs-lookup"><span data-stu-id="bb60e-129">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="bb60e-130">-Servicios de dominio de Active Directory (AD DS) se desconecta.</span><span class="sxs-lookup"><span data-stu-id="bb60e-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="bb60e-131">-Se mueven los buzones.</span><span class="sxs-lookup"><span data-stu-id="bb60e-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="bb60e-132">-La base de datos de mensajes (MDB) se desconecta.</span><span class="sxs-lookup"><span data-stu-id="bb60e-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="bb60e-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="bb60e-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="bb60e-134">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="bb60e-134">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="bb60e-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="bb60e-135">**Error**</span></span> <br/> | <span data-ttu-id="bb60e-136">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="bb60e-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="bb60e-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="bb60e-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="bb60e-138">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="bb60e-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="bb60e-139">-Atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="bb60e-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="bb60e-140">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="bb60e-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="bb60e-141">-Un atributo o elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="bb60e-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="bb60e-142">-Un intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="bb60e-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="bb60e-143">-Un error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="bb60e-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="bb60e-144">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="bb60e-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bb60e-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bb60e-145">Child elements</span></span>

|<span data-ttu-id="bb60e-146">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bb60e-146">**Element**</span></span>|<span data-ttu-id="bb60e-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bb60e-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb60e-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="bb60e-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="bb60e-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bb60e-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="bb60e-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="bb60e-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="bb60e-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bb60e-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="bb60e-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="bb60e-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="bb60e-153">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="bb60e-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="bb60e-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="bb60e-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="bb60e-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="bb60e-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="bb60e-156">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="bb60e-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="bb60e-157">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="bb60e-157">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md) <br/> |<span data-ttu-id="bb60e-158">Contiene los resultados de una búsqueda de una carpeta raíz única durante una [operación FindItem](finditem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="bb60e-158">Contains the results from a search of a single root folder during a [FindItem operation](finditem-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bb60e-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bb60e-159">Parent elements</span></span>

|<span data-ttu-id="bb60e-160">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bb60e-160">**Element**</span></span>|<span data-ttu-id="bb60e-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bb60e-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb60e-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="bb60e-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="bb60e-163">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="bb60e-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb60e-164">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb60e-164">Remarks</span></span>

<span data-ttu-id="bb60e-165">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="bb60e-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bb60e-166">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bb60e-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb60e-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="bb60e-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bb60e-168">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="bb60e-168">Schema name</span></span>  <br/> |<span data-ttu-id="bb60e-169">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="bb60e-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bb60e-170">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="bb60e-170">Validation file</span></span>  <br/> |<span data-ttu-id="bb60e-171">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="bb60e-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bb60e-172">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="bb60e-172">Can be empty</span></span>  <br/> |<span data-ttu-id="bb60e-173">Falso</span><span class="sxs-lookup"><span data-stu-id="bb60e-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bb60e-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb60e-174">See also</span></span>

- [<span data-ttu-id="bb60e-175">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="bb60e-175">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="bb60e-176">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="bb60e-176">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

