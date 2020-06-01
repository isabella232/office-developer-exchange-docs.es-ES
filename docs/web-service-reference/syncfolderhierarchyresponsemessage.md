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
ms.openlocfilehash: fda0a37178f89ba0fd5ef860f8b009f335a11391
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465348"
---
# <a name="syncfolderhierarchyresponsemessage"></a><span data-ttu-id="3e904-103">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3e904-103">SyncFolderHierarchyResponseMessage</span></span>

<span data-ttu-id="3e904-104">El elemento **SyncFolderHierarchyResponseMessage** contiene el estado y el resultado de una única solicitud de [operación SyncFolderHierarchy](syncfolderhierarchy-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="3e904-104">The **SyncFolderHierarchyResponseMessage** element contains the status and result of a single [SyncFolderHierarchy operation](syncfolderhierarchy-operation.md) request.</span></span> 
  
- [<span data-ttu-id="3e904-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="3e904-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md) 
- [<span data-ttu-id="3e904-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3e904-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="3e904-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3e904-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
  
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

 <span data-ttu-id="3e904-108">**SyncFolderHierarchyResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="3e904-108">**SyncFolderHierarchyResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3e904-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3e904-109">Attributes and elements</span></span>

<span data-ttu-id="3e904-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3e904-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3e904-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="3e904-111">Attributes</span></span>

|<span data-ttu-id="3e904-112">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="3e904-112">**Attribute**</span></span>|<span data-ttu-id="3e904-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3e904-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3e904-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="3e904-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="3e904-115">Describe el estado de una respuesta de [operación de SyncFolderHierarchy](syncfolderhierarchy-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="3e904-115">Describes the status of a [SyncFolderHierarchy operation](syncfolderhierarchy-operation.md) response.</span></span> <br/><br/><span data-ttu-id="3e904-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="3e904-116">The following values are valid for this attribute:</span></span><br/>  <br/><span data-ttu-id="3e904-117">-Correcto</span><span class="sxs-lookup"><span data-stu-id="3e904-117">-  Success</span></span>  <br/><span data-ttu-id="3e904-118">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="3e904-118">-  Warning</span></span>  <br/><span data-ttu-id="3e904-119">-Error</span><span class="sxs-lookup"><span data-stu-id="3e904-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="3e904-120">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="3e904-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="3e904-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3e904-121">**Value**</span></span>|<span data-ttu-id="3e904-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3e904-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3e904-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="3e904-123">**Success**</span></span> <br/> |<span data-ttu-id="3e904-124">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="3e904-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="3e904-125">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="3e904-125">**Warning**</span></span> <br/> | <span data-ttu-id="3e904-126">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="3e904-126">Describes a request that was not processed.</span></span> <span data-ttu-id="3e904-127">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="3e904-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="3e904-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="3e904-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="3e904-129">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="3e904-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="3e904-130">-Los servicios de dominio de Active Directory (AD DS) están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="3e904-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="3e904-131">-Se movieron los buzones.</span><span class="sxs-lookup"><span data-stu-id="3e904-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="3e904-132">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="3e904-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="3e904-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="3e904-133">-  A password has expired.</span></span>  <br/><span data-ttu-id="3e904-134">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="3e904-134">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="3e904-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="3e904-135">**Error**</span></span> <br/> | <span data-ttu-id="3e904-136">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="3e904-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="3e904-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="3e904-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="3e904-138">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="3e904-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="3e904-139">-Atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="3e904-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="3e904-140">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="3e904-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="3e904-141">-Un atributo o elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="3e904-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="3e904-142">-Un intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="3e904-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="3e904-143">-Un error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="3e904-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="3e904-144">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="3e904-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3e904-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3e904-145">Child elements</span></span>

|<span data-ttu-id="3e904-146">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3e904-146">**Element**</span></span>|<span data-ttu-id="3e904-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3e904-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3e904-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="3e904-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="3e904-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3e904-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="3e904-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="3e904-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="3e904-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3e904-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="3e904-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="3e904-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="3e904-153">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="3e904-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="3e904-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="3e904-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="3e904-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="3e904-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="3e904-156">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="3e904-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="3e904-157">SyncState</span><span class="sxs-lookup"><span data-stu-id="3e904-157">SyncState</span></span>](syncstate-ex15websvcsotherref.md) <br/> |<span data-ttu-id="3e904-158">Contiene una forma codificada en Base64 de los datos de sincronización que se actualizan después de cada solicitud correcta.</span><span class="sxs-lookup"><span data-stu-id="3e904-158">Contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="3e904-159">Se usa para identificar el estado de sincronización.</span><span class="sxs-lookup"><span data-stu-id="3e904-159">This is used to identify the synchronization state.</span></span>  <br/> |
|[<span data-ttu-id="3e904-160">IncludesLastFolderInRange</span><span class="sxs-lookup"><span data-stu-id="3e904-160">IncludesLastFolderInRange</span></span>](includeslastfolderinrange.md) <br/> |<span data-ttu-id="3e904-161">Indica si se ha incluido en la respuesta el último elemento que se va a sincronizar.</span><span class="sxs-lookup"><span data-stu-id="3e904-161">Indicates whether the last item to synchronize has been included in the response.</span></span>  <br/> |
|[<span data-ttu-id="3e904-162">Cambios (jerarquía)</span><span class="sxs-lookup"><span data-stu-id="3e904-162">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="3e904-163">Contiene una matriz de secuencias de tipos de cambio que representan los tipos de diferencias entre los elementos en el cliente y los elementos en el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3e904-163">Contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3e904-164">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3e904-164">Parent elements</span></span>

|<span data-ttu-id="3e904-165">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3e904-165">**Element**</span></span>|<span data-ttu-id="3e904-166">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3e904-166">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3e904-167">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3e904-167">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="3e904-168">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3e904-168">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e904-169">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3e904-169">Remarks</span></span>

<span data-ttu-id="3e904-170">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="3e904-170">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3e904-171">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3e904-171">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e904-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e904-172">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3e904-173">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3e904-173">Schema Name</span></span>  <br/> |<span data-ttu-id="3e904-174">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3e904-174">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3e904-175">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3e904-175">Validation File</span></span>  <br/> |<span data-ttu-id="3e904-176">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3e904-176">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3e904-177">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3e904-177">Can be Empty</span></span>  <br/> |<span data-ttu-id="3e904-178">Falso</span><span class="sxs-lookup"><span data-stu-id="3e904-178">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3e904-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e904-179">See also</span></span>

- [<span data-ttu-id="3e904-180">Operación SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="3e904-180">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)
- [<span data-ttu-id="3e904-181">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="3e904-181">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

