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
ms.openlocfilehash: 318a09e371043252d43a5197211e9623f34229fd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462566"
---
# <a name="findfolderresponsemessage"></a><span data-ttu-id="9d189-103">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9d189-103">FindFolderResponseMessage</span></span>

<span data-ttu-id="9d189-104">El elemento **FindFolderResponseMessage** contiene el estado y el resultado de una única solicitud de [operación FindFolder](findfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="9d189-104">The **FindFolderResponseMessage** element contains the status and result of a single [FindFolder operation](findfolder-operation.md) request.</span></span> 
  
[<span data-ttu-id="9d189-105">FindFolderResponse</span><span class="sxs-lookup"><span data-stu-id="9d189-105">FindFolderResponse</span></span>](findfolderresponse.md)
  
[<span data-ttu-id="9d189-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9d189-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="9d189-107">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9d189-107">FindFolderResponseMessage</span></span>](findfolderresponsemessage.md)
  
```xml
<FindFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RootFolder/>
</FindFolderResponseMessage>
```

 <span data-ttu-id="9d189-108">**FindFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="9d189-108">**FindFolderResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9d189-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9d189-109">Attributes and elements</span></span>

<span data-ttu-id="9d189-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9d189-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9d189-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d189-111">Attributes</span></span>

|<span data-ttu-id="9d189-112">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="9d189-112">**Attribute**</span></span>|<span data-ttu-id="9d189-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9d189-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9d189-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="9d189-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="9d189-115">Describe el estado de una respuesta de [operación de FindFolder](findfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="9d189-115">Describes the status of a [FindFolder operation](findfolder-operation.md) response.</span></span><br/><br/> <span data-ttu-id="9d189-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="9d189-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="9d189-117">-Correcto</span><span class="sxs-lookup"><span data-stu-id="9d189-117">-  Success</span></span>  <br/><span data-ttu-id="9d189-118">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="9d189-118">-  Warning</span></span>  <br/><span data-ttu-id="9d189-119">-Error</span><span class="sxs-lookup"><span data-stu-id="9d189-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="9d189-120">Atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="9d189-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="9d189-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9d189-121">**Value**</span></span>|<span data-ttu-id="9d189-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9d189-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9d189-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="9d189-123">**Success**</span></span> <br/> |<span data-ttu-id="9d189-124">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="9d189-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="9d189-125">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="9d189-125">**Warning**</span></span> <br/> | <span data-ttu-id="9d189-126">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="9d189-126">Describes a request that was not processed.</span></span> <span data-ttu-id="9d189-127">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="9d189-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="9d189-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="9d189-128">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="9d189-129">-El almacén de Exchange se desconecta durante el lote.</span><span class="sxs-lookup"><span data-stu-id="9d189-129">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="9d189-130">-Servicios de dominio de Active Directory (AD DS) se desconecta.</span><span class="sxs-lookup"><span data-stu-id="9d189-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="9d189-131">-Se mueven los buzones.</span><span class="sxs-lookup"><span data-stu-id="9d189-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="9d189-132">-La base de datos de mensajes (MDB) se desconecta.</span><span class="sxs-lookup"><span data-stu-id="9d189-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="9d189-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="9d189-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="9d189-134">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="9d189-134">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="9d189-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="9d189-135">**Error**</span></span> <br/> | <span data-ttu-id="9d189-136">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="9d189-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="9d189-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="9d189-137">The following are examples of sources of errors:</span></span>  <br/><span data-ttu-id="9d189-138">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="9d189-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="9d189-139">-Atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="9d189-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="9d189-140">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="9d189-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="9d189-141">-Atributo o elemento no válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="9d189-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="9d189-142">-Intento de acceso no autorizado por parte de un cliente</span><span class="sxs-lookup"><span data-stu-id="9d189-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="9d189-143">-Error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="9d189-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="9d189-144">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="9d189-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9d189-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9d189-145">Child elements</span></span>

|<span data-ttu-id="9d189-146">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9d189-146">**Element**</span></span>|<span data-ttu-id="9d189-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9d189-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d189-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="9d189-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="9d189-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9d189-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="9d189-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9d189-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="9d189-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9d189-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="9d189-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="9d189-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="9d189-153">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="9d189-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="9d189-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="9d189-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="9d189-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="9d189-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="9d189-156">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="9d189-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="9d189-157">RootFolder (FindFolderResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="9d189-157">RootFolder (FindFolderResponseMessage)</span></span>](rootfolder-findfolderresponsemessage.md) <br/> |<span data-ttu-id="9d189-158">Contiene los resultados de una búsqueda de una sola carpeta raíz durante una [operación FindFolder](findfolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="9d189-158">Contains the results from a search of a single root folder during a [FindFolder operation](findfolder-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9d189-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9d189-159">Parent elements</span></span>

|<span data-ttu-id="9d189-160">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9d189-160">**Element**</span></span>|<span data-ttu-id="9d189-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9d189-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d189-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9d189-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="9d189-163">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="9d189-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d189-164">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9d189-164">Remarks</span></span>

<span data-ttu-id="9d189-165">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="9d189-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9d189-166">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9d189-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d189-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d189-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9d189-168">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9d189-168">Schema name</span></span>  <br/> |<span data-ttu-id="9d189-169">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="9d189-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9d189-170">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9d189-170">Validation file</span></span>  <br/> |<span data-ttu-id="9d189-171">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="9d189-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9d189-172">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9d189-172">Can be empty</span></span>  <br/> |<span data-ttu-id="9d189-173">Falso</span><span class="sxs-lookup"><span data-stu-id="9d189-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9d189-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d189-174">See also</span></span>

- [<span data-ttu-id="9d189-175">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="9d189-175">FindFolder operation</span></span>](findfolder-operation.md)
- [<span data-ttu-id="9d189-176">Buscar carpetas</span><span class="sxs-lookup"><span data-stu-id="9d189-176">Finding Folders</span></span>](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

