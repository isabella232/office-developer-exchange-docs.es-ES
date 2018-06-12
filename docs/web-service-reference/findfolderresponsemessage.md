---
title: FindFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindFolderResponseMessage
api_type:
- schema
ms.assetid: 538d64fe-51ae-41d2-bfab-91698678aa1b
description: El elemento FindFolderResponseMessage contiene el estado y el resultado de una única solicitud de operación FindFolder.
ms.openlocfilehash: 5623e5e538e617e5bd4bbc4444328ac83d7b8065
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764625"
---
# <a name="findfolderresponsemessage"></a><span data-ttu-id="d0f00-103">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d0f00-103">FindFolderResponseMessage</span></span>

<span data-ttu-id="d0f00-104">El elemento **FindFolderResponseMessage** contiene el estado y el resultado de una única solicitud de [operación FindFolder](findfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="d0f00-104">The **FindFolderResponseMessage** element contains the status and result of a single [FindFolder operation](findfolder-operation.md) request.</span></span> 
  
[<span data-ttu-id="d0f00-105">FindFolderResponse</span><span class="sxs-lookup"><span data-stu-id="d0f00-105">FindFolderResponse</span></span>](findfolderresponse.md)
  
[<span data-ttu-id="d0f00-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d0f00-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="d0f00-107">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d0f00-107">FindFolderResponseMessage</span></span>](findfolderresponsemessage.md)
  
```xml
<FindFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RootFolder/>
</FindFolderResponseMessage>
```

 <span data-ttu-id="d0f00-108">**FindFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="d0f00-108">**FindFolderResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d0f00-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d0f00-109">Attributes and elements</span></span>

<span data-ttu-id="d0f00-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d0f00-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0f00-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="d0f00-111">Attributes</span></span>

|<span data-ttu-id="d0f00-112">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="d0f00-112">**Attribute**</span></span>|<span data-ttu-id="d0f00-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d0f00-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d0f00-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="d0f00-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="d0f00-115">Describe el estado de una respuesta de [la operación FindFolder](findfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="d0f00-115">Describes the status of a [FindFolder operation](findfolder-operation.md) response.</span></span><br/><br/> <span data-ttu-id="d0f00-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="d0f00-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="d0f00-117">-Éxito</span><span class="sxs-lookup"><span data-stu-id="d0f00-117">-  Success</span></span>  <br/><span data-ttu-id="d0f00-118">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="d0f00-118">-  Warning</span></span>  <br/><span data-ttu-id="d0f00-119">-Error</span><span class="sxs-lookup"><span data-stu-id="d0f00-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="d0f00-120">Atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="d0f00-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="d0f00-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d0f00-121">**Value**</span></span>|<span data-ttu-id="d0f00-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d0f00-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d0f00-123">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="d0f00-123">**Success**</span></span> <br/> |<span data-ttu-id="d0f00-124">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="d0f00-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="d0f00-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="d0f00-125">**Warning**</span></span> <br/> | <span data-ttu-id="d0f00-126">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="d0f00-126">Describes a request that was not processed.</span></span> <span data-ttu-id="d0f00-127">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="d0f00-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="d0f00-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="d0f00-128">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="d0f00-129">-El almacén de Exchange se desconecta durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="d0f00-129">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="d0f00-130">-Los servicios de dominio de Active Directory (AD DS) se queda sin conexión.</span><span class="sxs-lookup"><span data-stu-id="d0f00-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="d0f00-131">-Se mueven los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="d0f00-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="d0f00-132">-La base de datos de mensajes (MDB) se queda sin conexión.</span><span class="sxs-lookup"><span data-stu-id="d0f00-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="d0f00-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="d0f00-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="d0f00-134">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="d0f00-134">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="d0f00-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="d0f00-135">**Error**</span></span> <br/> | <span data-ttu-id="d0f00-136">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="d0f00-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="d0f00-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="d0f00-137">The following are examples of sources of errors:</span></span>  <br/><span data-ttu-id="d0f00-138">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="d0f00-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="d0f00-139">-Los atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="d0f00-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="d0f00-140">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="d0f00-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="d0f00-141">-De atributo o elemento no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="d0f00-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="d0f00-142">-Intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="d0f00-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="d0f00-143">-Error server-side en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="d0f00-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="d0f00-144">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="d0f00-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d0f00-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d0f00-145">Child elements</span></span>

|<span data-ttu-id="d0f00-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="d0f00-146">**Element**</span></span>|<span data-ttu-id="d0f00-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d0f00-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0f00-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="d0f00-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="d0f00-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0f00-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="d0f00-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d0f00-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="d0f00-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d0f00-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="d0f00-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d0f00-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="d0f00-153">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d0f00-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="d0f00-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="d0f00-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="d0f00-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="d0f00-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="d0f00-156">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="d0f00-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="d0f00-157">RootFolder (FindFolderResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="d0f00-157">RootFolder (FindFolderResponseMessage)</span></span>](rootfolder-findfolderresponsemessage.md) <br/> |<span data-ttu-id="d0f00-158">Contiene los resultados de una búsqueda de una sola carpeta raíz durante una [operación de FindFolder](findfolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="d0f00-158">Contains the results from a search of a single root folder during a [FindFolder operation](findfolder-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d0f00-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d0f00-159">Parent elements</span></span>

|<span data-ttu-id="d0f00-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="d0f00-160">**Element**</span></span>|<span data-ttu-id="d0f00-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d0f00-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0f00-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d0f00-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="d0f00-163">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d0f00-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0f00-164">Notas</span><span class="sxs-lookup"><span data-stu-id="d0f00-164">Remarks</span></span>

<span data-ttu-id="d0f00-165">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="d0f00-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d0f00-166">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d0f00-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0f00-167">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d0f00-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d0f00-168">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d0f00-168">Schema name</span></span>  <br/> |<span data-ttu-id="d0f00-169">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="d0f00-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d0f00-170">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d0f00-170">Validation file</span></span>  <br/> |<span data-ttu-id="d0f00-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d0f00-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d0f00-172">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d0f00-172">Can be empty</span></span>  <br/> |<span data-ttu-id="d0f00-173">False</span><span class="sxs-lookup"><span data-stu-id="d0f00-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0f00-174">Ver también</span><span class="sxs-lookup"><span data-stu-id="d0f00-174">See also</span></span>

- [<span data-ttu-id="d0f00-175">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="d0f00-175">FindFolder operation</span></span>](findfolder-operation.md)
- [<span data-ttu-id="d0f00-176">Buscar carpetas</span><span class="sxs-lookup"><span data-stu-id="d0f00-176">Finding Folders</span></span>](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

