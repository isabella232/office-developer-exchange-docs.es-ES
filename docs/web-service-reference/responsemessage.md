---
title: ResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseMessage
api_type:
- schema
ms.assetid: bf57265a-d354-4cd7-bbfc-d93e19cbede6
description: El elemento ResponseMessage proporciona información descriptiva sobre el estado de respuesta para una entidad única dentro de una solicitud.
ms.openlocfilehash: 69f1f6f12d10044045b72dd644536e742c479b9e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837191"
---
# <a name="responsemessage"></a><span data-ttu-id="638d1-103">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="638d1-103">ResponseMessage</span></span>

<span data-ttu-id="638d1-104">El elemento **ResponseMessage** proporciona información descriptiva sobre el estado de respuesta para una entidad única dentro de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="638d1-104">The **ResponseMessage** element provides descriptive information about the response status for a single entity within a request.</span></span> 
  
```xml
<ResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</ResponseMessage>
```

 <span data-ttu-id="638d1-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="638d1-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="638d1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="638d1-106">Attributes and elements</span></span>

<span data-ttu-id="638d1-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="638d1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="638d1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="638d1-108">Attributes</span></span>

|<span data-ttu-id="638d1-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="638d1-109">**Attribute**</span></span>|<span data-ttu-id="638d1-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="638d1-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="638d1-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="638d1-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="638d1-112">Representa el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="638d1-112">Represents the status of the response.</span></span> <br/><br/><span data-ttu-id="638d1-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="638d1-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="638d1-114">-Éxito</span><span class="sxs-lookup"><span data-stu-id="638d1-114">-  Success</span></span>  <br/><span data-ttu-id="638d1-115">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="638d1-115">-  Warning</span></span>  <br/><span data-ttu-id="638d1-116">-Error</span><span class="sxs-lookup"><span data-stu-id="638d1-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="638d1-117">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="638d1-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="638d1-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="638d1-118">**Value**</span></span>|<span data-ttu-id="638d1-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="638d1-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="638d1-120">Correcto</span><span class="sxs-lookup"><span data-stu-id="638d1-120">Success</span></span>  <br/> |<span data-ttu-id="638d1-121">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="638d1-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="638d1-122">Advertencia</span><span class="sxs-lookup"><span data-stu-id="638d1-122">Warning</span></span>  <br/> | <span data-ttu-id="638d1-123">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="638d1-123">Describes a request that was not processed.</span></span> <span data-ttu-id="638d1-124">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="638d1-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="638d1-125">Las siguientes son algunas posibles causas de advertencias:</span><span class="sxs-lookup"><span data-stu-id="638d1-125">The following are some possible causes for warnings:</span></span>  <br/><br/><span data-ttu-id="638d1-126">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="638d1-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="638d1-127">-El servicio de directorio de Active Directory está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="638d1-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="638d1-128">-Se mueven los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="638d1-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="638d1-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="638d1-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="638d1-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="638d1-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="638d1-131">-Se ha excedido una cuota.</span><span class="sxs-lookup"><span data-stu-id="638d1-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="638d1-132">Error</span><span class="sxs-lookup"><span data-stu-id="638d1-132">Error</span></span>  <br/> | <span data-ttu-id="638d1-133">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="638d1-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="638d1-134">Las siguientes son algunas posibles causas de errores:</span><span class="sxs-lookup"><span data-stu-id="638d1-134">The following are some possible causes for errors:</span></span>  <br/><br/><span data-ttu-id="638d1-135">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="638d1-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="638d1-136">-Los atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="638d1-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="638d1-137">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="638d1-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="638d1-138">-De atributo o elemento no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="638d1-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="638d1-139">-Intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="638d1-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="638d1-140">-Error server-side en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="638d1-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="638d1-141">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="638d1-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="638d1-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="638d1-142">Child elements</span></span>

|<span data-ttu-id="638d1-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="638d1-143">**Element**</span></span>|<span data-ttu-id="638d1-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="638d1-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="638d1-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="638d1-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="638d1-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="638d1-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="638d1-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="638d1-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="638d1-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="638d1-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="638d1-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="638d1-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="638d1-150">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="638d1-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="638d1-151">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="638d1-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="638d1-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="638d1-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="638d1-153">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="638d1-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="638d1-154">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="638d1-154">Parent elements</span></span>

|<span data-ttu-id="638d1-155">**Element**</span><span class="sxs-lookup"><span data-stu-id="638d1-155">**Element**</span></span>|<span data-ttu-id="638d1-156">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="638d1-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="638d1-157">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="638d1-157">FreeBusyResponse</span></span>](freebusyresponse.md) <br/> |<span data-ttu-id="638d1-158">Contiene la información de disponibilidad para un usuario de buzón único.</span><span class="sxs-lookup"><span data-stu-id="638d1-158">Contains the free/busy information for a single mailbox user.</span></span> <br/> <br/> <span data-ttu-id="638d1-159">La siguiente es la expresión de XPath 2.0 para este elemento:</span><span class="sxs-lookup"><span data-stu-id="638d1-159">The following is the XPath 2.0 expression to this element:</span></span> <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray[i]/FreeBusyResponse` <br/> |
|[<span data-ttu-id="638d1-160">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="638d1-160">SuggestionsResponse</span></span>](suggestionsresponse.md) <br/> |<span data-ttu-id="638d1-161">Contiene los datos de información y sugerencia de respuesta para solicitado sugerencias de reunión.</span><span class="sxs-lookup"><span data-stu-id="638d1-161">Contains response information and suggestion data for requested meeting suggestions.</span></span>  <br/><br/> <span data-ttu-id="638d1-162">La siguiente es la expresión de XPath 2.0 para este elemento:</span><span class="sxs-lookup"><span data-stu-id="638d1-162">The following is the XPath 2.0 expression to this element:</span></span><br/>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse` <br/> |
|[<span data-ttu-id="638d1-163">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="638d1-163">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md) <br/> |<span data-ttu-id="638d1-164">Contiene los resultados de la respuesta y la configuración de fuera de la oficina de un usuario.</span><span class="sxs-lookup"><span data-stu-id="638d1-164">Contains the response results and the OOF settings for a user.</span></span>  <br/><br/> <span data-ttu-id="638d1-165">La siguiente es la expresión de XPath 2.0 para este elemento:</span><span class="sxs-lookup"><span data-stu-id="638d1-165">The following is the XPath 2.0 expression to this element:</span></span>  <br/><br/>  `/GetUserOofSettingsResponse` <br/> |
|[<span data-ttu-id="638d1-166">SetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="638d1-166">SetUserOofSettingsResponse</span></span>](setuseroofsettingsresponse.md) <br/> |<span data-ttu-id="638d1-167">Contiene el resultado de un mensaje de [SetUserOofSettingsRequest](setuseroofsettingsrequest.md) intentado.</span><span class="sxs-lookup"><span data-stu-id="638d1-167">Contains the result of an attempted [SetUserOofSettingsRequest](setuseroofsettingsrequest.md) message.</span></span> <br/> <br/> <span data-ttu-id="638d1-168">La siguiente es la expresión de XPath 2.0 para este elemento:</span><span class="sxs-lookup"><span data-stu-id="638d1-168">The following is the XPath 2.0 expression to this element:</span></span>  <br/><br/>  `/SetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="638d1-169">Comentarios</span><span class="sxs-lookup"><span data-stu-id="638d1-169">Remarks</span></span>

<span data-ttu-id="638d1-170">El tipo **ResponseMessageType** es común a todas las respuestas de los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="638d1-170">The **ResponseMessageType** type is common to all Exchange Web Services responses.</span></span> <span data-ttu-id="638d1-171">El tipo de **ResponseMessageType** se extiende por los tipos complejos siguientes:</span><span class="sxs-lookup"><span data-stu-id="638d1-171">The **ResponseMessageType** type is extended by the following complex types:</span></span> 
  
- <span data-ttu-id="638d1-172">**ApplyConversationActionResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="638d1-172">**ApplyConversationActionResponseMessageType**</span></span>
    
- <span data-ttu-id="638d1-173">**AttachmentInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="638d1-173">**AttachmentInfoResponseMessageType**</span></span>
    
- <span data-ttu-id="638d1-174">**DeleteAttachmentResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="638d1-174">**DeleteAttachmentResponseMessageType**</span></span>
    
- <span data-ttu-id="638d1-175">**DeleteItemResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="638d1-175">**DeleteItemResponseMessageType**</span></span>
    
- <span data-ttu-id="638d1-176">**ExpandDLResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="638d1-176">**ExpandDLResponseMessageType**</span></span>
    
- <span data-ttu-id="638d1-177">**FindFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="638d1-177">**FindFolderResponseMessageType**</span></span>
    
- <span data-ttu-id="638d1-178">**FindItemResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="638d1-178">**FindItemResponseMessageType**</span></span>
    
- <span data-ttu-id="638d1-179">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="638d1-179">**FolderInfoResponseMessageType**</span></span>
    
- <span data-ttu-id="638d1-180">**GetEventsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="638d1-180">**GetEventsResponseMessageType**</span></span>
    
- <span data-ttu-id="638d1-181">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="638d1-181">**ItemInfoResponseMessageType**</span></span>
    
- <span data-ttu-id="638d1-182">**ResolveNamesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="638d1-182">**ResolveNamesResponseMessageType**</span></span>
    
- <span data-ttu-id="638d1-183">**SubscribeResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="638d1-183">**SubscribeResponseMessageType**</span></span>
    
- <span data-ttu-id="638d1-184">**SendNotificationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="638d1-184">**SendNotificationResponseMessageType**</span></span>
    
- <span data-ttu-id="638d1-185">**SyncFolderHierarchyResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="638d1-185">**SyncFolderHierarchyResponseMessageType**</span></span>
    
- <span data-ttu-id="638d1-186">**SyncFolderItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="638d1-186">**SyncFolderItemsResponseMessageType**</span></span>
    
<span data-ttu-id="638d1-187">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="638d1-187">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="638d1-188">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="638d1-188">Version differences</span></span>

<span data-ttu-id="638d1-189">Los tipos de **ApplyConversationActionResponseMessage** y **DeleteItemResponseMessageType** se introdujeron en Exchange compilación 15.00.0986.00.</span><span class="sxs-lookup"><span data-stu-id="638d1-189">The **ApplyConversationActionResponseMessage** and **DeleteItemResponseMessageType** types were introduced in Exchange build 15.00.0986.00.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="638d1-190">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="638d1-190">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="638d1-191">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="638d1-191">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="638d1-192">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="638d1-192">Schema Name</span></span>  <br/> |<span data-ttu-id="638d1-193">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="638d1-193">Messages schema</span></span>  <br/> |
|<span data-ttu-id="638d1-194">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="638d1-194">Validation File</span></span>  <br/> |<span data-ttu-id="638d1-195">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="638d1-195">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="638d1-196">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="638d1-196">Can be Empty</span></span>  <br/> |<span data-ttu-id="638d1-197">False</span><span class="sxs-lookup"><span data-stu-id="638d1-197">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="638d1-198">Vea también</span><span class="sxs-lookup"><span data-stu-id="638d1-198">See also</span></span>

- [<span data-ttu-id="638d1-199">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="638d1-199">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="638d1-200">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="638d1-200">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)
- [<span data-ttu-id="638d1-201">Operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="638d1-201">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
- [<span data-ttu-id="638d1-202">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="638d1-202">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

