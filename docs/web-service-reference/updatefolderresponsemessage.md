---
title: UpdateFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateFolderResponseMessage
api_type:
- schema
ms.assetid: 914bb683-49ee-44a2-b59d-ef560244dfb8
description: El elemento UpdateFolderResponseMessage contiene el estado y el resultado de las actualizaciones definidas por el elemento FolderChange de una solicitud de operación UpdateFolder.
ms.openlocfilehash: bbe01583072e6203e099d440f2a171012f51e7df
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466587"
---
# <a name="updatefolderresponsemessage"></a><span data-ttu-id="55fb3-103">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="55fb3-103">UpdateFolderResponseMessage</span></span>

<span data-ttu-id="55fb3-104">El elemento **UpdateFolderResponseMessage** contiene el estado y el resultado de las actualizaciones definidas por el elemento [FolderChange](folderchange.md) de una solicitud de [operación UpdateFolder](updatefolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="55fb3-104">The **UpdateFolderResponseMessage** element contains the status and result of updates defined by the [FolderChange](folderchange.md) element of an [UpdateFolder operation](updatefolder-operation.md) request.</span></span> 
  
- [<span data-ttu-id="55fb3-105">UpdateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="55fb3-105">UpdateFolderResponse</span></span>](updatefolderresponse.md) 
- [<span data-ttu-id="55fb3-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="55fb3-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="55fb3-107">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="55fb3-107">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md)
  
```xml
<UpdateFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</UpdateFolderResponseMessage>
```

 <span data-ttu-id="55fb3-108">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="55fb3-108">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="55fb3-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="55fb3-109">Attributes and elements</span></span>

<span data-ttu-id="55fb3-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="55fb3-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="55fb3-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="55fb3-111">Attributes</span></span>

|<span data-ttu-id="55fb3-112">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="55fb3-112">**Attribute**</span></span>|<span data-ttu-id="55fb3-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="55fb3-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="55fb3-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="55fb3-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="55fb3-115">Describe el estado de una respuesta de [operación de UpdateFolder](updatefolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="55fb3-115">Describes the status of an [UpdateFolder operation](updatefolder-operation.md) response.</span></span> <br/><br/><span data-ttu-id="55fb3-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="55fb3-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="55fb3-117">-Correcto</span><span class="sxs-lookup"><span data-stu-id="55fb3-117">-  Success</span></span>  <br/><span data-ttu-id="55fb3-118">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="55fb3-118">-  Warning</span></span>  <br/><span data-ttu-id="55fb3-119">-Error</span><span class="sxs-lookup"><span data-stu-id="55fb3-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="55fb3-120">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="55fb3-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="55fb3-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="55fb3-121">**Value**</span></span>|<span data-ttu-id="55fb3-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="55fb3-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="55fb3-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="55fb3-123">**Success**</span></span> <br/> |<span data-ttu-id="55fb3-124">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="55fb3-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="55fb3-125">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="55fb3-125">**Warning**</span></span> <br/> | <span data-ttu-id="55fb3-126">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="55fb3-126">Describes a request that was not processed.</span></span> <span data-ttu-id="55fb3-127">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="55fb3-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="55fb3-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="55fb3-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="55fb3-129">-El almacén de Exchange está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="55fb3-129">-  The Exchange store is offline.</span></span>  <br/><span data-ttu-id="55fb3-130">-Los servicios de dominio de Active Directory (AD DS) están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="55fb3-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="55fb3-131">-Se mueve un buzón.</span><span class="sxs-lookup"><span data-stu-id="55fb3-131">-  A mailbox is moved.</span></span>  <br/><span data-ttu-id="55fb3-132">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="55fb3-132">-  A password is expired.</span></span>  <br/><span data-ttu-id="55fb3-133">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="55fb3-133">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="55fb3-134">**Error**</span><span class="sxs-lookup"><span data-stu-id="55fb3-134">**Error**</span></span> <br/> | <span data-ttu-id="55fb3-135">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="55fb3-135">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="55fb3-136">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="55fb3-136">The following are examples of sources for errors:</span></span>  <br/><br/><span data-ttu-id="55fb3-137">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="55fb3-137">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="55fb3-138">-Atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="55fb3-138">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="55fb3-139">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="55fb3-139">-  Unknown tag</span></span>  <br/><span data-ttu-id="55fb3-140">-Atributo o elemento no válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="55fb3-140">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="55fb3-141">-Intento de acceso no autorizado por parte de un cliente</span><span class="sxs-lookup"><span data-stu-id="55fb3-141">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="55fb3-142">-Error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="55fb3-142">-  Server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="55fb3-143">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="55fb3-143">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="55fb3-144">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="55fb3-144">Child elements</span></span>

|<span data-ttu-id="55fb3-145">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="55fb3-145">**Element**</span></span>|<span data-ttu-id="55fb3-146">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="55fb3-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="55fb3-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="55fb3-147">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="55fb3-148">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="55fb3-148">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="55fb3-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="55fb3-149">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="55fb3-150">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="55fb3-150">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="55fb3-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="55fb3-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="55fb3-152">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="55fb3-152">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="55fb3-153">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="55fb3-153">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="55fb3-154">MessageXml</span><span class="sxs-lookup"><span data-stu-id="55fb3-154">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="55fb3-155">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="55fb3-155">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="55fb3-156">Folders</span><span class="sxs-lookup"><span data-stu-id="55fb3-156">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="55fb3-157">Contiene una matriz de carpetas que se usan en las operaciones de carpeta.</span><span class="sxs-lookup"><span data-stu-id="55fb3-157">Contains an array of folders used in folder operations.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="55fb3-158">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="55fb3-158">Parent elements</span></span>

|<span data-ttu-id="55fb3-159">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="55fb3-159">**Element**</span></span>|<span data-ttu-id="55fb3-160">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="55fb3-160">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="55fb3-161">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="55fb3-161">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="55fb3-162">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="55fb3-162">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55fb3-163">Comentarios</span><span class="sxs-lookup"><span data-stu-id="55fb3-163">Remarks</span></span>

<span data-ttu-id="55fb3-164">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="55fb3-164">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="55fb3-165">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="55fb3-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="55fb3-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="55fb3-166">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="55fb3-167">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="55fb3-167">Schema Name</span></span>  <br/> |<span data-ttu-id="55fb3-168">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="55fb3-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="55fb3-169">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="55fb3-169">Validation File</span></span>  <br/> |<span data-ttu-id="55fb3-170">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="55fb3-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="55fb3-171">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="55fb3-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="55fb3-172">Falso</span><span class="sxs-lookup"><span data-stu-id="55fb3-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="55fb3-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="55fb3-173">See also</span></span>

- [<span data-ttu-id="55fb3-174">Operación UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="55fb3-174">UpdateFolder operation</span></span>](updatefolder-operation.md)

