---
title: PlayOnPhoneResponse (servicios Web de Exchange)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PlayOnPhoneResponse
api_type:
- schema
ms.assetid: 578b70d1-dc9d-4bce-b859-0109b2d2bcec
description: El elemento PlayOnPhoneResponse especifica la respuesta a una solicitud para reproducir un correo de voz en el teléfono.
ms.openlocfilehash: 203309bdd6d17b1c78054e673f8a340c2f069b38
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836831"
---
# <a name="playonphoneresponse-exchange-web-services"></a><span data-ttu-id="6a788-103">PlayOnPhoneResponse (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="6a788-103">PlayOnPhoneResponse (Exchange Web Services)</span></span>

<span data-ttu-id="6a788-104">El elemento **PlayOnPhoneResponse** especifica la respuesta a una solicitud para reproducir un correo de voz en el teléfono.</span><span class="sxs-lookup"><span data-stu-id="6a788-104">The **PlayOnPhoneResponse** element specifies the response to a request to play a voice mail over the telephone.</span></span> 
  
```xml
<PlayOnPhoneResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <PhoneCallId/>
</PlayOnPhoneResponse>
```

 <span data-ttu-id="6a788-105">**PlayOnPhoneResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="6a788-105">**PlayOnPhoneResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6a788-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6a788-106">Attributes and elements</span></span>

<span data-ttu-id="6a788-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6a788-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6a788-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6a788-108">Attributes</span></span>

|<span data-ttu-id="6a788-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="6a788-109">**Attribute**</span></span>|<span data-ttu-id="6a788-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6a788-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6a788-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="6a788-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="6a788-112">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6a788-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="6a788-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="6a788-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="6a788-114">-Éxito</span><span class="sxs-lookup"><span data-stu-id="6a788-114">-  Success</span></span>  <br/><span data-ttu-id="6a788-115">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="6a788-115">-  Warning</span></span>  <br/><span data-ttu-id="6a788-116">-Error</span><span class="sxs-lookup"><span data-stu-id="6a788-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="6a788-117">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="6a788-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="6a788-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6a788-118">**Value**</span></span>|<span data-ttu-id="6a788-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6a788-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6a788-120">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="6a788-120">**Success**</span></span> <br/> |<span data-ttu-id="6a788-121">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="6a788-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="6a788-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="6a788-122">**Warning**</span></span> <br/> | <span data-ttu-id="6a788-123">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="6a788-123">Describes a request that was not processed.</span></span> <span data-ttu-id="6a788-124">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="6a788-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="6a788-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="6a788-125">The following are examples of sources of warnings:</span></span> <br/><br/><span data-ttu-id="6a788-126">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="6a788-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="6a788-127">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="6a788-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="6a788-128">-Buzones se han movido.</span><span class="sxs-lookup"><span data-stu-id="6a788-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="6a788-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="6a788-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="6a788-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="6a788-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="6a788-131">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="6a788-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="6a788-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="6a788-132">**Error**</span></span> <br/> | <span data-ttu-id="6a788-133">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="6a788-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="6a788-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="6a788-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="6a788-135">-No válida Atributos o elementos.</span><span class="sxs-lookup"><span data-stu-id="6a788-135">-  Invalid attributes or elements.</span></span>  <br/><span data-ttu-id="6a788-136">-Los atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="6a788-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="6a788-137">-Una etiqueta desconocida.</span><span class="sxs-lookup"><span data-stu-id="6a788-137">-  An unknown tag.</span></span>  <br/><span data-ttu-id="6a788-138">-Un atributo o un elemento que no es válido en el contexto.</span><span class="sxs-lookup"><span data-stu-id="6a788-138">-  An attribute or element that is not valid in the context.</span></span>  <br/><span data-ttu-id="6a788-139">-Un intento de acceso no autorizado por cualquier cliente.</span><span class="sxs-lookup"><span data-stu-id="6a788-139">-  An unauthorized access attempt by any client.</span></span>  <br/><span data-ttu-id="6a788-140">-Un error del servidor en respuesta a una llamada de cliente válida.</span><span class="sxs-lookup"><span data-stu-id="6a788-140">-  A server-side failure in response to a valid client-side call.</span></span>  <br/><br/>  <span data-ttu-id="6a788-141">Información sobre el error puede encontrarse en los temas de elemento de [textoMensaje](messagetext.md) y [ResponseCode](responsecode.md) .</span><span class="sxs-lookup"><span data-stu-id="6a788-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) element topics.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6a788-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6a788-142">Child elements</span></span>

|<span data-ttu-id="6a788-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="6a788-143">**Element**</span></span>|<span data-ttu-id="6a788-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6a788-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6a788-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="6a788-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="6a788-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6a788-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="6a788-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="6a788-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="6a788-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6a788-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="6a788-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="6a788-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="6a788-150">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="6a788-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="6a788-151">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="6a788-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="6a788-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="6a788-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="6a788-153">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="6a788-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="6a788-154">PhoneCallId</span><span class="sxs-lookup"><span data-stu-id="6a788-154">PhoneCallId</span></span>](phonecallid.md) <br/> |<span data-ttu-id="6a788-155">Especifica el identificador de llamada de teléfono.</span><span class="sxs-lookup"><span data-stu-id="6a788-155">Specifies the telephone call identifier.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6a788-156">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6a788-156">Parent elements</span></span>

<span data-ttu-id="6a788-157">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6a788-157">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6a788-158">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a788-158">Remarks</span></span>

<span data-ttu-id="6a788-159">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6a788-159">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6a788-160">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6a788-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6a788-161">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6a788-161">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6a788-162">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6a788-162">Schema Name</span></span>  <br/> |<span data-ttu-id="6a788-163">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="6a788-163">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6a788-164">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6a788-164">Validation File</span></span>  <br/> |<span data-ttu-id="6a788-165">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6a788-165">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6a788-166">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6a788-166">Can be Empty</span></span>  <br/> |<span data-ttu-id="6a788-167">False</span><span class="sxs-lookup"><span data-stu-id="6a788-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6a788-168">Ver también</span><span class="sxs-lookup"><span data-stu-id="6a788-168">See also</span></span>

- [<span data-ttu-id="6a788-169">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="6a788-169">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

