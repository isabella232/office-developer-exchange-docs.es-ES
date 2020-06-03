---
title: DeleteItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItemResponseMessage
api_type:
- schema
ms.assetid: c3d34c4d-8d83-4612-aa9e-66f9cc7314df
description: El elemento DeleteItemResponseMessage contiene el estado y el resultado de una única solicitud de operación DeleteItem.
ms.openlocfilehash: 78e3efc6a9e9e6629d7efe7f2dc294e0a731005a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526931"
---
# <a name="deleteitemresponsemessage"></a><span data-ttu-id="69622-103">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="69622-103">DeleteItemResponseMessage</span></span>

<span data-ttu-id="69622-104">El elemento **DeleteItemResponseMessage** contiene el estado y el resultado de una única solicitud de [operación DeleteItem](deleteitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="69622-104">The **DeleteItemResponseMessage** element contains the status and result of a single [DeleteItem operation](deleteitem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="69622-105">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="69622-105">DeleteItemResponse</span></span>](deleteitemresponse.md) 
- [<span data-ttu-id="69622-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="69622-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="69622-107">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="69622-107">DeleteItemResponseMessage</span></span>](deleteitemresponsemessage.md)
  
```xml
<DeleteItemResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</DeleteItemResponseMessage>
```

 <span data-ttu-id="69622-108">**DeleteItemResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="69622-108">**DeleteItemResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="69622-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="69622-109">Attributes and elements</span></span>

<span data-ttu-id="69622-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="69622-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="69622-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="69622-111">Attributes</span></span>

|<span data-ttu-id="69622-112">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="69622-112">**Attribute**</span></span>|<span data-ttu-id="69622-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="69622-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="69622-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="69622-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="69622-115">Describe el estado de una respuesta de la [operación DeleteItem](deleteitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="69622-115">Describes the status of a [DeleteItem operation](deleteitem-operation.md) response.</span></span><br/><br/><span data-ttu-id="69622-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="69622-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="69622-117">-Correcto</span><span class="sxs-lookup"><span data-stu-id="69622-117">- Success</span></span>  <br/><span data-ttu-id="69622-118">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="69622-118">-  Warning</span></span>  <br/><span data-ttu-id="69622-119">-Error</span><span class="sxs-lookup"><span data-stu-id="69622-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="69622-120">Atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="69622-120">ResponseClass attribute</span></span>

|<span data-ttu-id="69622-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="69622-121">**Value**</span></span>|<span data-ttu-id="69622-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="69622-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="69622-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="69622-123">**Success**</span></span> <br/> |<span data-ttu-id="69622-124">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="69622-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="69622-125">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="69622-125">**Warning**</span></span> <br/> | <span data-ttu-id="69622-126">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="69622-126">Describes a request that was not processed.</span></span> <span data-ttu-id="69622-127">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="69622-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="69622-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="69622-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="69622-129">-El almacén de Exchange se desconecta durante el lote.</span><span class="sxs-lookup"><span data-stu-id="69622-129">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="69622-130">-Servicios de dominio de Active Directory (AD DS) se desconecta.</span><span class="sxs-lookup"><span data-stu-id="69622-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="69622-131">-Se mueven los buzones.</span><span class="sxs-lookup"><span data-stu-id="69622-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="69622-132">-La base de datos de mensajes (MDB) se desconecta.</span><span class="sxs-lookup"><span data-stu-id="69622-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="69622-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="69622-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="69622-134">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="69622-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="69622-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="69622-135">**Error**</span></span> <br/> | <span data-ttu-id="69622-136">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="69622-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="69622-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="69622-137">The following are examples of sources of errors:</span></span><br/><br/><span data-ttu-id="69622-138">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="69622-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="69622-139">-Atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="69622-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="69622-140">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="69622-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="69622-141">-Atributo o elemento no válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="69622-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="69622-142">-Un cliente intenta establecer el nivel de registro de errores por encima del nivel máximo permitido por el administrador</span><span class="sxs-lookup"><span data-stu-id="69622-142">-  A client attempt to set the error logging level above the maximum level that is permitted by the administrator</span></span>  <br/><span data-ttu-id="69622-143">-Un cliente intenta establecer el nivel de error de gravedad por debajo del nivel predeterminado especificado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="69622-143">-  A client attempt to set the severity failure level below the default level that is specified by the administrator</span></span>  <br/><span data-ttu-id="69622-144">-Intento de acceso no autorizado por parte de un cliente</span><span class="sxs-lookup"><span data-stu-id="69622-144">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="69622-145">-Error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="69622-145">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="69622-146">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="69622-146">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="69622-147">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="69622-147">Child elements</span></span>

|<span data-ttu-id="69622-148">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="69622-148">**Element**</span></span>|<span data-ttu-id="69622-149">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="69622-149">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69622-150">MessageText</span><span class="sxs-lookup"><span data-stu-id="69622-150">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="69622-151">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="69622-151">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="69622-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="69622-152">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="69622-153">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="69622-153">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="69622-154">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="69622-154">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="69622-155">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="69622-155">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="69622-156">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="69622-156">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="69622-157">MessageXml</span><span class="sxs-lookup"><span data-stu-id="69622-157">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="69622-158">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="69622-158">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="69622-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="69622-159">Parent elements</span></span>

|<span data-ttu-id="69622-160">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="69622-160">**Element**</span></span>|<span data-ttu-id="69622-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="69622-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69622-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="69622-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="69622-163">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="69622-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69622-164">Comentarios</span><span class="sxs-lookup"><span data-stu-id="69622-164">Remarks</span></span>

<span data-ttu-id="69622-165">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="69622-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="69622-166">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="69622-166">Version differences</span></span>

<span data-ttu-id="69622-167">En las versiones de Exchange que comienzan con la compilación 15.00.0986.00, el elemento **DeleteItemResponseMessage** es del tipo **DeleteItemResponseMessageType**.</span><span class="sxs-lookup"><span data-stu-id="69622-167">In versions of Exchange starting with build 15.00.0986.00, the **DeleteItemResponseMessage** element is of type **DeleteItemResponseMessageType**.</span></span> <span data-ttu-id="69622-168">En versiones anteriores, el elemento es del tipo **ResponseMessageType**.</span><span class="sxs-lookup"><span data-stu-id="69622-168">In previous versions, the element is of type **ResponseMessageType**.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="69622-169">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="69622-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69622-170">Namespace</span><span class="sxs-lookup"><span data-stu-id="69622-170">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="69622-171">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="69622-171">Schema Name</span></span>  <br/> |<span data-ttu-id="69622-172">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="69622-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="69622-173">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="69622-173">Validation File</span></span>  <br/> |<span data-ttu-id="69622-174">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="69622-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="69622-175">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="69622-175">Can be Empty</span></span>  <br/> |<span data-ttu-id="69622-176">Falso</span><span class="sxs-lookup"><span data-stu-id="69622-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="69622-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="69622-177">See also</span></span>

- [<span data-ttu-id="69622-178">Operación DeleteItem</span><span class="sxs-lookup"><span data-stu-id="69622-178">DeleteItem operation</span></span>](deleteitem-operation.md)
- [<span data-ttu-id="69622-179">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="69622-179">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="69622-180">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="69622-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="69622-181">Eliminación de elementos (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="69622-181">Deleting Items (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/9bfc39e6-d944-4eb6-8aee-cbaf1e37c67d%28Office.15%29.aspx)

