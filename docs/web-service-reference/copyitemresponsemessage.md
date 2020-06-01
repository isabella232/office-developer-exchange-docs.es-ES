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
ms.openlocfilehash: 99449a4c05d0b2ea13dfca4235aa5f40d54d1214
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466447"
---
# <a name="copyitemresponsemessage"></a><span data-ttu-id="50f1f-103">CopyItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="50f1f-103">CopyItemResponseMessage</span></span>

<span data-ttu-id="50f1f-104">El elemento **CopyItemResponseMessage** contiene el estado y el resultado de una única solicitud de [operación CopyItem](copyitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="50f1f-104">The **CopyItemResponseMessage** element contains the status and result of a single [CopyItem operation](copyitem-operation.md) request.</span></span> 
  
```xml
<CopyItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</CopyItemResponseMessage>
```

 <span data-ttu-id="50f1f-105">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="50f1f-105">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="50f1f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="50f1f-106">Attributes and elements</span></span>

<span data-ttu-id="50f1f-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="50f1f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="50f1f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="50f1f-108">Attributes</span></span>

|<span data-ttu-id="50f1f-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="50f1f-109">**Attribute**</span></span>|<span data-ttu-id="50f1f-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="50f1f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="50f1f-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="50f1f-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="50f1f-112">Describe el estado de una respuesta de la [operación CopyItem](copyitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="50f1f-112">Describes the status of a [CopyItem operation](copyitem-operation.md) response.</span></span><br/><br/><span data-ttu-id="50f1f-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="50f1f-113">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="50f1f-114">-Correcto</span><span class="sxs-lookup"><span data-stu-id="50f1f-114">- Success</span></span>  <br/><span data-ttu-id="50f1f-115">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="50f1f-115">-  Warning</span></span>  <br/><span data-ttu-id="50f1f-116">-Error</span><span class="sxs-lookup"><span data-stu-id="50f1f-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="50f1f-117">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="50f1f-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="50f1f-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="50f1f-118">**Value**</span></span>|<span data-ttu-id="50f1f-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="50f1f-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="50f1f-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="50f1f-120">**Success**</span></span> <br/> |<span data-ttu-id="50f1f-121">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="50f1f-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="50f1f-122">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="50f1f-122">**Warning**</span></span> <br/> | <span data-ttu-id="50f1f-123">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="50f1f-123">Describes a request that was not processed.</span></span> <span data-ttu-id="50f1f-124">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="50f1f-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="50f1f-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="50f1f-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="50f1f-126">-El almacén de Exchange se desconecta durante el lote.</span><span class="sxs-lookup"><span data-stu-id="50f1f-126">- The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="50f1f-127">-Servicios de dominio de Active Directory (AD DS) se desconecta.</span><span class="sxs-lookup"><span data-stu-id="50f1f-127">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="50f1f-128">-Se mueven los buzones.</span><span class="sxs-lookup"><span data-stu-id="50f1f-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="50f1f-129">-La base de datos de buzones (MDB) se desconecta.</span><span class="sxs-lookup"><span data-stu-id="50f1f-129">-  The mailbox database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="50f1f-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="50f1f-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="50f1f-131">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="50f1f-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="50f1f-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="50f1f-132">**Error**</span></span> <br/> | <span data-ttu-id="50f1f-133">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="50f1f-133">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="50f1f-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="50f1f-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="50f1f-135">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="50f1f-135">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="50f1f-136">-Atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="50f1f-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="50f1f-137">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="50f1f-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="50f1f-138">-Atributo o elemento no válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="50f1f-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="50f1f-139">-Intento de acceso no autorizado por parte de un cliente</span><span class="sxs-lookup"><span data-stu-id="50f1f-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="50f1f-140">-Error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="50f1f-140">-  Server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="50f1f-141">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="50f1f-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="50f1f-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="50f1f-142">Child elements</span></span>

|<span data-ttu-id="50f1f-143">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="50f1f-143">**Element**</span></span>|<span data-ttu-id="50f1f-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="50f1f-144">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="50f1f-145">- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)</span><span class="sxs-lookup"><span data-stu-id="50f1f-145">- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)</span></span> <br/> [<span data-ttu-id="50f1f-146">MessageText</span><span class="sxs-lookup"><span data-stu-id="50f1f-146">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="50f1f-147">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="50f1f-147">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="50f1f-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="50f1f-148">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="50f1f-149">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="50f1f-149">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="50f1f-150">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="50f1f-150">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="50f1f-151">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="50f1f-151">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="50f1f-152">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="50f1f-152">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="50f1f-153">MessageXml</span><span class="sxs-lookup"><span data-stu-id="50f1f-153">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="50f1f-154">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="50f1f-154">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="50f1f-155">Items</span><span class="sxs-lookup"><span data-stu-id="50f1f-155">Items</span></span>](items.md) <br/> |<span data-ttu-id="50f1f-156">Contiene una matriz de elementos copiados</span><span class="sxs-lookup"><span data-stu-id="50f1f-156">Contains an array of copied items</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="50f1f-157">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="50f1f-157">Parent elements</span></span>

|<span data-ttu-id="50f1f-158">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="50f1f-158">**Element**</span></span>|<span data-ttu-id="50f1f-159">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="50f1f-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50f1f-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="50f1f-160">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="50f1f-161">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="50f1f-161">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50f1f-162">Comentarios</span><span class="sxs-lookup"><span data-stu-id="50f1f-162">Remarks</span></span>

<span data-ttu-id="50f1f-163">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="50f1f-163">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="50f1f-164">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="50f1f-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50f1f-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="50f1f-165">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="50f1f-166">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="50f1f-166">Schema name</span></span>  <br/> |<span data-ttu-id="50f1f-167">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="50f1f-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="50f1f-168">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="50f1f-168">Validation file</span></span>  <br/> |<span data-ttu-id="50f1f-169">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="50f1f-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="50f1f-170">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="50f1f-170">Can be empty</span></span>  <br/> |<span data-ttu-id="50f1f-171">Falso</span><span class="sxs-lookup"><span data-stu-id="50f1f-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="50f1f-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="50f1f-172">See also</span></span>

- [<span data-ttu-id="50f1f-173">Operación CopyItem</span><span class="sxs-lookup"><span data-stu-id="50f1f-173">CopyItem operation</span></span>](copyitem-operation.md)
- [<span data-ttu-id="50f1f-174">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="50f1f-174">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

