---
title: GetRoomsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetRoomsResponse
api_type:
- schema
ms.assetid: a8c85f65-bb63-4e7a-b0ca-7c9a04560a58
description: El elemento GetRoomsResponse define una respuesta a una solicitud de operación GetRooms.
ms.openlocfilehash: 7399ab910a99b39757eb752b11a4771ba81be46a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764965"
---
# <a name="getroomsresponse"></a><span data-ttu-id="2946f-103">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="2946f-103">GetRoomsResponse</span></span>

<span data-ttu-id="2946f-104">El elemento **GetRoomsResponse** define una respuesta a una solicitud de [operación GetRooms](getrooms-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="2946f-104">The **GetRoomsResponse** element defines a response to a [GetRooms operation](getrooms-operation.md) request.</span></span> 
  
- [<span data-ttu-id="2946f-105">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2946f-105">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="2946f-106">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="2946f-106">GetRoomsResponse</span></span>](getroomsresponse.md)
  
```XML
<GetRoomsResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Rooms/>
</GetRoomsResponse>
```

 <span data-ttu-id="2946f-107">**GetRoomsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2946f-107">**GetRoomsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2946f-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2946f-108">Attributes and elements</span></span>

<span data-ttu-id="2946f-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2946f-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2946f-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="2946f-110">Attributes</span></span>

|<span data-ttu-id="2946f-111">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="2946f-111">**Attribute**</span></span>|<span data-ttu-id="2946f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2946f-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2946f-113">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="2946f-113">**ResponseClass**</span></span> <br/> | <span data-ttu-id="2946f-114">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2946f-114">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="2946f-115">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="2946f-115">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="2946f-116">-Éxito</span><span class="sxs-lookup"><span data-stu-id="2946f-116">-  Success</span></span>  <br/><span data-ttu-id="2946f-117">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="2946f-117">-  Warning</span></span>  <br/><span data-ttu-id="2946f-118">-Error</span><span class="sxs-lookup"><span data-stu-id="2946f-118">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="2946f-119">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="2946f-119">ResponseClass attribute values</span></span>

|<span data-ttu-id="2946f-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2946f-120">**Value**</span></span>|<span data-ttu-id="2946f-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2946f-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2946f-122">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="2946f-122">**Success**</span></span> <br/> |<span data-ttu-id="2946f-123">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="2946f-123">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="2946f-124">**Warning**</span><span class="sxs-lookup"><span data-stu-id="2946f-124">**Warning**</span></span> <br/> | <span data-ttu-id="2946f-125">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="2946f-125">Describes a request that was not processed.</span></span> <span data-ttu-id="2946f-126">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="2946f-126">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="2946f-127">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="2946f-127">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="2946f-128">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="2946f-128">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="2946f-129">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="2946f-129">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="2946f-130">-Buzones se han movido.</span><span class="sxs-lookup"><span data-stu-id="2946f-130">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="2946f-131">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="2946f-131">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="2946f-132">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="2946f-132">-  A password is expired.</span></span>  <br/><span data-ttu-id="2946f-133">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="2946f-133">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="2946f-134">**Error**</span><span class="sxs-lookup"><span data-stu-id="2946f-134">**Error**</span></span> <br/> | <span data-ttu-id="2946f-135">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="2946f-135">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="2946f-136">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="2946f-136">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="2946f-137">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="2946f-137">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="2946f-138">-Los atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="2946f-138">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="2946f-139">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="2946f-139">-  An unknown tag</span></span>  <br/><span data-ttu-id="2946f-140">-Un atributo o un elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="2946f-140">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="2946f-141">-Un intento de acceso no autorizado por cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="2946f-141">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="2946f-142">-Un error del lado del servidor en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="2946f-142">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="2946f-143">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="2946f-143">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2946f-144">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2946f-144">Child elements</span></span>

|<span data-ttu-id="2946f-145">**Element**</span><span class="sxs-lookup"><span data-stu-id="2946f-145">**Element**</span></span>|<span data-ttu-id="2946f-146">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2946f-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2946f-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="2946f-147">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="2946f-148">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2946f-148">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="2946f-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2946f-149">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="2946f-150">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2946f-150">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="2946f-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2946f-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="2946f-152">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="2946f-152">Currently unused and reserved for future use.</span></span> <span data-ttu-id="2946f-153">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="2946f-153">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="2946f-154">MessageXml</span><span class="sxs-lookup"><span data-stu-id="2946f-154">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="2946f-155">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="2946f-155">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="2946f-156">Salones</span><span class="sxs-lookup"><span data-stu-id="2946f-156">Rooms</span></span>](rooms.md) <br/> |<span data-ttu-id="2946f-157">Proporciona una lista de direcciones de correo electrónico y nombres para mostrar que representan las salas de reuniones.</span><span class="sxs-lookup"><span data-stu-id="2946f-157">Provides a list of email addresses and display names that represent meeting rooms.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2946f-158">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2946f-158">Parent elements</span></span>

|<span data-ttu-id="2946f-159">**Element**</span><span class="sxs-lookup"><span data-stu-id="2946f-159">**Element**</span></span>|<span data-ttu-id="2946f-160">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2946f-160">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2946f-161">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2946f-161">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="2946f-162">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2946f-162">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2946f-163">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2946f-163">Remarks</span></span>

<span data-ttu-id="2946f-164">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="2946f-164">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2946f-165">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2946f-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2946f-166">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2946f-166">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2946f-167">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2946f-167">Schema Name</span></span>  <br/> |<span data-ttu-id="2946f-168">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="2946f-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2946f-169">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2946f-169">Validation File</span></span>  <br/> |<span data-ttu-id="2946f-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2946f-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2946f-171">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2946f-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="2946f-172">False</span><span class="sxs-lookup"><span data-stu-id="2946f-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2946f-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="2946f-173">See also</span></span>

- [<span data-ttu-id="2946f-174">Operación GetRooms</span><span class="sxs-lookup"><span data-stu-id="2946f-174">GetRooms operation</span></span>](getrooms-operation.md)
- [<span data-ttu-id="2946f-175">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="2946f-175">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

