---
title: CopyFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyFolderResponseMessage
api_type:
- schema
ms.assetid: c82092a9-50ff-4ae1-b819-ebabbf89262b
description: El elemento CopyFolderResponseMessage contiene el estado y el resultado de una única solicitud de operación CopyFolder.
ms.openlocfilehash: 2bb2b407e0ae6b854d214c4b9d68ac8ed65b2c7b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763897"
---
# <a name="copyfolderresponsemessage"></a><span data-ttu-id="0ec6e-103">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0ec6e-103">CopyFolderResponseMessage</span></span>

<span data-ttu-id="0ec6e-104">El elemento **CopyFolderResponseMessage** contiene el estado y el resultado de una única solicitud de [operación CopyFolder](copyfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="0ec6e-104">The **CopyFolderResponseMessage** element contains the status and result of a single [CopyFolder operation](copyfolder-operation.md) request.</span></span> 
  
- [<span data-ttu-id="0ec6e-105">CopyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="0ec6e-105">CopyFolderResponse</span></span>](copyfolderresponse.md) 
- [<span data-ttu-id="0ec6e-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0ec6e-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="0ec6e-107">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0ec6e-107">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md)
  
```xml
<CopyFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</CopyFolderResponseMessage>
```

 <span data-ttu-id="0ec6e-108">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="0ec6e-108">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0ec6e-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0ec6e-109">Attributes and elements</span></span>

<span data-ttu-id="0ec6e-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0ec6e-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0ec6e-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="0ec6e-111">Attributes</span></span>

|<span data-ttu-id="0ec6e-112">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="0ec6e-112">**Attribute**</span></span>|<span data-ttu-id="0ec6e-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0ec6e-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0ec6e-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="0ec6e-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="0ec6e-115">Describe el estado de una respuesta de [la operación CopyFolder](copyfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="0ec6e-115">Describes the status of a [CopyFolder operation](copyfolder-operation.md) response.</span></span><br/><br/><span data-ttu-id="0ec6e-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="0ec6e-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="0ec6e-117">-Éxito</span><span class="sxs-lookup"><span data-stu-id="0ec6e-117">- Success</span></span>  <br/><span data-ttu-id="0ec6e-118">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="0ec6e-118">-  Warning</span></span>  <br/><span data-ttu-id="0ec6e-119">-Error</span><span class="sxs-lookup"><span data-stu-id="0ec6e-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="0ec6e-120">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="0ec6e-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="0ec6e-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0ec6e-121">**Value**</span></span>|<span data-ttu-id="0ec6e-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0ec6e-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0ec6e-123">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="0ec6e-123">**Success**</span></span> <br/> |<span data-ttu-id="0ec6e-124">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="0ec6e-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="0ec6e-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="0ec6e-125">**Warning**</span></span> <br/> | <span data-ttu-id="0ec6e-126">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="0ec6e-126">Describes a request that was not processed.</span></span> <span data-ttu-id="0ec6e-127">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="0ec6e-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="0ec6e-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="0ec6e-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="0ec6e-129">-El almacén de Exchange se desconecta durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="0ec6e-129">- The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="0ec6e-130">-Los servicios de dominio de Active Directory (AD DS) se queda sin conexión.</span><span class="sxs-lookup"><span data-stu-id="0ec6e-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="0ec6e-131">-Se mueven los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="0ec6e-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="0ec6e-132">-La base de datos de mensajes (MDB) se queda sin conexión.</span><span class="sxs-lookup"><span data-stu-id="0ec6e-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="0ec6e-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="0ec6e-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="0ec6e-134">-Se ha excedido una cuota.</span><span class="sxs-lookup"><span data-stu-id="0ec6e-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="0ec6e-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="0ec6e-135">**Error**</span></span> <br/> | <span data-ttu-id="0ec6e-136">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="0ec6e-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="0ec6e-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="0ec6e-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="0ec6e-138">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="0ec6e-138">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="0ec6e-139">-Los atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="0ec6e-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="0ec6e-140">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="0ec6e-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="0ec6e-141">-De atributo o elemento no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="0ec6e-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="0ec6e-142">-Acceso no autorizado intenta establecer cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="0ec6e-142">-  Unauthorized access attempted by any client</span></span>  <br/><span data-ttu-id="0ec6e-143">-Error server-side en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="0ec6e-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="0ec6e-144">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="0ec6e-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0ec6e-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0ec6e-145">Child elements</span></span>

|<span data-ttu-id="0ec6e-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="0ec6e-146">**Element**</span></span>|<span data-ttu-id="0ec6e-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0ec6e-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ec6e-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="0ec6e-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="0ec6e-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0ec6e-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="0ec6e-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0ec6e-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="0ec6e-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0ec6e-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="0ec6e-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0ec6e-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="0ec6e-153">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="0ec6e-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="0ec6e-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="0ec6e-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="0ec6e-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="0ec6e-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="0ec6e-156">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="0ec6e-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="0ec6e-157">Carpetas</span><span class="sxs-lookup"><span data-stu-id="0ec6e-157">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="0ec6e-158">Contiene una matriz de carpetas copiadas.</span><span class="sxs-lookup"><span data-stu-id="0ec6e-158">Contains an array of copied folders.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0ec6e-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0ec6e-159">Parent elements</span></span>

|<span data-ttu-id="0ec6e-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="0ec6e-160">**Element**</span></span>|<span data-ttu-id="0ec6e-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0ec6e-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ec6e-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0ec6e-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="0ec6e-163">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0ec6e-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ec6e-164">Notas</span><span class="sxs-lookup"><span data-stu-id="0ec6e-164">Remarks</span></span>

<span data-ttu-id="0ec6e-165">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="0ec6e-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0ec6e-166">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0ec6e-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0ec6e-167">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0ec6e-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0ec6e-168">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0ec6e-168">Schema name</span></span>  <br/> |<span data-ttu-id="0ec6e-169">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="0ec6e-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0ec6e-170">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0ec6e-170">Validation file</span></span>  <br/> |<span data-ttu-id="0ec6e-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0ec6e-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0ec6e-172">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0ec6e-172">Can be empty</span></span>  <br/> |<span data-ttu-id="0ec6e-173">False</span><span class="sxs-lookup"><span data-stu-id="0ec6e-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0ec6e-174">Ver también</span><span class="sxs-lookup"><span data-stu-id="0ec6e-174">See also</span></span>

- [<span data-ttu-id="0ec6e-175">Operación CopyFolder</span><span class="sxs-lookup"><span data-stu-id="0ec6e-175">CopyFolder operation</span></span>](copyfolder-operation.md)
- [<span data-ttu-id="0ec6e-176">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="0ec6e-176">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="0ec6e-177">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0ec6e-177">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

