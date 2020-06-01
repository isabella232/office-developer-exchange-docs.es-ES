---
title: GetSharingFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingFolderResponseMessage
api_type:
- schema
ms.assetid: b6f5fd09-09f3-4e34-84b4-2f6c1f10f28f
description: El elemento GetSharingFolderResponseMessage contiene el estado y el resultado de una única solicitud de operación GetSharingFolder.
ms.openlocfilehash: 85a78a23bac72942c6278b5d97e2bb4c2992ab46
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463961"
---
# <a name="getsharingfolderresponsemessage"></a><span data-ttu-id="645cc-103">GetSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="645cc-103">GetSharingFolderResponseMessage</span></span>

<span data-ttu-id="645cc-104">El elemento **GetSharingFolderResponseMessage** contiene el estado y el resultado de una única solicitud de [operación GetSharingFolder](getsharingfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="645cc-104">The **GetSharingFolderResponseMessage** element contains the status and result of a single [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span> 
  
```xml
<GetSharingFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>   <SharingFolderId/>
</GetSharingFolderResponseMessage>
```

 <span data-ttu-id="645cc-105">**GetSharingFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="645cc-105">**GetSharingFolderResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="645cc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="645cc-106">Attributes and elements</span></span>

<span data-ttu-id="645cc-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="645cc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="645cc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="645cc-108">Attributes</span></span>

|<span data-ttu-id="645cc-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="645cc-109">**Attribute**</span></span>|<span data-ttu-id="645cc-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="645cc-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="645cc-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="645cc-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="645cc-112">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="645cc-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="645cc-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="645cc-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="645cc-114">-Correcto</span><span class="sxs-lookup"><span data-stu-id="645cc-114">-  Success</span></span>  <br/><span data-ttu-id="645cc-115">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="645cc-115">-  Warning</span></span>  <br/><span data-ttu-id="645cc-116">-Error</span><span class="sxs-lookup"><span data-stu-id="645cc-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="645cc-117">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="645cc-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="645cc-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="645cc-118">**Value**</span></span>|<span data-ttu-id="645cc-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="645cc-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="645cc-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="645cc-120">**Success**</span></span> <br/> |<span data-ttu-id="645cc-121">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="645cc-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="645cc-122">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="645cc-122">**Warning**</span></span> <br/> | <span data-ttu-id="645cc-123">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="645cc-123">Describes a request that was not processed.</span></span> <span data-ttu-id="645cc-124">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="645cc-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="645cc-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="645cc-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="645cc-126">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="645cc-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="645cc-127">-El servicio de directorio de Active Directory está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="645cc-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="645cc-128">-Se movieron los buzones.</span><span class="sxs-lookup"><span data-stu-id="645cc-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="645cc-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="645cc-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="645cc-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="645cc-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="645cc-131">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="645cc-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="645cc-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="645cc-132">**Error**</span></span> <br/> | <span data-ttu-id="645cc-133">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="645cc-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="645cc-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="645cc-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="645cc-135">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="645cc-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="645cc-136">-Atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="645cc-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="645cc-137">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="645cc-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="645cc-138">-Atributo o elemento no válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="645cc-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="645cc-139">-Intento de acceso no autorizado por parte de un cliente</span><span class="sxs-lookup"><span data-stu-id="645cc-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="645cc-140">-Error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="645cc-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="645cc-141">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="645cc-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="645cc-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="645cc-142">Child elements</span></span>

|<span data-ttu-id="645cc-143">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="645cc-143">**Element**</span></span>|<span data-ttu-id="645cc-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="645cc-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="645cc-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="645cc-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="645cc-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="645cc-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="645cc-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="645cc-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="645cc-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="645cc-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="645cc-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="645cc-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="645cc-150">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="645cc-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="645cc-151">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="645cc-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="645cc-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="645cc-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="645cc-153">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="645cc-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="645cc-154">SharingFolderId</span><span class="sxs-lookup"><span data-stu-id="645cc-154">SharingFolderId</span></span>](sharingfolderid.md) <br/> |<span data-ttu-id="645cc-155">Representa el identificador de la carpeta local en una relación de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="645cc-155">Represents the identifier of the local folder in a sharing relationship.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="645cc-156">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="645cc-156">Parent elements</span></span>

|<span data-ttu-id="645cc-157">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="645cc-157">**Element**</span></span>|<span data-ttu-id="645cc-158">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="645cc-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="645cc-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="645cc-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="645cc-160">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="645cc-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="645cc-161">Comentarios</span><span class="sxs-lookup"><span data-stu-id="645cc-161">Remarks</span></span>

<span data-ttu-id="645cc-162">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="645cc-162">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="645cc-163">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="645cc-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="645cc-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="645cc-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="645cc-165">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="645cc-165">Schema Name</span></span>  <br/> |<span data-ttu-id="645cc-166">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="645cc-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="645cc-167">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="645cc-167">Validation File</span></span>  <br/> |<span data-ttu-id="645cc-168">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="645cc-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="645cc-169">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="645cc-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="645cc-170">Falso</span><span class="sxs-lookup"><span data-stu-id="645cc-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="645cc-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="645cc-171">See also</span></span>

- [<span data-ttu-id="645cc-172">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="645cc-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

