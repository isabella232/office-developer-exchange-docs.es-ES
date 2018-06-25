---
title: FolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderIds
api_type:
- schema
ms.assetid: 3ff9d15a-7220-4785-ae6b-583a7eb82005
description: El elemento FolderIds contiene una matriz de identificadores de carpeta que se usa para identificar las carpetas para copiar, mover, obtener, eliminar o supervisar para las notificaciones de eventos.
ms.openlocfilehash: 911a74ca778ee988c270c16c67620a40656d82d8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764681"
---
# <a name="folderids"></a><span data-ttu-id="414e0-103">FolderIds</span><span class="sxs-lookup"><span data-stu-id="414e0-103">FolderIds</span></span>

<span data-ttu-id="414e0-104">El elemento **FolderIds** contiene una matriz de identificadores de carpeta que se usa para identificar las carpetas para copiar, mover, obtener, eliminar o supervisar para las notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="414e0-104">The **FolderIds** element contains an array of folder identifiers that are used to identify folders to copy, move, get, delete, or monitor for event notifications.</span></span> 
  
```xml
<FolderIds>
   <FolderId/>
   <DistinguishedFolderId/>
</FolderIds>
```

 <span data-ttu-id="414e0-105">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="414e0-105">**NonEmptyArrayOfBaseFolderIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="414e0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="414e0-106">Attributes and elements</span></span>

<span data-ttu-id="414e0-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="414e0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="414e0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="414e0-108">Attributes</span></span>

<span data-ttu-id="414e0-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="414e0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="414e0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="414e0-110">Child elements</span></span>

|<span data-ttu-id="414e0-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="414e0-111">**Element**</span></span>|<span data-ttu-id="414e0-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="414e0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="414e0-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="414e0-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="414e0-114">Contiene el identificador y cambiar la clave de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="414e0-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="414e0-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="414e0-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="414e0-116">Identifica las carpetas de Microsoft Exchange Server que se pueden hacer referencia por su nombre.</span><span class="sxs-lookup"><span data-stu-id="414e0-116">Identifies Microsoft Exchange Server folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="414e0-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="414e0-117">Parent elements</span></span>

|<span data-ttu-id="414e0-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="414e0-118">**Element**</span></span>|<span data-ttu-id="414e0-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="414e0-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="414e0-120">GetFolder</span><span class="sxs-lookup"><span data-stu-id="414e0-120">GetFolder</span></span>](getfolder.md) <br/> |<span data-ttu-id="414e0-121">Define una solicitud para obtener una carpeta desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="414e0-121">Defines a request to get a folder from the Exchange store.</span></span>  <br/> <span data-ttu-id="414e0-122">La siguiente es la expresión de XPath para este elemento:`/GetFolder`</span><span class="sxs-lookup"><span data-stu-id="414e0-122">The following is the XPath expression to this element:  `/GetFolder`</span></span> <br/> |
|[<span data-ttu-id="414e0-123">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="414e0-123">DeleteFolder</span></span>](deletefolder.md) <br/> |<span data-ttu-id="414e0-124">Define una solicitud para eliminar las carpetas del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="414e0-124">Defines a request to delete folders from the Exchange store.</span></span>  <br/> <span data-ttu-id="414e0-125">La siguiente es la expresión de XPath para este elemento:`/DeleteFolder`</span><span class="sxs-lookup"><span data-stu-id="414e0-125">The following is the XPath expression to this element:  `/DeleteFolder`</span></span> <br/> |
|[<span data-ttu-id="414e0-126">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="414e0-126">EmptyFolder</span></span>](emptyfolder.md) <br/> |<span data-ttu-id="414e0-127">Define una solicitud para eliminar las carpetas del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="414e0-127">Defines a request to delete folders from the Exchange store.</span></span>  <br/> <span data-ttu-id="414e0-128">La siguiente es la expresión de XPath para este elemento:`/EmptyFolder`</span><span class="sxs-lookup"><span data-stu-id="414e0-128">The following is the XPath expression to this element:  `/EmptyFolder`</span></span> <br/> |
|[<span data-ttu-id="414e0-129">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="414e0-129">MoveFolder</span></span>](movefolder.md) <br/> |<span data-ttu-id="414e0-130">Define una solicitud para mover una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="414e0-130">Defines a request to move a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="414e0-131">La siguiente es la expresión de XPath para este elemento:`/MoveFolder`</span><span class="sxs-lookup"><span data-stu-id="414e0-131">The following is the XPath expression to this element:  `/MoveFolder`</span></span> <br/> |
|[<span data-ttu-id="414e0-132">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="414e0-132">CopyFolder</span></span>](copyfolder.md) <br/> |<span data-ttu-id="414e0-133">Define una solicitud para copiar una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="414e0-133">Defines a request to copy a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="414e0-134">La siguiente es la expresión de XPath para este elemento:`/CopyFolder`</span><span class="sxs-lookup"><span data-stu-id="414e0-134">The following is the XPath expression to this element:  `/CopyFolder`</span></span> <br/> |
|[<span data-ttu-id="414e0-135">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="414e0-135">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="414e0-136">Representa una suscripción a una suscripción de notificación de evento basada en inserción.</span><span class="sxs-lookup"><span data-stu-id="414e0-136">Represents a subscription to a push-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="414e0-137">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="414e0-137">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="414e0-138">Representa una suscripción a una suscripción de notificación de eventos basado en la extracción.</span><span class="sxs-lookup"><span data-stu-id="414e0-138">Represents a subscription to a pull-based event notification subscription.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="414e0-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="414e0-139">Remarks</span></span>

<span data-ttu-id="414e0-140">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="414e0-140">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="414e0-141">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="414e0-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="414e0-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="414e0-142">Namespace</span></span>  <br/> |<span data-ttu-id="414e0-143">http://schemas.microsoft.com/exchange/services/2006/messages y http://schemas.microsoft.com/exchange/services/2006/types</span><span class="sxs-lookup"><span data-stu-id="414e0-143">http://schemas.microsoft.com/exchange/services/2006/messages and http://schemas.microsoft.com/exchange/services/2006/types</span></span>  <br/> |
|<span data-ttu-id="414e0-144">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="414e0-144">Schema Name</span></span>  <br/> |<span data-ttu-id="414e0-145">Esquema de los mensajes; Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="414e0-145">Messages schema; Types schema</span></span>  <br/> |
|<span data-ttu-id="414e0-146">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="414e0-146">Validation File</span></span>  <br/> |<span data-ttu-id="414e0-147">Messages.xsd; Types.xsd</span><span class="sxs-lookup"><span data-stu-id="414e0-147">Messages.xsd; Types.xsd</span></span>  <br/> |
|<span data-ttu-id="414e0-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="414e0-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="414e0-149">False</span><span class="sxs-lookup"><span data-stu-id="414e0-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="414e0-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="414e0-150">See also</span></span>



[<span data-ttu-id="414e0-151">Operación GetFolder</span><span class="sxs-lookup"><span data-stu-id="414e0-151">GetFolder operation</span></span>](getfolder-operation.md)
  
[<span data-ttu-id="414e0-152">Operación DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="414e0-152">DeleteFolder operation</span></span>](deletefolder-operation.md)
  
[<span data-ttu-id="414e0-153">Operación MoveFolder</span><span class="sxs-lookup"><span data-stu-id="414e0-153">MoveFolder operation</span></span>](movefolder-operation.md)
  
[<span data-ttu-id="414e0-154">Operación CopyFolder</span><span class="sxs-lookup"><span data-stu-id="414e0-154">CopyFolder operation</span></span>](copyfolder-operation.md)
  
[<span data-ttu-id="414e0-155">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="414e0-155">Subscribe operation</span></span>](subscribe-operation.md)

