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
ms.openlocfilehash: f2cc357298d523b418d2c45598639627c5a63252
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468673"
---
# <a name="refreshsharingfolderresponsemessage"></a><span data-ttu-id="9fabc-103">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9fabc-103">RefreshSharingFolderResponseMessage</span></span>

<span data-ttu-id="9fabc-104">El elemento **RefreshSharingFolderResponseMessage** contiene el estado y el resultado de una única solicitud de [operación RefreshSharingFolder](refreshsharingfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="9fabc-104">The **RefreshSharingFolderResponseMessage** element contains the status and result of a single [RefreshSharingFolder operation](refreshsharingfolder-operation.md) request.</span></span> 
  
```xml
<RefreshSharingFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</RefreshSharingFolderResponseMessage>
```

 <span data-ttu-id="9fabc-105">**RefreshSharingFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="9fabc-105">**RefreshSharingFolderResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9fabc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9fabc-106">Attributes and elements</span></span>

<span data-ttu-id="9fabc-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9fabc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9fabc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9fabc-108">Attributes</span></span>

|<span data-ttu-id="9fabc-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="9fabc-109">**Attribute**</span></span>|<span data-ttu-id="9fabc-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9fabc-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9fabc-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="9fabc-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="9fabc-112">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9fabc-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="9fabc-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="9fabc-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="9fabc-114">-Correcto</span><span class="sxs-lookup"><span data-stu-id="9fabc-114">-  Success</span></span>  <br/><span data-ttu-id="9fabc-115">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="9fabc-115">-  Warning</span></span>  <br/><span data-ttu-id="9fabc-116">-Error</span><span class="sxs-lookup"><span data-stu-id="9fabc-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="9fabc-117">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="9fabc-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="9fabc-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9fabc-118">**Value**</span></span>|<span data-ttu-id="9fabc-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9fabc-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9fabc-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="9fabc-120">**Success**</span></span> <br/> |<span data-ttu-id="9fabc-121">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="9fabc-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="9fabc-122">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="9fabc-122">**Warning**</span></span> <br/> | <span data-ttu-id="9fabc-123">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="9fabc-123">Describes a request that was not processed.</span></span> <span data-ttu-id="9fabc-124">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="9fabc-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="9fabc-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="9fabc-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="9fabc-126">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="9fabc-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="9fabc-127">-El servicio de directorio de Active Directory está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="9fabc-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="9fabc-128">-Se movieron los buzones.</span><span class="sxs-lookup"><span data-stu-id="9fabc-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="9fabc-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="9fabc-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="9fabc-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="9fabc-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="9fabc-131">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="9fabc-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="9fabc-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="9fabc-132">**Error**</span></span> <br/> | <span data-ttu-id="9fabc-133">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="9fabc-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="9fabc-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="9fabc-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="9fabc-135">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="9fabc-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="9fabc-136">-Atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="9fabc-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="9fabc-137">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="9fabc-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="9fabc-138">-Atributo o elemento no válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="9fabc-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="9fabc-139">-Intento de acceso no autorizado por parte de un cliente</span><span class="sxs-lookup"><span data-stu-id="9fabc-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="9fabc-140">-Error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="9fabc-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="9fabc-141">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="9fabc-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9fabc-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9fabc-142">Child elements</span></span>

|<span data-ttu-id="9fabc-143">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9fabc-143">**Element**</span></span>|<span data-ttu-id="9fabc-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9fabc-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9fabc-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="9fabc-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="9fabc-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9fabc-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="9fabc-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9fabc-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="9fabc-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9fabc-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="9fabc-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="9fabc-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="9fabc-150">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="9fabc-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="9fabc-151">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="9fabc-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="9fabc-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="9fabc-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="9fabc-153">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="9fabc-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9fabc-154">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9fabc-154">Parent elements</span></span>

|<span data-ttu-id="9fabc-155">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9fabc-155">**Element**</span></span>|<span data-ttu-id="9fabc-156">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9fabc-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9fabc-157">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9fabc-157">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="9fabc-158">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="9fabc-158">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9fabc-159">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9fabc-159">Remarks</span></span>

<span data-ttu-id="9fabc-160">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="9fabc-160">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9fabc-161">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9fabc-161">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fabc-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="9fabc-162">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9fabc-163">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9fabc-163">Schema Name</span></span>  <br/> |<span data-ttu-id="9fabc-164">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="9fabc-164">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9fabc-165">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9fabc-165">Validation File</span></span>  <br/> |<span data-ttu-id="9fabc-166">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="9fabc-166">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9fabc-167">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9fabc-167">Can be Empty</span></span>  <br/> |<span data-ttu-id="9fabc-168">Falso</span><span class="sxs-lookup"><span data-stu-id="9fabc-168">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9fabc-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fabc-169">See also</span></span>

- [<span data-ttu-id="9fabc-170">Operación RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="9fabc-170">RefreshSharingFolder operation</span></span>](refreshsharingfolder-operation.md)
- [<span data-ttu-id="9fabc-171">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="9fabc-171">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

