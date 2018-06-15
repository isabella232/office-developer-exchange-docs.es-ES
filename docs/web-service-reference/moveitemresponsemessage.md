---
title: MoveItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveItemResponseMessage
api_type:
- schema
ms.assetid: 1efacb2c-cb76-44ad-b0be-bb47bf2553be
description: El elemento MoveItemResponseMessage contiene el estado y el resultado de una única solicitud de operación MoveItem.
ms.openlocfilehash: af1c10391d9b5b761ab87983eea6321d61231152
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836493"
---
# <a name="moveitemresponsemessage"></a><span data-ttu-id="0ff0b-103">MoveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0ff0b-103">MoveItemResponseMessage</span></span>

<span data-ttu-id="0ff0b-104">El elemento **MoveItemResponseMessage** contiene el estado y el resultado de una única solicitud de [operación MoveItem](moveitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="0ff0b-104">The **MoveItemResponseMessage** element contains the status and result of a single [MoveItem operation](moveitem-operation.md) request.</span></span> 
  
```xml
<MoveItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</MoveItemResponseMessage>
```

 <span data-ttu-id="0ff0b-105">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="0ff0b-105">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0ff0b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0ff0b-106">Attributes and elements</span></span>

<span data-ttu-id="0ff0b-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0ff0b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0ff0b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0ff0b-108">Attributes</span></span>

|<span data-ttu-id="0ff0b-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="0ff0b-109">**Attribute**</span></span>|<span data-ttu-id="0ff0b-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0ff0b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0ff0b-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="0ff0b-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="0ff0b-112">Describe el estado de una respuesta de [la operación MoveItem](moveitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="0ff0b-112">Describes the status of a [MoveItem operation](moveitem-operation.md) response.</span></span> <br/><br/><span data-ttu-id="0ff0b-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="0ff0b-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="0ff0b-114">-Éxito</span><span class="sxs-lookup"><span data-stu-id="0ff0b-114">-  Success</span></span>  <br/><span data-ttu-id="0ff0b-115">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="0ff0b-115">-  Warning</span></span>  <br/><span data-ttu-id="0ff0b-116">-Error</span><span class="sxs-lookup"><span data-stu-id="0ff0b-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="0ff0b-117">Atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="0ff0b-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="0ff0b-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0ff0b-118">**Value**</span></span>|<span data-ttu-id="0ff0b-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0ff0b-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0ff0b-120">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="0ff0b-120">**Success**</span></span> <br/> |<span data-ttu-id="0ff0b-121">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="0ff0b-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="0ff0b-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="0ff0b-122">**Warning**</span></span> <br/> | <span data-ttu-id="0ff0b-123">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="0ff0b-123">Describes a request that was not processed.</span></span> <span data-ttu-id="0ff0b-124">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="0ff0b-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="0ff0b-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="0ff0b-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="0ff0b-126">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="0ff0b-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="0ff0b-127">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="0ff0b-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="0ff0b-128">-Se mueven los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="0ff0b-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="0ff0b-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="0ff0b-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="0ff0b-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="0ff0b-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="0ff0b-131">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="0ff0b-131">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="0ff0b-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="0ff0b-132">**Error**</span></span> <br/> | <span data-ttu-id="0ff0b-133">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="0ff0b-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="0ff0b-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="0ff0b-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="0ff0b-135">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="0ff0b-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="0ff0b-136">-Los atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="0ff0b-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="0ff0b-137">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="0ff0b-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="0ff0b-138">-De atributo o elemento no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="0ff0b-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="0ff0b-139">-Cualquier acceso no autorizado intenta establecer cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="0ff0b-139">-  Any unauthorized access attempted by any client</span></span>  <br/><span data-ttu-id="0ff0b-140">-Cualquier error del servidor en respuesta a una llamada de cliente válida.</span><span class="sxs-lookup"><span data-stu-id="0ff0b-140">-  Any server-side failure in response to a valid client-side call.</span></span>  <br/><br/>  <span data-ttu-id="0ff0b-141">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="0ff0b-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0ff0b-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0ff0b-142">Child elements</span></span>

|<span data-ttu-id="0ff0b-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="0ff0b-143">**Element**</span></span>|<span data-ttu-id="0ff0b-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0ff0b-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ff0b-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="0ff0b-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="0ff0b-146">Una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0ff0b-146">A text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="0ff0b-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0ff0b-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="0ff0b-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0ff0b-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="0ff0b-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0ff0b-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="0ff0b-150">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="0ff0b-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="0ff0b-151">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="0ff0b-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="0ff0b-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="0ff0b-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="0ff0b-153">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="0ff0b-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="0ff0b-154">Items</span><span class="sxs-lookup"><span data-stu-id="0ff0b-154">Items</span></span>](items.md) <br/> |<span data-ttu-id="0ff0b-155">Contiene una matriz de elementos que se ha movido.</span><span class="sxs-lookup"><span data-stu-id="0ff0b-155">Contains an array of moved items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0ff0b-156">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0ff0b-156">Parent elements</span></span>

|<span data-ttu-id="0ff0b-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="0ff0b-157">**Element**</span></span>|<span data-ttu-id="0ff0b-158">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0ff0b-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ff0b-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0ff0b-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="0ff0b-160">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0ff0b-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ff0b-161">Notas</span><span class="sxs-lookup"><span data-stu-id="0ff0b-161">Remarks</span></span>

<span data-ttu-id="0ff0b-162">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con la función de servidor de acceso de cliente instalada.</span><span class="sxs-lookup"><span data-stu-id="0ff0b-162">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0ff0b-163">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0ff0b-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0ff0b-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0ff0b-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0ff0b-165">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0ff0b-165">Schema Name</span></span>  <br/> |<span data-ttu-id="0ff0b-166">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="0ff0b-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0ff0b-167">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0ff0b-167">Validation File</span></span>  <br/> |<span data-ttu-id="0ff0b-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0ff0b-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0ff0b-169">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0ff0b-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="0ff0b-170">False</span><span class="sxs-lookup"><span data-stu-id="0ff0b-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0ff0b-171">Ver también</span><span class="sxs-lookup"><span data-stu-id="0ff0b-171">See also</span></span>

- [<span data-ttu-id="0ff0b-172">Operación MoveItem</span><span class="sxs-lookup"><span data-stu-id="0ff0b-172">MoveItem operation</span></span>](moveitem-operation.md)
- [<span data-ttu-id="0ff0b-173">MoveItem</span><span class="sxs-lookup"><span data-stu-id="0ff0b-173">MoveItem</span></span>](moveitem.md)
