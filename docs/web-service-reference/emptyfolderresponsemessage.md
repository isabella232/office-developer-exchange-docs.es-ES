---
title: EmptyFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 678dd5ce-8d9e-4939-bf1b-a8e148f4f449
description: El elemento EmptyFolderResponseMessage contiene el estado y el resultado de una única solicitud EmptyFolder.
ms.openlocfilehash: ebdaac28cdd16a55811276ef0d11c03b00d3897a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764387"
---
# <a name="emptyfolderresponsemessage"></a><span data-ttu-id="d9e8a-103">EmptyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d9e8a-103">EmptyFolderResponseMessage</span></span>

<span data-ttu-id="d9e8a-104">El elemento **EmptyFolderResponseMessage** contiene el estado y el resultado de una única solicitud [EmptyFolder](emptyfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="d9e8a-104">The **EmptyFolderResponseMessage** element contains the status and result of a single [EmptyFolder](emptyfolder.md) request.</span></span> 
  
```XML
<EmptyFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</EmptyFolderResponseMessage>
```

 <span data-ttu-id="d9e8a-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="d9e8a-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d9e8a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d9e8a-106">Attributes and elements</span></span>

<span data-ttu-id="d9e8a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d9e8a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d9e8a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d9e8a-108">Attributes</span></span>

|<span data-ttu-id="d9e8a-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="d9e8a-109">**Attribute**</span></span>|<span data-ttu-id="d9e8a-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d9e8a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d9e8a-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="d9e8a-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="d9e8a-112">Describe el estado de una respuesta de [la operación EmptyFolder](emptyfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="d9e8a-112">Describes the status of an [EmptyFolder operation](emptyfolder-operation.md) response.</span></span><br/><br/><span data-ttu-id="d9e8a-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="d9e8a-113">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="d9e8a-114">-Éxito</span><span class="sxs-lookup"><span data-stu-id="d9e8a-114">-  Success</span></span>  <br/><span data-ttu-id="d9e8a-115">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="d9e8a-115">-  Warning</span></span>  <br/><span data-ttu-id="d9e8a-116">-Error</span><span class="sxs-lookup"><span data-stu-id="d9e8a-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="d9e8a-117">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="d9e8a-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="d9e8a-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d9e8a-118">**Value**</span></span>|<span data-ttu-id="d9e8a-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d9e8a-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d9e8a-120">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="d9e8a-120">**Success**</span></span> <br/> |<span data-ttu-id="d9e8a-121">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="d9e8a-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="d9e8a-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="d9e8a-122">**Warning**</span></span> <br/> | <span data-ttu-id="d9e8a-123">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="d9e8a-123">Describes a request that was not processed.</span></span> <span data-ttu-id="d9e8a-124">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="d9e8a-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="d9e8a-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="d9e8a-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="d9e8a-126">-El almacén de Exchange se desconecta durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="d9e8a-126">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="d9e8a-127">-Los servicios de dominio de Active Directory (AD DS) se queda sin conexión.</span><span class="sxs-lookup"><span data-stu-id="d9e8a-127">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="d9e8a-128">-Se mueven los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="d9e8a-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="d9e8a-129">-La base de datos de mensajes (MDB) se queda sin conexión.</span><span class="sxs-lookup"><span data-stu-id="d9e8a-129">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="d9e8a-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="d9e8a-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="d9e8a-131">-Se ha excedido una cuota.</span><span class="sxs-lookup"><span data-stu-id="d9e8a-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="d9e8a-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="d9e8a-132">**Error**</span></span> <br/> | <span data-ttu-id="d9e8a-133">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="d9e8a-133">Describes a request that cannot be fulfilled.</span></span><br/><br/> <span data-ttu-id="d9e8a-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="d9e8a-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="d9e8a-135">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="d9e8a-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="d9e8a-136">-Los atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="d9e8a-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="d9e8a-137">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="d9e8a-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="d9e8a-138">-Un atributo o un elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="d9e8a-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="d9e8a-139">-Un intento de acceso no autorizado por cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="d9e8a-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="d9e8a-140">-Un error del lado del servidor en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="d9e8a-140">-  A server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="d9e8a-141">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="d9e8a-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d9e8a-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d9e8a-142">Child elements</span></span>

|<span data-ttu-id="d9e8a-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="d9e8a-143">**Element**</span></span>|<span data-ttu-id="d9e8a-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d9e8a-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9e8a-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="d9e8a-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="d9e8a-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d9e8a-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="d9e8a-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d9e8a-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="d9e8a-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d9e8a-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="d9e8a-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d9e8a-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="d9e8a-150">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d9e8a-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="d9e8a-151">Contiene el valor de 0.</span><span class="sxs-lookup"><span data-stu-id="d9e8a-151">It contains the value of 0.</span></span>  <br/> |
|[<span data-ttu-id="d9e8a-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="d9e8a-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="d9e8a-153">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="d9e8a-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d9e8a-154">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d9e8a-154">Parent elements</span></span>

|<span data-ttu-id="d9e8a-155">**Element**</span><span class="sxs-lookup"><span data-stu-id="d9e8a-155">**Element**</span></span>|<span data-ttu-id="d9e8a-156">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d9e8a-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9e8a-157">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d9e8a-157">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="d9e8a-158">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d9e8a-158">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d9e8a-159">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d9e8a-159">Text value</span></span>

<span data-ttu-id="d9e8a-160">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d9e8a-160">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d9e8a-161">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d9e8a-161">Remarks</span></span>

<span data-ttu-id="d9e8a-162">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d9e8a-162">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d9e8a-163">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d9e8a-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9e8a-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d9e8a-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d9e8a-165">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d9e8a-165">Schema Name</span></span>  <br/> |<span data-ttu-id="d9e8a-166">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="d9e8a-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d9e8a-167">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d9e8a-167">Validation File</span></span>  <br/> |<span data-ttu-id="d9e8a-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d9e8a-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d9e8a-169">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d9e8a-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="d9e8a-170">False</span><span class="sxs-lookup"><span data-stu-id="d9e8a-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9e8a-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9e8a-171">See also</span></span>

- [<span data-ttu-id="d9e8a-172">Operación EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="d9e8a-172">EmptyFolder operation</span></span>](emptyfolder-operation.md)
- [<span data-ttu-id="d9e8a-173">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="d9e8a-173">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="d9e8a-174">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d9e8a-174">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

