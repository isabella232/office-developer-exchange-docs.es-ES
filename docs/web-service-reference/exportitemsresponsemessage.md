---
title: ExportItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExportItemsResponseMessage
api_type:
- schema
ms.assetid: 830fb008-3c45-4988-9041-91a3da3fe689
description: El elemento ExportItemsResponseMessage contiene el estado y los resultados de una solicitud para exportar un solo elemento de buzón.
ms.openlocfilehash: 3265836ce6d9d6ef97a4e598bbb3f50e7c5047c6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468949"
---
# <a name="exportitemsresponsemessage"></a><span data-ttu-id="cd238-103">ExportItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="cd238-103">ExportItemsResponseMessage</span></span>

<span data-ttu-id="cd238-104">El elemento **ExportItemsResponseMessage** contiene el estado y los resultados de una solicitud para exportar un solo elemento de buzón.</span><span class="sxs-lookup"><span data-stu-id="cd238-104">The **ExportItemsResponseMessage** element contains the status and results of a request to export a single mailbox item.</span></span> 
  
- [<span data-ttu-id="cd238-105">ExportItemsResponse</span><span class="sxs-lookup"><span data-stu-id="cd238-105">ExportItemsResponse</span></span>](exportitemsresponse.md)  
- [<span data-ttu-id="cd238-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="cd238-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="cd238-107">ExportItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="cd238-107">ExportItemsResponseMessage</span></span>](exportitemsresponsemessage.md)
  
```XML
<ExportItemsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ItemId/>
   <Data/>
</ExportItemsResponseMessage>
```

<span data-ttu-id="cd238-108">**ExportItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="cd238-108">**ExportItemsResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="cd238-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cd238-109">Attributes and elements</span></span>

<span data-ttu-id="cd238-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cd238-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd238-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="cd238-111">Attributes</span></span>

|<span data-ttu-id="cd238-112">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="cd238-112">**Attribute**</span></span>|<span data-ttu-id="cd238-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cd238-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd238-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="cd238-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="cd238-115">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cd238-115">Describes the status of the response.</span></span><br/><br/> <span data-ttu-id="cd238-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="cd238-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="cd238-117">-Correcto</span><span class="sxs-lookup"><span data-stu-id="cd238-117">-  Success</span></span>  <br/><span data-ttu-id="cd238-118">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="cd238-118">-  Warning</span></span>  <br/><span data-ttu-id="cd238-119">-Error</span><span class="sxs-lookup"><span data-stu-id="cd238-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="cd238-120">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="cd238-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="cd238-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cd238-121">**Value**</span></span>|<span data-ttu-id="cd238-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cd238-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd238-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="cd238-123">**Success**</span></span> <br/> |<span data-ttu-id="cd238-124">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="cd238-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="cd238-125">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="cd238-125">**Warning**</span></span> <br/> | <span data-ttu-id="cd238-126">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="cd238-126">Describes a request that was not processed.</span></span> <span data-ttu-id="cd238-127">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="cd238-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="cd238-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="cd238-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="cd238-129">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="cd238-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="cd238-130">-Los servicios de dominio de Active Directory (AD DS) están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="cd238-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="cd238-131">-Se movieron los buzones.</span><span class="sxs-lookup"><span data-stu-id="cd238-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="cd238-132">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="cd238-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="cd238-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="cd238-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="cd238-134">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="cd238-134">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="cd238-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="cd238-135">**Error**</span></span> <br/> | <span data-ttu-id="cd238-136">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="cd238-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="cd238-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="cd238-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="cd238-138">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="cd238-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="cd238-139">-Atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="cd238-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="cd238-140">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="cd238-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="cd238-141">-Un atributo o elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="cd238-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="cd238-142">-Un intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="cd238-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="cd238-143">-Un error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="cd238-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="cd238-144">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="cd238-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cd238-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cd238-145">Child elements</span></span>

|<span data-ttu-id="cd238-146">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cd238-146">**Element**</span></span>|<span data-ttu-id="cd238-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cd238-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd238-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="cd238-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="cd238-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cd238-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="cd238-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="cd238-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="cd238-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cd238-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="cd238-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="cd238-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="cd238-153">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="cd238-153">Currently unused and reserved for future use.</span></span> <span data-ttu-id="cd238-154">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="cd238-154">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="cd238-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="cd238-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="cd238-156">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="cd238-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="cd238-157">ItemId</span><span class="sxs-lookup"><span data-stu-id="cd238-157">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="cd238-158">Contiene el identificador de elemento de un elemento exportado.</span><span class="sxs-lookup"><span data-stu-id="cd238-158">Contains the item identifier of an exported item.</span></span>  <br/> |
|[<span data-ttu-id="cd238-159">Datos (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="cd238-159">Data (base64Binary)</span></span>](data-base64binary.md) <br/> |<span data-ttu-id="cd238-160">Contiene el contenido de un elemento exportado.</span><span class="sxs-lookup"><span data-stu-id="cd238-160">Contains the contents of an exported item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cd238-161">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cd238-161">Parent elements</span></span>

|<span data-ttu-id="cd238-162">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cd238-162">**Element**</span></span>|<span data-ttu-id="cd238-163">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cd238-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd238-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="cd238-164">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="cd238-165">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="cd238-165">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cd238-166">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="cd238-166">Text value</span></span>

<span data-ttu-id="cd238-167">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cd238-167">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cd238-168">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cd238-168">Remarks</span></span>

<span data-ttu-id="cd238-169">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="cd238-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cd238-170">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cd238-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd238-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd238-171">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cd238-172">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cd238-172">Schema Name</span></span>  <br/> |<span data-ttu-id="cd238-173">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="cd238-173">Message schema</span></span>  <br/> |
|<span data-ttu-id="cd238-174">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cd238-174">Validation File</span></span>  <br/> |<span data-ttu-id="cd238-175">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="cd238-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cd238-176">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cd238-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="cd238-177">Falso</span><span class="sxs-lookup"><span data-stu-id="cd238-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cd238-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd238-178">See also</span></span>

- [<span data-ttu-id="cd238-179">Operación ExportItems</span><span class="sxs-lookup"><span data-stu-id="cd238-179">ExportItems operation</span></span>](exportitems-operation.md) 
- [<span data-ttu-id="cd238-180">Operación UploadItems</span><span class="sxs-lookup"><span data-stu-id="cd238-180">UploadItems operation</span></span>](uploaditems-operation.md)

