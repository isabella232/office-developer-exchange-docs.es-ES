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
ms.openlocfilehash: ef25dcf26e06f199587cef885d8cbc9e93b52bdb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457945"
---
# <a name="updateitemresponsemessage"></a><span data-ttu-id="b5815-103">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b5815-103">UpdateItemResponseMessage</span></span>

<span data-ttu-id="b5815-104">El elemento **UpdateItemResponseMessage** contiene el estado y el resultado de una única solicitud de [operación UpdateItem](updateitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="b5815-104">The **UpdateItemResponseMessage** element contains the status and result of a single [UpdateItem operation](updateitem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="b5815-105">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="b5815-105">UpdateItemResponse</span></span>](updateitemresponse.md)
- [<span data-ttu-id="b5815-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b5815-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="b5815-107">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b5815-107">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
  
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

 <span data-ttu-id="b5815-108">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="b5815-108">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b5815-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b5815-109">Attributes and elements</span></span>

<span data-ttu-id="b5815-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b5815-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5815-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="b5815-111">Attributes</span></span>

|<span data-ttu-id="b5815-112">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="b5815-112">**Attribute**</span></span>|<span data-ttu-id="b5815-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b5815-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b5815-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="b5815-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="b5815-115">Describe el estado de una respuesta de [operación de UpdateItem](updateitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="b5815-115">Describes the status of an [UpdateItem operation](updateitem-operation.md) response.</span></span> <br/><br/><span data-ttu-id="b5815-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="b5815-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="b5815-117">-Correcto</span><span class="sxs-lookup"><span data-stu-id="b5815-117">-  Success</span></span>  <br/><span data-ttu-id="b5815-118">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="b5815-118">-  Warning</span></span>  <br/><span data-ttu-id="b5815-119">-Error</span><span class="sxs-lookup"><span data-stu-id="b5815-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="b5815-120">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="b5815-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="b5815-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b5815-121">**Value**</span></span>|<span data-ttu-id="b5815-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b5815-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b5815-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="b5815-123">**Success**</span></span> <br/> |<span data-ttu-id="b5815-124">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="b5815-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="b5815-125">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="b5815-125">**Warning**</span></span> <br/> | <span data-ttu-id="b5815-126">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="b5815-126">Describes a request that was not processed.</span></span> <span data-ttu-id="b5815-127">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="b5815-127">A warning may be returned if an error occurred while an item in the request was processed and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="b5815-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="b5815-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="b5815-129">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="b5815-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="b5815-130">-Los servicios de dominio de Active Directory (AD DS) están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="b5815-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="b5815-131">-Se mueven los buzones.</span><span class="sxs-lookup"><span data-stu-id="b5815-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="b5815-132">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="b5815-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="b5815-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="b5815-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="b5815-134">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="b5815-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="b5815-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="b5815-135">**Error**</span></span> <br/> | <span data-ttu-id="b5815-136">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="b5815-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="b5815-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="b5815-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="b5815-138">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="b5815-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="b5815-139">-Atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="b5815-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="b5815-140">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="b5815-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="b5815-141">-Atributo o elemento no válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="b5815-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="b5815-142">-Intento de acceso no autorizado por parte de un cliente</span><span class="sxs-lookup"><span data-stu-id="b5815-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="b5815-143">-Error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="b5815-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="b5815-144">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="b5815-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b5815-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b5815-145">Child elements</span></span>

|<span data-ttu-id="b5815-146">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b5815-146">**Element**</span></span>|<span data-ttu-id="b5815-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b5815-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b5815-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="b5815-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="b5815-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b5815-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="b5815-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b5815-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="b5815-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b5815-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="b5815-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="b5815-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="b5815-153">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b5815-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="b5815-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="b5815-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="b5815-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="b5815-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="b5815-156">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="b5815-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="b5815-157">Items</span><span class="sxs-lookup"><span data-stu-id="b5815-157">Items</span></span>](items.md) <br/> |<span data-ttu-id="b5815-158">Contiene una matriz de elementos actualizados.</span><span class="sxs-lookup"><span data-stu-id="b5815-158">Contains an array of updated items.</span></span>  <br/> |
|[<span data-ttu-id="b5815-159">ConflictResults</span><span class="sxs-lookup"><span data-stu-id="b5815-159">ConflictResults</span></span>](conflictresults.md) <br/> |<span data-ttu-id="b5815-160">Contiene el número de conflictos en una respuesta de [operación UpdateItem](updateitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="b5815-160">Contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b5815-161">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b5815-161">Parent elements</span></span>

|<span data-ttu-id="b5815-162">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b5815-162">**Element**</span></span>|<span data-ttu-id="b5815-163">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b5815-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b5815-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b5815-164">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="b5815-165">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b5815-165">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5815-166">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b5815-166">Remarks</span></span>

<span data-ttu-id="b5815-167">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="b5815-167">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5815-168">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b5815-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5815-169">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5815-169">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b5815-170">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b5815-170">Schema Name</span></span>  <br/> |<span data-ttu-id="b5815-171">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b5815-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b5815-172">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b5815-172">Validation File</span></span>  <br/> |<span data-ttu-id="b5815-173">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b5815-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b5815-174">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b5815-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="b5815-175">Falso</span><span class="sxs-lookup"><span data-stu-id="b5815-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b5815-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5815-176">See also</span></span>

- [<span data-ttu-id="b5815-177">Operación UpdateItem</span><span class="sxs-lookup"><span data-stu-id="b5815-177">UpdateItem operation</span></span>](updateitem-operation.md)
- [<span data-ttu-id="b5815-178">Actualizar contactos</span><span class="sxs-lookup"><span data-stu-id="b5815-178">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
- [<span data-ttu-id="b5815-179">Actualización de tareas</span><span class="sxs-lookup"><span data-stu-id="b5815-179">Updating Tasks</span></span>](https://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)

