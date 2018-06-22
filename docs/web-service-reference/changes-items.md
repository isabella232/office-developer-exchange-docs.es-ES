---
title: Cambios (elementos)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Changes
api_type:
- schema
ms.assetid: d3139fef-0455-4b89-babd-5d6783b50a58
description: El elemento de cambios contiene una matriz de secuencia de tipos de cambio que representan los tipos de las diferencias entre los elementos en el cliente y los elementos en el servidor de Exchange.
ms.openlocfilehash: 8e38597276e3e3051a5c1494619d3220280e401f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763735"
---
# <a name="changes-items"></a><span data-ttu-id="5b538-103">Cambios (elementos)</span><span class="sxs-lookup"><span data-stu-id="5b538-103">Changes (Items)</span></span>

<span data-ttu-id="5b538-104">El elemento de **cambios** contiene una matriz de secuencia de tipos de cambio que representan los tipos de las diferencias entre los elementos en el cliente y los elementos en el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5b538-104">The **Changes** element contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span> 
  
[<span data-ttu-id="5b538-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="5b538-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)
  
[<span data-ttu-id="5b538-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5b538-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="5b538-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5b538-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)
  
[<span data-ttu-id="5b538-108">Cambios (elementos)</span><span class="sxs-lookup"><span data-stu-id="5b538-108">Changes (Items)</span></span>](changes-items.md)
  
```xml
<Changes>
   <Create/>
   <Update/>
   <Delete/>
</Changes>
```

 <span data-ttu-id="5b538-109">**SyncFolderItemsChangesType**</span><span class="sxs-lookup"><span data-stu-id="5b538-109">**SyncFolderItemsChangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5b538-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5b538-110">Attributes and elements</span></span>

<span data-ttu-id="5b538-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5b538-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5b538-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="5b538-112">Attributes</span></span>

<span data-ttu-id="5b538-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5b538-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5b538-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5b538-114">Child elements</span></span>

|<span data-ttu-id="5b538-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="5b538-115">**Element**</span></span>|<span data-ttu-id="5b538-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5b538-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5b538-117">Crear (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="5b538-117">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="5b538-118">Identifica un solo elemento para crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="5b538-118">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="5b538-119">Actualización (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="5b538-119">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="5b538-120">Identifica un solo elemento que se debe actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="5b538-120">Identifies a single item to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="5b538-121">Eliminar (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="5b538-121">Delete (ItemSync)</span></span>](delete-itemsync.md) <br/> |<span data-ttu-id="5b538-122">Identifica un solo elemento para eliminar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="5b538-122">Identifies a single item to delete in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="5b538-123">ReadFlagChange</span><span class="sxs-lookup"><span data-stu-id="5b538-123">ReadFlagChange</span></span>](readflagchange.md) <br/> |<span data-ttu-id="5b538-124">Se devuelven en las respuestas de [operación SyncFolderItems](syncfolderitems-operation.md) cuando se leyó un elemento.</span><span class="sxs-lookup"><span data-stu-id="5b538-124">Returned in [SyncFolderItems operation](syncfolderitems-operation.md) responses when an item has been read.</span></span> <span data-ttu-id="5b538-125">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="5b538-125">This property is read-only.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5b538-126">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5b538-126">Parent elements</span></span>

|<span data-ttu-id="5b538-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="5b538-127">**Element**</span></span>|<span data-ttu-id="5b538-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5b538-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5b538-129">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5b538-129">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md) <br/> |<span data-ttu-id="5b538-130">Contiene el estado y el resultado de una solicitud de [operación SyncFolderItems](syncfolderitems-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="5b538-130">Contains the status and result of a [SyncFolderItems operation](syncfolderitems-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b538-131">Notas</span><span class="sxs-lookup"><span data-stu-id="5b538-131">Remarks</span></span>

<span data-ttu-id="5b538-132">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="5b538-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5b538-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5b538-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b538-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5b538-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5b538-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5b538-135">Schema name</span></span>  <br/> |<span data-ttu-id="5b538-136">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="5b538-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5b538-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5b538-137">Validation file</span></span>  <br/> |<span data-ttu-id="5b538-138">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5b538-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5b538-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5b538-139">Can be empty</span></span>  <br/> |<span data-ttu-id="5b538-140">False</span><span class="sxs-lookup"><span data-stu-id="5b538-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5b538-141">Ver también</span><span class="sxs-lookup"><span data-stu-id="5b538-141">See also</span></span>



[<span data-ttu-id="5b538-142">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="5b538-142">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="5b538-143">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="5b538-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

