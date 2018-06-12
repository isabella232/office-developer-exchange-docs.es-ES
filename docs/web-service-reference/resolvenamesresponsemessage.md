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
ms.openlocfilehash: 953a1f0b19c078d969ffe175c22df02b58c5e939
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837170"
---
# <a name="resolvenamesresponsemessage"></a><span data-ttu-id="3ac35-103">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3ac35-103">ResolveNamesResponseMessage</span></span>

<span data-ttu-id="3ac35-104">El elemento **ResolveNamesResponseMessage** contiene el estado y el resultado de una solicitud de [operación ResolveNames](resolvenames-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="3ac35-104">The **ResolveNamesResponseMessage** element contains the status and result of a [ResolveNames operation](resolvenames-operation.md) request.</span></span> 
  
- [<span data-ttu-id="3ac35-105">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="3ac35-105">ResolveNamesResponse</span></span>](resolvenamesresponse.md) 
- [<span data-ttu-id="3ac35-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3ac35-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="3ac35-107">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3ac35-107">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
  
```xml
<ResolveNamesResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ResolutionSet/>
</ResolveNamesResponseMessage>
```

 <span data-ttu-id="3ac35-108">**ResolveNamesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="3ac35-108">**ResolveNamesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3ac35-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3ac35-109">Attributes and elements</span></span>

<span data-ttu-id="3ac35-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3ac35-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3ac35-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="3ac35-111">Attributes</span></span>

|<span data-ttu-id="3ac35-112">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="3ac35-112">**Attribute**</span></span>|<span data-ttu-id="3ac35-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3ac35-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3ac35-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="3ac35-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="3ac35-115">Describe el estado de una respuesta de [la operación ResolveNames](resolvenames-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="3ac35-115">Describes the status of a [ResolveNames operation](resolvenames-operation.md) response.</span></span> <br/><br/><span data-ttu-id="3ac35-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="3ac35-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="3ac35-117">-Éxito</span><span class="sxs-lookup"><span data-stu-id="3ac35-117">-  Success</span></span>  <br/><span data-ttu-id="3ac35-118">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="3ac35-118">-  Warning</span></span>  <br/><span data-ttu-id="3ac35-119">-Error</span><span class="sxs-lookup"><span data-stu-id="3ac35-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="3ac35-120">Atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="3ac35-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="3ac35-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3ac35-121">**Value**</span></span>|<span data-ttu-id="3ac35-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3ac35-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3ac35-123">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="3ac35-123">**Success**</span></span> <br/> |<span data-ttu-id="3ac35-124">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="3ac35-124">Describes a request that is fulfilled.</span></span> <span data-ttu-id="3ac35-125">Esto se produce cuando el nombre solicitado es inequívoco y la respuesta contiene a un solo destinatario.</span><span class="sxs-lookup"><span data-stu-id="3ac35-125">This occurs when the requested name is unambiguous and the response contains a single recipient.</span></span>  <br/> |
|<span data-ttu-id="3ac35-126">**Warning**</span><span class="sxs-lookup"><span data-stu-id="3ac35-126">**Warning**</span></span> <br/> | <span data-ttu-id="3ac35-127">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="3ac35-127">Describes a request that was not processed.</span></span> <span data-ttu-id="3ac35-128">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="3ac35-128">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="3ac35-129">Ejemplo de los orígenes de las advertencias de es lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3ac35-129">The following are example of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="3ac35-130">-El almacén de Exchange se desconecta durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="3ac35-130">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="3ac35-131">-Los servicios de dominio de Active Directory (AD DS) se queda sin conexión.</span><span class="sxs-lookup"><span data-stu-id="3ac35-131">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="3ac35-132">-Se mueven los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="3ac35-132">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="3ac35-133">-La base de datos de buzón (MDB) se queda sin conexión.</span><span class="sxs-lookup"><span data-stu-id="3ac35-133">-  The mailbox database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="3ac35-134">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="3ac35-134">-  A password is expired.</span></span>  <br/><span data-ttu-id="3ac35-135">-Se ha excedido una cuota.</span><span class="sxs-lookup"><span data-stu-id="3ac35-135">-  A quota is exceeded.</span></span>  <br/><span data-ttu-id="3ac35-136">-El nombre solicitado es ambiguo y la respuesta contiene a varios destinatarios.</span><span class="sxs-lookup"><span data-stu-id="3ac35-136">-  The requested name is ambiguous and the response contains multiple recipients.</span></span>  <br/> |
|<span data-ttu-id="3ac35-137">**Error**</span><span class="sxs-lookup"><span data-stu-id="3ac35-137">**Error**</span></span> <br/> | <span data-ttu-id="3ac35-138">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="3ac35-138">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="3ac35-139">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="3ac35-139">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="3ac35-140">-No se pudo resolver el nombre solicitado.</span><span class="sxs-lookup"><span data-stu-id="3ac35-140">-  The requested name could not be resolved.</span></span>  <br/><span data-ttu-id="3ac35-141">-Los atributos o elementos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="3ac35-141">-  Attributes or elements are invalid.</span></span>  <br/><span data-ttu-id="3ac35-142">-Los atributos o elementos que están fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="3ac35-142">-  Attributes or elements are out of range.</span></span>  <br/><span data-ttu-id="3ac35-143">-Una etiqueta es desconocida.</span><span class="sxs-lookup"><span data-stu-id="3ac35-143">-  A tag is unknown.</span></span>  <br/><span data-ttu-id="3ac35-144">-Un atributo o elemento no es válido en el contexto.</span><span class="sxs-lookup"><span data-stu-id="3ac35-144">-  An attribute or element is not valid in the context.</span></span>  <br/><span data-ttu-id="3ac35-145">-Se ha producido un intento de acceso no autorizado por cualquier cliente.</span><span class="sxs-lookup"><span data-stu-id="3ac35-145">-  An unauthorized access attempt by any client occurred.</span></span>  <br/><span data-ttu-id="3ac35-146">-Un error del lado del servidor se produjo en respuesta a una llamada de cliente válida.</span><span class="sxs-lookup"><span data-stu-id="3ac35-146">-  A server-side failure occurred in response to a valid client-side call.</span></span>  <br/>  <br/><span data-ttu-id="3ac35-147">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="3ac35-147">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3ac35-148">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3ac35-148">Child elements</span></span>

|<span data-ttu-id="3ac35-149">**Element**</span><span class="sxs-lookup"><span data-stu-id="3ac35-149">**Element**</span></span>|<span data-ttu-id="3ac35-150">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3ac35-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3ac35-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="3ac35-151">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="3ac35-152">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3ac35-152">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="3ac35-153">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="3ac35-153">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="3ac35-154">Proporciona información de error sobre la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3ac35-154">Provides error information about the request.</span></span>  <br/> |
|[<span data-ttu-id="3ac35-155">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="3ac35-155">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="3ac35-156">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="3ac35-156">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="3ac35-157">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="3ac35-157">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="3ac35-158">MessageXml</span><span class="sxs-lookup"><span data-stu-id="3ac35-158">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="3ac35-159">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="3ac35-159">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="3ac35-160">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="3ac35-160">ResolutionSet</span></span>](resolutionset.md) <br/> |<span data-ttu-id="3ac35-161">Contiene una matriz de soluciones para un nombre ambiguo.</span><span class="sxs-lookup"><span data-stu-id="3ac35-161">Contains an array of resolutions for an ambiguous name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3ac35-162">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3ac35-162">Parent elements</span></span>

|<span data-ttu-id="3ac35-163">**Element**</span><span class="sxs-lookup"><span data-stu-id="3ac35-163">**Element**</span></span>|<span data-ttu-id="3ac35-164">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3ac35-164">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3ac35-165">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3ac35-165">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="3ac35-166">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3ac35-166">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3ac35-167">Notas</span><span class="sxs-lookup"><span data-stu-id="3ac35-167">Remarks</span></span>

<span data-ttu-id="3ac35-168">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="3ac35-168">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3ac35-169">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3ac35-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ac35-170">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3ac35-170">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3ac35-171">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3ac35-171">Schema name</span></span>  <br/> |<span data-ttu-id="3ac35-172">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3ac35-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3ac35-173">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3ac35-173">Validation file</span></span>  <br/> |<span data-ttu-id="3ac35-174">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3ac35-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3ac35-175">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3ac35-175">Can be empty</span></span>  <br/> |<span data-ttu-id="3ac35-176">False</span><span class="sxs-lookup"><span data-stu-id="3ac35-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3ac35-177">Ver también</span><span class="sxs-lookup"><span data-stu-id="3ac35-177">See also</span></span>

- [<span data-ttu-id="3ac35-178">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="3ac35-178">ResolveNames</span></span>](resolvenames.md)
- [<span data-ttu-id="3ac35-179">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="3ac35-179">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
- [<span data-ttu-id="3ac35-180">Operación ResolveNames</span><span class="sxs-lookup"><span data-stu-id="3ac35-180">ResolveNames operation</span></span>](resolvenames-operation.md)

