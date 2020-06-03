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
ms.openlocfilehash: b6d7c2baa2861309d72bcbf880eaed2ad0989175
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462946"
---
# <a name="getroomlistsresponse"></a><span data-ttu-id="cf4c0-103">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="cf4c0-103">GetRoomListsResponse</span></span>

<span data-ttu-id="cf4c0-104">El elemento **GetRoomListsResponse** define la respuesta de una solicitud de [operación GetRoomLists](getroomlists-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="cf4c0-104">The **GetRoomListsResponse** element defines the response from a [GetRoomLists operation](getroomlists-operation.md) request.</span></span> 
  
- [<span data-ttu-id="cf4c0-105">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="cf4c0-105">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="cf4c0-106">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="cf4c0-106">GetRoomListsResponse</span></span>](getroomlistsresponse.md)
  
```XML
<GetRoomListsResponse ResponseClass="">   
<MessageText/>   
<ResponseCode/>   
<DescriptiveLinkKey/>   
<MessageXml/>   
<RoomLists/>
</GetRoomListsResponse>
```

 <span data-ttu-id="cf4c0-107">**GetRoomListsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="cf4c0-107">**GetRoomListsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cf4c0-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cf4c0-108">Attributes and elements</span></span>

<span data-ttu-id="cf4c0-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cf4c0-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="cf4c0-110">Attributes</span></span>

|<span data-ttu-id="cf4c0-111">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="cf4c0-111">**Attribute**</span></span>|<span data-ttu-id="cf4c0-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf4c0-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf4c0-113">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="cf4c0-113">**ResponseClass**</span></span> <br/> | <span data-ttu-id="cf4c0-114">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-114">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="cf4c0-115">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="cf4c0-115">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="cf4c0-116">-Correcto</span><span class="sxs-lookup"><span data-stu-id="cf4c0-116">-  Success</span></span>  <br/><span data-ttu-id="cf4c0-117">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="cf4c0-117">-  Warning</span></span>  <br/><span data-ttu-id="cf4c0-118">-Error</span><span class="sxs-lookup"><span data-stu-id="cf4c0-118">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="cf4c0-119">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="cf4c0-119">ResponseClass attribute values</span></span>

|<span data-ttu-id="cf4c0-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cf4c0-120">**Value**</span></span>|<span data-ttu-id="cf4c0-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf4c0-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf4c0-122">**Success**</span><span class="sxs-lookup"><span data-stu-id="cf4c0-122">**Success**</span></span> <br/> |<span data-ttu-id="cf4c0-123">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-123">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="cf4c0-124">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="cf4c0-124">**Warning**</span></span> <br/> | <span data-ttu-id="cf4c0-125">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-125">Describes a request that was not processed.</span></span> <span data-ttu-id="cf4c0-126">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-126">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="cf4c0-127">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="cf4c0-127">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="cf4c0-128">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-128">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="cf4c0-129">-El servicio de directorio de Active Directory está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-129">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="cf4c0-130">-Se movieron los buzones.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-130">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="cf4c0-131">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-131">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="cf4c0-132">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-132">-  A password is expired.</span></span>  <br/><span data-ttu-id="cf4c0-133">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-133">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="cf4c0-134">**Error**</span><span class="sxs-lookup"><span data-stu-id="cf4c0-134">**Error**</span></span> <br/> | <span data-ttu-id="cf4c0-135">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-135">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="cf4c0-136">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="cf4c0-136">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="cf4c0-137">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="cf4c0-137">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="cf4c0-138">-Atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="cf4c0-138">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="cf4c0-139">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="cf4c0-139">-  Unknown tag</span></span>  <br/><span data-ttu-id="cf4c0-140">-Atributo o elemento no válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="cf4c0-140">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="cf4c0-141">-Intento de acceso no autorizado por parte de un cliente</span><span class="sxs-lookup"><span data-stu-id="cf4c0-141">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="cf4c0-142">-Error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="cf4c0-142">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="cf4c0-143">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="cf4c0-143">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/>- |
   
### <a name="child-elements"></a><span data-ttu-id="cf4c0-144">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cf4c0-144">Child elements</span></span>

|<span data-ttu-id="cf4c0-145">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cf4c0-145">**Element**</span></span>|<span data-ttu-id="cf4c0-146">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf4c0-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf4c0-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="cf4c0-147">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="cf4c0-148">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-148">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="cf4c0-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="cf4c0-149">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="cf4c0-150">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-150">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="cf4c0-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="cf4c0-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="cf4c0-152">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-152">Currently unused and reserved for future use.</span></span> <span data-ttu-id="cf4c0-153">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-153">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="cf4c0-154">MessageXml</span><span class="sxs-lookup"><span data-stu-id="cf4c0-154">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="cf4c0-155">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-155">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="cf4c0-156">RoomLists</span><span class="sxs-lookup"><span data-stu-id="cf4c0-156">RoomLists</span></span>](roomlists.md) <br/> |<span data-ttu-id="cf4c0-157">Proporciona una lista de direcciones de correo electrónico y nombres para mostrar que representan listas de salas de reuniones.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-157">Provides a list of e-mail addresses and display names that represent lists of meeting rooms.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cf4c0-158">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cf4c0-158">Parent elements</span></span>

|<span data-ttu-id="cf4c0-159">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cf4c0-159">**Element**</span></span>|<span data-ttu-id="cf4c0-160">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf4c0-160">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf4c0-161">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="cf4c0-161">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="cf4c0-162">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="cf4c0-162">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="cf4c0-163">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cf4c0-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf4c0-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="cf4c0-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cf4c0-165">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cf4c0-165">Schema Name</span></span>  <br/> |<span data-ttu-id="cf4c0-166">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="cf4c0-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cf4c0-167">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cf4c0-167">Validation File</span></span>  <br/> |<span data-ttu-id="cf4c0-168">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="cf4c0-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cf4c0-169">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cf4c0-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="cf4c0-170">Falso</span><span class="sxs-lookup"><span data-stu-id="cf4c0-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf4c0-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf4c0-171">See also</span></span>

- [<span data-ttu-id="cf4c0-172">Operación GetRoomLists</span><span class="sxs-lookup"><span data-stu-id="cf4c0-172">GetRoomLists operation</span></span>](getroomlists-operation.md)
- [<span data-ttu-id="cf4c0-173">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="cf4c0-173">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

