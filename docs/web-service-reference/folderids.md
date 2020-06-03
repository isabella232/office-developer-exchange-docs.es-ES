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
description: El elemento FolderIds contiene una matriz de identificadores de carpeta que se usan para identificar las carpetas que se van a copiar, mover, obtener, eliminar o supervisar las notificaciones de eventos.
ms.openlocfilehash: ff0476f72c7da088bd2b39f58ab560dcc82197e4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530996"
---
# <a name="folderids"></a><span data-ttu-id="c1d16-103">FolderIds</span><span class="sxs-lookup"><span data-stu-id="c1d16-103">FolderIds</span></span>

<span data-ttu-id="c1d16-104">El elemento **FolderIds** contiene una matriz de identificadores de carpeta que se usan para identificar las carpetas que se van a copiar, mover, obtener, eliminar o supervisar las notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="c1d16-104">The **FolderIds** element contains an array of folder identifiers that are used to identify folders to copy, move, get, delete, or monitor for event notifications.</span></span> 
  
```xml
<FolderIds>
   <FolderId/>
   <DistinguishedFolderId/>
</FolderIds>
```

 <span data-ttu-id="c1d16-105">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="c1d16-105">**NonEmptyArrayOfBaseFolderIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1d16-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c1d16-106">Attributes and elements</span></span>

<span data-ttu-id="c1d16-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c1d16-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1d16-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c1d16-108">Attributes</span></span>

<span data-ttu-id="c1d16-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c1d16-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c1d16-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c1d16-110">Child elements</span></span>

|<span data-ttu-id="c1d16-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c1d16-111">**Element**</span></span>|<span data-ttu-id="c1d16-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1d16-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1d16-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="c1d16-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="c1d16-114">Contiene el identificador y la clave de cambio de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="c1d16-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="c1d16-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="c1d16-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="c1d16-116">Identifica las carpetas de Microsoft Exchange Server a las que se puede hacer referencia por su nombre.</span><span class="sxs-lookup"><span data-stu-id="c1d16-116">Identifies Microsoft Exchange Server folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c1d16-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c1d16-117">Parent elements</span></span>

|<span data-ttu-id="c1d16-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c1d16-118">**Element**</span></span>|<span data-ttu-id="c1d16-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1d16-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1d16-120">GetFolder</span><span class="sxs-lookup"><span data-stu-id="c1d16-120">GetFolder</span></span>](getfolder.md) <br/> |<span data-ttu-id="c1d16-121">Define una solicitud para obtener una carpeta del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c1d16-121">Defines a request to get a folder from the Exchange store.</span></span>  <br/> <span data-ttu-id="c1d16-122">La siguiente es la expresión XPath a este elemento:`/GetFolder`</span><span class="sxs-lookup"><span data-stu-id="c1d16-122">The following is the XPath expression to this element:  `/GetFolder`</span></span> <br/> |
|[<span data-ttu-id="c1d16-123">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="c1d16-123">DeleteFolder</span></span>](deletefolder.md) <br/> |<span data-ttu-id="c1d16-124">Define una solicitud para eliminar carpetas del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c1d16-124">Defines a request to delete folders from the Exchange store.</span></span>  <br/> <span data-ttu-id="c1d16-125">La siguiente es la expresión XPath a este elemento:`/DeleteFolder`</span><span class="sxs-lookup"><span data-stu-id="c1d16-125">The following is the XPath expression to this element:  `/DeleteFolder`</span></span> <br/> |
|[<span data-ttu-id="c1d16-126">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="c1d16-126">EmptyFolder</span></span>](emptyfolder.md) <br/> |<span data-ttu-id="c1d16-127">Define una solicitud para eliminar carpetas del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c1d16-127">Defines a request to delete folders from the Exchange store.</span></span>  <br/> <span data-ttu-id="c1d16-128">La siguiente es la expresión XPath a este elemento:`/EmptyFolder`</span><span class="sxs-lookup"><span data-stu-id="c1d16-128">The following is the XPath expression to this element:  `/EmptyFolder`</span></span> <br/> |
|[<span data-ttu-id="c1d16-129">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="c1d16-129">MoveFolder</span></span>](movefolder.md) <br/> |<span data-ttu-id="c1d16-130">Define una solicitud para mover una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c1d16-130">Defines a request to move a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="c1d16-131">La siguiente es la expresión XPath a este elemento:`/MoveFolder`</span><span class="sxs-lookup"><span data-stu-id="c1d16-131">The following is the XPath expression to this element:  `/MoveFolder`</span></span> <br/> |
|[<span data-ttu-id="c1d16-132">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="c1d16-132">CopyFolder</span></span>](copyfolder.md) <br/> |<span data-ttu-id="c1d16-133">Define una solicitud para copiar una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c1d16-133">Defines a request to copy a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="c1d16-134">La siguiente es la expresión XPath a este elemento:`/CopyFolder`</span><span class="sxs-lookup"><span data-stu-id="c1d16-134">The following is the XPath expression to this element:  `/CopyFolder`</span></span> <br/> |
|[<span data-ttu-id="c1d16-135">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="c1d16-135">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="c1d16-136">Representa una suscripción a una suscripción de notificación de eventos basada en inserción.</span><span class="sxs-lookup"><span data-stu-id="c1d16-136">Represents a subscription to a push-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="c1d16-137">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="c1d16-137">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="c1d16-138">Representa una suscripción a una suscripción de notificación de eventos basada en extracción.</span><span class="sxs-lookup"><span data-stu-id="c1d16-138">Represents a subscription to a pull-based event notification subscription.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1d16-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c1d16-139">Remarks</span></span>

<span data-ttu-id="c1d16-140">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="c1d16-140">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1d16-141">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c1d16-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1d16-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1d16-142">Namespace</span></span>  <br/> |<span data-ttu-id="c1d16-143">https://schemas.microsoft.com/exchange/services/2006/messages y https://schemas.microsoft.com/exchange/services/2006/types</span><span class="sxs-lookup"><span data-stu-id="c1d16-143">https://schemas.microsoft.com/exchange/services/2006/messages and https://schemas.microsoft.com/exchange/services/2006/types</span></span>  <br/> |
|<span data-ttu-id="c1d16-144">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c1d16-144">Schema Name</span></span>  <br/> |<span data-ttu-id="c1d16-145">Esquema de mensajes; Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c1d16-145">Messages schema; Types schema</span></span>  <br/> |
|<span data-ttu-id="c1d16-146">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c1d16-146">Validation File</span></span>  <br/> |<span data-ttu-id="c1d16-147">Messages. xsd; Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c1d16-147">Messages.xsd; Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c1d16-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c1d16-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="c1d16-149">Falso</span><span class="sxs-lookup"><span data-stu-id="c1d16-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1d16-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1d16-150">See also</span></span>



[<span data-ttu-id="c1d16-151">Operación GetFolder</span><span class="sxs-lookup"><span data-stu-id="c1d16-151">GetFolder operation</span></span>](getfolder-operation.md)
  
[<span data-ttu-id="c1d16-152">Operación DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="c1d16-152">DeleteFolder operation</span></span>](deletefolder-operation.md)
  
[<span data-ttu-id="c1d16-153">Operación MoveFolder</span><span class="sxs-lookup"><span data-stu-id="c1d16-153">MoveFolder operation</span></span>](movefolder-operation.md)
  
[<span data-ttu-id="c1d16-154">Operación CopyFolder</span><span class="sxs-lookup"><span data-stu-id="c1d16-154">CopyFolder operation</span></span>](copyfolder-operation.md)
  
[<span data-ttu-id="c1d16-155">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="c1d16-155">Subscribe operation</span></span>](subscribe-operation.md)

