---
title: EmptyFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 678dd5ce-8d9e-4939-bf1b-a8e148f4f449
description: El elemento EmptyFolderResponseMessage contiene el estado y el resultado de una sola solicitud EmptyFolder.
ms.openlocfilehash: fd69df45d7e1d6538a977b79711baa769413ea66
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526217"
---
# <a name="emptyfolderresponsemessage"></a><span data-ttu-id="e6bf5-103">EmptyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e6bf5-103">EmptyFolderResponseMessage</span></span>

<span data-ttu-id="e6bf5-104">El elemento **EmptyFolderResponseMessage** contiene el estado y el resultado de una sola solicitud [EmptyFolder](emptyfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="e6bf5-104">The **EmptyFolderResponseMessage** element contains the status and result of a single [EmptyFolder](emptyfolder.md) request.</span></span> 
  
```XML
<EmptyFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</EmptyFolderResponseMessage>
```

 <span data-ttu-id="e6bf5-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="e6bf5-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e6bf5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e6bf5-106">Attributes and elements</span></span>

<span data-ttu-id="e6bf5-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e6bf5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e6bf5-108">Attributes</span></span>

|<span data-ttu-id="e6bf5-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="e6bf5-109">**Attribute**</span></span>|<span data-ttu-id="e6bf5-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e6bf5-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e6bf5-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="e6bf5-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="e6bf5-112">Describe el estado de una respuesta de [operación de EmptyFolder](emptyfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="e6bf5-112">Describes the status of an [EmptyFolder operation](emptyfolder-operation.md) response.</span></span><br/><br/><span data-ttu-id="e6bf5-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="e6bf5-113">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="e6bf5-114">-Correcto</span><span class="sxs-lookup"><span data-stu-id="e6bf5-114">-  Success</span></span>  <br/><span data-ttu-id="e6bf5-115">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="e6bf5-115">-  Warning</span></span>  <br/><span data-ttu-id="e6bf5-116">-Error</span><span class="sxs-lookup"><span data-stu-id="e6bf5-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="e6bf5-117">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="e6bf5-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="e6bf5-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e6bf5-118">**Value**</span></span>|<span data-ttu-id="e6bf5-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e6bf5-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e6bf5-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="e6bf5-120">**Success**</span></span> <br/> |<span data-ttu-id="e6bf5-121">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="e6bf5-122">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="e6bf5-122">**Warning**</span></span> <br/> | <span data-ttu-id="e6bf5-123">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-123">Describes a request that was not processed.</span></span> <span data-ttu-id="e6bf5-124">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="e6bf5-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="e6bf5-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="e6bf5-126">-El almacén de Exchange se desconecta durante el lote.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-126">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="e6bf5-127">-Servicios de dominio de Active Directory (AD DS) se desconecta.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-127">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="e6bf5-128">-Se mueven los buzones.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="e6bf5-129">-La base de datos de mensajes (MDB) se desconecta.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-129">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="e6bf5-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="e6bf5-131">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="e6bf5-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="e6bf5-132">**Error**</span></span> <br/> | <span data-ttu-id="e6bf5-133">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-133">Describes a request that cannot be fulfilled.</span></span><br/><br/> <span data-ttu-id="e6bf5-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="e6bf5-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="e6bf5-135">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="e6bf5-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="e6bf5-136">-Atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="e6bf5-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="e6bf5-137">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="e6bf5-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="e6bf5-138">-Un atributo o elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="e6bf5-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="e6bf5-139">-Un intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="e6bf5-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="e6bf5-140">-Un error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="e6bf5-140">-  A server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="e6bf5-141">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="e6bf5-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e6bf5-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e6bf5-142">Child elements</span></span>

|<span data-ttu-id="e6bf5-143">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e6bf5-143">**Element**</span></span>|<span data-ttu-id="e6bf5-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e6bf5-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6bf5-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="e6bf5-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="e6bf5-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="e6bf5-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e6bf5-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="e6bf5-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="e6bf5-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e6bf5-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="e6bf5-150">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="e6bf5-151">Contiene el valor de 0.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-151">It contains the value of 0.</span></span>  <br/> |
|[<span data-ttu-id="e6bf5-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="e6bf5-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="e6bf5-153">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e6bf5-154">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e6bf5-154">Parent elements</span></span>

|<span data-ttu-id="e6bf5-155">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e6bf5-155">**Element**</span></span>|<span data-ttu-id="e6bf5-156">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e6bf5-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6bf5-157">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e6bf5-157">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="e6bf5-158">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-158">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e6bf5-159">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e6bf5-159">Text value</span></span>

<span data-ttu-id="e6bf5-160">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-160">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e6bf5-161">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e6bf5-161">Remarks</span></span>

<span data-ttu-id="e6bf5-162">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e6bf5-162">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e6bf5-163">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e6bf5-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e6bf5-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="e6bf5-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e6bf5-165">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e6bf5-165">Schema Name</span></span>  <br/> |<span data-ttu-id="e6bf5-166">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="e6bf5-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e6bf5-167">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e6bf5-167">Validation File</span></span>  <br/> |<span data-ttu-id="e6bf5-168">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e6bf5-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e6bf5-169">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e6bf5-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="e6bf5-170">Falso</span><span class="sxs-lookup"><span data-stu-id="e6bf5-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e6bf5-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6bf5-171">See also</span></span>

- [<span data-ttu-id="e6bf5-172">Operación EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="e6bf5-172">EmptyFolder operation</span></span>](emptyfolder-operation.md)
- [<span data-ttu-id="e6bf5-173">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="e6bf5-173">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="e6bf5-174">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e6bf5-174">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

