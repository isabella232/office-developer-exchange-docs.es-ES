---
title: ConvertIdResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConvertIdResponseMessage
api_type:
- schema
ms.assetid: 7a439cae-0268-4328-9ded-af56ad642227
description: El elemento ConvertIdResponseMessage contiene el estado y el resultado de una solicitud de operación ConvertId.
ms.openlocfilehash: 6668c0b3254191ca628413bae5ff957c3cb95b5e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763895"
---
# <a name="convertidresponsemessage"></a><span data-ttu-id="d3736-103">ConvertIdResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d3736-103">ConvertIdResponseMessage</span></span>

<span data-ttu-id="d3736-104">El elemento **ConvertIdResponseMessage** contiene el estado y el resultado de una solicitud de [operación ConvertId](convertid-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="d3736-104">The **ConvertIdResponseMessage** element contains the status and result of a [ConvertId operation](convertid-operation.md) request.</span></span> 
  
- [<span data-ttu-id="d3736-105">ConvertIdResponse</span><span class="sxs-lookup"><span data-stu-id="d3736-105">ConvertIdResponse</span></span>](convertidresponse.md) 
- [<span data-ttu-id="d3736-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d3736-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="d3736-107">ConvertIdResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d3736-107">ConvertIdResponseMessage</span></span>](convertidresponsemessage.md)
  
```xml
<ConvertIdResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <AlternateId/>
</ConvertIdResponseMessage>
```

 <span data-ttu-id="d3736-108">**ConvertIdResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="d3736-108">**ConvertIdResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d3736-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d3736-109">Attributes and elements</span></span>

<span data-ttu-id="d3736-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d3736-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d3736-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="d3736-111">Attributes</span></span>

|<span data-ttu-id="d3736-112">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="d3736-112">**Attribute**</span></span>|<span data-ttu-id="d3736-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d3736-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d3736-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="d3736-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="d3736-115">Describe el estado de una respuesta de [la operación ConvertId](convertid-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="d3736-115">Describes the status of a [ConvertId operation](convertid-operation.md) response.</span></span><br/><br/><span data-ttu-id="d3736-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="d3736-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="d3736-117">-Éxito</span><span class="sxs-lookup"><span data-stu-id="d3736-117">- Success</span></span>  <br/><span data-ttu-id="d3736-118">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="d3736-118">-  Warning</span></span>  <br/><span data-ttu-id="d3736-119">-Error</span><span class="sxs-lookup"><span data-stu-id="d3736-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="d3736-120">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="d3736-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="d3736-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d3736-121">**Value**</span></span>|<span data-ttu-id="d3736-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d3736-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d3736-123">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="d3736-123">**Success**</span></span> <br/> |<span data-ttu-id="d3736-124">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="d3736-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="d3736-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="d3736-125">**Warning**</span></span> <br/> | <span data-ttu-id="d3736-126">Describe una solicitud que no se procesaron totalmente o para la que se produjo un resultado imprevisto.</span><span class="sxs-lookup"><span data-stu-id="d3736-126">Describes a request that was not fully processed or for which an unintended result occurred.</span></span>  <br/> |
|<span data-ttu-id="d3736-127">**Error**</span><span class="sxs-lookup"><span data-stu-id="d3736-127">**Error**</span></span> <br/> | <span data-ttu-id="d3736-128">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="d3736-128">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="d3736-129">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="d3736-129">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="d3736-130">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="d3736-130">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="d3736-131">-Los atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="d3736-131">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="d3736-132">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="d3736-132">-  An unknown tag</span></span>  <br/><span data-ttu-id="d3736-133">-Un atributo o un elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="d3736-133">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="d3736-134">-Un intento de acceso no autorizado por cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="d3736-134">- An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="d3736-135">-Un error del lado del servidor en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="d3736-135">-  A server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="d3736-136">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="d3736-136">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d3736-137">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d3736-137">Child elements</span></span>

|<span data-ttu-id="d3736-138">**Element**</span><span class="sxs-lookup"><span data-stu-id="d3736-138">**Element**</span></span>|<span data-ttu-id="d3736-139">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d3736-139">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3736-140">MessageText</span><span class="sxs-lookup"><span data-stu-id="d3736-140">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="d3736-141">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d3736-141">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="d3736-142">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d3736-142">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="d3736-143">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d3736-143">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="d3736-144">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d3736-144">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="d3736-145">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d3736-145">Currently unused and reserved for future use.</span></span> <span data-ttu-id="d3736-146">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="d3736-146">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="d3736-147">MessageXml</span><span class="sxs-lookup"><span data-stu-id="d3736-147">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="d3736-148">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="d3736-148">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="d3736-149">AlternateId</span><span class="sxs-lookup"><span data-stu-id="d3736-149">AlternateId</span></span>](alternateid.md) <br/> |<span data-ttu-id="d3736-150">Se describe un identificador convertido en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d3736-150">Describes a converted identifier in the response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d3736-151">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d3736-151">Parent elements</span></span>

|<span data-ttu-id="d3736-152">**Element**</span><span class="sxs-lookup"><span data-stu-id="d3736-152">**Element**</span></span>|<span data-ttu-id="d3736-153">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d3736-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3736-154">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d3736-154">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="d3736-155">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d3736-155">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3736-156">Notas</span><span class="sxs-lookup"><span data-stu-id="d3736-156">Remarks</span></span>

<span data-ttu-id="d3736-157">Se devuelve un mensaje de respuesta por identificador convertido.</span><span class="sxs-lookup"><span data-stu-id="d3736-157">One response message per converted identifier is returned.</span></span> <span data-ttu-id="d3736-158">El elemento [AlternateId](alternateid.md) no aparecerá en la respuesta si se devuelve un código de respuesta de error,</span><span class="sxs-lookup"><span data-stu-id="d3736-158">The [AlternateId](alternateid.md) element will be missing from the response if an error response code is returned,</span></span> 
  
<span data-ttu-id="d3736-159">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="d3736-159">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d3736-160">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d3736-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d3736-161">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d3736-161">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d3736-162">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d3736-162">Schema Name</span></span>  <br/> |<span data-ttu-id="d3736-163">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="d3736-163">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d3736-164">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d3736-164">Validation File</span></span>  <br/> |<span data-ttu-id="d3736-165">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d3736-165">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d3736-166">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d3736-166">Can be Empty</span></span>  <br/> |<span data-ttu-id="d3736-167">False</span><span class="sxs-lookup"><span data-stu-id="d3736-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d3736-168">Ver también</span><span class="sxs-lookup"><span data-stu-id="d3736-168">See also</span></span>

- [<span data-ttu-id="d3736-169">Operación ConvertId</span><span class="sxs-lookup"><span data-stu-id="d3736-169">ConvertId operation</span></span>](convertid-operation.md)
- [<span data-ttu-id="d3736-170">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d3736-170">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

