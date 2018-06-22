---
title: CreateFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateFolderResponseMessage
api_type:
- schema
ms.assetid: 1301dd15-b008-4fd9-8c89-b15a20b186e2
description: El elemento CreateFolderResponseMessage contiene el estado y el resultado de una única solicitud de operación CreateFolder.
ms.openlocfilehash: c587cca1f935b295a0ed30ab2210de40af28d06d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763942"
---
# <a name="createfolderresponsemessage"></a><span data-ttu-id="46ba4-103">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="46ba4-103">CreateFolderResponseMessage</span></span>

<span data-ttu-id="46ba4-104">El elemento **CreateFolderResponseMessage** contiene el estado y el resultado de una única solicitud de [operación CreateFolder](createfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="46ba4-104">The **CreateFolderResponseMessage** element contains the status and result of a single [CreateFolder operation](createfolder-operation.md) request.</span></span> 
  
```xml
<CreateFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</CreateFolderResponseMessage>
```

<span data-ttu-id="46ba4-105">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="46ba4-105">**FolderInfoResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="46ba4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="46ba4-106">Attributes and elements</span></span>

<span data-ttu-id="46ba4-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="46ba4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="46ba4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="46ba4-108">Attributes</span></span>

|<span data-ttu-id="46ba4-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="46ba4-109">**Attribute**</span></span>|<span data-ttu-id="46ba4-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="46ba4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="46ba4-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="46ba4-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="46ba4-112">Describe el estado de una respuesta de [la operación CreateFolder](createfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="46ba4-112">Describes the status of a [CreateFolder operation](createfolder-operation.md) response.</span></span><br/><br/><span data-ttu-id="46ba4-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="46ba4-113">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="46ba4-114">-Éxito</span><span class="sxs-lookup"><span data-stu-id="46ba4-114">-  Success</span></span>  <br/><span data-ttu-id="46ba4-115">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="46ba4-115">-  Warning</span></span>  <br/><span data-ttu-id="46ba4-116">-Error</span><span class="sxs-lookup"><span data-stu-id="46ba4-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="46ba4-117">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="46ba4-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="46ba4-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="46ba4-118">**Value**</span></span>|<span data-ttu-id="46ba4-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="46ba4-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="46ba4-120">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="46ba4-120">**Success**</span></span> <br/> |<span data-ttu-id="46ba4-121">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="46ba4-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="46ba4-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="46ba4-122">**Warning**</span></span> <br/> | <span data-ttu-id="46ba4-123">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="46ba4-123">Describes a request that was not processed.</span></span> <span data-ttu-id="46ba4-124">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="46ba4-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="46ba4-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="46ba4-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="46ba4-126">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="46ba4-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="46ba4-127">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="46ba4-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="46ba4-128">-Se mueven los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="46ba4-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="46ba4-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="46ba4-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="46ba4-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="46ba4-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="46ba4-131">-Se ha excedido una cuota.</span><span class="sxs-lookup"><span data-stu-id="46ba4-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="46ba4-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="46ba4-132">**Error**</span></span> <br/> | <span data-ttu-id="46ba4-133">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="46ba4-133">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="46ba4-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="46ba4-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="46ba4-135">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="46ba4-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="46ba4-136">-Los atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="46ba4-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="46ba4-137">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="46ba4-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="46ba4-138">-De atributo o elemento no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="46ba4-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="46ba4-139">-Intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="46ba4-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="46ba4-140">-Error server-side en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="46ba4-140">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="46ba4-141">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="46ba4-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="46ba4-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="46ba4-142">Child elements</span></span>

|<span data-ttu-id="46ba4-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="46ba4-143">**Element**</span></span>|<span data-ttu-id="46ba4-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="46ba4-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46ba4-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="46ba4-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="46ba4-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="46ba4-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="46ba4-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="46ba4-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="46ba4-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="46ba4-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="46ba4-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="46ba4-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="46ba4-150">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="46ba4-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="46ba4-151">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="46ba4-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="46ba4-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="46ba4-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="46ba4-153">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="46ba4-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="46ba4-154">Carpetas</span><span class="sxs-lookup"><span data-stu-id="46ba4-154">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="46ba4-155">Contiene una matriz de carpetas creadas.</span><span class="sxs-lookup"><span data-stu-id="46ba4-155">Contains an array of created folders.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="46ba4-156">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="46ba4-156">Parent elements</span></span>

|<span data-ttu-id="46ba4-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="46ba4-157">**Element**</span></span>|<span data-ttu-id="46ba4-158">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="46ba4-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46ba4-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="46ba4-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="46ba4-160">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="46ba4-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46ba4-161">Notas</span><span class="sxs-lookup"><span data-stu-id="46ba4-161">Remarks</span></span>

<span data-ttu-id="46ba4-162">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con la función de servidor de acceso de cliente instalada.</span><span class="sxs-lookup"><span data-stu-id="46ba4-162">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="46ba4-163">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="46ba4-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46ba4-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="46ba4-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="46ba4-165">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="46ba4-165">Schema Name</span></span>  <br/> |<span data-ttu-id="46ba4-166">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="46ba4-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="46ba4-167">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="46ba4-167">Validation File</span></span>  <br/> |<span data-ttu-id="46ba4-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="46ba4-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="46ba4-169">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="46ba4-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="46ba4-170">False</span><span class="sxs-lookup"><span data-stu-id="46ba4-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="46ba4-171">Ver también</span><span class="sxs-lookup"><span data-stu-id="46ba4-171">See also</span></span>

- [<span data-ttu-id="46ba4-172">Operación CreateFolder</span><span class="sxs-lookup"><span data-stu-id="46ba4-172">CreateFolder operation</span></span>](createfolder-operation.md)
- [<span data-ttu-id="46ba4-173">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="46ba4-173">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="46ba4-174">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="46ba4-174">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

