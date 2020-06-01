---
title: ServiceConfigurationResponseMessageType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ServiceConfigurationResponseMessageType
api_type:
- schema
ms.assetid: ccfb0578-c648-44c2-ac4d-7620d881363e
description: El elemento ServiceConfigurationResponseMessageType contiene opciones de configuración de servicio.
ms.openlocfilehash: 4c84a49b2403343a1defd00696858489497d6214
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44439108"
---
# <a name="serviceconfigurationresponsemessagetype"></a><span data-ttu-id="cf290-103">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="cf290-103">ServiceConfigurationResponseMessageType</span></span>

<span data-ttu-id="cf290-104">El elemento **ServiceConfigurationResponseMessageType** contiene opciones de configuración de servicio.</span><span class="sxs-lookup"><span data-stu-id="cf290-104">The **ServiceConfigurationResponseMessageType** element contains service configuration settings.</span></span> 
  
```XML
<ServiceConfigurationResponseMessageType ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MailTipsConfiguration/>
   <UnifiedMessagingConfiguration/>
   <ProtectionRulesConfiguration/>
</ServiceConfigurationResponseMessageType>
```

 <span data-ttu-id="cf290-105">**ServiceConfigurationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="cf290-105">**ServiceConfigurationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cf290-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cf290-106">Attributes and elements</span></span>

<span data-ttu-id="cf290-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cf290-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cf290-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="cf290-108">Attributes</span></span>

|<span data-ttu-id="cf290-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="cf290-109">**Attribute**</span></span>|<span data-ttu-id="cf290-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf290-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf290-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="cf290-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="cf290-112">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf290-112">Describes the status of the response.</span></span><br/><br/> <span data-ttu-id="cf290-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="cf290-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="cf290-114">-Correcto</span><span class="sxs-lookup"><span data-stu-id="cf290-114">-  Success</span></span>  <br/><span data-ttu-id="cf290-115">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="cf290-115">-  Warning</span></span>  <br/><span data-ttu-id="cf290-116">-Error</span><span class="sxs-lookup"><span data-stu-id="cf290-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="cf290-117">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="cf290-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="cf290-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cf290-118">**Value**</span></span>|<span data-ttu-id="cf290-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf290-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf290-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="cf290-120">**Success**</span></span> <br/> |<span data-ttu-id="cf290-121">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="cf290-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="cf290-122">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="cf290-122">**Warning**</span></span> <br/> | <span data-ttu-id="cf290-123">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="cf290-123">Describes a request that was not processed.</span></span> <span data-ttu-id="cf290-124">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="cf290-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="cf290-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="cf290-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="cf290-126">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="cf290-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="cf290-127">-Los servicios de dominio de Active Directory (AD DS) están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="cf290-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="cf290-128">-Se movieron los buzones.</span><span class="sxs-lookup"><span data-stu-id="cf290-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="cf290-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="cf290-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="cf290-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="cf290-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="cf290-131">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="cf290-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="cf290-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="cf290-132">**Error**</span></span> <br/> | <span data-ttu-id="cf290-133">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="cf290-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="cf290-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="cf290-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="cf290-135">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="cf290-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="cf290-136">-Atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="cf290-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="cf290-137">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="cf290-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="cf290-138">-Un atributo o elemento no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="cf290-138">-  An attribute or element is not valid in the context</span></span>  <br/><span data-ttu-id="cf290-139">-Un intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="cf290-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="cf290-140">-Un error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="cf290-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="cf290-141">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="cf290-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cf290-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cf290-142">Child elements</span></span>

|<span data-ttu-id="cf290-143">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cf290-143">**Element**</span></span>|<span data-ttu-id="cf290-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf290-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf290-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="cf290-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="cf290-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf290-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="cf290-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="cf290-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="cf290-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf290-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="cf290-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="cf290-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="cf290-150">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="cf290-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="cf290-151">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="cf290-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="cf290-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="cf290-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="cf290-153">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="cf290-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="cf290-154">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="cf290-154">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="cf290-155">Contiene información de configuración del servicio para el servicio de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="cf290-155">Contains service configuration information for the mail tips service.</span></span>  <br/> |
|[<span data-ttu-id="cf290-156">UnifiedMessagingConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf290-156">UnifiedMessagingConfiguration</span></span>](unifiedmessagingconfiguration.md) <br/> |<span data-ttu-id="cf290-157">Contiene información de configuración del servicio para el servicio de mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="cf290-157">Contains service configuration information for the Unified Messaging service.</span></span>  <br/> |
|[<span data-ttu-id="cf290-158">ProtectionRulesConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf290-158">ProtectionRulesConfiguration</span></span>](protectionrulesconfiguration.md) <br/> |<span data-ttu-id="cf290-159">Contiene la información de configuración del servicio para el servicio de reglas de protección.</span><span class="sxs-lookup"><span data-stu-id="cf290-159">Contains service configuration information for the protection rules service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cf290-160">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cf290-160">Parent elements</span></span>

|<span data-ttu-id="cf290-161">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cf290-161">**Element**</span></span>|<span data-ttu-id="cf290-162">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf290-162">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf290-163">ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="cf290-163">ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)</span></span>](responsemessages-arrayofserviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="cf290-164">Contiene una matriz de mensajes de respuesta de configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="cf290-164">Contains an array of service configuration response messages.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cf290-165">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="cf290-165">Text value</span></span>

<span data-ttu-id="cf290-166">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cf290-166">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cf290-167">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cf290-167">Remarks</span></span>

<span data-ttu-id="cf290-168">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="cf290-168">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cf290-169">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cf290-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf290-170">Namespace</span><span class="sxs-lookup"><span data-stu-id="cf290-170">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cf290-171">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cf290-171">Schema Name</span></span>  <br/> |<span data-ttu-id="cf290-172">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="cf290-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cf290-173">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cf290-173">Validation File</span></span>  <br/> |<span data-ttu-id="cf290-174">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="cf290-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cf290-175">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cf290-175">Can be Empty</span></span>  <br/> |<span data-ttu-id="cf290-176">Falso</span><span class="sxs-lookup"><span data-stu-id="cf290-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf290-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf290-177">See also</span></span>

- [<span data-ttu-id="cf290-178">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="cf290-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

