---
title: SendItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendItemResponseMessage
api_type:
- schema
ms.assetid: 264f6a2f-c8cc-4c96-86e1-1aabb6f9d8ab
description: El elemento SendItemResponseMessage contiene el estado y el resultado de una única solicitud de operación de SendItem.
ms.openlocfilehash: 70355aa2b46303bfceafa2cfe89f1c84896f3158
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837344"
---
# <a name="senditemresponsemessage"></a><span data-ttu-id="1431f-103">SendItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1431f-103">SendItemResponseMessage</span></span>

<span data-ttu-id="1431f-104">El elemento **SendItemResponseMessage** contiene el estado y el resultado de una única solicitud de [la operación de SendItem](senditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="1431f-104">The **SendItemResponseMessage** element contains the status and result of a single [SendItem operation](senditem-operation.md) request.</span></span> 
  
```xml
<SendItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</SendItemResponseMessage>
```

 <span data-ttu-id="1431f-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="1431f-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1431f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1431f-106">Attributes and elements</span></span>

<span data-ttu-id="1431f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1431f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1431f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1431f-108">Attributes</span></span>

|<span data-ttu-id="1431f-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="1431f-109">**Attribute**</span></span>|<span data-ttu-id="1431f-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1431f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1431f-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="1431f-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="1431f-112">Describe el estado de una respuesta de [la operación de SendItem](senditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="1431f-112">Describes the status of a [SendItem operation](senditem-operation.md) response.</span></span> <br/><br/><span data-ttu-id="1431f-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="1431f-113">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="1431f-114">-Éxito</span><span class="sxs-lookup"><span data-stu-id="1431f-114">-  Success</span></span>  <br/><span data-ttu-id="1431f-115">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="1431f-115">-  Warning</span></span>  <br/><span data-ttu-id="1431f-116">-Error</span><span class="sxs-lookup"><span data-stu-id="1431f-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="1431f-117">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="1431f-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="1431f-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1431f-118">**Value**</span></span>|<span data-ttu-id="1431f-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1431f-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1431f-120">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="1431f-120">**Success**</span></span> <br/> |<span data-ttu-id="1431f-121">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="1431f-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="1431f-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="1431f-122">**Warning**</span></span> <br/> | <span data-ttu-id="1431f-123">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="1431f-123">Describes a request that was not processed.</span></span> <span data-ttu-id="1431f-124">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="1431f-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="1431f-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="1431f-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="1431f-126">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="1431f-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="1431f-127">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="1431f-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="1431f-128">-Se mueven los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="1431f-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="1431f-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="1431f-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="1431f-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="1431f-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="1431f-131">-Se ha excedido una cuota.</span><span class="sxs-lookup"><span data-stu-id="1431f-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="1431f-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="1431f-132">**Error**</span></span> <br/> | <span data-ttu-id="1431f-133">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="1431f-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="1431f-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="1431f-134">The following are examples of sources of errors:</span></span>  <br/> <br/><span data-ttu-id="1431f-135">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="1431f-135">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="1431f-136">-Los atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="1431f-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="1431f-137">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="1431f-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="1431f-138">-De atributo o elemento no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="1431f-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="1431f-139">-Intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="1431f-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="1431f-140">-Error server-side en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="1431f-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="1431f-141">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="1431f-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1431f-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1431f-142">Child elements</span></span>

|<span data-ttu-id="1431f-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="1431f-143">**Element**</span></span>|<span data-ttu-id="1431f-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1431f-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1431f-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="1431f-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="1431f-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1431f-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="1431f-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1431f-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="1431f-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1431f-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="1431f-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="1431f-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="1431f-150">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="1431f-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="1431f-151">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="1431f-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="1431f-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="1431f-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="1431f-153">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="1431f-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1431f-154">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1431f-154">Parent elements</span></span>

|<span data-ttu-id="1431f-155">**Element**</span><span class="sxs-lookup"><span data-stu-id="1431f-155">**Element**</span></span>|<span data-ttu-id="1431f-156">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1431f-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1431f-157">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="1431f-157">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="1431f-158">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1431f-158">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1431f-159">Notas</span><span class="sxs-lookup"><span data-stu-id="1431f-159">Remarks</span></span>

<span data-ttu-id="1431f-160">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con la función de servidor de acceso de cliente instalada.</span><span class="sxs-lookup"><span data-stu-id="1431f-160">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1431f-161">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1431f-161">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1431f-162">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1431f-162">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1431f-163">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1431f-163">Schema Name</span></span>  <br/> |<span data-ttu-id="1431f-164">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="1431f-164">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1431f-165">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1431f-165">Validation File</span></span>  <br/> |<span data-ttu-id="1431f-166">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1431f-166">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1431f-167">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1431f-167">Can be Empty</span></span>  <br/> |<span data-ttu-id="1431f-168">False</span><span class="sxs-lookup"><span data-stu-id="1431f-168">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1431f-169">Ver también</span><span class="sxs-lookup"><span data-stu-id="1431f-169">See also</span></span>

- [<span data-ttu-id="1431f-170">Operación SendItem</span><span class="sxs-lookup"><span data-stu-id="1431f-170">SendItem operation</span></span>](senditem-operation.md)
- [<span data-ttu-id="1431f-171">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="1431f-171">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

