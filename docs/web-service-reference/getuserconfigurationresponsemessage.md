---
title: GetUserConfigurationResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserConfigurationResponseMessage
api_type:
- schema
ms.assetid: f75e29eb-ae98-46fd-8da2-1c76a57f5458
description: El elemento GetUserConfigurationResponseMessage representa una respuesta que devuelve un objeto de configuración de usuario.
ms.openlocfilehash: 28c14d11218294bd8dd64f70e755cda8f8335856
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835690"
---
# <a name="getuserconfigurationresponsemessage"></a><span data-ttu-id="0dbea-103">GetUserConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0dbea-103">GetUserConfigurationResponseMessage</span></span>

<span data-ttu-id="0dbea-104">El elemento **GetUserConfigurationResponseMessage** representa una respuesta que devuelve un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="0dbea-104">The **GetUserConfigurationResponseMessage** element represents a response that returns a user configuration object.</span></span> 
  
```xml
<GetUserConfigurationResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <UserConfiguration/>
</GetUserConfigurationResponseMessage>
```

 <span data-ttu-id="0dbea-105">**GetUserConfigurationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="0dbea-105">**GetUserConfigurationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0dbea-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0dbea-106">Attributes and elements</span></span>

<span data-ttu-id="0dbea-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0dbea-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0dbea-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0dbea-108">Attributes</span></span>

|<span data-ttu-id="0dbea-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="0dbea-109">**Attribute**</span></span>|<span data-ttu-id="0dbea-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0dbea-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0dbea-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="0dbea-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="0dbea-112">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0dbea-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="0dbea-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="0dbea-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="0dbea-114">-Éxito</span><span class="sxs-lookup"><span data-stu-id="0dbea-114">-  Success</span></span>  <br/><span data-ttu-id="0dbea-115">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="0dbea-115">-  Warning</span></span>  <br/><span data-ttu-id="0dbea-116">-Error</span><span class="sxs-lookup"><span data-stu-id="0dbea-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="0dbea-117">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="0dbea-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="0dbea-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0dbea-118">**Value**</span></span>|<span data-ttu-id="0dbea-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0dbea-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0dbea-120">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="0dbea-120">**Success**</span></span> <br/> |<span data-ttu-id="0dbea-121">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="0dbea-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="0dbea-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="0dbea-122">**Warning**</span></span> <br/> | <span data-ttu-id="0dbea-123">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="0dbea-123">Describes a request that was not processed.</span></span> <span data-ttu-id="0dbea-124">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="0dbea-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="0dbea-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="0dbea-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="0dbea-126">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="0dbea-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="0dbea-127">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="0dbea-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="0dbea-128">-Buzones se han movido.</span><span class="sxs-lookup"><span data-stu-id="0dbea-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="0dbea-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="0dbea-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="0dbea-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="0dbea-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="0dbea-131">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="0dbea-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="0dbea-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="0dbea-132">**Error**</span></span> <br/> | <span data-ttu-id="0dbea-133">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="0dbea-133">Describes a request that cannot be fulfilled.</span></span><br/><br/> <span data-ttu-id="0dbea-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="0dbea-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="0dbea-135">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="0dbea-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="0dbea-136">-Los atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="0dbea-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="0dbea-137">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="0dbea-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="0dbea-138">-Un atributo o elemento no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="0dbea-138">-  An attribute or element is not valid in the context</span></span>  <br/><span data-ttu-id="0dbea-139">-Un intento de acceso no autorizado por cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="0dbea-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="0dbea-140">-Un error del lado del servidor en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="0dbea-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="0dbea-141">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="0dbea-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0dbea-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0dbea-142">Child elements</span></span>

|<span data-ttu-id="0dbea-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="0dbea-143">**Element**</span></span>|<span data-ttu-id="0dbea-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0dbea-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0dbea-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="0dbea-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="0dbea-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0dbea-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="0dbea-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0dbea-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="0dbea-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0dbea-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="0dbea-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0dbea-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="0dbea-150">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="0dbea-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="0dbea-151">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="0dbea-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="0dbea-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="0dbea-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="0dbea-153">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="0dbea-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="0dbea-154">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="0dbea-154">UserConfiguration</span></span>](userconfiguration.md) <br/> |<span data-ttu-id="0dbea-155">Contiene un objeto de configuración de usuario único.</span><span class="sxs-lookup"><span data-stu-id="0dbea-155">Contains a single user configuration object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0dbea-156">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0dbea-156">Parent elements</span></span>

|<span data-ttu-id="0dbea-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="0dbea-157">**Element**</span></span>|<span data-ttu-id="0dbea-158">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0dbea-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0dbea-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0dbea-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="0dbea-160">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0dbea-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0dbea-161">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0dbea-161">Text value</span></span>

<span data-ttu-id="0dbea-162">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0dbea-162">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0dbea-163">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0dbea-163">Remarks</span></span>

<span data-ttu-id="0dbea-164">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0dbea-164">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0dbea-165">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0dbea-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0dbea-166">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0dbea-166">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0dbea-167">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0dbea-167">Schema Name</span></span>  <br/> |<span data-ttu-id="0dbea-168">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="0dbea-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0dbea-169">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0dbea-169">Validation File</span></span>  <br/> |<span data-ttu-id="0dbea-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0dbea-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0dbea-171">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0dbea-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="0dbea-172">False</span><span class="sxs-lookup"><span data-stu-id="0dbea-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0dbea-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="0dbea-173">See also</span></span>

- [<span data-ttu-id="0dbea-174">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0dbea-174">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

