---
title: GetServiceConfigurationResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServiceConfigurationResponse
api_type:
- schema
ms.assetid: 313dac99-0e5c-4198-bafa-89e749934ac7
description: El elemento GetServiceConfigurationResponse define una respuesta a una solicitud de GetServiceConfiguration.
ms.openlocfilehash: 7abc81222125334de2a6ab6e4a618b48fe0caf4f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835668"
---
# <a name="getserviceconfigurationresponse"></a><span data-ttu-id="217d4-103">GetServiceConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="217d4-103">GetServiceConfigurationResponse</span></span>

<span data-ttu-id="217d4-104">El elemento **GetServiceConfigurationResponse** define una respuesta a una solicitud de GetServiceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="217d4-104">The **GetServiceConfigurationResponse** element defines a response to a GetServiceConfiguration request.</span></span> 
  
```XML
<GetServiceConfigurationResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ResponseMessages/>
</GetServiceConfigurationResponse>
```

 <span data-ttu-id="217d4-105">**GetServiceConfigurationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="217d4-105">**GetServiceConfigurationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="217d4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="217d4-106">Attributes and elements</span></span>

<span data-ttu-id="217d4-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="217d4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="217d4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="217d4-108">Attributes</span></span>

|<span data-ttu-id="217d4-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="217d4-109">**Attribute**</span></span>|<span data-ttu-id="217d4-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="217d4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="217d4-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="217d4-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="217d4-112">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="217d4-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="217d4-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="217d4-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="217d4-114">-Éxito</span><span class="sxs-lookup"><span data-stu-id="217d4-114">-  Success</span></span>  <br/><span data-ttu-id="217d4-115">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="217d4-115">-  Warning</span></span>  <br/><span data-ttu-id="217d4-116">-Error</span><span class="sxs-lookup"><span data-stu-id="217d4-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="217d4-117">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="217d4-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="217d4-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="217d4-118">**Value**</span></span>|<span data-ttu-id="217d4-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="217d4-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="217d4-120">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="217d4-120">**Success**</span></span> <br/> |<span data-ttu-id="217d4-121">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="217d4-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="217d4-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="217d4-122">**Warning**</span></span> <br/> | <span data-ttu-id="217d4-123">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="217d4-123">Describes a request that was not processed.</span></span> <span data-ttu-id="217d4-124">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="217d4-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="217d4-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="217d4-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="217d4-126">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="217d4-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="217d4-127">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="217d4-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="217d4-128">-Buzones se han movido.</span><span class="sxs-lookup"><span data-stu-id="217d4-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="217d4-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="217d4-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="217d4-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="217d4-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="217d4-131">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="217d4-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="217d4-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="217d4-132">**Error**</span></span> <br/> | <span data-ttu-id="217d4-133">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="217d4-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="217d4-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="217d4-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="217d4-135">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="217d4-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="217d4-136">-Los atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="217d4-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="217d4-137">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="217d4-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="217d4-138">-Un atributo o un elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="217d4-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="217d4-139">-Un intento de acceso no autorizado por cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="217d4-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="217d4-140">-Un error del lado del servidor en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="217d4-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="217d4-141">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="217d4-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="217d4-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="217d4-142">Child elements</span></span>

|<span data-ttu-id="217d4-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="217d4-143">**Element**</span></span>|<span data-ttu-id="217d4-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="217d4-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="217d4-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="217d4-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="217d4-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="217d4-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="217d4-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="217d4-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="217d4-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="217d4-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="217d4-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="217d4-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="217d4-150">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="217d4-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="217d4-151">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="217d4-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="217d4-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="217d4-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="217d4-153">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="217d4-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="217d4-154">ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="217d4-154">ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)</span></span>](responsemessages-arrayofserviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="217d4-155">Contiene una matriz de los mensajes de respuesta de configuración de servicio.</span><span class="sxs-lookup"><span data-stu-id="217d4-155">Contains an array of service configuration response messages.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="217d4-156">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="217d4-156">Parent elements</span></span>

<span data-ttu-id="217d4-157">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="217d4-157">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="217d4-158">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="217d4-158">Text value</span></span>

<span data-ttu-id="217d4-159">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="217d4-159">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="217d4-160">Comentarios</span><span class="sxs-lookup"><span data-stu-id="217d4-160">Remarks</span></span>

<span data-ttu-id="217d4-161">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="217d4-161">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="217d4-162">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="217d4-162">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="217d4-163">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="217d4-163">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="217d4-164">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="217d4-164">Schema Name</span></span>  <br/> |<span data-ttu-id="217d4-165">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="217d4-165">Messages schema</span></span>  <br/> |
|<span data-ttu-id="217d4-166">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="217d4-166">Validation File</span></span>  <br/> |<span data-ttu-id="217d4-167">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="217d4-167">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="217d4-168">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="217d4-168">Can be Empty</span></span>  <br/> |<span data-ttu-id="217d4-169">False</span><span class="sxs-lookup"><span data-stu-id="217d4-169">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="217d4-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="217d4-170">See also</span></span>

- [<span data-ttu-id="217d4-171">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="217d4-171">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

