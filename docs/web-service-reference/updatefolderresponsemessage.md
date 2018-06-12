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
description: El elemento UpdateFolderResponseMessage contiene el estado y el resultado de actualizaciones definido por el elemento FolderChange de una solicitud de operación UpdateFolder.
ms.openlocfilehash: 4cd00232bcc233f6534d844418f523c248ce54bf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840828"
---
# <a name="updatefolderresponsemessage"></a><span data-ttu-id="fae2c-103">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="fae2c-103">UpdateFolderResponseMessage</span></span>

<span data-ttu-id="fae2c-104">El elemento **UpdateFolderResponseMessage** contiene el estado y el resultado de actualizaciones definido por el elemento [FolderChange](folderchange.md) de una solicitud de [operación UpdateFolder](updatefolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="fae2c-104">The **UpdateFolderResponseMessage** element contains the status and result of updates defined by the [FolderChange](folderchange.md) element of an [UpdateFolder operation](updatefolder-operation.md) request.</span></span> 
  
- [<span data-ttu-id="fae2c-105">UpdateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="fae2c-105">UpdateFolderResponse</span></span>](updatefolderresponse.md) 
- [<span data-ttu-id="fae2c-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="fae2c-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="fae2c-107">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="fae2c-107">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md)
  
```xml
<UpdateFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</UpdateFolderResponseMessage>
```

 <span data-ttu-id="fae2c-108">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="fae2c-108">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fae2c-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fae2c-109">Attributes and elements</span></span>

<span data-ttu-id="fae2c-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fae2c-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fae2c-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="fae2c-111">Attributes</span></span>

|<span data-ttu-id="fae2c-112">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="fae2c-112">**Attribute**</span></span>|<span data-ttu-id="fae2c-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fae2c-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fae2c-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="fae2c-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="fae2c-115">Describe el estado de una respuesta de [la operación UpdateFolder](updatefolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="fae2c-115">Describes the status of an [UpdateFolder operation](updatefolder-operation.md) response.</span></span> <br/><br/><span data-ttu-id="fae2c-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="fae2c-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="fae2c-117">-Éxito</span><span class="sxs-lookup"><span data-stu-id="fae2c-117">-  Success</span></span>  <br/><span data-ttu-id="fae2c-118">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="fae2c-118">-  Warning</span></span>  <br/><span data-ttu-id="fae2c-119">-Error</span><span class="sxs-lookup"><span data-stu-id="fae2c-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="fae2c-120">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="fae2c-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="fae2c-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fae2c-121">**Value**</span></span>|<span data-ttu-id="fae2c-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fae2c-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fae2c-123">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="fae2c-123">**Success**</span></span> <br/> |<span data-ttu-id="fae2c-124">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="fae2c-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="fae2c-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="fae2c-125">**Warning**</span></span> <br/> | <span data-ttu-id="fae2c-126">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="fae2c-126">Describes a request that was not processed.</span></span> <span data-ttu-id="fae2c-127">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="fae2c-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="fae2c-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="fae2c-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="fae2c-129">-El almacén de Exchange está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="fae2c-129">-  The Exchange store is offline.</span></span>  <br/><span data-ttu-id="fae2c-130">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="fae2c-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="fae2c-131">-Un buzón se mueve.</span><span class="sxs-lookup"><span data-stu-id="fae2c-131">-  A mailbox is moved.</span></span>  <br/><span data-ttu-id="fae2c-132">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="fae2c-132">-  A password is expired.</span></span>  <br/><span data-ttu-id="fae2c-133">-Se ha excedido una cuota.</span><span class="sxs-lookup"><span data-stu-id="fae2c-133">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="fae2c-134">**Error**</span><span class="sxs-lookup"><span data-stu-id="fae2c-134">**Error**</span></span> <br/> | <span data-ttu-id="fae2c-135">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="fae2c-135">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="fae2c-136">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="fae2c-136">The following are examples of sources for errors:</span></span>  <br/><br/><span data-ttu-id="fae2c-137">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="fae2c-137">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="fae2c-138">-Los atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="fae2c-138">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="fae2c-139">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="fae2c-139">-  Unknown tag</span></span>  <br/><span data-ttu-id="fae2c-140">-De atributo o elemento no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="fae2c-140">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="fae2c-141">-Intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="fae2c-141">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="fae2c-142">-Error server-side en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="fae2c-142">-  Server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="fae2c-143">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="fae2c-143">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fae2c-144">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fae2c-144">Child elements</span></span>

|<span data-ttu-id="fae2c-145">**Element**</span><span class="sxs-lookup"><span data-stu-id="fae2c-145">**Element**</span></span>|<span data-ttu-id="fae2c-146">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fae2c-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fae2c-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="fae2c-147">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="fae2c-148">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fae2c-148">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="fae2c-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="fae2c-149">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="fae2c-150">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fae2c-150">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="fae2c-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="fae2c-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="fae2c-152">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="fae2c-152">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="fae2c-153">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="fae2c-153">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="fae2c-154">MessageXml</span><span class="sxs-lookup"><span data-stu-id="fae2c-154">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="fae2c-155">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="fae2c-155">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="fae2c-156">Carpetas</span><span class="sxs-lookup"><span data-stu-id="fae2c-156">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="fae2c-157">Contiene una matriz de carpetas que se utilizan en las operaciones de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="fae2c-157">Contains an array of folders used in folder operations.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fae2c-158">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fae2c-158">Parent elements</span></span>

|<span data-ttu-id="fae2c-159">**Element**</span><span class="sxs-lookup"><span data-stu-id="fae2c-159">**Element**</span></span>|<span data-ttu-id="fae2c-160">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fae2c-160">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fae2c-161">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="fae2c-161">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="fae2c-162">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fae2c-162">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fae2c-163">Notas</span><span class="sxs-lookup"><span data-stu-id="fae2c-163">Remarks</span></span>

<span data-ttu-id="fae2c-164">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="fae2c-164">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fae2c-165">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fae2c-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fae2c-166">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fae2c-166">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fae2c-167">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fae2c-167">Schema Name</span></span>  <br/> |<span data-ttu-id="fae2c-168">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="fae2c-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fae2c-169">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fae2c-169">Validation File</span></span>  <br/> |<span data-ttu-id="fae2c-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fae2c-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fae2c-171">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fae2c-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="fae2c-172">False</span><span class="sxs-lookup"><span data-stu-id="fae2c-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fae2c-173">Ver también</span><span class="sxs-lookup"><span data-stu-id="fae2c-173">See also</span></span>

- [<span data-ttu-id="fae2c-174">Operación UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="fae2c-174">UpdateFolder operation</span></span>](updatefolder-operation.md)

