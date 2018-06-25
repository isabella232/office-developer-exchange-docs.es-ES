---
title: GetItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItemResponseMessage
api_type:
- schema
ms.assetid: cc583723-54d1-4a17-8c1f-6586f70fdefd
description: El elemento GetItemResponseMessage contiene el estado y el resultado de una única solicitud de operación GetItem.
ms.openlocfilehash: 0c8527258d4637ede053e189dfb918b910c859d6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764900"
---
# <a name="getitemresponsemessage"></a><span data-ttu-id="f26b1-103">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f26b1-103">GetItemResponseMessage</span></span>

<span data-ttu-id="f26b1-104">El elemento **GetItemResponseMessage** contiene el estado y el resultado de una única solicitud [GetItem operation](getitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="f26b1-104">The **GetItemResponseMessage** element contains the status and result of a single [GetItem operation](getitem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="f26b1-105">GetItemResponse</span><span class="sxs-lookup"><span data-stu-id="f26b1-105">GetItemResponse</span></span>](getitemresponse.md) 
- [<span data-ttu-id="f26b1-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f26b1-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="f26b1-107">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f26b1-107">GetItemResponseMessage</span></span>](getitemresponsemessage.md)
  
```xml
<GetItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</GetItemResponseMessage>
```

<span data-ttu-id="f26b1-108">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f26b1-108">**ItemInfoResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f26b1-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f26b1-109">Attributes and elements</span></span>

<span data-ttu-id="f26b1-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f26b1-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f26b1-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="f26b1-111">Attributes</span></span>

|<span data-ttu-id="f26b1-112">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="f26b1-112">**Attribute**</span></span>|<span data-ttu-id="f26b1-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f26b1-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f26b1-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="f26b1-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="f26b1-115">Describe el estado de una respuesta de [la operación GetItem](getitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="f26b1-115">Describes the status of a [GetItem operation](getitem-operation.md) response.</span></span> <br/><br/><span data-ttu-id="f26b1-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="f26b1-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="f26b1-117">-Éxito</span><span class="sxs-lookup"><span data-stu-id="f26b1-117">- Success</span></span><br/><span data-ttu-id="f26b1-118">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="f26b1-118">- Warning</span></span><br/><span data-ttu-id="f26b1-119">-Error</span><span class="sxs-lookup"><span data-stu-id="f26b1-119">- Error</span></span> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="f26b1-120">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="f26b1-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="f26b1-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f26b1-121">**Value**</span></span>|<span data-ttu-id="f26b1-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f26b1-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f26b1-123">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="f26b1-123">**Success**</span></span> <br/> |<span data-ttu-id="f26b1-124">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="f26b1-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="f26b1-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="f26b1-125">**Warning**</span></span> <br/> | <span data-ttu-id="f26b1-126">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="f26b1-126">Describes a request that was not processed.</span></span> <span data-ttu-id="f26b1-127">Es posible que se devuelve una advertencia si se produjo un error mientras se procesó un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="f26b1-127">A warning may be returned if an error occurred while an item in the request was processed and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="f26b1-128">Los siguientes son ejemplos de fuentes para las advertencias de:</span><span class="sxs-lookup"><span data-stu-id="f26b1-128">The following are examples of sources for warnings:</span></span><br/><br/><span data-ttu-id="f26b1-129">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="f26b1-129">- The Exchange store is offline during the batch.</span></span><br/><span data-ttu-id="f26b1-130">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="f26b1-130">- Active Directory Domain Services (AD DS) is offline.</span></span><br/><span data-ttu-id="f26b1-131">-Se mueven los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="f26b1-131">- Mailboxes are moved.</span></span><br/><span data-ttu-id="f26b1-132">-MDB está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="f26b1-132">- MDB is offline.</span></span><br/><span data-ttu-id="f26b1-133">-Contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="f26b1-133">- Password is expired.</span></span>  <br/><span data-ttu-id="f26b1-134">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="f26b1-134">- Quota is exceeded.</span></span> |
|<span data-ttu-id="f26b1-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="f26b1-135">**Error**</span></span> <br/> | <span data-ttu-id="f26b1-136">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="f26b1-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="f26b1-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="f26b1-137">The following are examples of sources for errors:</span></span><br/><br/><span data-ttu-id="f26b1-138">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="f26b1-138">- Invalid attributes or elements</span></span><br/><span data-ttu-id="f26b1-139">-Los atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="f26b1-139">- Attributes or elements out of range</span></span><br/><span data-ttu-id="f26b1-140">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="f26b1-140">- Unknown tag</span></span><br/><span data-ttu-id="f26b1-141">-De atributo o elemento no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="f26b1-141">- Attribute or element not valid in the context</span></span><br/><span data-ttu-id="f26b1-142">-Acceso no autorizado intenta establecer cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="f26b1-142">- Unauthorized access attempted by any client</span></span><br/><span data-ttu-id="f26b1-143">-Error server-side en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="f26b1-143">- Server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="f26b1-144">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="f26b1-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span> |
   
### <a name="child-elements"></a><span data-ttu-id="f26b1-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f26b1-145">Child elements</span></span>

|<span data-ttu-id="f26b1-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="f26b1-146">**Element**</span></span>|<span data-ttu-id="f26b1-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f26b1-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f26b1-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="f26b1-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="f26b1-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f26b1-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="f26b1-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f26b1-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="f26b1-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f26b1-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="f26b1-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f26b1-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="f26b1-153">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="f26b1-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="f26b1-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="f26b1-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="f26b1-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="f26b1-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="f26b1-156">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="f26b1-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="f26b1-157">Items</span><span class="sxs-lookup"><span data-stu-id="f26b1-157">Items</span></span>](items.md) <br/> |<span data-ttu-id="f26b1-158">Contiene una matriz de elementos devueltos.</span><span class="sxs-lookup"><span data-stu-id="f26b1-158">Contains an array of returned items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f26b1-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f26b1-159">Parent elements</span></span>

|<span data-ttu-id="f26b1-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="f26b1-160">**Element**</span></span>|<span data-ttu-id="f26b1-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f26b1-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f26b1-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f26b1-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="f26b1-163">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f26b1-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f26b1-164">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f26b1-164">Remarks</span></span>

<span data-ttu-id="f26b1-165">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="f26b1-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f26b1-166">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f26b1-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f26b1-167">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f26b1-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f26b1-168">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f26b1-168">Schema Name</span></span>  <br/> |<span data-ttu-id="f26b1-169">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="f26b1-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f26b1-170">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f26b1-170">Validation File</span></span>  <br/> |<span data-ttu-id="f26b1-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f26b1-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f26b1-172">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f26b1-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="f26b1-173">False</span><span class="sxs-lookup"><span data-stu-id="f26b1-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f26b1-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="f26b1-174">See also</span></span>

- [<span data-ttu-id="f26b1-175">GetItem</span><span class="sxs-lookup"><span data-stu-id="f26b1-175">GetItem</span></span>](getitem.md)
- [<span data-ttu-id="f26b1-176">Operación GetItem</span><span class="sxs-lookup"><span data-stu-id="f26b1-176">GetItem operation</span></span>](getitem-operation.md)

