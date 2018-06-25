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
ms.openlocfilehash: 1f0cc3d49bfa5fba6da32cf65df6b6718ccfbded
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764113"
---
# <a name="deleteitemresponsemessage"></a><span data-ttu-id="cf1fd-103">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="cf1fd-103">DeleteItemResponseMessage</span></span>

<span data-ttu-id="cf1fd-104">El elemento **DeleteItemResponseMessage** contiene el estado y el resultado de una única solicitud de [operación DeleteItem](deleteitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="cf1fd-104">The **DeleteItemResponseMessage** element contains the status and result of a single [DeleteItem operation](deleteitem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="cf1fd-105">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="cf1fd-105">DeleteItemResponse</span></span>](deleteitemresponse.md) 
- [<span data-ttu-id="cf1fd-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="cf1fd-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="cf1fd-107">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="cf1fd-107">DeleteItemResponseMessage</span></span>](deleteitemresponsemessage.md)
  
```xml
<DeleteItemResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</DeleteItemResponseMessage>
```

 <span data-ttu-id="cf1fd-108">**DeleteItemResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-108">**DeleteItemResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cf1fd-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cf1fd-109">Attributes and elements</span></span>

<span data-ttu-id="cf1fd-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cf1fd-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="cf1fd-111">Attributes</span></span>

|<span data-ttu-id="cf1fd-112">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-112">**Attribute**</span></span>|<span data-ttu-id="cf1fd-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf1fd-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="cf1fd-115">Describe el estado de una respuesta de [la operación DeleteItem](deleteitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="cf1fd-115">Describes the status of a [DeleteItem operation](deleteitem-operation.md) response.</span></span><br/><br/><span data-ttu-id="cf1fd-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="cf1fd-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="cf1fd-117">-Éxito</span><span class="sxs-lookup"><span data-stu-id="cf1fd-117">- Success</span></span>  <br/><span data-ttu-id="cf1fd-118">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="cf1fd-118">-  Warning</span></span>  <br/><span data-ttu-id="cf1fd-119">-Error</span><span class="sxs-lookup"><span data-stu-id="cf1fd-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="cf1fd-120">Atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="cf1fd-120">ResponseClass attribute</span></span>

|<span data-ttu-id="cf1fd-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-121">**Value**</span></span>|<span data-ttu-id="cf1fd-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf1fd-123">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-123">**Success**</span></span> <br/> |<span data-ttu-id="cf1fd-124">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="cf1fd-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-125">**Warning**</span></span> <br/> | <span data-ttu-id="cf1fd-126">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-126">Describes a request that was not processed.</span></span> <span data-ttu-id="cf1fd-127">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="cf1fd-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="cf1fd-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="cf1fd-129">-El almacén de Exchange se desconecta durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-129">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="cf1fd-130">-Los servicios de dominio de Active Directory (AD DS) se queda sin conexión.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="cf1fd-131">-Se mueven los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="cf1fd-132">-La base de datos de mensajes (MDB) se queda sin conexión.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="cf1fd-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="cf1fd-134">-Se ha excedido una cuota.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="cf1fd-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-135">**Error**</span></span> <br/> | <span data-ttu-id="cf1fd-136">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="cf1fd-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="cf1fd-137">The following are examples of sources of errors:</span></span><br/><br/><span data-ttu-id="cf1fd-138">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="cf1fd-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="cf1fd-139">-Los atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="cf1fd-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="cf1fd-140">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="cf1fd-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="cf1fd-141">-De atributo o elemento no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="cf1fd-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="cf1fd-142">-Un cliente intenta establecer el nivel de registro de error por encima del nivel máximo permitido por el administrador</span><span class="sxs-lookup"><span data-stu-id="cf1fd-142">-  A client attempt to set the error logging level above the maximum level that is permitted by the administrator</span></span>  <br/><span data-ttu-id="cf1fd-143">-Un cliente intenta establecer el nivel de error de gravedad por debajo del nivel predeterminado que es especificado por el administrador</span><span class="sxs-lookup"><span data-stu-id="cf1fd-143">-  A client attempt to set the severity failure level below the default level that is specified by the administrator</span></span>  <br/><span data-ttu-id="cf1fd-144">-Intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="cf1fd-144">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="cf1fd-145">-Error server-side en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="cf1fd-145">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="cf1fd-146">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="cf1fd-146">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cf1fd-147">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cf1fd-147">Child elements</span></span>

|<span data-ttu-id="cf1fd-148">**Element**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-148">**Element**</span></span>|<span data-ttu-id="cf1fd-149">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-149">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf1fd-150">MessageText</span><span class="sxs-lookup"><span data-stu-id="cf1fd-150">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="cf1fd-151">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-151">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="cf1fd-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="cf1fd-152">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="cf1fd-153">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-153">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="cf1fd-154">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="cf1fd-154">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="cf1fd-155">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-155">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="cf1fd-156">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-156">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="cf1fd-157">MessageXml</span><span class="sxs-lookup"><span data-stu-id="cf1fd-157">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="cf1fd-158">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-158">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cf1fd-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cf1fd-159">Parent elements</span></span>

|<span data-ttu-id="cf1fd-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-160">**Element**</span></span>|<span data-ttu-id="cf1fd-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf1fd-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf1fd-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="cf1fd-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="cf1fd-163">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf1fd-164">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cf1fd-164">Remarks</span></span>

<span data-ttu-id="cf1fd-165">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="cf1fd-166">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="cf1fd-166">Version differences</span></span>

<span data-ttu-id="cf1fd-167">En las versiones de Exchange a partir de compilación 15.00.0986.00, el elemento **DeleteItemResponseMessage** es del tipo **DeleteItemResponseMessageType**.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-167">In versions of Exchange starting with build 15.00.0986.00, the **DeleteItemResponseMessage** element is of type **DeleteItemResponseMessageType**.</span></span> <span data-ttu-id="cf1fd-168">En versiones anteriores, el elemento es de tipo **ResponseMessageType**.</span><span class="sxs-lookup"><span data-stu-id="cf1fd-168">In previous versions, the element is of type **ResponseMessageType**.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cf1fd-169">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cf1fd-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf1fd-170">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cf1fd-170">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cf1fd-171">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cf1fd-171">Schema Name</span></span>  <br/> |<span data-ttu-id="cf1fd-172">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="cf1fd-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cf1fd-173">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cf1fd-173">Validation File</span></span>  <br/> |<span data-ttu-id="cf1fd-174">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cf1fd-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cf1fd-175">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cf1fd-175">Can be Empty</span></span>  <br/> |<span data-ttu-id="cf1fd-176">False</span><span class="sxs-lookup"><span data-stu-id="cf1fd-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf1fd-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf1fd-177">See also</span></span>

- [<span data-ttu-id="cf1fd-178">Operación DeleteItem</span><span class="sxs-lookup"><span data-stu-id="cf1fd-178">DeleteItem operation</span></span>](deleteitem-operation.md)
- [<span data-ttu-id="cf1fd-179">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="cf1fd-179">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="cf1fd-180">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="cf1fd-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="cf1fd-181">Eliminación de elementos (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="cf1fd-181">Deleting Items (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/9bfc39e6-d944-4eb6-8aee-cbaf1e37c67d%28Office.15%29.aspx)

