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
ms.openlocfilehash: cd0154f87390be3516ced4be53f5371d4a348c49
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456223"
---
# <a name="convertidresponsemessage"></a><span data-ttu-id="6d2c0-103">ConvertIdResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6d2c0-103">ConvertIdResponseMessage</span></span>

<span data-ttu-id="6d2c0-104">El elemento **ConvertIdResponseMessage** contiene el estado y el resultado de una solicitud de [operación ConvertId](convertid-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="6d2c0-104">The **ConvertIdResponseMessage** element contains the status and result of a [ConvertId operation](convertid-operation.md) request.</span></span> 
  
- [<span data-ttu-id="6d2c0-105">ConvertIdResponse</span><span class="sxs-lookup"><span data-stu-id="6d2c0-105">ConvertIdResponse</span></span>](convertidresponse.md) 
- [<span data-ttu-id="6d2c0-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="6d2c0-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="6d2c0-107">ConvertIdResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6d2c0-107">ConvertIdResponseMessage</span></span>](convertidresponsemessage.md)
  
```xml
<ConvertIdResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <AlternateId/>
</ConvertIdResponseMessage>
```

 <span data-ttu-id="6d2c0-108">**ConvertIdResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="6d2c0-108">**ConvertIdResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6d2c0-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6d2c0-109">Attributes and elements</span></span>

<span data-ttu-id="6d2c0-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6d2c0-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6d2c0-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="6d2c0-111">Attributes</span></span>

|<span data-ttu-id="6d2c0-112">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="6d2c0-112">**Attribute**</span></span>|<span data-ttu-id="6d2c0-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6d2c0-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6d2c0-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="6d2c0-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="6d2c0-115">Describe el estado de una respuesta de [operación de ConvertId](convertid-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="6d2c0-115">Describes the status of a [ConvertId operation](convertid-operation.md) response.</span></span><br/><br/><span data-ttu-id="6d2c0-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="6d2c0-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="6d2c0-117">-Correcto</span><span class="sxs-lookup"><span data-stu-id="6d2c0-117">- Success</span></span>  <br/><span data-ttu-id="6d2c0-118">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="6d2c0-118">-  Warning</span></span>  <br/><span data-ttu-id="6d2c0-119">-Error</span><span class="sxs-lookup"><span data-stu-id="6d2c0-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="6d2c0-120">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="6d2c0-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="6d2c0-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6d2c0-121">**Value**</span></span>|<span data-ttu-id="6d2c0-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6d2c0-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6d2c0-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="6d2c0-123">**Success**</span></span> <br/> |<span data-ttu-id="6d2c0-124">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="6d2c0-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="6d2c0-125">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="6d2c0-125">**Warning**</span></span> <br/> | <span data-ttu-id="6d2c0-126">Describe una solicitud que no se ha procesado completamente o para la que se ha producido un resultado no intencionado.</span><span class="sxs-lookup"><span data-stu-id="6d2c0-126">Describes a request that was not fully processed or for which an unintended result occurred.</span></span>  <br/> |
|<span data-ttu-id="6d2c0-127">**Error**</span><span class="sxs-lookup"><span data-stu-id="6d2c0-127">**Error**</span></span> <br/> | <span data-ttu-id="6d2c0-128">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="6d2c0-128">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="6d2c0-129">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="6d2c0-129">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="6d2c0-130">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="6d2c0-130">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="6d2c0-131">-Atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="6d2c0-131">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="6d2c0-132">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="6d2c0-132">-  An unknown tag</span></span>  <br/><span data-ttu-id="6d2c0-133">-Un atributo o elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="6d2c0-133">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="6d2c0-134">-Un intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="6d2c0-134">- An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="6d2c0-135">-Un error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="6d2c0-135">-  A server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="6d2c0-136">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="6d2c0-136">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6d2c0-137">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6d2c0-137">Child elements</span></span>

|<span data-ttu-id="6d2c0-138">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6d2c0-138">**Element**</span></span>|<span data-ttu-id="6d2c0-139">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6d2c0-139">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6d2c0-140">MessageText</span><span class="sxs-lookup"><span data-stu-id="6d2c0-140">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="6d2c0-141">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6d2c0-141">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="6d2c0-142">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="6d2c0-142">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="6d2c0-143">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6d2c0-143">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="6d2c0-144">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="6d2c0-144">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="6d2c0-145">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="6d2c0-145">Currently unused and reserved for future use.</span></span> <span data-ttu-id="6d2c0-146">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="6d2c0-146">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="6d2c0-147">MessageXml</span><span class="sxs-lookup"><span data-stu-id="6d2c0-147">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="6d2c0-148">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="6d2c0-148">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="6d2c0-149">AlternateId</span><span class="sxs-lookup"><span data-stu-id="6d2c0-149">AlternateId</span></span>](alternateid.md) <br/> |<span data-ttu-id="6d2c0-150">Describe un identificador convertido en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6d2c0-150">Describes a converted identifier in the response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6d2c0-151">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6d2c0-151">Parent elements</span></span>

|<span data-ttu-id="6d2c0-152">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6d2c0-152">**Element**</span></span>|<span data-ttu-id="6d2c0-153">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6d2c0-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6d2c0-154">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="6d2c0-154">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="6d2c0-155">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6d2c0-155">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d2c0-156">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6d2c0-156">Remarks</span></span>

<span data-ttu-id="6d2c0-157">Se devuelve un mensaje de respuesta por identificador convertido.</span><span class="sxs-lookup"><span data-stu-id="6d2c0-157">One response message per converted identifier is returned.</span></span> <span data-ttu-id="6d2c0-158">El elemento [AlternateId](alternateid.md) no estará en la respuesta si se devuelve un código de respuesta de error,</span><span class="sxs-lookup"><span data-stu-id="6d2c0-158">The [AlternateId](alternateid.md) element will be missing from the response if an error response code is returned,</span></span> 
  
<span data-ttu-id="6d2c0-159">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange 2010 y que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="6d2c0-159">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6d2c0-160">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6d2c0-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6d2c0-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="6d2c0-161">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6d2c0-162">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6d2c0-162">Schema Name</span></span>  <br/> |<span data-ttu-id="6d2c0-163">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="6d2c0-163">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6d2c0-164">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6d2c0-164">Validation File</span></span>  <br/> |<span data-ttu-id="6d2c0-165">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6d2c0-165">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6d2c0-166">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6d2c0-166">Can be Empty</span></span>  <br/> |<span data-ttu-id="6d2c0-167">Falso</span><span class="sxs-lookup"><span data-stu-id="6d2c0-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6d2c0-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d2c0-168">See also</span></span>

- [<span data-ttu-id="6d2c0-169">Operación ConvertId</span><span class="sxs-lookup"><span data-stu-id="6d2c0-169">ConvertId operation</span></span>](convertid-operation.md)
- [<span data-ttu-id="6d2c0-170">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6d2c0-170">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

