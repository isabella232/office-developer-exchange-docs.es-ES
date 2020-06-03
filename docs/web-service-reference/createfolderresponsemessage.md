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
ms.openlocfilehash: 386dd2aa4e114d8382d5c83a3d6da70b1ccbbada
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457532"
---
# <a name="createfolderresponsemessage"></a><span data-ttu-id="c66ce-103">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c66ce-103">CreateFolderResponseMessage</span></span>

<span data-ttu-id="c66ce-104">El elemento **CreateFolderResponseMessage** contiene el estado y el resultado de una única solicitud de [operación CreateFolder](createfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="c66ce-104">The **CreateFolderResponseMessage** element contains the status and result of a single [CreateFolder operation](createfolder-operation.md) request.</span></span> 
  
```xml
<CreateFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</CreateFolderResponseMessage>
```

<span data-ttu-id="c66ce-105">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="c66ce-105">**FolderInfoResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c66ce-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c66ce-106">Attributes and elements</span></span>

<span data-ttu-id="c66ce-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c66ce-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c66ce-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c66ce-108">Attributes</span></span>

|<span data-ttu-id="c66ce-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c66ce-109">**Attribute**</span></span>|<span data-ttu-id="c66ce-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c66ce-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c66ce-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="c66ce-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="c66ce-112">Describe el estado de una respuesta de la [operación CreateFolder](createfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="c66ce-112">Describes the status of a [CreateFolder operation](createfolder-operation.md) response.</span></span><br/><br/><span data-ttu-id="c66ce-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="c66ce-113">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="c66ce-114">-Correcto</span><span class="sxs-lookup"><span data-stu-id="c66ce-114">-  Success</span></span>  <br/><span data-ttu-id="c66ce-115">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="c66ce-115">-  Warning</span></span>  <br/><span data-ttu-id="c66ce-116">-Error</span><span class="sxs-lookup"><span data-stu-id="c66ce-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="c66ce-117">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="c66ce-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="c66ce-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c66ce-118">**Value**</span></span>|<span data-ttu-id="c66ce-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c66ce-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c66ce-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="c66ce-120">**Success**</span></span> <br/> |<span data-ttu-id="c66ce-121">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="c66ce-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="c66ce-122">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="c66ce-122">**Warning**</span></span> <br/> | <span data-ttu-id="c66ce-123">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="c66ce-123">Describes a request that was not processed.</span></span> <span data-ttu-id="c66ce-124">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="c66ce-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="c66ce-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="c66ce-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="c66ce-126">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="c66ce-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="c66ce-127">-Los servicios de dominio de Active Directory (AD DS) están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="c66ce-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="c66ce-128">-Se mueven los buzones.</span><span class="sxs-lookup"><span data-stu-id="c66ce-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="c66ce-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="c66ce-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="c66ce-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="c66ce-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="c66ce-131">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="c66ce-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="c66ce-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="c66ce-132">**Error**</span></span> <br/> | <span data-ttu-id="c66ce-133">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="c66ce-133">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="c66ce-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="c66ce-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="c66ce-135">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="c66ce-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="c66ce-136">-Atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="c66ce-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="c66ce-137">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="c66ce-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="c66ce-138">-Atributo o elemento no válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="c66ce-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="c66ce-139">-Intento de acceso no autorizado por parte de un cliente</span><span class="sxs-lookup"><span data-stu-id="c66ce-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="c66ce-140">-Error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="c66ce-140">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="c66ce-141">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="c66ce-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c66ce-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c66ce-142">Child elements</span></span>

|<span data-ttu-id="c66ce-143">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c66ce-143">**Element**</span></span>|<span data-ttu-id="c66ce-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c66ce-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c66ce-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="c66ce-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="c66ce-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c66ce-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="c66ce-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c66ce-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="c66ce-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c66ce-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="c66ce-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c66ce-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="c66ce-150">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="c66ce-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="c66ce-151">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="c66ce-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="c66ce-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="c66ce-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="c66ce-153">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="c66ce-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="c66ce-154">Folders</span><span class="sxs-lookup"><span data-stu-id="c66ce-154">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="c66ce-155">Contiene una matriz de carpetas creadas.</span><span class="sxs-lookup"><span data-stu-id="c66ce-155">Contains an array of created folders.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c66ce-156">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c66ce-156">Parent elements</span></span>

|<span data-ttu-id="c66ce-157">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c66ce-157">**Element**</span></span>|<span data-ttu-id="c66ce-158">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c66ce-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c66ce-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c66ce-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="c66ce-160">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c66ce-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c66ce-161">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c66ce-161">Remarks</span></span>

<span data-ttu-id="c66ce-162">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con el rol de servidor acceso de clientes instalado.</span><span class="sxs-lookup"><span data-stu-id="c66ce-162">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c66ce-163">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c66ce-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c66ce-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="c66ce-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c66ce-165">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c66ce-165">Schema Name</span></span>  <br/> |<span data-ttu-id="c66ce-166">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c66ce-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c66ce-167">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c66ce-167">Validation File</span></span>  <br/> |<span data-ttu-id="c66ce-168">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c66ce-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c66ce-169">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c66ce-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="c66ce-170">Falso</span><span class="sxs-lookup"><span data-stu-id="c66ce-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c66ce-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="c66ce-171">See also</span></span>

- [<span data-ttu-id="c66ce-172">Operación CreateFolder</span><span class="sxs-lookup"><span data-stu-id="c66ce-172">CreateFolder operation</span></span>](createfolder-operation.md)
- [<span data-ttu-id="c66ce-173">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="c66ce-173">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="c66ce-174">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c66ce-174">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

