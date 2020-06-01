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
description: El elemento GetServiceConfigurationResponse define una respuesta a una solicitud GetServiceConfiguration.
ms.openlocfilehash: ae74bc13a59e1c7a6a4ad0dbfddeea37671c52b0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460529"
---
# <a name="getserviceconfigurationresponse"></a><span data-ttu-id="102b0-103">GetServiceConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="102b0-103">GetServiceConfigurationResponse</span></span>

<span data-ttu-id="102b0-104">El elemento **GetServiceConfigurationResponse** define una respuesta a una solicitud GetServiceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="102b0-104">The **GetServiceConfigurationResponse** element defines a response to a GetServiceConfiguration request.</span></span> 
  
```XML
<GetServiceConfigurationResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ResponseMessages/>
</GetServiceConfigurationResponse>
```

 <span data-ttu-id="102b0-105">**GetServiceConfigurationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="102b0-105">**GetServiceConfigurationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="102b0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="102b0-106">Attributes and elements</span></span>

<span data-ttu-id="102b0-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="102b0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="102b0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="102b0-108">Attributes</span></span>

|<span data-ttu-id="102b0-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="102b0-109">**Attribute**</span></span>|<span data-ttu-id="102b0-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="102b0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="102b0-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="102b0-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="102b0-112">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="102b0-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="102b0-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="102b0-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="102b0-114">-Correcto</span><span class="sxs-lookup"><span data-stu-id="102b0-114">-  Success</span></span>  <br/><span data-ttu-id="102b0-115">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="102b0-115">-  Warning</span></span>  <br/><span data-ttu-id="102b0-116">-Error</span><span class="sxs-lookup"><span data-stu-id="102b0-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="102b0-117">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="102b0-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="102b0-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="102b0-118">**Value**</span></span>|<span data-ttu-id="102b0-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="102b0-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="102b0-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="102b0-120">**Success**</span></span> <br/> |<span data-ttu-id="102b0-121">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="102b0-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="102b0-122">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="102b0-122">**Warning**</span></span> <br/> | <span data-ttu-id="102b0-123">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="102b0-123">Describes a request that was not processed.</span></span> <span data-ttu-id="102b0-124">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="102b0-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="102b0-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="102b0-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="102b0-126">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="102b0-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="102b0-127">-Los servicios de dominio de Active Directory (AD DS) están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="102b0-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="102b0-128">-Se movieron los buzones.</span><span class="sxs-lookup"><span data-stu-id="102b0-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="102b0-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="102b0-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="102b0-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="102b0-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="102b0-131">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="102b0-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="102b0-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="102b0-132">**Error**</span></span> <br/> | <span data-ttu-id="102b0-133">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="102b0-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="102b0-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="102b0-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="102b0-135">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="102b0-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="102b0-136">-Atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="102b0-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="102b0-137">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="102b0-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="102b0-138">-Un atributo o elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="102b0-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="102b0-139">-Un intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="102b0-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="102b0-140">-Un error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="102b0-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="102b0-141">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="102b0-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="102b0-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="102b0-142">Child elements</span></span>

|<span data-ttu-id="102b0-143">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="102b0-143">**Element**</span></span>|<span data-ttu-id="102b0-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="102b0-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="102b0-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="102b0-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="102b0-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="102b0-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="102b0-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="102b0-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="102b0-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="102b0-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="102b0-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="102b0-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="102b0-150">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="102b0-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="102b0-151">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="102b0-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="102b0-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="102b0-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="102b0-153">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="102b0-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="102b0-154">ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="102b0-154">ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)</span></span>](responsemessages-arrayofserviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="102b0-155">Contiene una matriz de mensajes de respuesta de configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="102b0-155">Contains an array of service configuration response messages.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="102b0-156">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="102b0-156">Parent elements</span></span>

<span data-ttu-id="102b0-157">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="102b0-157">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="102b0-158">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="102b0-158">Text value</span></span>

<span data-ttu-id="102b0-159">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="102b0-159">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="102b0-160">Comentarios</span><span class="sxs-lookup"><span data-stu-id="102b0-160">Remarks</span></span>

<span data-ttu-id="102b0-161">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="102b0-161">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="102b0-162">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="102b0-162">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="102b0-163">Namespace</span><span class="sxs-lookup"><span data-stu-id="102b0-163">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="102b0-164">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="102b0-164">Schema Name</span></span>  <br/> |<span data-ttu-id="102b0-165">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="102b0-165">Messages schema</span></span>  <br/> |
|<span data-ttu-id="102b0-166">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="102b0-166">Validation File</span></span>  <br/> |<span data-ttu-id="102b0-167">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="102b0-167">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="102b0-168">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="102b0-168">Can be Empty</span></span>  <br/> |<span data-ttu-id="102b0-169">Falso</span><span class="sxs-lookup"><span data-stu-id="102b0-169">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="102b0-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="102b0-170">See also</span></span>

- [<span data-ttu-id="102b0-171">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="102b0-171">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

