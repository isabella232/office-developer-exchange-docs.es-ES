---
title: UpdateItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItemResponseMessage
api_type:
- schema
ms.assetid: dc585b05-5afc-4c74-8763-5a54f9a650ec
description: El elemento UpdateItemResponseMessage contiene el estado y el resultado de una única solicitud de operación UpdateItem.
ms.openlocfilehash: c971657813784e68a01539899e8fabea67847325
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840850"
---
# <a name="updateitemresponsemessage"></a><span data-ttu-id="a2685-103">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a2685-103">UpdateItemResponseMessage</span></span>

<span data-ttu-id="a2685-104">El elemento **UpdateItemResponseMessage** contiene el estado y el resultado de una única solicitud de [operación UpdateItem](updateitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="a2685-104">The **UpdateItemResponseMessage** element contains the status and result of a single [UpdateItem operation](updateitem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="a2685-105">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="a2685-105">UpdateItemResponse</span></span>](updateitemresponse.md)
- [<span data-ttu-id="a2685-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a2685-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="a2685-107">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a2685-107">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
  
```xml
<UpdateItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
   <ConflictResults/>
</UpdateItemResponseMessage>
```

 <span data-ttu-id="a2685-108">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="a2685-108">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a2685-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a2685-109">Attributes and elements</span></span>

<span data-ttu-id="a2685-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a2685-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a2685-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="a2685-111">Attributes</span></span>

|<span data-ttu-id="a2685-112">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="a2685-112">**Attribute**</span></span>|<span data-ttu-id="a2685-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a2685-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a2685-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="a2685-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="a2685-115">Describe el estado de una respuesta de [la operación UpdateItem](updateitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="a2685-115">Describes the status of an [UpdateItem operation](updateitem-operation.md) response.</span></span> <br/><br/><span data-ttu-id="a2685-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="a2685-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="a2685-117">-Éxito</span><span class="sxs-lookup"><span data-stu-id="a2685-117">-  Success</span></span>  <br/><span data-ttu-id="a2685-118">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="a2685-118">-  Warning</span></span>  <br/><span data-ttu-id="a2685-119">-Error</span><span class="sxs-lookup"><span data-stu-id="a2685-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="a2685-120">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="a2685-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="a2685-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a2685-121">**Value**</span></span>|<span data-ttu-id="a2685-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a2685-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a2685-123">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="a2685-123">**Success**</span></span> <br/> |<span data-ttu-id="a2685-124">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="a2685-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="a2685-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="a2685-125">**Warning**</span></span> <br/> | <span data-ttu-id="a2685-126">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="a2685-126">Describes a request that was not processed.</span></span> <span data-ttu-id="a2685-127">Es posible que se devuelve una advertencia si se produjo un error mientras se procesó un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="a2685-127">A warning may be returned if an error occurred while an item in the request was processed and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="a2685-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="a2685-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="a2685-129">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="a2685-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="a2685-130">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="a2685-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="a2685-131">-Se mueven los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="a2685-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="a2685-132">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="a2685-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="a2685-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="a2685-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="a2685-134">-Se ha excedido una cuota.</span><span class="sxs-lookup"><span data-stu-id="a2685-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="a2685-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="a2685-135">**Error**</span></span> <br/> | <span data-ttu-id="a2685-136">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="a2685-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="a2685-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="a2685-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="a2685-138">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="a2685-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="a2685-139">-Los atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="a2685-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="a2685-140">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="a2685-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="a2685-141">-De atributo o elemento no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="a2685-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="a2685-142">-Intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="a2685-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="a2685-143">-Error server-side en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="a2685-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="a2685-144">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="a2685-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a2685-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a2685-145">Child elements</span></span>

|<span data-ttu-id="a2685-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="a2685-146">**Element**</span></span>|<span data-ttu-id="a2685-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a2685-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a2685-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="a2685-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="a2685-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2685-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="a2685-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a2685-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="a2685-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2685-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="a2685-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="a2685-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="a2685-153">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="a2685-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="a2685-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="a2685-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="a2685-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="a2685-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="a2685-156">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="a2685-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="a2685-157">Items</span><span class="sxs-lookup"><span data-stu-id="a2685-157">Items</span></span>](items.md) <br/> |<span data-ttu-id="a2685-158">Contiene una matriz de elementos actualizados.</span><span class="sxs-lookup"><span data-stu-id="a2685-158">Contains an array of updated items.</span></span>  <br/> |
|[<span data-ttu-id="a2685-159">ConflictResults</span><span class="sxs-lookup"><span data-stu-id="a2685-159">ConflictResults</span></span>](conflictresults.md) <br/> |<span data-ttu-id="a2685-160">Contiene el número de conflictos en una respuesta de [la operación UpdateItem](updateitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="a2685-160">Contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a2685-161">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a2685-161">Parent elements</span></span>

|<span data-ttu-id="a2685-162">**Element**</span><span class="sxs-lookup"><span data-stu-id="a2685-162">**Element**</span></span>|<span data-ttu-id="a2685-163">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a2685-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a2685-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a2685-164">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="a2685-165">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a2685-165">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2685-166">Notas</span><span class="sxs-lookup"><span data-stu-id="a2685-166">Remarks</span></span>

<span data-ttu-id="a2685-167">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="a2685-167">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a2685-168">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a2685-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a2685-169">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a2685-169">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a2685-170">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a2685-170">Schema Name</span></span>  <br/> |<span data-ttu-id="a2685-171">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="a2685-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a2685-172">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a2685-172">Validation File</span></span>  <br/> |<span data-ttu-id="a2685-173">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a2685-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a2685-174">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a2685-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="a2685-175">False</span><span class="sxs-lookup"><span data-stu-id="a2685-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a2685-176">Ver también</span><span class="sxs-lookup"><span data-stu-id="a2685-176">See also</span></span>

- [<span data-ttu-id="a2685-177">Operación UpdateItem</span><span class="sxs-lookup"><span data-stu-id="a2685-177">UpdateItem operation</span></span>](updateitem-operation.md)
- [<span data-ttu-id="a2685-178">Actualizar contactos</span><span class="sxs-lookup"><span data-stu-id="a2685-178">Updating Contacts</span></span>](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
- [<span data-ttu-id="a2685-179">Actualización de tareas</span><span class="sxs-lookup"><span data-stu-id="a2685-179">Updating Tasks</span></span>](http://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)

