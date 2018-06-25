---
title: RefreshSharingFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RefreshSharingFolderResponseMessage
api_type:
- schema
ms.assetid: 53ee65bd-cf75-4e04-9b27-eff1b040ae82
description: El elemento RefreshSharingFolderResponseMessage contiene el estado y el resultado de una única solicitud de operación RefreshSharingFolder.
ms.openlocfilehash: 9dbb66c294439f33a9307d51c03dd1cd127e95e2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837052"
---
# <a name="refreshsharingfolderresponsemessage"></a><span data-ttu-id="591d8-103">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="591d8-103">RefreshSharingFolderResponseMessage</span></span>

<span data-ttu-id="591d8-104">El elemento **RefreshSharingFolderResponseMessage** contiene el estado y el resultado de una única solicitud de [operación RefreshSharingFolder](refreshsharingfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="591d8-104">The **RefreshSharingFolderResponseMessage** element contains the status and result of a single [RefreshSharingFolder operation](refreshsharingfolder-operation.md) request.</span></span> 
  
```xml
<RefreshSharingFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</RefreshSharingFolderResponseMessage>
```

 <span data-ttu-id="591d8-105">**RefreshSharingFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="591d8-105">**RefreshSharingFolderResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="591d8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="591d8-106">Attributes and elements</span></span>

<span data-ttu-id="591d8-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="591d8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="591d8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="591d8-108">Attributes</span></span>

|<span data-ttu-id="591d8-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="591d8-109">**Attribute**</span></span>|<span data-ttu-id="591d8-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="591d8-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="591d8-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="591d8-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="591d8-112">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="591d8-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="591d8-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="591d8-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="591d8-114">-Éxito</span><span class="sxs-lookup"><span data-stu-id="591d8-114">-  Success</span></span>  <br/><span data-ttu-id="591d8-115">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="591d8-115">-  Warning</span></span>  <br/><span data-ttu-id="591d8-116">-Error</span><span class="sxs-lookup"><span data-stu-id="591d8-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="591d8-117">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="591d8-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="591d8-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="591d8-118">**Value**</span></span>|<span data-ttu-id="591d8-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="591d8-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="591d8-120">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="591d8-120">**Success**</span></span> <br/> |<span data-ttu-id="591d8-121">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="591d8-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="591d8-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="591d8-122">**Warning**</span></span> <br/> | <span data-ttu-id="591d8-123">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="591d8-123">Describes a request that was not processed.</span></span> <span data-ttu-id="591d8-124">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="591d8-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="591d8-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="591d8-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="591d8-126">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="591d8-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="591d8-127">-El servicio de directorio de Active Directory está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="591d8-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="591d8-128">-Buzones se han movido.</span><span class="sxs-lookup"><span data-stu-id="591d8-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="591d8-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="591d8-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="591d8-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="591d8-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="591d8-131">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="591d8-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="591d8-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="591d8-132">**Error**</span></span> <br/> | <span data-ttu-id="591d8-133">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="591d8-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="591d8-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="591d8-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="591d8-135">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="591d8-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="591d8-136">-Los atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="591d8-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="591d8-137">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="591d8-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="591d8-138">-De atributo o elemento no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="591d8-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="591d8-139">-Intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="591d8-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="591d8-140">-Error server-side en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="591d8-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="591d8-141">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="591d8-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="591d8-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="591d8-142">Child elements</span></span>

|<span data-ttu-id="591d8-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="591d8-143">**Element**</span></span>|<span data-ttu-id="591d8-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="591d8-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="591d8-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="591d8-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="591d8-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="591d8-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="591d8-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="591d8-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="591d8-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="591d8-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="591d8-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="591d8-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="591d8-150">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="591d8-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="591d8-151">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="591d8-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="591d8-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="591d8-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="591d8-153">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="591d8-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="591d8-154">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="591d8-154">Parent elements</span></span>

|<span data-ttu-id="591d8-155">**Element**</span><span class="sxs-lookup"><span data-stu-id="591d8-155">**Element**</span></span>|<span data-ttu-id="591d8-156">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="591d8-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="591d8-157">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="591d8-157">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="591d8-158">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="591d8-158">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="591d8-159">Comentarios</span><span class="sxs-lookup"><span data-stu-id="591d8-159">Remarks</span></span>

<span data-ttu-id="591d8-160">El esquema que describe este elemento se encuentra en el directorio Virtual de IIS que hospeda los servicios Web Exchange del equipo que ejecuta a Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="591d8-160">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="591d8-161">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="591d8-161">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="591d8-162">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="591d8-162">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="591d8-163">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="591d8-163">Schema Name</span></span>  <br/> |<span data-ttu-id="591d8-164">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="591d8-164">Messages schema</span></span>  <br/> |
|<span data-ttu-id="591d8-165">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="591d8-165">Validation File</span></span>  <br/> |<span data-ttu-id="591d8-166">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="591d8-166">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="591d8-167">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="591d8-167">Can be Empty</span></span>  <br/> |<span data-ttu-id="591d8-168">False</span><span class="sxs-lookup"><span data-stu-id="591d8-168">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="591d8-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="591d8-169">See also</span></span>

- [<span data-ttu-id="591d8-170">Operación RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="591d8-170">RefreshSharingFolder operation</span></span>](refreshsharingfolder-operation.md)
- [<span data-ttu-id="591d8-171">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="591d8-171">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

