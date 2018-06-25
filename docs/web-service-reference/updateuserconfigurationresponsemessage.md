---
title: UpdateUserConfigurationResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateUserConfigurationResponseMessage
api_type:
- schema
ms.assetid: 27728e57-5a9b-4314-ad64-df7869098f62
description: El elemento UpdateUserConfigurationResponseMessage contiene el estado y el resultado de una única solicitud de operación UpdateUserConfiguration.
ms.openlocfilehash: db26bb4bc821ac9a09c350009ab8132466e759bf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840875"
---
# <a name="updateuserconfigurationresponsemessage"></a><span data-ttu-id="b3f35-103">UpdateUserConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b3f35-103">UpdateUserConfigurationResponseMessage</span></span>

<span data-ttu-id="b3f35-104">El elemento **UpdateUserConfigurationResponseMessage** contiene el estado y el resultado de una única solicitud de operación UpdateUserConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b3f35-104">The **UpdateUserConfigurationResponseMessage** element contains the status and result of a single UpdateUserConfiguration operation request.</span></span> 
  
```xml
<UpdateUserConfigurationResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</UpdateUserConfigurationResponseMessage>
```

 <span data-ttu-id="b3f35-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="b3f35-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b3f35-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b3f35-106">Attributes and elements</span></span>

<span data-ttu-id="b3f35-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b3f35-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b3f35-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b3f35-108">Attributes</span></span>

|<span data-ttu-id="b3f35-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="b3f35-109">**Attribute**</span></span>|<span data-ttu-id="b3f35-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b3f35-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b3f35-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="b3f35-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="b3f35-112">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b3f35-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="b3f35-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="b3f35-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="b3f35-114">-Éxito</span><span class="sxs-lookup"><span data-stu-id="b3f35-114">-  Success</span></span>  <br/><span data-ttu-id="b3f35-115">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="b3f35-115">-  Warning</span></span>  <br/><span data-ttu-id="b3f35-116">-Error</span><span class="sxs-lookup"><span data-stu-id="b3f35-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="b3f35-117">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="b3f35-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="b3f35-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b3f35-118">**Value**</span></span>|<span data-ttu-id="b3f35-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b3f35-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b3f35-120">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="b3f35-120">**Success**</span></span> <br/> |<span data-ttu-id="b3f35-121">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="b3f35-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="b3f35-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="b3f35-122">**Warning**</span></span> <br/> | <span data-ttu-id="b3f35-123">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="b3f35-123">Describes a request that was not processed.</span></span> <span data-ttu-id="b3f35-124">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="b3f35-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="b3f35-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="b3f35-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="b3f35-126">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="b3f35-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="b3f35-127">-El servicio de directorio de Active Directory está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="b3f35-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="b3f35-128">-Buzones se han movido.</span><span class="sxs-lookup"><span data-stu-id="b3f35-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="b3f35-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="b3f35-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="b3f35-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="b3f35-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="b3f35-131">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="b3f35-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="b3f35-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="b3f35-132">**Error**</span></span> <br/> | <span data-ttu-id="b3f35-133">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="b3f35-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="b3f35-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="b3f35-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="b3f35-135">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="b3f35-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="b3f35-136">-Los atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="b3f35-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="b3f35-137">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="b3f35-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="b3f35-138">-De atributo o elemento no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="b3f35-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="b3f35-139">-Intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="b3f35-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="b3f35-140">-Error server-side en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="b3f35-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="b3f35-141">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="b3f35-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b3f35-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b3f35-142">Child elements</span></span>

|<span data-ttu-id="b3f35-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="b3f35-143">**Element**</span></span>|<span data-ttu-id="b3f35-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b3f35-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3f35-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="b3f35-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="b3f35-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b3f35-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="b3f35-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b3f35-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="b3f35-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b3f35-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="b3f35-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="b3f35-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="b3f35-150">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="b3f35-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="b3f35-151">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="b3f35-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="b3f35-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="b3f35-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="b3f35-153">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="b3f35-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b3f35-154">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b3f35-154">Parent elements</span></span>

|<span data-ttu-id="b3f35-155">**Element**</span><span class="sxs-lookup"><span data-stu-id="b3f35-155">**Element**</span></span>|<span data-ttu-id="b3f35-156">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b3f35-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3f35-157">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b3f35-157">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="b3f35-158">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b3f35-158">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3f35-159">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b3f35-159">Remarks</span></span>

<span data-ttu-id="b3f35-160">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con la función de servidor de acceso de cliente instalada.</span><span class="sxs-lookup"><span data-stu-id="b3f35-160">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b3f35-161">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b3f35-161">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b3f35-162">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b3f35-162">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b3f35-163">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b3f35-163">Schema Name</span></span>  <br/> |<span data-ttu-id="b3f35-164">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b3f35-164">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b3f35-165">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b3f35-165">Validation File</span></span>  <br/> |<span data-ttu-id="b3f35-166">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b3f35-166">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b3f35-167">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b3f35-167">Can be Empty</span></span>  <br/> |<span data-ttu-id="b3f35-168">False</span><span class="sxs-lookup"><span data-stu-id="b3f35-168">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b3f35-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3f35-169">See also</span></span>

- [<span data-ttu-id="b3f35-170">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b3f35-170">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

