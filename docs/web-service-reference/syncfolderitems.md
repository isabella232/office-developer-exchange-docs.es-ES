---
title: SyncFolderItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderItems
api_type:
- schema
ms.assetid: 463ed78c-bf82-4cd8-971a-d18425e9e7be
description: El elemento SyncFolderItems define una solicitud para sincronizar los elementos en una carpeta de almacén de Exchange.
ms.openlocfilehash: 368e19babfccaeab40380103495c63d30647905c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840614"
---
# <a name="syncfolderitems"></a><span data-ttu-id="5b865-103">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="5b865-103">SyncFolderItems</span></span>

<span data-ttu-id="5b865-104">El elemento **SyncFolderItems** define una solicitud para sincronizar los elementos en una carpeta de almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5b865-104">The **SyncFolderItems** element defines a request to synchronize items in an Exchange store folder.</span></span> 
  
```xml
<SyncFolderItems>
   <ItemShape/>
   <SyncFolderId/>
   <SyncState/>
   <Ignore/>
   <MaxChangesReturned/>   <SyncScope/>
</SyncFolderItems>
```

 <span data-ttu-id="5b865-105">**SyncFolderItemsType**</span><span class="sxs-lookup"><span data-stu-id="5b865-105">**SyncFolderItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5b865-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5b865-106">Attributes and elements</span></span>

<span data-ttu-id="5b865-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5b865-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5b865-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5b865-108">Attributes</span></span>

<span data-ttu-id="5b865-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5b865-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5b865-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5b865-110">Child elements</span></span>

|<span data-ttu-id="5b865-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="5b865-111">**Element**</span></span>|<span data-ttu-id="5b865-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5b865-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5b865-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="5b865-113">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="5b865-114">Identifica las propiedades de elemento y el contenido que desea incluir en una respuesta SyncFolderItems.</span><span class="sxs-lookup"><span data-stu-id="5b865-114">Identifies the item properties and content to include in a SyncFolderItems response.</span></span> <span data-ttu-id="5b865-115">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="5b865-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="5b865-116">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="5b865-116">SyncFolderId</span></span>](syncfolderid.md) <br/> |<span data-ttu-id="5b865-117">Representa la carpeta que contiene los elementos para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="5b865-117">Represents the folder that contains the items to synchronize.</span></span> <span data-ttu-id="5b865-118">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="5b865-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="5b865-119">Estado de sincronización</span><span class="sxs-lookup"><span data-stu-id="5b865-119">SyncState</span></span>](syncstate-ex15websvcsotherref.md) <br/> |<span data-ttu-id="5b865-120">Contiene un formulario con codificación base64 de los datos de sincronización que se actualizan después de cada solicitud realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="5b865-120">Contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="5b865-121">Esto se usa para identificar el estado de sincronización.</span><span class="sxs-lookup"><span data-stu-id="5b865-121">This is used to identify the synchronization state.</span></span> <span data-ttu-id="5b865-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="5b865-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="5b865-123">Ignorar</span><span class="sxs-lookup"><span data-stu-id="5b865-123">Ignore</span></span>](ignore.md) <br/> |<span data-ttu-id="5b865-124">Identifica a los elementos que se debe omitir durante la sincronización.</span><span class="sxs-lookup"><span data-stu-id="5b865-124">Identifies items to skip during synchronization.</span></span> <span data-ttu-id="5b865-125">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="5b865-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="5b865-126">MaxChangesReturned</span><span class="sxs-lookup"><span data-stu-id="5b865-126">MaxChangesReturned</span></span>](maxchangesreturned.md) <br/> |<span data-ttu-id="5b865-127">Describe el número máximo de cambios que se pueden devolver en una respuesta de sincronización.</span><span class="sxs-lookup"><span data-stu-id="5b865-127">Describes the maximum number of changes that can be returned in a synchronization response.</span></span> <span data-ttu-id="5b865-128">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="5b865-128">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="5b865-129">SyncScope</span><span class="sxs-lookup"><span data-stu-id="5b865-129">SyncScope</span></span>](syncscope.md) <br/> |<span data-ttu-id="5b865-130">Especifica si se devuelven sólo los elementos o elementos y la carpeta asociada información en una respuesta de sincronización.</span><span class="sxs-lookup"><span data-stu-id="5b865-130">Specifies whether just items or items and folder associated information are returned in a synchronization response.</span></span> <span data-ttu-id="5b865-131">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="5b865-131">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5b865-132">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5b865-132">Parent elements</span></span>

<span data-ttu-id="5b865-133">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5b865-133">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5b865-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5b865-134">Remarks</span></span>

<span data-ttu-id="5b865-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="5b865-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5b865-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5b865-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b865-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5b865-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5b865-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5b865-138">Schema name</span></span>  <br/> |<span data-ttu-id="5b865-139">esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="5b865-139">messages schema</span></span>  <br/> |
|<span data-ttu-id="5b865-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5b865-140">Validation file</span></span>  <br/> |<span data-ttu-id="5b865-141">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5b865-141">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5b865-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5b865-142">Can be empty</span></span>  <br/> |<span data-ttu-id="5b865-143">False</span><span class="sxs-lookup"><span data-stu-id="5b865-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5b865-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b865-144">See also</span></span>



[<span data-ttu-id="5b865-145">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="5b865-145">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="5b865-146">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="5b865-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

