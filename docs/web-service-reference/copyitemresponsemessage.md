---
title: CopyItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyItemResponseMessage
api_type:
- schema
ms.assetid: a43fe442-12c8-44ab-912c-8a226c9bb3e7
description: El elemento CopyItemResponseMessage contiene el estado y el resultado de una única solicitud de operación CopyItem.
ms.openlocfilehash: 6c1acaff422fd731ca81a3ab244d76a73f3b5c15
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763903"
---
# <a name="copyitemresponsemessage"></a><span data-ttu-id="6263b-103">CopyItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6263b-103">CopyItemResponseMessage</span></span>

<span data-ttu-id="6263b-104">El elemento **CopyItemResponseMessage** contiene el estado y el resultado de una única solicitud de [operación CopyItem](copyitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="6263b-104">The **CopyItemResponseMessage** element contains the status and result of a single [CopyItem operation](copyitem-operation.md) request.</span></span> 
  
```xml
<CopyItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</CopyItemResponseMessage>
```

 <span data-ttu-id="6263b-105">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="6263b-105">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6263b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6263b-106">Attributes and elements</span></span>

<span data-ttu-id="6263b-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6263b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6263b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6263b-108">Attributes</span></span>

|<span data-ttu-id="6263b-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="6263b-109">**Attribute**</span></span>|<span data-ttu-id="6263b-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6263b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6263b-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="6263b-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="6263b-112">Describe el estado de una respuesta de [la operación CopyItem](copyitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="6263b-112">Describes the status of a [CopyItem operation](copyitem-operation.md) response.</span></span><br/><br/><span data-ttu-id="6263b-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="6263b-113">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="6263b-114">-Éxito</span><span class="sxs-lookup"><span data-stu-id="6263b-114">- Success</span></span>  <br/><span data-ttu-id="6263b-115">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="6263b-115">-  Warning</span></span>  <br/><span data-ttu-id="6263b-116">-Error</span><span class="sxs-lookup"><span data-stu-id="6263b-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="6263b-117">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="6263b-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="6263b-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6263b-118">**Value**</span></span>|<span data-ttu-id="6263b-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6263b-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6263b-120">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="6263b-120">**Success**</span></span> <br/> |<span data-ttu-id="6263b-121">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="6263b-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="6263b-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="6263b-122">**Warning**</span></span> <br/> | <span data-ttu-id="6263b-123">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="6263b-123">Describes a request that was not processed.</span></span> <span data-ttu-id="6263b-124">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="6263b-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="6263b-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="6263b-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="6263b-126">-El almacén de Exchange se desconecta durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="6263b-126">- The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="6263b-127">-Los servicios de dominio de Active Directory (AD DS) se queda sin conexión.</span><span class="sxs-lookup"><span data-stu-id="6263b-127">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="6263b-128">-Se mueven los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="6263b-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="6263b-129">-La base de datos de buzón (MDB) se queda sin conexión.</span><span class="sxs-lookup"><span data-stu-id="6263b-129">-  The mailbox database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="6263b-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="6263b-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="6263b-131">-Se ha excedido una cuota.</span><span class="sxs-lookup"><span data-stu-id="6263b-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="6263b-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="6263b-132">**Error**</span></span> <br/> | <span data-ttu-id="6263b-133">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="6263b-133">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="6263b-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="6263b-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="6263b-135">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="6263b-135">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="6263b-136">-Los atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="6263b-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="6263b-137">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="6263b-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="6263b-138">-De atributo o elemento no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="6263b-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="6263b-139">-Intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="6263b-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="6263b-140">-Error server-side en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="6263b-140">-  Server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="6263b-141">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="6263b-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6263b-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6263b-142">Child elements</span></span>

|<span data-ttu-id="6263b-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="6263b-143">**Element**</span></span>|<span data-ttu-id="6263b-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6263b-144">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6263b-145">- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)</span><span class="sxs-lookup"><span data-stu-id="6263b-145">- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)</span></span> <br/> [<span data-ttu-id="6263b-146">MessageText</span><span class="sxs-lookup"><span data-stu-id="6263b-146">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="6263b-147">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6263b-147">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="6263b-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="6263b-148">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="6263b-149">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6263b-149">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="6263b-150">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="6263b-150">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="6263b-151">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="6263b-151">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="6263b-152">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="6263b-152">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="6263b-153">MessageXml</span><span class="sxs-lookup"><span data-stu-id="6263b-153">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="6263b-154">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="6263b-154">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="6263b-155">Items</span><span class="sxs-lookup"><span data-stu-id="6263b-155">Items</span></span>](items.md) <br/> |<span data-ttu-id="6263b-156">Contiene una matriz de elementos copiados</span><span class="sxs-lookup"><span data-stu-id="6263b-156">Contains an array of copied items</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6263b-157">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6263b-157">Parent elements</span></span>

|<span data-ttu-id="6263b-158">**Element**</span><span class="sxs-lookup"><span data-stu-id="6263b-158">**Element**</span></span>|<span data-ttu-id="6263b-159">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6263b-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6263b-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="6263b-160">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="6263b-161">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6263b-161">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6263b-162">Notas</span><span class="sxs-lookup"><span data-stu-id="6263b-162">Remarks</span></span>

<span data-ttu-id="6263b-163">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="6263b-163">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6263b-164">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6263b-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6263b-165">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6263b-165">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6263b-166">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6263b-166">Schema name</span></span>  <br/> |<span data-ttu-id="6263b-167">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="6263b-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6263b-168">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6263b-168">Validation file</span></span>  <br/> |<span data-ttu-id="6263b-169">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6263b-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6263b-170">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6263b-170">Can be empty</span></span>  <br/> |<span data-ttu-id="6263b-171">False</span><span class="sxs-lookup"><span data-stu-id="6263b-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6263b-172">Ver también</span><span class="sxs-lookup"><span data-stu-id="6263b-172">See also</span></span>

- [<span data-ttu-id="6263b-173">Operación CopyItem</span><span class="sxs-lookup"><span data-stu-id="6263b-173">CopyItem operation</span></span>](copyitem-operation.md)
- [<span data-ttu-id="6263b-174">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="6263b-174">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

