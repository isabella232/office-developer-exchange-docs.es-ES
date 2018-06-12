---
title: FindConversationResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindConversationResponse
api_type:
- schema
ms.assetid: a689e29d-5f3d-4deb-81ee-8b6cc60f6dea
description: El elemento FindConversationResponse define una respuesta a una solicitud de operación FindConversation.
ms.openlocfilehash: 5754ea7540fa6daac8cd725386ca213d5bf05c8e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764615"
---
# <a name="findconversationresponse"></a><span data-ttu-id="8df81-103">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="8df81-103">FindConversationResponse</span></span>

<span data-ttu-id="8df81-104">El elemento **FindConversationResponse** define una respuesta a una solicitud de [operación FindConversation](findconversation-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="8df81-104">The **FindConversationResponse** element defines a response to a [FindConversation operation](findconversation-operation.md) request.</span></span> 
  
[<span data-ttu-id="8df81-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="8df81-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
```XML
<FindConversationResponse ResponseClass="">
   <Conversations/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</FindConversationResponse>

```

 <span data-ttu-id="8df81-106">**FindConversationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="8df81-106">**FindConversationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8df81-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8df81-107">Attributes and elements</span></span>

<span data-ttu-id="8df81-108">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8df81-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8df81-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="8df81-109">Attributes</span></span>

|<span data-ttu-id="8df81-110">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="8df81-110">**Attribute**</span></span>|<span data-ttu-id="8df81-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8df81-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8df81-112">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="8df81-112">**ResponseClass**</span></span> <br/> | <span data-ttu-id="8df81-113">Describe el estado de una respuesta de [la operación FindConversation](findconversation-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="8df81-113">Describes the status of a [FindConversation operation](findconversation-operation.md) response.</span></span> <br/><br/><span data-ttu-id="8df81-114">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="8df81-114">The following values are valid for this attribute:</span></span><br/>  <br/><span data-ttu-id="8df81-115">-Éxito</span><span class="sxs-lookup"><span data-stu-id="8df81-115">-  Success</span></span>  <br/><span data-ttu-id="8df81-116">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="8df81-116">-  Warning</span></span>  <br/><span data-ttu-id="8df81-117">-Error</span><span class="sxs-lookup"><span data-stu-id="8df81-117">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="8df81-118">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="8df81-118">ResponseClass attribute values</span></span>

|<span data-ttu-id="8df81-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8df81-119">**Value**</span></span>|<span data-ttu-id="8df81-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8df81-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8df81-121">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="8df81-121">**Success**</span></span> <br/> |<span data-ttu-id="8df81-122">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="8df81-122">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="8df81-123">**Warning**</span><span class="sxs-lookup"><span data-stu-id="8df81-123">**Warning**</span></span> <br/> | <span data-ttu-id="8df81-124">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="8df81-124">Describes a request that was not processed.</span></span> <span data-ttu-id="8df81-125">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="8df81-125">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="8df81-126">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="8df81-126">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="8df81-127">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="8df81-127">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="8df81-128">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="8df81-128">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="8df81-129">-Buzones se han movido.</span><span class="sxs-lookup"><span data-stu-id="8df81-129">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="8df81-130">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="8df81-130">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="8df81-131">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="8df81-131">-  A password is expired.</span></span>  <br/><span data-ttu-id="8df81-132">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="8df81-132">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="8df81-133">**Error**</span><span class="sxs-lookup"><span data-stu-id="8df81-133">**Error**</span></span> <br/> | <span data-ttu-id="8df81-134">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="8df81-134">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="8df81-135">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="8df81-135">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="8df81-136">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="8df81-136">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="8df81-137">-Los atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="8df81-137">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="8df81-138">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="8df81-138">-  An unknown tag</span></span>  <br/><span data-ttu-id="8df81-139">-Un atributo o un elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="8df81-139">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="8df81-140">-Un intento de acceso no autorizado por cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="8df81-140">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="8df81-141">-Un error del lado del servidor en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="8df81-141">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="8df81-142">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="8df81-142">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8df81-143">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8df81-143">Child elements</span></span>

|<span data-ttu-id="8df81-144">**Element**</span><span class="sxs-lookup"><span data-stu-id="8df81-144">**Element**</span></span>|<span data-ttu-id="8df81-145">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8df81-145">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8df81-146">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="8df81-146">Conversations</span></span>](conversations-ex15websvcsotherref.md) <br/> |<span data-ttu-id="8df81-147">Contiene una matriz de las conversaciones.</span><span class="sxs-lookup"><span data-stu-id="8df81-147">Contains an array of conversations.</span></span>  <br/> |
|[<span data-ttu-id="8df81-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="8df81-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="8df81-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8df81-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="8df81-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8df81-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="8df81-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8df81-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="8df81-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="8df81-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="8df81-153">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="8df81-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="8df81-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="8df81-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="8df81-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="8df81-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="8df81-156">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="8df81-156">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8df81-157">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8df81-157">Parent elements</span></span>

<span data-ttu-id="8df81-158">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8df81-158">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="8df81-159">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="8df81-159">Text value</span></span>

<span data-ttu-id="8df81-160">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8df81-160">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8df81-161">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8df81-161">Remarks</span></span>

<span data-ttu-id="8df81-162">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="8df81-162">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8df81-163">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8df81-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8df81-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8df81-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8df81-165">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8df81-165">Schema name</span></span>  <br/> |<span data-ttu-id="8df81-166">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="8df81-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8df81-167">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8df81-167">Validation file</span></span>  <br/> |<span data-ttu-id="8df81-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8df81-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8df81-169">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8df81-169">Can be empty</span></span>  <br/> |<span data-ttu-id="8df81-170">False</span><span class="sxs-lookup"><span data-stu-id="8df81-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8df81-171">Ver también</span><span class="sxs-lookup"><span data-stu-id="8df81-171">See also</span></span>

- [<span data-ttu-id="8df81-172">Operación de FindConversation</span><span class="sxs-lookup"><span data-stu-id="8df81-172">FindConversation operation</span></span>](findconversation-operation.md)
- [<span data-ttu-id="8df81-173">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="8df81-173">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="8df81-174">Conversaciones de EWS</span><span class="sxs-lookup"><span data-stu-id="8df81-174">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

