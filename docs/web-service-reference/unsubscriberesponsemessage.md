---
title: UnsubscribeResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnsubscribeResponseMessage
api_type:
- schema
ms.assetid: 92c53b13-0ca1-4b44-b925-b23682e9417c
description: El elemento UnsubscribeResponseMessage contiene el estado y el resultado de una única solicitud de operación de cancelación de suscripción.
ms.openlocfilehash: e5b42404d09e6367c134934409ec2a45351e135e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467168"
---
# <a name="unsubscriberesponsemessage"></a><span data-ttu-id="604f6-103">UnsubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="604f6-103">UnsubscribeResponseMessage</span></span>

<span data-ttu-id="604f6-104">El elemento **UnsubscribeResponseMessage** contiene el estado y el resultado de una única solicitud de [operación de cancelación de suscripción](unsubscribe-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="604f6-104">The **UnsubscribeResponseMessage** element contains the status and result of a single [Unsubscribe operation](unsubscribe-operation.md) request.</span></span> 
  
- [<span data-ttu-id="604f6-105">UnsubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="604f6-105">UnsubscribeResponse</span></span>](unsubscriberesponse.md)
- [<span data-ttu-id="604f6-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="604f6-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="604f6-107">UnsubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="604f6-107">UnsubscribeResponseMessage</span></span>](unsubscriberesponsemessage.md)
  
```xml
<UnsubscribeResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</UnsubscribeResponseMessage>
```

 <span data-ttu-id="604f6-108">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="604f6-108">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="604f6-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="604f6-109">Attributes and elements</span></span>

<span data-ttu-id="604f6-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="604f6-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="604f6-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="604f6-111">Attributes</span></span>

|<span data-ttu-id="604f6-112">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="604f6-112">**Attribute**</span></span>|<span data-ttu-id="604f6-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="604f6-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="604f6-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="604f6-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="604f6-115">Describe el estado de una respuesta de [operación de cancelación de suscripción](unsubscribe-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="604f6-115">Describes the status of an [Unsubscribe operation](unsubscribe-operation.md) response.</span></span> <br/><br/><span data-ttu-id="604f6-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="604f6-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="604f6-117">-Correcto</span><span class="sxs-lookup"><span data-stu-id="604f6-117">-  Success</span></span>  <br/><span data-ttu-id="604f6-118">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="604f6-118">-  Warning</span></span>  <br/><span data-ttu-id="604f6-119">-Error</span><span class="sxs-lookup"><span data-stu-id="604f6-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="604f6-120">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="604f6-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="604f6-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="604f6-121">**Value**</span></span>|<span data-ttu-id="604f6-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="604f6-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="604f6-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="604f6-123">**Success**</span></span> <br/> |<span data-ttu-id="604f6-124">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="604f6-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="604f6-125">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="604f6-125">**Warning**</span></span> <br/> | <span data-ttu-id="604f6-126">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="604f6-126">Describes a request that was not processed.</span></span> <span data-ttu-id="604f6-127">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="604f6-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="604f6-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="604f6-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="604f6-129">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="604f6-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="604f6-130">-Los servicios de dominio de Active Directory (AD DS) están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="604f6-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="604f6-131">-Se mueven los buzones.</span><span class="sxs-lookup"><span data-stu-id="604f6-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="604f6-132">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="604f6-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="604f6-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="604f6-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="604f6-134">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="604f6-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="604f6-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="604f6-135">**Error**</span></span> <br/> | <span data-ttu-id="604f6-136">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="604f6-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="604f6-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="604f6-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="604f6-138">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="604f6-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="604f6-139">-Atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="604f6-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="604f6-140">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="604f6-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="604f6-141">-Atributo o elemento no válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="604f6-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="604f6-142">-Intento de acceso no autorizado por parte de un cliente</span><span class="sxs-lookup"><span data-stu-id="604f6-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="604f6-143">-Error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="604f6-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="604f6-144">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="604f6-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="604f6-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="604f6-145">Child elements</span></span>

|<span data-ttu-id="604f6-146">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="604f6-146">**Element**</span></span>|<span data-ttu-id="604f6-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="604f6-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="604f6-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="604f6-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="604f6-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="604f6-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="604f6-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="604f6-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="604f6-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="604f6-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="604f6-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="604f6-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="604f6-153">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="604f6-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="604f6-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="604f6-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="604f6-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="604f6-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="604f6-156">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="604f6-156">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="604f6-157">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="604f6-157">Parent elements</span></span>

|<span data-ttu-id="604f6-158">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="604f6-158">**Element**</span></span>|<span data-ttu-id="604f6-159">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="604f6-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="604f6-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="604f6-160">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="604f6-161">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="604f6-161">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="604f6-162">Comentarios</span><span class="sxs-lookup"><span data-stu-id="604f6-162">Remarks</span></span>

<span data-ttu-id="604f6-163">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="604f6-163">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="604f6-164">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="604f6-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="604f6-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="604f6-165">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="604f6-166">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="604f6-166">Schema Name</span></span>  <br/> |<span data-ttu-id="604f6-167">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="604f6-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="604f6-168">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="604f6-168">Validation File</span></span>  <br/> |<span data-ttu-id="604f6-169">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="604f6-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="604f6-170">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="604f6-170">Can be Empty</span></span>  <br/> |<span data-ttu-id="604f6-171">Falso</span><span class="sxs-lookup"><span data-stu-id="604f6-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="604f6-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="604f6-172">See also</span></span>

- [<span data-ttu-id="604f6-173">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="604f6-173">Unsubscribe operation</span></span>](unsubscribe-operation.md)
- [<span data-ttu-id="604f6-174">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="604f6-174">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

