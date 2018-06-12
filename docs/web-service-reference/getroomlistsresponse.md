---
title: GetRoomListsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetRoomListsResponse
api_type:
- schema
ms.assetid: 8c736f68-1026-496a-b12f-c169c078abd0
description: El elemento GetRoomListsResponse define la respuesta de una solicitud de operación GetRoomLists.
ms.openlocfilehash: 8231435f7dc348a070852f57d6152550326b5df6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764971"
---
# <a name="getroomlistsresponse"></a><span data-ttu-id="b9fa6-103">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="b9fa6-103">GetRoomListsResponse</span></span>

<span data-ttu-id="b9fa6-104">El elemento **GetRoomListsResponse** define la respuesta de una solicitud de [operación GetRoomLists](getroomlists-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="b9fa6-104">The **GetRoomListsResponse** element defines the response from a [GetRoomLists operation](getroomlists-operation.md) request.</span></span> 
  
- [<span data-ttu-id="b9fa6-105">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b9fa6-105">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="b9fa6-106">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="b9fa6-106">GetRoomListsResponse</span></span>](getroomlistsresponse.md)
  
```XML
<GetRoomListsResponse ResponseClass="">   
<MessageText/>   
<ResponseCode/>   
<DescriptiveLinkKey/>   
<MessageXml/>   
<RoomLists/>
</GetRoomListsResponse>
```

 <span data-ttu-id="b9fa6-107">**GetRoomListsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="b9fa6-107">**GetRoomListsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b9fa6-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b9fa6-108">Attributes and elements</span></span>

<span data-ttu-id="b9fa6-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b9fa6-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="b9fa6-110">Attributes</span></span>

|<span data-ttu-id="b9fa6-111">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="b9fa6-111">**Attribute**</span></span>|<span data-ttu-id="b9fa6-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b9fa6-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b9fa6-113">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="b9fa6-113">**ResponseClass**</span></span> <br/> | <span data-ttu-id="b9fa6-114">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-114">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="b9fa6-115">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="b9fa6-115">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="b9fa6-116">-Éxito</span><span class="sxs-lookup"><span data-stu-id="b9fa6-116">-  Success</span></span>  <br/><span data-ttu-id="b9fa6-117">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="b9fa6-117">-  Warning</span></span>  <br/><span data-ttu-id="b9fa6-118">-Error</span><span class="sxs-lookup"><span data-stu-id="b9fa6-118">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="b9fa6-119">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="b9fa6-119">ResponseClass attribute values</span></span>

|<span data-ttu-id="b9fa6-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b9fa6-120">**Value**</span></span>|<span data-ttu-id="b9fa6-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b9fa6-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b9fa6-122">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="b9fa6-122">**Success**</span></span> <br/> |<span data-ttu-id="b9fa6-123">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-123">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="b9fa6-124">**Warning**</span><span class="sxs-lookup"><span data-stu-id="b9fa6-124">**Warning**</span></span> <br/> | <span data-ttu-id="b9fa6-125">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-125">Describes a request that was not processed.</span></span> <span data-ttu-id="b9fa6-126">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-126">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="b9fa6-127">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="b9fa6-127">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="b9fa6-128">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-128">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="b9fa6-129">-El servicio de directorio de Active Directory está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-129">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="b9fa6-130">-Buzones se han movido.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-130">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="b9fa6-131">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-131">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="b9fa6-132">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-132">-  A password is expired.</span></span>  <br/><span data-ttu-id="b9fa6-133">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-133">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="b9fa6-134">**Error**</span><span class="sxs-lookup"><span data-stu-id="b9fa6-134">**Error**</span></span> <br/> | <span data-ttu-id="b9fa6-135">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-135">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="b9fa6-136">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="b9fa6-136">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="b9fa6-137">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="b9fa6-137">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="b9fa6-138">-Los atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="b9fa6-138">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="b9fa6-139">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="b9fa6-139">-  Unknown tag</span></span>  <br/><span data-ttu-id="b9fa6-140">-De atributo o elemento no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="b9fa6-140">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="b9fa6-141">-Intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="b9fa6-141">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="b9fa6-142">-Error server-side en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="b9fa6-142">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="b9fa6-143">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="b9fa6-143">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/>- |
   
### <a name="child-elements"></a><span data-ttu-id="b9fa6-144">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b9fa6-144">Child elements</span></span>

|<span data-ttu-id="b9fa6-145">**Element**</span><span class="sxs-lookup"><span data-stu-id="b9fa6-145">**Element**</span></span>|<span data-ttu-id="b9fa6-146">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b9fa6-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b9fa6-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="b9fa6-147">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="b9fa6-148">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-148">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="b9fa6-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b9fa6-149">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="b9fa6-150">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-150">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="b9fa6-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="b9fa6-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="b9fa6-152">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-152">Currently unused and reserved for future use.</span></span> <span data-ttu-id="b9fa6-153">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-153">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="b9fa6-154">MessageXml</span><span class="sxs-lookup"><span data-stu-id="b9fa6-154">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="b9fa6-155">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-155">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="b9fa6-156">RoomLists</span><span class="sxs-lookup"><span data-stu-id="b9fa6-156">RoomLists</span></span>](roomlists.md) <br/> |<span data-ttu-id="b9fa6-157">Proporciona una lista de direcciones de correo electrónico y nombres para mostrar que representan las listas de las salas de reuniones.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-157">Provides a list of e-mail addresses and display names that represent lists of meeting rooms.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b9fa6-158">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b9fa6-158">Parent elements</span></span>

|<span data-ttu-id="b9fa6-159">**Element**</span><span class="sxs-lookup"><span data-stu-id="b9fa6-159">**Element**</span></span>|<span data-ttu-id="b9fa6-160">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b9fa6-160">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b9fa6-161">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b9fa6-161">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="b9fa6-162">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-162">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="b9fa6-163">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b9fa6-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b9fa6-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b9fa6-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b9fa6-165">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b9fa6-165">Schema Name</span></span>  <br/> |<span data-ttu-id="b9fa6-166">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b9fa6-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b9fa6-167">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b9fa6-167">Validation File</span></span>  <br/> |<span data-ttu-id="b9fa6-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b9fa6-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b9fa6-169">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b9fa6-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="b9fa6-170">False</span><span class="sxs-lookup"><span data-stu-id="b9fa6-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b9fa6-171">Ver también</span><span class="sxs-lookup"><span data-stu-id="b9fa6-171">See also</span></span>

- [<span data-ttu-id="b9fa6-172">Operación GetRoomLists</span><span class="sxs-lookup"><span data-stu-id="b9fa6-172">GetRoomLists operation</span></span>](getroomlists-operation.md)
- [<span data-ttu-id="b9fa6-173">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b9fa6-173">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

