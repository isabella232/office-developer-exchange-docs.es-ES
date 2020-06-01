---
title: ResolveNamesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResolveNamesResponseMessage
api_type:
- schema
ms.assetid: edcdaf58-ef63-412e-8c58-409213e6ab0d
description: El elemento ResolveNamesResponseMessage contiene el estado y el resultado de una solicitud de operación ResolveNames.
ms.openlocfilehash: 12f32008dbbc603fca7adf26057f1f1904d3cfb2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455600"
---
# <a name="resolvenamesresponsemessage"></a><span data-ttu-id="65736-103">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="65736-103">ResolveNamesResponseMessage</span></span>

<span data-ttu-id="65736-104">El elemento **ResolveNamesResponseMessage** contiene el estado y el resultado de una solicitud de [operación ResolveNames](resolvenames-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="65736-104">The **ResolveNamesResponseMessage** element contains the status and result of a [ResolveNames operation](resolvenames-operation.md) request.</span></span> 
  
- [<span data-ttu-id="65736-105">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="65736-105">ResolveNamesResponse</span></span>](resolvenamesresponse.md) 
- [<span data-ttu-id="65736-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="65736-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="65736-107">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="65736-107">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
  
```xml
<ResolveNamesResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ResolutionSet/>
</ResolveNamesResponseMessage>
```

 <span data-ttu-id="65736-108">**ResolveNamesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="65736-108">**ResolveNamesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="65736-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="65736-109">Attributes and elements</span></span>

<span data-ttu-id="65736-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="65736-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="65736-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="65736-111">Attributes</span></span>

|<span data-ttu-id="65736-112">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="65736-112">**Attribute**</span></span>|<span data-ttu-id="65736-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65736-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="65736-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="65736-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="65736-115">Describe el estado de una respuesta de [operación de ResolveNames](resolvenames-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="65736-115">Describes the status of a [ResolveNames operation](resolvenames-operation.md) response.</span></span> <br/><br/><span data-ttu-id="65736-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="65736-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="65736-117">-Correcto</span><span class="sxs-lookup"><span data-stu-id="65736-117">-  Success</span></span>  <br/><span data-ttu-id="65736-118">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="65736-118">-  Warning</span></span>  <br/><span data-ttu-id="65736-119">-Error</span><span class="sxs-lookup"><span data-stu-id="65736-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="65736-120">Atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="65736-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="65736-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="65736-121">**Value**</span></span>|<span data-ttu-id="65736-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65736-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="65736-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="65736-123">**Success**</span></span> <br/> |<span data-ttu-id="65736-124">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="65736-124">Describes a request that is fulfilled.</span></span> <span data-ttu-id="65736-125">Esto ocurre cuando el nombre solicitado es inequívoco y la respuesta contiene un único destinatario.</span><span class="sxs-lookup"><span data-stu-id="65736-125">This occurs when the requested name is unambiguous and the response contains a single recipient.</span></span>  <br/> |
|<span data-ttu-id="65736-126">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="65736-126">**Warning**</span></span> <br/> | <span data-ttu-id="65736-127">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="65736-127">Describes a request that was not processed.</span></span> <span data-ttu-id="65736-128">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="65736-128">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="65736-129">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="65736-129">The following are example of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="65736-130">-El almacén de Exchange se desconecta durante el lote.</span><span class="sxs-lookup"><span data-stu-id="65736-130">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="65736-131">-Servicios de dominio de Active Directory (AD DS) se desconecta.</span><span class="sxs-lookup"><span data-stu-id="65736-131">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="65736-132">-Se mueven los buzones.</span><span class="sxs-lookup"><span data-stu-id="65736-132">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="65736-133">-La base de datos de buzones (MDB) se desconecta.</span><span class="sxs-lookup"><span data-stu-id="65736-133">-  The mailbox database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="65736-134">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="65736-134">-  A password is expired.</span></span>  <br/><span data-ttu-id="65736-135">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="65736-135">-  A quota is exceeded.</span></span>  <br/><span data-ttu-id="65736-136">-El nombre solicitado es ambiguo y la respuesta contiene varios destinatarios.</span><span class="sxs-lookup"><span data-stu-id="65736-136">-  The requested name is ambiguous and the response contains multiple recipients.</span></span>  <br/> |
|<span data-ttu-id="65736-137">**Error**</span><span class="sxs-lookup"><span data-stu-id="65736-137">**Error**</span></span> <br/> | <span data-ttu-id="65736-138">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="65736-138">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="65736-139">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="65736-139">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="65736-140">-No se pudo resolver el nombre solicitado.</span><span class="sxs-lookup"><span data-stu-id="65736-140">-  The requested name could not be resolved.</span></span>  <br/><span data-ttu-id="65736-141">-Los atributos o elementos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="65736-141">-  Attributes or elements are invalid.</span></span>  <br/><span data-ttu-id="65736-142">-Los atributos o elementos están fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="65736-142">-  Attributes or elements are out of range.</span></span>  <br/><span data-ttu-id="65736-143">-Se desconoce la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="65736-143">-  A tag is unknown.</span></span>  <br/><span data-ttu-id="65736-144">-Un atributo o elemento no es válido en el contexto.</span><span class="sxs-lookup"><span data-stu-id="65736-144">-  An attribute or element is not valid in the context.</span></span>  <br/><span data-ttu-id="65736-145">-Se produjo un intento de acceso no autorizado por parte de cualquier cliente.</span><span class="sxs-lookup"><span data-stu-id="65736-145">-  An unauthorized access attempt by any client occurred.</span></span>  <br/><span data-ttu-id="65736-146">-Se produjo un error del servidor en respuesta a una llamada válida del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="65736-146">-  A server-side failure occurred in response to a valid client-side call.</span></span>  <br/>  <br/><span data-ttu-id="65736-147">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="65736-147">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="65736-148">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="65736-148">Child elements</span></span>

|<span data-ttu-id="65736-149">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="65736-149">**Element**</span></span>|<span data-ttu-id="65736-150">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65736-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65736-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="65736-151">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="65736-152">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="65736-152">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="65736-153">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="65736-153">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="65736-154">Proporciona información de error sobre la solicitud.</span><span class="sxs-lookup"><span data-stu-id="65736-154">Provides error information about the request.</span></span>  <br/> |
|[<span data-ttu-id="65736-155">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="65736-155">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="65736-156">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="65736-156">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="65736-157">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="65736-157">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="65736-158">MessageXml</span><span class="sxs-lookup"><span data-stu-id="65736-158">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="65736-159">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="65736-159">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="65736-160">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="65736-160">ResolutionSet</span></span>](resolutionset.md) <br/> |<span data-ttu-id="65736-161">Contiene una matriz de resoluciones para un nombre ambiguo.</span><span class="sxs-lookup"><span data-stu-id="65736-161">Contains an array of resolutions for an ambiguous name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="65736-162">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="65736-162">Parent elements</span></span>

|<span data-ttu-id="65736-163">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="65736-163">**Element**</span></span>|<span data-ttu-id="65736-164">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65736-164">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65736-165">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="65736-165">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="65736-166">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="65736-166">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65736-167">Comentarios</span><span class="sxs-lookup"><span data-stu-id="65736-167">Remarks</span></span>

<span data-ttu-id="65736-168">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="65736-168">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="65736-169">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="65736-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65736-170">Namespace</span><span class="sxs-lookup"><span data-stu-id="65736-170">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="65736-171">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="65736-171">Schema name</span></span>  <br/> |<span data-ttu-id="65736-172">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="65736-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="65736-173">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="65736-173">Validation file</span></span>  <br/> |<span data-ttu-id="65736-174">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="65736-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="65736-175">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="65736-175">Can be empty</span></span>  <br/> |<span data-ttu-id="65736-176">Falso</span><span class="sxs-lookup"><span data-stu-id="65736-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="65736-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="65736-177">See also</span></span>

- [<span data-ttu-id="65736-178">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="65736-178">ResolveNames</span></span>](resolvenames.md)
- [<span data-ttu-id="65736-179">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="65736-179">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
- [<span data-ttu-id="65736-180">Operación ResolveNames</span><span class="sxs-lookup"><span data-stu-id="65736-180">ResolveNames operation</span></span>](resolvenames-operation.md)

