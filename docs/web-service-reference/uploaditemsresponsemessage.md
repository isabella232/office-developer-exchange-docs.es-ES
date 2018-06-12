---
title: UploadItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UploadItemsResponseMessage
api_type:
- schema
ms.assetid: 03febd08-c015-4009-b291-1b4296182ffe
description: El elemento UploadItemsResponseMessage contiene el estado y los resultados de una solicitud para cargar un elemento de un solo buzón de correo.
ms.openlocfilehash: 9a1a33011aa1e240ab7e15794e2e89401238ffda
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840886"
---
# <a name="uploaditemsresponsemessage"></a><span data-ttu-id="724fa-103">UploadItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="724fa-103">UploadItemsResponseMessage</span></span>

<span data-ttu-id="724fa-104">El elemento **UploadItemsResponseMessage** contiene el estado y los resultados de una solicitud para cargar un elemento de un solo buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="724fa-104">The **UploadItemsResponseMessage** element contains the status and results of a request to upload a single mailbox item.</span></span> 
  
- [<span data-ttu-id="724fa-105">UploadItemsResponse</span><span class="sxs-lookup"><span data-stu-id="724fa-105">UploadItemsResponse</span></span>](uploaditemsresponse.md) 
- [<span data-ttu-id="724fa-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="724fa-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="724fa-107">UploadItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="724fa-107">UploadItemsResponseMessage</span></span>](uploaditemsresponsemessage.md)
  
```XML
<UploadItemsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ItemId/>
</UploadItemsResponseMessage>
```

 <span data-ttu-id="724fa-108">**UploadItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="724fa-108">**UploadItemsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="724fa-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="724fa-109">Attributes and elements</span></span>

<span data-ttu-id="724fa-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="724fa-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="724fa-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="724fa-111">Attributes</span></span>

|<span data-ttu-id="724fa-112">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="724fa-112">**Attribute**</span></span>|<span data-ttu-id="724fa-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="724fa-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="724fa-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="724fa-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="724fa-115">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="724fa-115">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="724fa-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="724fa-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="724fa-117">-Éxito</span><span class="sxs-lookup"><span data-stu-id="724fa-117">-  Success</span></span>  <br/><span data-ttu-id="724fa-118">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="724fa-118">-  Warning</span></span>  <br/><span data-ttu-id="724fa-119">-Error</span><span class="sxs-lookup"><span data-stu-id="724fa-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="724fa-120">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="724fa-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="724fa-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="724fa-121">**Value**</span></span>|<span data-ttu-id="724fa-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="724fa-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="724fa-123">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="724fa-123">**Success**</span></span> <br/> |<span data-ttu-id="724fa-124">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="724fa-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="724fa-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="724fa-125">**Warning**</span></span> <br/> | <span data-ttu-id="724fa-126">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="724fa-126">Describes a request that was not processed.</span></span> <span data-ttu-id="724fa-127">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="724fa-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="724fa-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="724fa-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="724fa-129">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="724fa-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="724fa-130">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="724fa-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="724fa-131">-Buzones se han movido.</span><span class="sxs-lookup"><span data-stu-id="724fa-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="724fa-132">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="724fa-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="724fa-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="724fa-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="724fa-134">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="724fa-134">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="724fa-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="724fa-135">**Error**</span></span> <br/> | <span data-ttu-id="724fa-136">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="724fa-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="724fa-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="724fa-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="724fa-138">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="724fa-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="724fa-139">-Los atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="724fa-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="724fa-140">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="724fa-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="724fa-141">-Un atributo o un elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="724fa-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="724fa-142">-Un intento de acceso no autorizado por cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="724fa-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="724fa-143">-Un error del lado del servidor en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="724fa-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="724fa-144">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="724fa-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="724fa-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="724fa-145">Child elements</span></span>

|<span data-ttu-id="724fa-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="724fa-146">**Element**</span></span>|<span data-ttu-id="724fa-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="724fa-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="724fa-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="724fa-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="724fa-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="724fa-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="724fa-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="724fa-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="724fa-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="724fa-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="724fa-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="724fa-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="724fa-153">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="724fa-153">Currently unused and reserved for future use.</span></span> <span data-ttu-id="724fa-154">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="724fa-154">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="724fa-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="724fa-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="724fa-156">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="724fa-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="724fa-157">ItemId</span><span class="sxs-lookup"><span data-stu-id="724fa-157">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="724fa-158">Contiene el identificador del elemento de un elemento que se cargan.</span><span class="sxs-lookup"><span data-stu-id="724fa-158">Contains the item identifier of an uploaded item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="724fa-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="724fa-159">Parent elements</span></span>

|<span data-ttu-id="724fa-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="724fa-160">**Element**</span></span>|<span data-ttu-id="724fa-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="724fa-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="724fa-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="724fa-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="724fa-163">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="724fa-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="724fa-164">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="724fa-164">Text value</span></span>

<span data-ttu-id="724fa-165">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="724fa-165">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="724fa-166">Observaciones</span><span class="sxs-lookup"><span data-stu-id="724fa-166">Remarks</span></span>

<span data-ttu-id="724fa-167">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="724fa-167">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="724fa-168">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="724fa-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="724fa-169">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="724fa-169">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="724fa-170">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="724fa-170">Schema Name</span></span>  <br/> |<span data-ttu-id="724fa-171">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="724fa-171">Message schema</span></span>  <br/> |
|<span data-ttu-id="724fa-172">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="724fa-172">Validation File</span></span>  <br/> |<span data-ttu-id="724fa-173">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="724fa-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="724fa-174">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="724fa-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="724fa-175">False</span><span class="sxs-lookup"><span data-stu-id="724fa-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="724fa-176">Ver también</span><span class="sxs-lookup"><span data-stu-id="724fa-176">See also</span></span>

- [<span data-ttu-id="724fa-177">Operación ExportItems</span><span class="sxs-lookup"><span data-stu-id="724fa-177">ExportItems operation</span></span>](exportitems-operation.md)
- [<span data-ttu-id="724fa-178">Operación UploadItems</span><span class="sxs-lookup"><span data-stu-id="724fa-178">UploadItems operation</span></span>](uploaditems-operation.md)
- [<span data-ttu-id="724fa-179">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="724fa-179">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

