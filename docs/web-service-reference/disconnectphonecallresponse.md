---
title: DisconnectPhoneCallResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DisconnectPhoneCallResponse
api_type:
- schema
ms.assetid: 05041799-5b81-4b87-ada8-ce6c506ffe01
description: El elemento DisconnectPhoneCallResponse contiene el estado y el resultado de una sola solicitud DisconnectPhoneCall.
ms.openlocfilehash: 6c0696a1d9ab3242920d051b409105644a6b03aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458449"
---
# <a name="disconnectphonecallresponse"></a><span data-ttu-id="cb543-103">DisconnectPhoneCallResponse</span><span class="sxs-lookup"><span data-stu-id="cb543-103">DisconnectPhoneCallResponse</span></span>

<span data-ttu-id="cb543-104">El elemento **DisconnectPhoneCallResponse** contiene el estado y el resultado de una sola solicitud **DisconnectPhoneCall** .</span><span class="sxs-lookup"><span data-stu-id="cb543-104">The **DisconnectPhoneCallResponse** element contains the status and result of a single **DisconnectPhoneCall** request.</span></span> 
  
```xml
<DisconnectPhoneCallResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</DisconnectPhoneCallResponse>
```

 <span data-ttu-id="cb543-105">**DisconnectPhoneCallResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="cb543-105">**DisconnectPhoneCallResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cb543-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cb543-106">Attributes and elements</span></span>

<span data-ttu-id="cb543-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cb543-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb543-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="cb543-108">Attributes</span></span>

|<span data-ttu-id="cb543-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="cb543-109">**Attribute**</span></span>|<span data-ttu-id="cb543-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cb543-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cb543-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="cb543-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="cb543-112">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cb543-112">Describes the status of the response.</span></span><br/><br/><span data-ttu-id="cb543-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="cb543-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="cb543-114">-Correcto</span><span class="sxs-lookup"><span data-stu-id="cb543-114">-  Success</span></span>  <br/><span data-ttu-id="cb543-115">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="cb543-115">-  Warning</span></span>  <br/><span data-ttu-id="cb543-116">-Error</span><span class="sxs-lookup"><span data-stu-id="cb543-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="cb543-117">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="cb543-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="cb543-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cb543-118">**Value**</span></span>|<span data-ttu-id="cb543-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cb543-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cb543-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="cb543-120">**Success**</span></span> <br/> |<span data-ttu-id="cb543-121">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="cb543-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="cb543-122">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="cb543-122">**Warning**</span></span> <br/> | <span data-ttu-id="cb543-123">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="cb543-123">Describes a request that was not processed.</span></span> <span data-ttu-id="cb543-124">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="cb543-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="cb543-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="cb543-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="cb543-126">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="cb543-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="cb543-127">-Los servicios de dominio de Active Directory (AD DS) están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="cb543-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="cb543-128">-Se movieron los buzones.</span><span class="sxs-lookup"><span data-stu-id="cb543-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="cb543-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="cb543-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="cb543-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="cb543-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="cb543-131">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="cb543-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="cb543-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="cb543-132">**Error**</span></span> <br/> | <span data-ttu-id="cb543-133">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="cb543-133">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="cb543-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="cb543-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="cb543-135">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="cb543-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="cb543-136">-Atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="cb543-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="cb543-137">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="cb543-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="cb543-138">-Un atributo o elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="cb543-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="cb543-139">-Un intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="cb543-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="cb543-140">-Un error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="cb543-140">-  A server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="cb543-141">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="cb543-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cb543-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cb543-142">Child elements</span></span>

|<span data-ttu-id="cb543-143">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cb543-143">**Element**</span></span>|<span data-ttu-id="cb543-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cb543-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb543-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="cb543-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="cb543-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cb543-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="cb543-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="cb543-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="cb543-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cb543-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="cb543-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="cb543-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="cb543-150">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="cb543-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="cb543-151">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="cb543-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="cb543-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="cb543-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="cb543-153">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="cb543-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cb543-154">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cb543-154">Parent elements</span></span>

<span data-ttu-id="cb543-155">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cb543-155">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="cb543-156">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="cb543-156">Text value</span></span>

<span data-ttu-id="cb543-157">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cb543-157">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cb543-158">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cb543-158">Remarks</span></span>

<span data-ttu-id="cb543-159">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="cb543-159">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cb543-160">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cb543-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb543-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="cb543-161">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cb543-162">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cb543-162">Schema Name</span></span>  <br/> |<span data-ttu-id="cb543-163">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="cb543-163">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cb543-164">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cb543-164">Validation File</span></span>  <br/> |<span data-ttu-id="cb543-165">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="cb543-165">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cb543-166">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cb543-166">Can be Empty</span></span>  <br/> |<span data-ttu-id="cb543-167">Falso</span><span class="sxs-lookup"><span data-stu-id="cb543-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb543-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb543-168">See also</span></span>

- [<span data-ttu-id="cb543-169">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="cb543-169">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

