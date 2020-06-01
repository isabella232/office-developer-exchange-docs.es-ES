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
description: El elemento ResponseMessage proporciona información descriptiva sobre el estado de respuesta para una única entidad dentro de una solicitud.
ms.openlocfilehash: a7f4240b1e988cb69d67118c6db58db0d7babba5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467161"
---
# <a name="responsemessage"></a><span data-ttu-id="ccfad-103">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ccfad-103">ResponseMessage</span></span>

<span data-ttu-id="ccfad-104">El elemento **ResponseMessage** proporciona información descriptiva sobre el estado de respuesta para una única entidad dentro de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="ccfad-104">The **ResponseMessage** element provides descriptive information about the response status for a single entity within a request.</span></span> 
  
```xml
<ResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</ResponseMessage>
```

 <span data-ttu-id="ccfad-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ccfad-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ccfad-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ccfad-106">Attributes and elements</span></span>

<span data-ttu-id="ccfad-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ccfad-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ccfad-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ccfad-108">Attributes</span></span>

|<span data-ttu-id="ccfad-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ccfad-109">**Attribute**</span></span>|<span data-ttu-id="ccfad-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ccfad-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ccfad-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="ccfad-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="ccfad-112">Representa el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ccfad-112">Represents the status of the response.</span></span> <br/><br/><span data-ttu-id="ccfad-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="ccfad-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="ccfad-114">-Correcto</span><span class="sxs-lookup"><span data-stu-id="ccfad-114">-  Success</span></span>  <br/><span data-ttu-id="ccfad-115">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="ccfad-115">-  Warning</span></span>  <br/><span data-ttu-id="ccfad-116">-Error</span><span class="sxs-lookup"><span data-stu-id="ccfad-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="ccfad-117">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="ccfad-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="ccfad-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ccfad-118">**Value**</span></span>|<span data-ttu-id="ccfad-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ccfad-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ccfad-120">Correcto</span><span class="sxs-lookup"><span data-stu-id="ccfad-120">Success</span></span>  <br/> |<span data-ttu-id="ccfad-121">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="ccfad-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="ccfad-122">Advertencia</span><span class="sxs-lookup"><span data-stu-id="ccfad-122">Warning</span></span>  <br/> | <span data-ttu-id="ccfad-123">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="ccfad-123">Describes a request that was not processed.</span></span> <span data-ttu-id="ccfad-124">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="ccfad-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="ccfad-125">Las siguientes son algunas causas posibles de las advertencias:</span><span class="sxs-lookup"><span data-stu-id="ccfad-125">The following are some possible causes for warnings:</span></span>  <br/><br/><span data-ttu-id="ccfad-126">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="ccfad-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="ccfad-127">-El servicio de directorio de Active Directory está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="ccfad-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="ccfad-128">-Se mueven los buzones.</span><span class="sxs-lookup"><span data-stu-id="ccfad-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="ccfad-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="ccfad-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="ccfad-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="ccfad-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="ccfad-131">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="ccfad-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="ccfad-132">Error</span><span class="sxs-lookup"><span data-stu-id="ccfad-132">Error</span></span>  <br/> | <span data-ttu-id="ccfad-133">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="ccfad-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="ccfad-134">Las siguientes son algunas causas posibles de errores:</span><span class="sxs-lookup"><span data-stu-id="ccfad-134">The following are some possible causes for errors:</span></span>  <br/><br/><span data-ttu-id="ccfad-135">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="ccfad-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="ccfad-136">-Atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="ccfad-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="ccfad-137">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="ccfad-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="ccfad-138">-Atributo o elemento no válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="ccfad-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="ccfad-139">-Intento de acceso no autorizado por parte de un cliente</span><span class="sxs-lookup"><span data-stu-id="ccfad-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="ccfad-140">-Error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="ccfad-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="ccfad-141">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="ccfad-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ccfad-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ccfad-142">Child elements</span></span>

|<span data-ttu-id="ccfad-143">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ccfad-143">**Element**</span></span>|<span data-ttu-id="ccfad-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ccfad-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ccfad-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="ccfad-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="ccfad-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ccfad-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="ccfad-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ccfad-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="ccfad-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ccfad-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="ccfad-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ccfad-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="ccfad-150">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="ccfad-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="ccfad-151">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="ccfad-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="ccfad-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="ccfad-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="ccfad-153">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="ccfad-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ccfad-154">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ccfad-154">Parent elements</span></span>

|<span data-ttu-id="ccfad-155">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ccfad-155">**Element**</span></span>|<span data-ttu-id="ccfad-156">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ccfad-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ccfad-157">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="ccfad-157">FreeBusyResponse</span></span>](freebusyresponse.md) <br/> |<span data-ttu-id="ccfad-158">Contiene la información de disponibilidad de un único usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="ccfad-158">Contains the free/busy information for a single mailbox user.</span></span> <br/> <br/> <span data-ttu-id="ccfad-159">La siguiente es la expresión XPath 2,0 a este elemento:</span><span class="sxs-lookup"><span data-stu-id="ccfad-159">The following is the XPath 2.0 expression to this element:</span></span> <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray[i]/FreeBusyResponse` <br/> |
|[<span data-ttu-id="ccfad-160">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="ccfad-160">SuggestionsResponse</span></span>](suggestionsresponse.md) <br/> |<span data-ttu-id="ccfad-161">Contiene información de respuesta y datos de sugerencias para las sugerencias de reunión solicitadas.</span><span class="sxs-lookup"><span data-stu-id="ccfad-161">Contains response information and suggestion data for requested meeting suggestions.</span></span>  <br/><br/> <span data-ttu-id="ccfad-162">La siguiente es la expresión XPath 2,0 a este elemento:</span><span class="sxs-lookup"><span data-stu-id="ccfad-162">The following is the XPath 2.0 expression to this element:</span></span><br/>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse` <br/> |
|[<span data-ttu-id="ccfad-163">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="ccfad-163">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md) <br/> |<span data-ttu-id="ccfad-164">Contiene los resultados de la respuesta y la configuración de OOF para un usuario.</span><span class="sxs-lookup"><span data-stu-id="ccfad-164">Contains the response results and the OOF settings for a user.</span></span>  <br/><br/> <span data-ttu-id="ccfad-165">La siguiente es la expresión XPath 2,0 a este elemento:</span><span class="sxs-lookup"><span data-stu-id="ccfad-165">The following is the XPath 2.0 expression to this element:</span></span>  <br/><br/>  `/GetUserOofSettingsResponse` <br/> |
|[<span data-ttu-id="ccfad-166">SetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="ccfad-166">SetUserOofSettingsResponse</span></span>](setuseroofsettingsresponse.md) <br/> |<span data-ttu-id="ccfad-167">Contiene el resultado de un mensaje [SetUserOofSettingsRequest](setuseroofsettingsrequest.md) intentó.</span><span class="sxs-lookup"><span data-stu-id="ccfad-167">Contains the result of an attempted [SetUserOofSettingsRequest](setuseroofsettingsrequest.md) message.</span></span> <br/> <br/> <span data-ttu-id="ccfad-168">La siguiente es la expresión XPath 2,0 a este elemento:</span><span class="sxs-lookup"><span data-stu-id="ccfad-168">The following is the XPath 2.0 expression to this element:</span></span>  <br/><br/>  `/SetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ccfad-169">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ccfad-169">Remarks</span></span>

<span data-ttu-id="ccfad-170">El tipo **ResponseMessageType** es común a todas las respuestas de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ccfad-170">The **ResponseMessageType** type is common to all Exchange Web Services responses.</span></span> <span data-ttu-id="ccfad-171">El tipo **ResponseMessageType** se extiende mediante los tipos complejos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ccfad-171">The **ResponseMessageType** type is extended by the following complex types:</span></span> 
  
- <span data-ttu-id="ccfad-172">**ApplyConversationActionResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ccfad-172">**ApplyConversationActionResponseMessageType**</span></span>
    
- <span data-ttu-id="ccfad-173">**AttachmentInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ccfad-173">**AttachmentInfoResponseMessageType**</span></span>
    
- <span data-ttu-id="ccfad-174">**DeleteAttachmentResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ccfad-174">**DeleteAttachmentResponseMessageType**</span></span>
    
- <span data-ttu-id="ccfad-175">**DeleteItemResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ccfad-175">**DeleteItemResponseMessageType**</span></span>
    
- <span data-ttu-id="ccfad-176">**ExpandDLResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ccfad-176">**ExpandDLResponseMessageType**</span></span>
    
- <span data-ttu-id="ccfad-177">**FindFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ccfad-177">**FindFolderResponseMessageType**</span></span>
    
- <span data-ttu-id="ccfad-178">**FindItemResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ccfad-178">**FindItemResponseMessageType**</span></span>
    
- <span data-ttu-id="ccfad-179">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ccfad-179">**FolderInfoResponseMessageType**</span></span>
    
- <span data-ttu-id="ccfad-180">**GetEventsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ccfad-180">**GetEventsResponseMessageType**</span></span>
    
- <span data-ttu-id="ccfad-181">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ccfad-181">**ItemInfoResponseMessageType**</span></span>
    
- <span data-ttu-id="ccfad-182">**ResolveNamesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ccfad-182">**ResolveNamesResponseMessageType**</span></span>
    
- <span data-ttu-id="ccfad-183">**SubscribeResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ccfad-183">**SubscribeResponseMessageType**</span></span>
    
- <span data-ttu-id="ccfad-184">**SendNotificationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ccfad-184">**SendNotificationResponseMessageType**</span></span>
    
- <span data-ttu-id="ccfad-185">**SyncFolderHierarchyResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ccfad-185">**SyncFolderHierarchyResponseMessageType**</span></span>
    
- <span data-ttu-id="ccfad-186">**SyncFolderItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ccfad-186">**SyncFolderItemsResponseMessageType**</span></span>
    
<span data-ttu-id="ccfad-187">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="ccfad-187">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="ccfad-188">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="ccfad-188">Version differences</span></span>

<span data-ttu-id="ccfad-189">Los tipos **ApplyConversationActionResponseMessage** y **DeleteItemResponseMessageType** se introdujeron en Exchange Build 15.00.0986.00.</span><span class="sxs-lookup"><span data-stu-id="ccfad-189">The **ApplyConversationActionResponseMessage** and **DeleteItemResponseMessageType** types were introduced in Exchange build 15.00.0986.00.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="ccfad-190">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ccfad-190">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ccfad-191">Namespace</span><span class="sxs-lookup"><span data-stu-id="ccfad-191">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ccfad-192">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ccfad-192">Schema Name</span></span>  <br/> |<span data-ttu-id="ccfad-193">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ccfad-193">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ccfad-194">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ccfad-194">Validation File</span></span>  <br/> |<span data-ttu-id="ccfad-195">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ccfad-195">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ccfad-196">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ccfad-196">Can be Empty</span></span>  <br/> |<span data-ttu-id="ccfad-197">Falso</span><span class="sxs-lookup"><span data-stu-id="ccfad-197">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ccfad-198">Vea también</span><span class="sxs-lookup"><span data-stu-id="ccfad-198">See also</span></span>

- [<span data-ttu-id="ccfad-199">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="ccfad-199">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="ccfad-200">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="ccfad-200">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)
- [<span data-ttu-id="ccfad-201">Operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="ccfad-201">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
- [<span data-ttu-id="ccfad-202">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="ccfad-202">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

