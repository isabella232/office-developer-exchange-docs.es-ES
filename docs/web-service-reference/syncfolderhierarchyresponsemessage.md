---
title: SyncFolderHierarchyResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderHierarchyResponseMessage
api_type:
- schema
ms.assetid: ab96c649-1005-401c-9d1c-9917f0b19a60
description: El elemento SyncFolderHierarchyResponseMessage contiene el estado y el resultado de una única solicitud de operación SyncFolderHierarchy.
ms.openlocfilehash: e4141299b128ffb7f67c55bbb09390b77a79e043
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840613"
---
# <a name="syncfolderhierarchyresponsemessage"></a><span data-ttu-id="7d58e-103">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7d58e-103">SyncFolderHierarchyResponseMessage</span></span>

<span data-ttu-id="7d58e-104">El elemento **SyncFolderHierarchyResponseMessage** contiene el estado y el resultado de una única solicitud de [operación SyncFolderHierarchy](syncfolderhierarchy-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="7d58e-104">The **SyncFolderHierarchyResponseMessage** element contains the status and result of a single [SyncFolderHierarchy operation](syncfolderhierarchy-operation.md) request.</span></span> 
  
- [<span data-ttu-id="7d58e-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="7d58e-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md) 
- [<span data-ttu-id="7d58e-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7d58e-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="7d58e-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7d58e-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
  
```xml
<SyncFolderHierarchyResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <SyncState/>
   <IncludesLastFolderInRange/>
   <Changes/>
</SyncFolderHierarchyResponseMessage>
```

 <span data-ttu-id="7d58e-108">**SyncFolderHierarchyResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="7d58e-108">**SyncFolderHierarchyResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7d58e-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7d58e-109">Attributes and elements</span></span>

<span data-ttu-id="7d58e-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7d58e-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7d58e-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="7d58e-111">Attributes</span></span>

|<span data-ttu-id="7d58e-112">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="7d58e-112">**Attribute**</span></span>|<span data-ttu-id="7d58e-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7d58e-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7d58e-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="7d58e-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="7d58e-115">Describe el estado de una respuesta de [la operación SyncFolderHierarchy](syncfolderhierarchy-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="7d58e-115">Describes the status of a [SyncFolderHierarchy operation](syncfolderhierarchy-operation.md) response.</span></span> <br/><br/><span data-ttu-id="7d58e-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="7d58e-116">The following values are valid for this attribute:</span></span><br/>  <br/><span data-ttu-id="7d58e-117">-Éxito</span><span class="sxs-lookup"><span data-stu-id="7d58e-117">-  Success</span></span>  <br/><span data-ttu-id="7d58e-118">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="7d58e-118">-  Warning</span></span>  <br/><span data-ttu-id="7d58e-119">-Error</span><span class="sxs-lookup"><span data-stu-id="7d58e-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="7d58e-120">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="7d58e-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="7d58e-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7d58e-121">**Value**</span></span>|<span data-ttu-id="7d58e-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7d58e-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7d58e-123">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="7d58e-123">**Success**</span></span> <br/> |<span data-ttu-id="7d58e-124">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="7d58e-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="7d58e-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="7d58e-125">**Warning**</span></span> <br/> | <span data-ttu-id="7d58e-126">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="7d58e-126">Describes a request that was not processed.</span></span> <span data-ttu-id="7d58e-127">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="7d58e-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="7d58e-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="7d58e-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="7d58e-129">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="7d58e-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="7d58e-130">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="7d58e-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="7d58e-131">-Buzones se han movido.</span><span class="sxs-lookup"><span data-stu-id="7d58e-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="7d58e-132">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="7d58e-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="7d58e-133">-Una contraseña ha caducado.</span><span class="sxs-lookup"><span data-stu-id="7d58e-133">-  A password has expired.</span></span>  <br/><span data-ttu-id="7d58e-134">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="7d58e-134">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="7d58e-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="7d58e-135">**Error**</span></span> <br/> | <span data-ttu-id="7d58e-136">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="7d58e-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="7d58e-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="7d58e-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="7d58e-138">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="7d58e-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="7d58e-139">-Los atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="7d58e-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="7d58e-140">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="7d58e-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="7d58e-141">-Un atributo o un elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="7d58e-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="7d58e-142">-Un intento de acceso no autorizado por cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="7d58e-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="7d58e-143">-Un error del lado del servidor en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="7d58e-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="7d58e-144">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="7d58e-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7d58e-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7d58e-145">Child elements</span></span>

|<span data-ttu-id="7d58e-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="7d58e-146">**Element**</span></span>|<span data-ttu-id="7d58e-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7d58e-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7d58e-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="7d58e-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="7d58e-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7d58e-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="7d58e-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7d58e-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="7d58e-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7d58e-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="7d58e-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="7d58e-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="7d58e-153">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="7d58e-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="7d58e-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="7d58e-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="7d58e-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="7d58e-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="7d58e-156">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="7d58e-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="7d58e-157">Estado de sincronización</span><span class="sxs-lookup"><span data-stu-id="7d58e-157">SyncState</span></span>](syncstate-ex15websvcsotherref.md) <br/> |<span data-ttu-id="7d58e-158">Contiene un formulario con codificación base64 de los datos de sincronización que se actualizan después de cada solicitud realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="7d58e-158">Contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="7d58e-159">Esto se usa para identificar el estado de sincronización.</span><span class="sxs-lookup"><span data-stu-id="7d58e-159">This is used to identify the synchronization state.</span></span>  <br/> |
|[<span data-ttu-id="7d58e-160">IncludesLastFolderInRange</span><span class="sxs-lookup"><span data-stu-id="7d58e-160">IncludesLastFolderInRange</span></span>](includeslastfolderinrange.md) <br/> |<span data-ttu-id="7d58e-161">Indica si el último elemento para sincronizar se ha incluido en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7d58e-161">Indicates whether the last item to synchronize has been included in the response.</span></span>  <br/> |
|[<span data-ttu-id="7d58e-162">Cambios (jerarquía)</span><span class="sxs-lookup"><span data-stu-id="7d58e-162">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="7d58e-163">Contiene una matriz de secuencia de tipos de cambios que representan los tipos de las diferencias entre los elementos en el cliente y los elementos en el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7d58e-163">Contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7d58e-164">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7d58e-164">Parent elements</span></span>

|<span data-ttu-id="7d58e-165">**Element**</span><span class="sxs-lookup"><span data-stu-id="7d58e-165">**Element**</span></span>|<span data-ttu-id="7d58e-166">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7d58e-166">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7d58e-167">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7d58e-167">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="7d58e-168">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7d58e-168">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d58e-169">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7d58e-169">Remarks</span></span>

<span data-ttu-id="7d58e-170">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="7d58e-170">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7d58e-171">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7d58e-171">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d58e-172">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7d58e-172">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7d58e-173">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7d58e-173">Schema Name</span></span>  <br/> |<span data-ttu-id="7d58e-174">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="7d58e-174">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7d58e-175">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7d58e-175">Validation File</span></span>  <br/> |<span data-ttu-id="7d58e-176">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7d58e-176">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7d58e-177">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7d58e-177">Can be Empty</span></span>  <br/> |<span data-ttu-id="7d58e-178">False</span><span class="sxs-lookup"><span data-stu-id="7d58e-178">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7d58e-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d58e-179">See also</span></span>

- [<span data-ttu-id="7d58e-180">Operación SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="7d58e-180">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)
- [<span data-ttu-id="7d58e-181">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="7d58e-181">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

