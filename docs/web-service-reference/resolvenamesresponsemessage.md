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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455600"
---
# <a name="resolvenamesresponsemessage"></a><span data-ttu-id="8dfc2-103">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8dfc2-103">ResolveNamesResponseMessage</span></span>

<span data-ttu-id="8dfc2-104">El elemento **ResolveNamesResponseMessage** contiene el estado y el resultado de una solicitud de [operación ResolveNames](resolvenames-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="8dfc2-104">The **ResolveNamesResponseMessage** element contains the status and result of a [ResolveNames operation](resolvenames-operation.md) request.</span></span> 
  
- [<span data-ttu-id="8dfc2-105">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="8dfc2-105">ResolveNamesResponse</span></span>](resolvenamesresponse.md) 
- [<span data-ttu-id="8dfc2-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8dfc2-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="8dfc2-107">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8dfc2-107">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
  
```xml
<ResolveNamesResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ResolutionSet/>
</ResolveNamesResponseMessage>
```

 <span data-ttu-id="8dfc2-108">**ResolveNamesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="8dfc2-108">**ResolveNamesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8dfc2-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8dfc2-109">Attributes and elements</span></span>

<span data-ttu-id="8dfc2-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8dfc2-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="8dfc2-111">Attributes</span></span>

|<span data-ttu-id="8dfc2-112">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="8dfc2-112">**Attribute**</span></span>|<span data-ttu-id="8dfc2-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8dfc2-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8dfc2-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="8dfc2-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="8dfc2-115">Describe el estado de una respuesta de [operación de ResolveNames](resolvenames-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="8dfc2-115">Describes the status of a [ResolveNames operation](resolvenames-operation.md) response.</span></span> <br/><br/><span data-ttu-id="8dfc2-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="8dfc2-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="8dfc2-117">-Correcto</span><span class="sxs-lookup"><span data-stu-id="8dfc2-117">-  Success</span></span>  <br/><span data-ttu-id="8dfc2-118">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="8dfc2-118">-  Warning</span></span>  <br/><span data-ttu-id="8dfc2-119">-Error</span><span class="sxs-lookup"><span data-stu-id="8dfc2-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="8dfc2-120">Atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="8dfc2-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="8dfc2-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8dfc2-121">**Value**</span></span>|<span data-ttu-id="8dfc2-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8dfc2-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8dfc2-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="8dfc2-123">**Success**</span></span> <br/> |<span data-ttu-id="8dfc2-124">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-124">Describes a request that is fulfilled.</span></span> <span data-ttu-id="8dfc2-125">Esto ocurre cuando el nombre solicitado es inequívoco y la respuesta contiene un único destinatario.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-125">This occurs when the requested name is unambiguous and the response contains a single recipient.</span></span>  <br/> |
|<span data-ttu-id="8dfc2-126">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="8dfc2-126">**Warning**</span></span> <br/> | <span data-ttu-id="8dfc2-127">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-127">Describes a request that was not processed.</span></span> <span data-ttu-id="8dfc2-128">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-128">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="8dfc2-129">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="8dfc2-129">The following are example of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="8dfc2-130">-El almacén de Exchange se desconecta durante el lote.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-130">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="8dfc2-131">-Servicios de dominio de Active Directory (AD DS) se desconecta.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-131">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="8dfc2-132">-Se mueven los buzones.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-132">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="8dfc2-133">-La base de datos de buzones (MDB) se desconecta.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-133">-  The mailbox database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="8dfc2-134">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-134">-  A password is expired.</span></span>  <br/><span data-ttu-id="8dfc2-135">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-135">-  A quota is exceeded.</span></span>  <br/><span data-ttu-id="8dfc2-136">-El nombre solicitado es ambiguo y la respuesta contiene varios destinatarios.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-136">-  The requested name is ambiguous and the response contains multiple recipients.</span></span>  <br/> |
|<span data-ttu-id="8dfc2-137">**Error**</span><span class="sxs-lookup"><span data-stu-id="8dfc2-137">**Error**</span></span> <br/> | <span data-ttu-id="8dfc2-138">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-138">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="8dfc2-139">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="8dfc2-139">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="8dfc2-140">-No se pudo resolver el nombre solicitado.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-140">-  The requested name could not be resolved.</span></span>  <br/><span data-ttu-id="8dfc2-141">-Los atributos o elementos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-141">-  Attributes or elements are invalid.</span></span>  <br/><span data-ttu-id="8dfc2-142">-Los atributos o elementos están fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-142">-  Attributes or elements are out of range.</span></span>  <br/><span data-ttu-id="8dfc2-143">-Se desconoce la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-143">-  A tag is unknown.</span></span>  <br/><span data-ttu-id="8dfc2-144">-Un atributo o elemento no es válido en el contexto.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-144">-  An attribute or element is not valid in the context.</span></span>  <br/><span data-ttu-id="8dfc2-145">-Se produjo un intento de acceso no autorizado por parte de cualquier cliente.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-145">-  An unauthorized access attempt by any client occurred.</span></span>  <br/><span data-ttu-id="8dfc2-146">-Se produjo un error del servidor en respuesta a una llamada válida del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-146">-  A server-side failure occurred in response to a valid client-side call.</span></span>  <br/>  <br/><span data-ttu-id="8dfc2-147">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="8dfc2-147">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8dfc2-148">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8dfc2-148">Child elements</span></span>

|<span data-ttu-id="8dfc2-149">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8dfc2-149">**Element**</span></span>|<span data-ttu-id="8dfc2-150">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8dfc2-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8dfc2-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="8dfc2-151">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="8dfc2-152">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-152">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="8dfc2-153">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8dfc2-153">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="8dfc2-154">Proporciona información de error sobre la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-154">Provides error information about the request.</span></span>  <br/> |
|[<span data-ttu-id="8dfc2-155">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="8dfc2-155">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="8dfc2-156">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-156">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="8dfc2-157">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-157">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="8dfc2-158">MessageXml</span><span class="sxs-lookup"><span data-stu-id="8dfc2-158">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="8dfc2-159">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-159">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="8dfc2-160">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="8dfc2-160">ResolutionSet</span></span>](resolutionset.md) <br/> |<span data-ttu-id="8dfc2-161">Contiene una matriz de resoluciones para un nombre ambiguo.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-161">Contains an array of resolutions for an ambiguous name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8dfc2-162">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8dfc2-162">Parent elements</span></span>

|<span data-ttu-id="8dfc2-163">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8dfc2-163">**Element**</span></span>|<span data-ttu-id="8dfc2-164">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8dfc2-164">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8dfc2-165">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8dfc2-165">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="8dfc2-166">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-166">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8dfc2-167">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8dfc2-167">Remarks</span></span>

<span data-ttu-id="8dfc2-168">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="8dfc2-168">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8dfc2-169">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8dfc2-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8dfc2-170">Namespace</span><span class="sxs-lookup"><span data-stu-id="8dfc2-170">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8dfc2-171">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8dfc2-171">Schema name</span></span>  <br/> |<span data-ttu-id="8dfc2-172">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="8dfc2-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8dfc2-173">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8dfc2-173">Validation file</span></span>  <br/> |<span data-ttu-id="8dfc2-174">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="8dfc2-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8dfc2-175">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8dfc2-175">Can be empty</span></span>  <br/> |<span data-ttu-id="8dfc2-176">Falso</span><span class="sxs-lookup"><span data-stu-id="8dfc2-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8dfc2-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="8dfc2-177">See also</span></span>

- [<span data-ttu-id="8dfc2-178">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="8dfc2-178">ResolveNames</span></span>](resolvenames.md)
- [<span data-ttu-id="8dfc2-179">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="8dfc2-179">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
- [<span data-ttu-id="8dfc2-180">Operación ResolveNames</span><span class="sxs-lookup"><span data-stu-id="8dfc2-180">ResolveNames operation</span></span>](resolvenames-operation.md)

