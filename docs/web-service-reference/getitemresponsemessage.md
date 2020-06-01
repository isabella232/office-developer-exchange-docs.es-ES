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
ms.openlocfilehash: bd25a82641259e1546bad6eef5c2f6f8f03e98cb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458673"
---
# <a name="getitemresponsemessage"></a><span data-ttu-id="4eaee-103">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4eaee-103">GetItemResponseMessage</span></span>

<span data-ttu-id="4eaee-104">El elemento **GetItemResponseMessage** contiene el estado y el resultado de una única solicitud de [operación GetItem](getitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="4eaee-104">The **GetItemResponseMessage** element contains the status and result of a single [GetItem operation](getitem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="4eaee-105">GetItemResponse</span><span class="sxs-lookup"><span data-stu-id="4eaee-105">GetItemResponse</span></span>](getitemresponse.md) 
- [<span data-ttu-id="4eaee-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4eaee-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="4eaee-107">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4eaee-107">GetItemResponseMessage</span></span>](getitemresponsemessage.md)
  
```xml
<GetItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</GetItemResponseMessage>
```

<span data-ttu-id="4eaee-108">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="4eaee-108">**ItemInfoResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="4eaee-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4eaee-109">Attributes and elements</span></span>

<span data-ttu-id="4eaee-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4eaee-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4eaee-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="4eaee-111">Attributes</span></span>

|<span data-ttu-id="4eaee-112">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="4eaee-112">**Attribute**</span></span>|<span data-ttu-id="4eaee-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4eaee-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4eaee-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="4eaee-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="4eaee-115">Describe el estado de una respuesta de la [operación GetItem](getitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="4eaee-115">Describes the status of a [GetItem operation](getitem-operation.md) response.</span></span> <br/><br/><span data-ttu-id="4eaee-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="4eaee-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="4eaee-117">-Correcto</span><span class="sxs-lookup"><span data-stu-id="4eaee-117">- Success</span></span><br/><span data-ttu-id="4eaee-118">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="4eaee-118">- Warning</span></span><br/><span data-ttu-id="4eaee-119">-Error</span><span class="sxs-lookup"><span data-stu-id="4eaee-119">- Error</span></span> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="4eaee-120">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="4eaee-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="4eaee-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4eaee-121">**Value**</span></span>|<span data-ttu-id="4eaee-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4eaee-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4eaee-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="4eaee-123">**Success**</span></span> <br/> |<span data-ttu-id="4eaee-124">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="4eaee-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="4eaee-125">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="4eaee-125">**Warning**</span></span> <br/> | <span data-ttu-id="4eaee-126">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="4eaee-126">Describes a request that was not processed.</span></span> <span data-ttu-id="4eaee-127">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="4eaee-127">A warning may be returned if an error occurred while an item in the request was processed and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="4eaee-128">Los siguientes son ejemplos de orígenes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="4eaee-128">The following are examples of sources for warnings:</span></span><br/><br/><span data-ttu-id="4eaee-129">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="4eaee-129">- The Exchange store is offline during the batch.</span></span><br/><span data-ttu-id="4eaee-130">-Los servicios de dominio de Active Directory (AD DS) están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="4eaee-130">- Active Directory Domain Services (AD DS) is offline.</span></span><br/><span data-ttu-id="4eaee-131">-Se mueven los buzones.</span><span class="sxs-lookup"><span data-stu-id="4eaee-131">- Mailboxes are moved.</span></span><br/><span data-ttu-id="4eaee-132">-MDB está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="4eaee-132">- MDB is offline.</span></span><br/><span data-ttu-id="4eaee-133">-La contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="4eaee-133">- Password is expired.</span></span>  <br/><span data-ttu-id="4eaee-134">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="4eaee-134">- Quota is exceeded.</span></span> |
|<span data-ttu-id="4eaee-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="4eaee-135">**Error**</span></span> <br/> | <span data-ttu-id="4eaee-136">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="4eaee-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="4eaee-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="4eaee-137">The following are examples of sources for errors:</span></span><br/><br/><span data-ttu-id="4eaee-138">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="4eaee-138">- Invalid attributes or elements</span></span><br/><span data-ttu-id="4eaee-139">-Atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="4eaee-139">- Attributes or elements out of range</span></span><br/><span data-ttu-id="4eaee-140">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="4eaee-140">- Unknown tag</span></span><br/><span data-ttu-id="4eaee-141">-Atributo o elemento no válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="4eaee-141">- Attribute or element not valid in the context</span></span><br/><span data-ttu-id="4eaee-142">-Acceso no autorizado intentado por cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="4eaee-142">- Unauthorized access attempted by any client</span></span><br/><span data-ttu-id="4eaee-143">-Error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="4eaee-143">- Server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="4eaee-144">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="4eaee-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span> |
   
### <a name="child-elements"></a><span data-ttu-id="4eaee-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4eaee-145">Child elements</span></span>

|<span data-ttu-id="4eaee-146">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4eaee-146">**Element**</span></span>|<span data-ttu-id="4eaee-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4eaee-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4eaee-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="4eaee-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="4eaee-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4eaee-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="4eaee-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4eaee-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="4eaee-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4eaee-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="4eaee-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="4eaee-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="4eaee-153">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="4eaee-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="4eaee-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="4eaee-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="4eaee-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="4eaee-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="4eaee-156">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="4eaee-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="4eaee-157">Items</span><span class="sxs-lookup"><span data-stu-id="4eaee-157">Items</span></span>](items.md) <br/> |<span data-ttu-id="4eaee-158">Contiene una matriz de elementos devueltos.</span><span class="sxs-lookup"><span data-stu-id="4eaee-158">Contains an array of returned items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4eaee-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4eaee-159">Parent elements</span></span>

|<span data-ttu-id="4eaee-160">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4eaee-160">**Element**</span></span>|<span data-ttu-id="4eaee-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4eaee-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4eaee-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4eaee-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="4eaee-163">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="4eaee-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4eaee-164">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4eaee-164">Remarks</span></span>

<span data-ttu-id="4eaee-165">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="4eaee-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4eaee-166">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4eaee-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4eaee-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="4eaee-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4eaee-168">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4eaee-168">Schema Name</span></span>  <br/> |<span data-ttu-id="4eaee-169">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="4eaee-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4eaee-170">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4eaee-170">Validation File</span></span>  <br/> |<span data-ttu-id="4eaee-171">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4eaee-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4eaee-172">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4eaee-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="4eaee-173">Falso</span><span class="sxs-lookup"><span data-stu-id="4eaee-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4eaee-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="4eaee-174">See also</span></span>

- [<span data-ttu-id="4eaee-175">GetItem</span><span class="sxs-lookup"><span data-stu-id="4eaee-175">GetItem</span></span>](getitem.md)
- [<span data-ttu-id="4eaee-176">Operación GetItem</span><span class="sxs-lookup"><span data-stu-id="4eaee-176">GetItem operation</span></span>](getitem-operation.md)

