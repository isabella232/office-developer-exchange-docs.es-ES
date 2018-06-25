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
ms.openlocfilehash: 099dc799bedb527472bbe7d34cad0dbc8e98bec5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763965"
---
# <a name="createitemresponsemessage"></a><span data-ttu-id="0fd5b-103">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0fd5b-103">CreateItemResponseMessage</span></span>

<span data-ttu-id="0fd5b-104">El elemento **CreateItemResponseMessage** contiene el estado y el resultado de una única solicitud [CreateItem operation](createitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="0fd5b-104">The **CreateItemResponseMessage** element contains the status and result of a single [CreateItem operation](createitem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="0fd5b-105">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="0fd5b-105">CreateItemResponse</span></span>](createitemresponse.md)  
- [<span data-ttu-id="0fd5b-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0fd5b-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="0fd5b-107">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0fd5b-107">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
  
```xml
<CreateItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</CreateItemResponseMessage>
```

 <span data-ttu-id="0fd5b-108">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="0fd5b-108">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0fd5b-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0fd5b-109">Attributes and elements</span></span>

<span data-ttu-id="0fd5b-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0fd5b-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="0fd5b-111">Attributes</span></span>

|<span data-ttu-id="0fd5b-112">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="0fd5b-112">**Attribute**</span></span>|<span data-ttu-id="0fd5b-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0fd5b-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0fd5b-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="0fd5b-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="0fd5b-115">Describe el estado de una respuesta de [la operación CreateItem](createitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="0fd5b-115">Describes the status of a [CreateItem operation](createitem-operation.md) response.</span></span><br/><br/><span data-ttu-id="0fd5b-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="0fd5b-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="0fd5b-117">-Éxito</span><span class="sxs-lookup"><span data-stu-id="0fd5b-117">-  Success</span></span>  <br/><span data-ttu-id="0fd5b-118">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="0fd5b-118">-  Warning</span></span>  <br/><span data-ttu-id="0fd5b-119">-Error</span><span class="sxs-lookup"><span data-stu-id="0fd5b-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="0fd5b-120">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="0fd5b-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="0fd5b-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0fd5b-121">**Value**</span></span>|<span data-ttu-id="0fd5b-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0fd5b-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0fd5b-123">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="0fd5b-123">**Success**</span></span> <br/> |<span data-ttu-id="0fd5b-124">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="0fd5b-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="0fd5b-125">**Warning**</span></span> <br/> | <span data-ttu-id="0fd5b-126">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-126">Describes a request that was not processed.</span></span> <span data-ttu-id="0fd5b-127">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="0fd5b-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="0fd5b-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="0fd5b-129">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="0fd5b-130">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="0fd5b-131">-Se mueven los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="0fd5b-132">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="0fd5b-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="0fd5b-134">-Se ha excedido una cuota.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="0fd5b-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="0fd5b-135">**Error**</span></span> <br/> | <span data-ttu-id="0fd5b-136">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="0fd5b-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="0fd5b-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="0fd5b-138">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="0fd5b-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="0fd5b-139">-Los atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="0fd5b-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="0fd5b-140">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="0fd5b-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="0fd5b-141">-De atributo o elemento no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="0fd5b-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="0fd5b-142">-Intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="0fd5b-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="0fd5b-143">-Error server-side en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="0fd5b-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="0fd5b-144">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="0fd5b-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0fd5b-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0fd5b-145">Child elements</span></span>

|<span data-ttu-id="0fd5b-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="0fd5b-146">**Element**</span></span>|<span data-ttu-id="0fd5b-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0fd5b-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0fd5b-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="0fd5b-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="0fd5b-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="0fd5b-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0fd5b-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="0fd5b-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="0fd5b-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0fd5b-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="0fd5b-153">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="0fd5b-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="0fd5b-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="0fd5b-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="0fd5b-156">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="0fd5b-157">Items</span><span class="sxs-lookup"><span data-stu-id="0fd5b-157">Items</span></span>](items.md) <br/> |<span data-ttu-id="0fd5b-158">Contiene una matriz de elementos creados.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-158">Contains an array of created items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0fd5b-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0fd5b-159">Parent elements</span></span>

|<span data-ttu-id="0fd5b-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="0fd5b-160">**Element**</span></span>|<span data-ttu-id="0fd5b-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0fd5b-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0fd5b-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0fd5b-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="0fd5b-163">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0fd5b-164">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0fd5b-164">Remarks</span></span>

<span data-ttu-id="0fd5b-165">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0fd5b-166">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0fd5b-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0fd5b-167">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0fd5b-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0fd5b-168">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0fd5b-168">Schema Name</span></span>  <br/> |<span data-ttu-id="0fd5b-169">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="0fd5b-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0fd5b-170">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0fd5b-170">Validation File</span></span>  <br/> |<span data-ttu-id="0fd5b-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0fd5b-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0fd5b-172">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0fd5b-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="0fd5b-173">False</span><span class="sxs-lookup"><span data-stu-id="0fd5b-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0fd5b-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="0fd5b-174">See also</span></span>

- [<span data-ttu-id="0fd5b-175">Operación CreateItem</span><span class="sxs-lookup"><span data-stu-id="0fd5b-175">CreateItem operation</span></span>](createitem-operation.md)
- [<span data-ttu-id="0fd5b-176">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="0fd5b-176">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="0fd5b-177">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0fd5b-177">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

