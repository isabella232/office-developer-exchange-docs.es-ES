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
ms.openlocfilehash: 796ec57116e4b4943ca370e45cf0abefe7782c08
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458512"
---
# <a name="copyfolderresponsemessage"></a><span data-ttu-id="9bae5-103">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9bae5-103">CopyFolderResponseMessage</span></span>

<span data-ttu-id="9bae5-104">El elemento **CopyFolderResponseMessage** contiene el estado y el resultado de una única solicitud de [operación CopyFolder](copyfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="9bae5-104">The **CopyFolderResponseMessage** element contains the status and result of a single [CopyFolder operation](copyfolder-operation.md) request.</span></span> 
  
- [<span data-ttu-id="9bae5-105">CopyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="9bae5-105">CopyFolderResponse</span></span>](copyfolderresponse.md) 
- [<span data-ttu-id="9bae5-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9bae5-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="9bae5-107">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9bae5-107">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md)
  
```xml
<CopyFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</CopyFolderResponseMessage>
```

 <span data-ttu-id="9bae5-108">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="9bae5-108">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9bae5-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9bae5-109">Attributes and elements</span></span>

<span data-ttu-id="9bae5-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9bae5-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9bae5-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="9bae5-111">Attributes</span></span>

|<span data-ttu-id="9bae5-112">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="9bae5-112">**Attribute**</span></span>|<span data-ttu-id="9bae5-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9bae5-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9bae5-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="9bae5-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="9bae5-115">Describe el estado de una respuesta de [operación de CopyFolder](copyfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="9bae5-115">Describes the status of a [CopyFolder operation](copyfolder-operation.md) response.</span></span><br/><br/><span data-ttu-id="9bae5-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="9bae5-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="9bae5-117">-Correcto</span><span class="sxs-lookup"><span data-stu-id="9bae5-117">- Success</span></span>  <br/><span data-ttu-id="9bae5-118">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="9bae5-118">-  Warning</span></span>  <br/><span data-ttu-id="9bae5-119">-Error</span><span class="sxs-lookup"><span data-stu-id="9bae5-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="9bae5-120">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="9bae5-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="9bae5-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9bae5-121">**Value**</span></span>|<span data-ttu-id="9bae5-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9bae5-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9bae5-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="9bae5-123">**Success**</span></span> <br/> |<span data-ttu-id="9bae5-124">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="9bae5-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="9bae5-125">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="9bae5-125">**Warning**</span></span> <br/> | <span data-ttu-id="9bae5-126">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="9bae5-126">Describes a request that was not processed.</span></span> <span data-ttu-id="9bae5-127">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="9bae5-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="9bae5-128">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="9bae5-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="9bae5-129">-El almacén de Exchange se desconecta durante el lote.</span><span class="sxs-lookup"><span data-stu-id="9bae5-129">- The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="9bae5-130">-Servicios de dominio de Active Directory (AD DS) se desconecta.</span><span class="sxs-lookup"><span data-stu-id="9bae5-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="9bae5-131">-Se mueven los buzones.</span><span class="sxs-lookup"><span data-stu-id="9bae5-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="9bae5-132">-La base de datos de mensajes (MDB) se desconecta.</span><span class="sxs-lookup"><span data-stu-id="9bae5-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="9bae5-133">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="9bae5-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="9bae5-134">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="9bae5-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="9bae5-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="9bae5-135">**Error**</span></span> <br/> | <span data-ttu-id="9bae5-136">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="9bae5-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="9bae5-137">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="9bae5-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="9bae5-138">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="9bae5-138">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="9bae5-139">-Atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="9bae5-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="9bae5-140">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="9bae5-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="9bae5-141">-Atributo o elemento no válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="9bae5-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="9bae5-142">-Acceso no autorizado intentado por cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="9bae5-142">-  Unauthorized access attempted by any client</span></span>  <br/><span data-ttu-id="9bae5-143">-Error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="9bae5-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="9bae5-144">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="9bae5-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9bae5-145">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9bae5-145">Child elements</span></span>

|<span data-ttu-id="9bae5-146">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9bae5-146">**Element**</span></span>|<span data-ttu-id="9bae5-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9bae5-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9bae5-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="9bae5-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="9bae5-149">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9bae5-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="9bae5-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9bae5-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="9bae5-151">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9bae5-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="9bae5-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="9bae5-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="9bae5-153">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="9bae5-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="9bae5-154">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="9bae5-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="9bae5-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="9bae5-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="9bae5-156">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="9bae5-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="9bae5-157">Folders</span><span class="sxs-lookup"><span data-stu-id="9bae5-157">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="9bae5-158">Contiene una matriz de carpetas copiadas.</span><span class="sxs-lookup"><span data-stu-id="9bae5-158">Contains an array of copied folders.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9bae5-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9bae5-159">Parent elements</span></span>

|<span data-ttu-id="9bae5-160">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9bae5-160">**Element**</span></span>|<span data-ttu-id="9bae5-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9bae5-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9bae5-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9bae5-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="9bae5-163">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="9bae5-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9bae5-164">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9bae5-164">Remarks</span></span>

<span data-ttu-id="9bae5-165">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="9bae5-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9bae5-166">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9bae5-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9bae5-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="9bae5-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9bae5-168">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9bae5-168">Schema name</span></span>  <br/> |<span data-ttu-id="9bae5-169">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="9bae5-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9bae5-170">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9bae5-170">Validation file</span></span>  <br/> |<span data-ttu-id="9bae5-171">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="9bae5-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9bae5-172">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9bae5-172">Can be empty</span></span>  <br/> |<span data-ttu-id="9bae5-173">Falso</span><span class="sxs-lookup"><span data-stu-id="9bae5-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9bae5-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="9bae5-174">See also</span></span>

- [<span data-ttu-id="9bae5-175">Operación CopyFolder</span><span class="sxs-lookup"><span data-stu-id="9bae5-175">CopyFolder operation</span></span>](copyfolder-operation.md)
- [<span data-ttu-id="9bae5-176">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="9bae5-176">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="9bae5-177">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="9bae5-177">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

