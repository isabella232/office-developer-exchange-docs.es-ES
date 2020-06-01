---
title: CreateItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateItemResponseMessage
api_type:
- schema
ms.assetid: 595d36c2-f87a-4d50-8e8b-f58d7641564b
description: El elemento CreateItemResponseMessage contiene el estado y el resultado de una única solicitud de operación CreateItem.
ms.openlocfilehash: 6304d2c7a3c9253c03c07eb37e9a57226e794a24
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457854"
---
# <a name="createitemresponsemessage"></a><span data-ttu-id="a7f49-103">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a7f49-103">CreateItemResponseMessage</span></span>

<span data-ttu-id="a7f49-104">El elemento **CreateItemResponseMessage** contiene el estado y el resultado de una única solicitud de [operación CreateItem](createitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="a7f49-104">The **CreateItemResponseMessage** element contains the status and result of a single [CreateItem operation](createitem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="a7f49-105">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="a7f49-105">CreateItemResponse</span></span>](createitemresponse.md)  
- [<span data-ttu-id="a7f49-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a7f49-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="a7f49-107">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a7f49-107">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
  
```xml
<CreateItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</CreateItemResponseMessage>
```

 <span data-ttu-id="a7f49-108">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="a7f49-108">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a7f49-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a7f49-109">Attributes and elements</span></span>

<span data-ttu-id="a7f49-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a7f49-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a7f49-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="a7f49-111">Attributes</span></span>

|<span data-ttu-id="a7f49-112">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a7f49-112">**Attribute**</span></span>|<span data-ttu-id="a7f49-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a7f49-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a7f49-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="a7f49-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="a7f49-115">Describe el estado de una respuesta de la [operación CreateItem](createitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="a7f49-115">Describes the status of a [CreateItem operation](createitem-operation.md) response.</span></span><br/><br/><span data-ttu-id="a7f49-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="a7f49-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="a7f49-117">-Correcto</span><span class="sxs-lookup"><span data-stu-id="a7f49-117">-  Success</span></span>  <br/><span data-ttu-id="a7f49-118">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="a7f49-118">-  Warning</span></span>  <br/><span data-ttu-id="a7f49-119">-Error</span><span class="sxs-lookup"><span data-stu-id="a7f49-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="a7f49-120">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="a7f49-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="a7f49-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a7f49-121">**Value**</span></span>|<span data-ttu-id="a7f49-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a7f49-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a7f49-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="a7f49-123">**Success**</span></span> <br/> |<span data-ttu-id="a7f49-124">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="a7f49-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="a7f49-125">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="a7f49-125">**Warning**</span></span> <br/> | <span data-ttu-id="a7f49-126">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="a7f49-126">Describes a request that was not processed.</span></span> <span data-ttu-id="a7f49-127">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="a7f49-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="a7f49-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="a7f49-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="a7f49-129">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="a7f49-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="a7f49-130">-Los servicios de dominio de Active Directory (AD DS) están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="a7f49-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="a7f49-131">-Se mueven los buzones.</span><span class="sxs-lookup"><span data-stu-id="a7f49-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="a7f49-132">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="a7f49-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="a7f49-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="a7f49-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="a7f49-134">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="a7f49-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="a7f49-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="a7f49-135">**Error**</span></span> <br/> | <span data-ttu-id="a7f49-136">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="a7f49-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="a7f49-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="a7f49-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="a7f49-138">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="a7f49-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="a7f49-139">-Atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="a7f49-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="a7f49-140">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="a7f49-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="a7f49-141">-Atributo o elemento no válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="a7f49-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="a7f49-142">-Intento de acceso no autorizado por parte de un cliente</span><span class="sxs-lookup"><span data-stu-id="a7f49-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="a7f49-143">-Error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="a7f49-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="a7f49-144">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="a7f49-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a7f49-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a7f49-145">Child elements</span></span>

|<span data-ttu-id="a7f49-146">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a7f49-146">**Element**</span></span>|<span data-ttu-id="a7f49-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a7f49-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7f49-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="a7f49-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="a7f49-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a7f49-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="a7f49-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a7f49-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="a7f49-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a7f49-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="a7f49-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="a7f49-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="a7f49-153">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="a7f49-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="a7f49-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="a7f49-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="a7f49-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="a7f49-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="a7f49-156">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="a7f49-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="a7f49-157">Items</span><span class="sxs-lookup"><span data-stu-id="a7f49-157">Items</span></span>](items.md) <br/> |<span data-ttu-id="a7f49-158">Contiene una matriz de elementos creados.</span><span class="sxs-lookup"><span data-stu-id="a7f49-158">Contains an array of created items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a7f49-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a7f49-159">Parent elements</span></span>

|<span data-ttu-id="a7f49-160">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a7f49-160">**Element**</span></span>|<span data-ttu-id="a7f49-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a7f49-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7f49-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a7f49-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="a7f49-163">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a7f49-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7f49-164">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a7f49-164">Remarks</span></span>

<span data-ttu-id="a7f49-165">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="a7f49-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a7f49-166">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a7f49-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7f49-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="a7f49-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a7f49-168">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a7f49-168">Schema Name</span></span>  <br/> |<span data-ttu-id="a7f49-169">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="a7f49-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a7f49-170">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a7f49-170">Validation File</span></span>  <br/> |<span data-ttu-id="a7f49-171">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a7f49-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a7f49-172">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a7f49-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="a7f49-173">Falso</span><span class="sxs-lookup"><span data-stu-id="a7f49-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a7f49-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7f49-174">See also</span></span>

- [<span data-ttu-id="a7f49-175">Operación CreateItem</span><span class="sxs-lookup"><span data-stu-id="a7f49-175">CreateItem operation</span></span>](createitem-operation.md)
- [<span data-ttu-id="a7f49-176">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="a7f49-176">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="a7f49-177">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a7f49-177">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

