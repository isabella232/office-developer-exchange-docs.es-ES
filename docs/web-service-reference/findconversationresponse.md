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
ms.openlocfilehash: 68acc42045b91ab4b574f32ba3fd622057863015
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462643"
---
# <a name="findconversationresponse"></a><span data-ttu-id="ce26f-103">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="ce26f-103">FindConversationResponse</span></span>

<span data-ttu-id="ce26f-104">El elemento **FindConversationResponse** define una respuesta a una solicitud de [operación FindConversation](findconversation-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="ce26f-104">The **FindConversationResponse** element defines a response to a [FindConversation operation](findconversation-operation.md) request.</span></span> 
  
[<span data-ttu-id="ce26f-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="ce26f-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
```XML
<FindConversationResponse ResponseClass="">
   <Conversations/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</FindConversationResponse>

```

 <span data-ttu-id="ce26f-106">**FindConversationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ce26f-106">**FindConversationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ce26f-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ce26f-107">Attributes and elements</span></span>

<span data-ttu-id="ce26f-108">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ce26f-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ce26f-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="ce26f-109">Attributes</span></span>

|<span data-ttu-id="ce26f-110">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ce26f-110">**Attribute**</span></span>|<span data-ttu-id="ce26f-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ce26f-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ce26f-112">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="ce26f-112">**ResponseClass**</span></span> <br/> | <span data-ttu-id="ce26f-113">Describe el estado de una respuesta de [operación de FindConversation](findconversation-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="ce26f-113">Describes the status of a [FindConversation operation](findconversation-operation.md) response.</span></span> <br/><br/><span data-ttu-id="ce26f-114">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="ce26f-114">The following values are valid for this attribute:</span></span><br/>  <br/><span data-ttu-id="ce26f-115">-Correcto</span><span class="sxs-lookup"><span data-stu-id="ce26f-115">-  Success</span></span>  <br/><span data-ttu-id="ce26f-116">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="ce26f-116">-  Warning</span></span>  <br/><span data-ttu-id="ce26f-117">-Error</span><span class="sxs-lookup"><span data-stu-id="ce26f-117">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="ce26f-118">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="ce26f-118">ResponseClass attribute values</span></span>

|<span data-ttu-id="ce26f-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ce26f-119">**Value**</span></span>|<span data-ttu-id="ce26f-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ce26f-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ce26f-121">**Success**</span><span class="sxs-lookup"><span data-stu-id="ce26f-121">**Success**</span></span> <br/> |<span data-ttu-id="ce26f-122">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="ce26f-122">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="ce26f-123">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="ce26f-123">**Warning**</span></span> <br/> | <span data-ttu-id="ce26f-124">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="ce26f-124">Describes a request that was not processed.</span></span> <span data-ttu-id="ce26f-125">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="ce26f-125">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="ce26f-126">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="ce26f-126">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="ce26f-127">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="ce26f-127">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="ce26f-128">-Los servicios de dominio de Active Directory (AD DS) están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="ce26f-128">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="ce26f-129">-Se movieron los buzones.</span><span class="sxs-lookup"><span data-stu-id="ce26f-129">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="ce26f-130">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="ce26f-130">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="ce26f-131">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="ce26f-131">-  A password is expired.</span></span>  <br/><span data-ttu-id="ce26f-132">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="ce26f-132">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="ce26f-133">**Error**</span><span class="sxs-lookup"><span data-stu-id="ce26f-133">**Error**</span></span> <br/> | <span data-ttu-id="ce26f-134">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="ce26f-134">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="ce26f-135">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="ce26f-135">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="ce26f-136">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="ce26f-136">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="ce26f-137">-Atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="ce26f-137">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="ce26f-138">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="ce26f-138">-  An unknown tag</span></span>  <br/><span data-ttu-id="ce26f-139">-Un atributo o elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="ce26f-139">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="ce26f-140">-Un intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="ce26f-140">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="ce26f-141">-Un error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="ce26f-141">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="ce26f-142">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="ce26f-142">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ce26f-143">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ce26f-143">Child elements</span></span>

|<span data-ttu-id="ce26f-144">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ce26f-144">**Element**</span></span>|<span data-ttu-id="ce26f-145">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ce26f-145">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ce26f-146">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="ce26f-146">Conversations</span></span>](conversations-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ce26f-147">Contiene una matriz de conversaciones.</span><span class="sxs-lookup"><span data-stu-id="ce26f-147">Contains an array of conversations.</span></span>  <br/> |
|[<span data-ttu-id="ce26f-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="ce26f-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="ce26f-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ce26f-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="ce26f-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ce26f-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="ce26f-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ce26f-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="ce26f-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ce26f-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="ce26f-153">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="ce26f-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="ce26f-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="ce26f-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="ce26f-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="ce26f-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="ce26f-156">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="ce26f-156">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ce26f-157">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ce26f-157">Parent elements</span></span>

<span data-ttu-id="ce26f-158">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ce26f-158">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="ce26f-159">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ce26f-159">Text value</span></span>

<span data-ttu-id="ce26f-160">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ce26f-160">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ce26f-161">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ce26f-161">Remarks</span></span>

<span data-ttu-id="ce26f-162">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ce26f-162">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ce26f-163">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ce26f-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ce26f-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="ce26f-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ce26f-165">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ce26f-165">Schema name</span></span>  <br/> |<span data-ttu-id="ce26f-166">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ce26f-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ce26f-167">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ce26f-167">Validation file</span></span>  <br/> |<span data-ttu-id="ce26f-168">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ce26f-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ce26f-169">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ce26f-169">Can be empty</span></span>  <br/> |<span data-ttu-id="ce26f-170">Falso</span><span class="sxs-lookup"><span data-stu-id="ce26f-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce26f-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce26f-171">See also</span></span>

- [<span data-ttu-id="ce26f-172">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="ce26f-172">FindConversation operation</span></span>](findconversation-operation.md)
- [<span data-ttu-id="ce26f-173">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ce26f-173">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="ce26f-174">Conversaciones en EWS</span><span class="sxs-lookup"><span data-stu-id="ce26f-174">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

