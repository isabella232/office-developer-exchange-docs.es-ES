---
title: GetSharingMetadataResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingMetadataResponseMessage
api_type:
- schema
ms.assetid: d81b8708-ebb2-45c2-861f-b9a814eee6ba
description: El elemento GetSharingMetadataResponseMessage contiene el estado y el resultado de una única solicitud de operación GetSharingMetadata.
ms.openlocfilehash: 24da0a78870b2c92e0751eba0631d58076b96eae
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835674"
---
# <a name="getsharingmetadataresponsemessage"></a><span data-ttu-id="8e879-103">GetSharingMetadataResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8e879-103">GetSharingMetadataResponseMessage</span></span>

<span data-ttu-id="8e879-104">El elemento **GetSharingMetadataResponseMessage** contiene el estado y el resultado de una única solicitud de [operación GetSharingMetadata](getsharingmetadata-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="8e879-104">The **GetSharingMetadataResponseMessage** element contains the status and result of a single [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span> 
  
```xml
<GetSharingMetadataResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>   <EncryptedSharedFolderDataCollection/>   <InvalidRecipients/>
</GetSharingMetadataResponseMessage>
```

 <span data-ttu-id="8e879-105">**GetSharingMetadataResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="8e879-105">**GetSharingMetadataResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8e879-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8e879-106">Attributes and elements</span></span>

<span data-ttu-id="8e879-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8e879-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8e879-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8e879-108">Attributes</span></span>

|<span data-ttu-id="8e879-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="8e879-109">**Attribute**</span></span>|<span data-ttu-id="8e879-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8e879-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8e879-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="8e879-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="8e879-112">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8e879-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="8e879-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="8e879-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="8e879-114">-Éxito</span><span class="sxs-lookup"><span data-stu-id="8e879-114">-  Success</span></span>  <br/><span data-ttu-id="8e879-115">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="8e879-115">-  Warning</span></span>  <br/><span data-ttu-id="8e879-116">-Error</span><span class="sxs-lookup"><span data-stu-id="8e879-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="8e879-117">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="8e879-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="8e879-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8e879-118">**Value**</span></span>|<span data-ttu-id="8e879-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8e879-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8e879-120">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="8e879-120">**Success**</span></span> <br/> |<span data-ttu-id="8e879-121">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="8e879-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="8e879-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="8e879-122">**Warning**</span></span> <br/> | <span data-ttu-id="8e879-123">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="8e879-123">Describes a request that was not processed.</span></span> <span data-ttu-id="8e879-124">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="8e879-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="8e879-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="8e879-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="8e879-126">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="8e879-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="8e879-127">-El servicio de directorio de Active Directory está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="8e879-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="8e879-128">-Buzones se han movido.</span><span class="sxs-lookup"><span data-stu-id="8e879-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="8e879-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="8e879-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="8e879-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="8e879-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="8e879-131">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="8e879-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="8e879-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="8e879-132">**Error**</span></span> <br/> | <span data-ttu-id="8e879-133">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="8e879-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="8e879-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="8e879-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="8e879-135">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="8e879-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="8e879-136">-Los atributos o elementos fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="8e879-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="8e879-137">-Etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="8e879-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="8e879-138">-De atributo o elemento no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="8e879-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="8e879-139">-Intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="8e879-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="8e879-140">-Error server-side en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="8e879-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="8e879-141">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="8e879-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8e879-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8e879-142">Child elements</span></span>

|<span data-ttu-id="8e879-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="8e879-143">**Element**</span></span>|<span data-ttu-id="8e879-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8e879-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8e879-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="8e879-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="8e879-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8e879-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="8e879-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8e879-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="8e879-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8e879-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="8e879-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="8e879-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="8e879-150">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="8e879-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="8e879-151">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="8e879-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="8e879-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="8e879-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="8e879-153">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="8e879-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="8e879-154">EncryptedSharedFolderDataCollection</span><span class="sxs-lookup"><span data-stu-id="8e879-154">EncryptedSharedFolderDataCollection</span></span>](encryptedsharedfolderdatacollection.md) <br/> |<span data-ttu-id="8e879-155">Contiene una colección de estructuras de datos que un cliente puede usar para autorizar el uso compartido de su calendario o póngase en contacto con datos con otros clientes.</span><span class="sxs-lookup"><span data-stu-id="8e879-155">Contains a collection of data structures that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span>  <br/> |
|[<span data-ttu-id="8e879-156">InvalidRecipients</span><span class="sxs-lookup"><span data-stu-id="8e879-156">InvalidRecipients</span></span>](invalidrecipients.md) <br/> |<span data-ttu-id="8e879-157">Representa a los destinatarios de la solicitud de compartir carpetas que no son válidos.</span><span class="sxs-lookup"><span data-stu-id="8e879-157">Represents recipients of the folder sharing request that are invalid.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8e879-158">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8e879-158">Parent elements</span></span>

|<span data-ttu-id="8e879-159">**Element**</span><span class="sxs-lookup"><span data-stu-id="8e879-159">**Element**</span></span>|<span data-ttu-id="8e879-160">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8e879-160">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8e879-161">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8e879-161">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="8e879-162">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8e879-162">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e879-163">Notas</span><span class="sxs-lookup"><span data-stu-id="8e879-163">Remarks</span></span>

<span data-ttu-id="8e879-164">El esquema que describe este elemento se encuentra en el directorio Virtual de IIS que hospeda los servicios Web Exchange del equipo que ejecuta a Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="8e879-164">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8e879-165">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8e879-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8e879-166">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8e879-166">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8e879-167">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8e879-167">Schema Name</span></span>  <br/> |<span data-ttu-id="8e879-168">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="8e879-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8e879-169">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8e879-169">Validation File</span></span>  <br/> |<span data-ttu-id="8e879-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8e879-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8e879-171">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8e879-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="8e879-172">False</span><span class="sxs-lookup"><span data-stu-id="8e879-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8e879-173">Ver también</span><span class="sxs-lookup"><span data-stu-id="8e879-173">See also</span></span>

- [<span data-ttu-id="8e879-174">Operación GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="8e879-174">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)
- [<span data-ttu-id="8e879-175">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="8e879-175">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

