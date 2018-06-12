---
title: MailTipsResponseMessageType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTipsResponseMessageType
api_type:
- schema
ms.assetid: 532cb9d9-1232-4e88-80aa-4cf163eb05da
description: El elemento MailTipsResponseMessageType representa la configuración de sugerencias de correo.
ms.openlocfilehash: 76a1e33ae189b96a96a41d1bc7a8f79116761c4f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836334"
---
# <a name="mailtipsresponsemessagetype"></a><span data-ttu-id="615f7-103">MailTipsResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="615f7-103">MailTipsResponseMessageType</span></span>

<span data-ttu-id="615f7-104">El elemento **MailTipsResponseMessageType** representa la configuración de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="615f7-104">The **MailTipsResponseMessageType** element represents mail tips settings.</span></span> 
  
```XML
<MailTipsResponseMessageType ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MailTips/>
</MailTipsResponseMessageType>
```

 <span data-ttu-id="615f7-105">**MailTipsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="615f7-105">**MailTipsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="615f7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="615f7-106">Attributes and elements</span></span>

<span data-ttu-id="615f7-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="615f7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="615f7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="615f7-108">Attributes</span></span>

|<span data-ttu-id="615f7-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="615f7-109">**Attribute**</span></span>|<span data-ttu-id="615f7-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="615f7-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="615f7-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="615f7-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="615f7-112">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="615f7-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="615f7-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="615f7-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="615f7-114">-Éxito</span><span class="sxs-lookup"><span data-stu-id="615f7-114">-  Success</span></span>  <br/><span data-ttu-id="615f7-115">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="615f7-115">-  Warning</span></span>  <br/><span data-ttu-id="615f7-116">-Error</span><span class="sxs-lookup"><span data-stu-id="615f7-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="615f7-117">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="615f7-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="615f7-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="615f7-118">**Value**</span></span>|<span data-ttu-id="615f7-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="615f7-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="615f7-120">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="615f7-120">**Success**</span></span> <br/> |<span data-ttu-id="615f7-121">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="615f7-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="615f7-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="615f7-122">**Warning**</span></span> <br/> | <span data-ttu-id="615f7-123">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="615f7-123">Describes a request that was not processed.</span></span> <span data-ttu-id="615f7-124">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="615f7-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="615f7-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="615f7-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="615f7-126">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="615f7-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="615f7-127">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="615f7-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="615f7-128">-Buzones se han movido.</span><span class="sxs-lookup"><span data-stu-id="615f7-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="615f7-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="615f7-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="615f7-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="615f7-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="615f7-131">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="615f7-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="615f7-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="615f7-132">**Error**</span></span> <br/> | <span data-ttu-id="615f7-133">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="615f7-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="615f7-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="615f7-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="615f7-135">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="615f7-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="615f7-136">-Los atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="615f7-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="615f7-137">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="615f7-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="615f7-138">-Un atributo o un elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="615f7-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="615f7-139">-Un intento de acceso no autorizado por cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="615f7-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="615f7-140">-Un error del lado del servidor en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="615f7-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="615f7-141">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="615f7-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="615f7-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="615f7-142">Child elements</span></span>

|<span data-ttu-id="615f7-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="615f7-143">**Element**</span></span>|<span data-ttu-id="615f7-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="615f7-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="615f7-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="615f7-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="615f7-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="615f7-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="615f7-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="615f7-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="615f7-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="615f7-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="615f7-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="615f7-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="615f7-150">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="615f7-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="615f7-151">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="615f7-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="615f7-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="615f7-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="615f7-153">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="615f7-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="615f7-154">Sugerencias de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="615f7-154">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="615f7-155">Representa los valores de distintos tipos de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="615f7-155">Represents values for various types of mail tips.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="615f7-156">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="615f7-156">Parent elements</span></span>

|<span data-ttu-id="615f7-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="615f7-157">**Element**</span></span>|<span data-ttu-id="615f7-158">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="615f7-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="615f7-159">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="615f7-159">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span></span>](responsemessages-arrayofmailtipsresponsemessagetype.md) <br/> |<span data-ttu-id="615f7-160">Representa una lista de los mensajes de respuesta de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="615f7-160">Represents a list of mail tips response messages.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="615f7-161">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="615f7-161">Text value</span></span>

<span data-ttu-id="615f7-162">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="615f7-162">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="615f7-163">Observaciones</span><span class="sxs-lookup"><span data-stu-id="615f7-163">Remarks</span></span>

<span data-ttu-id="615f7-164">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="615f7-164">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="615f7-165">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="615f7-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="615f7-166">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="615f7-166">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="615f7-167">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="615f7-167">Schema Name</span></span>  <br/> |<span data-ttu-id="615f7-168">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="615f7-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="615f7-169">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="615f7-169">Validation File</span></span>  <br/> |<span data-ttu-id="615f7-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="615f7-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="615f7-171">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="615f7-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="615f7-172">False</span><span class="sxs-lookup"><span data-stu-id="615f7-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="615f7-173">Ver también</span><span class="sxs-lookup"><span data-stu-id="615f7-173">See also</span></span>

- [<span data-ttu-id="615f7-174">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="615f7-174">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

