---
title: SyncFolderItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderItemsResponseMessage
api_type:
- schema
ms.assetid: f58e773f-94a7-4729-90f0-ac4c71b4ba59
description: El elemento SyncFolderItemsResponseMessage contiene el estado y el resultado de una única solicitud de operación SyncFolderItems.
ms.openlocfilehash: 9bb32232143df56ad9de93480e10a5941e68025a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840620"
---
# <a name="syncfolderitemsresponsemessage"></a><span data-ttu-id="26090-103">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="26090-103">SyncFolderItemsResponseMessage</span></span>

<span data-ttu-id="26090-104">El elemento **SyncFolderItemsResponseMessage** contiene el estado y el resultado de una única solicitud de [operación SyncFolderItems](syncfolderitems-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="26090-104">The **SyncFolderItemsResponseMessage** element contains the status and result of a single [SyncFolderItems operation](syncfolderitems-operation.md) request.</span></span> 
  
- [<span data-ttu-id="26090-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="26090-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md) 
- [<span data-ttu-id="26090-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="26090-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="26090-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="26090-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)
  
```xml
<SyncFolderItemsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <SyncState/>
   <IncludesLastItemInRange/>
   <Changes/>
</SyncFolderItemsResponseMessage>
```

 <span data-ttu-id="26090-108">**SyncFolderItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="26090-108">**SyncFolderItemsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="26090-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="26090-109">Attributes and elements</span></span>

<span data-ttu-id="26090-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="26090-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="26090-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="26090-111">Attributes</span></span>

|<span data-ttu-id="26090-112">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="26090-112">**Attribute**</span></span>|<span data-ttu-id="26090-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26090-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="26090-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="26090-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="26090-115">Describe el estado de una respuesta de [la operación SyncFolderItems](syncfolderitems-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="26090-115">Describes the status of a [SyncFolderItems operation](syncfolderitems-operation.md) response.</span></span> <br/><br/><span data-ttu-id="26090-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="26090-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="26090-117">-Éxito</span><span class="sxs-lookup"><span data-stu-id="26090-117">-  Success</span></span>  <br/><span data-ttu-id="26090-118">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="26090-118">-  Warning</span></span>  <br/><span data-ttu-id="26090-119">-Error</span><span class="sxs-lookup"><span data-stu-id="26090-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="26090-120">Atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="26090-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="26090-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="26090-121">**Value**</span></span>|<span data-ttu-id="26090-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26090-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="26090-123">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="26090-123">**Success**</span></span> <br/> |<span data-ttu-id="26090-124">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="26090-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="26090-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="26090-125">**Warning**</span></span> <br/> | <span data-ttu-id="26090-126">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="26090-126">Describes a request that was not processed.</span></span> <span data-ttu-id="26090-127">Es posible que se devuelve una advertencia si se produjo un error al procesar un elemento de la solicitud y no se puede procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="26090-127">A warning may be returned if an error occurred while processing an item in the request and subsequent items cannot be processed.</span></span> <br/><br/><span data-ttu-id="26090-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="26090-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="26090-129">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="26090-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="26090-130">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="26090-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="26090-131">-Buzones se han movido.</span><span class="sxs-lookup"><span data-stu-id="26090-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="26090-132">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="26090-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="26090-133">-Una contraseña ha caducado.</span><span class="sxs-lookup"><span data-stu-id="26090-133">-  A password has expired.</span></span>  <br/><span data-ttu-id="26090-134">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="26090-134">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="26090-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="26090-135">**Error**</span></span> <br/> | <span data-ttu-id="26090-136">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="26090-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="26090-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="26090-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="26090-138">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="26090-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="26090-139">-Los atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="26090-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="26090-140">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="26090-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="26090-141">-Un atributo o un elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="26090-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="26090-142">-Cualquier intento de acceso no autorizado por cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="26090-142">-  Any unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="26090-143">-Cualquier error de servidor en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="26090-143">-  Any server-side failure in response to a valid client-side call</span></span>  <br/>  <br/><span data-ttu-id="26090-144">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="26090-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="26090-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="26090-145">Child elements</span></span>

|<span data-ttu-id="26090-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="26090-146">**Element**</span></span>|<span data-ttu-id="26090-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26090-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26090-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="26090-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="26090-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="26090-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="26090-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="26090-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="26090-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="26090-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="26090-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="26090-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="26090-153">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="26090-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="26090-154">Contiene el valor de 0.</span><span class="sxs-lookup"><span data-stu-id="26090-154">It contains the value of 0.</span></span>  <br/> |
|[<span data-ttu-id="26090-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="26090-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="26090-156">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="26090-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="26090-157">Estado de sincronización</span><span class="sxs-lookup"><span data-stu-id="26090-157">SyncState</span></span>](syncstate-ex15websvcsotherref.md) <br/> |<span data-ttu-id="26090-158">Contiene un formulario con codificación base64 de los datos de sincronización que se actualizan después de cada solicitud realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="26090-158">Contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="26090-159">Esto se usa para identificar el estado de sincronización.</span><span class="sxs-lookup"><span data-stu-id="26090-159">This is used to identify the synchronization state.</span></span>  <br/> |
|[<span data-ttu-id="26090-160">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="26090-160">IncludesLastItemInRange</span></span>](includeslastiteminrange.md) <br/> |<span data-ttu-id="26090-161">Indica si el último elemento para sincronizar se ha incluido en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="26090-161">Indicates whether the last item to synchronize has been included in the response.</span></span>  <br/> |
|[<span data-ttu-id="26090-162">Cambios (elementos)</span><span class="sxs-lookup"><span data-stu-id="26090-162">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="26090-163">Contiene una matriz de secuencia de tipos de cambios que representan los tipos de las diferencias entre los elementos en el cliente y los elementos en el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="26090-163">Contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="26090-164">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="26090-164">Parent elements</span></span>

|<span data-ttu-id="26090-165">**Element**</span><span class="sxs-lookup"><span data-stu-id="26090-165">**Element**</span></span>|<span data-ttu-id="26090-166">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26090-166">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26090-167">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="26090-167">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="26090-168">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="26090-168">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26090-169">Notas</span><span class="sxs-lookup"><span data-stu-id="26090-169">Remarks</span></span>

<span data-ttu-id="26090-170">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="26090-170">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="26090-171">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="26090-171">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26090-172">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="26090-172">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="26090-173">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="26090-173">Schema Name</span></span>  <br/> |<span data-ttu-id="26090-174">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="26090-174">Messages schema</span></span>  <br/> |
|<span data-ttu-id="26090-175">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="26090-175">Validation File</span></span>  <br/> |<span data-ttu-id="26090-176">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="26090-176">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="26090-177">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="26090-177">Can be Empty</span></span>  <br/> |<span data-ttu-id="26090-178">False</span><span class="sxs-lookup"><span data-stu-id="26090-178">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="26090-179">Ver también</span><span class="sxs-lookup"><span data-stu-id="26090-179">See also</span></span>

- [<span data-ttu-id="26090-180">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="26090-180">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="26090-181">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="26090-181">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

