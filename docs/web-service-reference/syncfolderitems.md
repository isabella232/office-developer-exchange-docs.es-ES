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
description: El elemento SyncFolderItems define una solicitud para sincronizar elementos en una carpeta de almacén de Exchange.
ms.openlocfilehash: 0fa5b1544d5627d1423287369e72f97662c28d12
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465152"
---
# <a name="syncfolderitems"></a><span data-ttu-id="db9b1-103">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="db9b1-103">SyncFolderItems</span></span>

<span data-ttu-id="db9b1-104">El elemento **SyncFolderItems** define una solicitud para sincronizar elementos en una carpeta de almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="db9b1-104">The **SyncFolderItems** element defines a request to synchronize items in an Exchange store folder.</span></span> 
  
```xml
<SyncFolderItems>
   <ItemShape/>
   <SyncFolderId/>
   <SyncState/>
   <Ignore/>
   <MaxChangesReturned/>   <SyncScope/>
</SyncFolderItems>
```

 <span data-ttu-id="db9b1-105">**SyncFolderItemsType**</span><span class="sxs-lookup"><span data-stu-id="db9b1-105">**SyncFolderItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="db9b1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="db9b1-106">Attributes and elements</span></span>

<span data-ttu-id="db9b1-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="db9b1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="db9b1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="db9b1-108">Attributes</span></span>

<span data-ttu-id="db9b1-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="db9b1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="db9b1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="db9b1-110">Child elements</span></span>

|<span data-ttu-id="db9b1-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="db9b1-111">**Element**</span></span>|<span data-ttu-id="db9b1-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="db9b1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="db9b1-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="db9b1-113">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="db9b1-114">Identifica las propiedades de elemento y el contenido que se incluirá en una respuesta SyncFolderItems.</span><span class="sxs-lookup"><span data-stu-id="db9b1-114">Identifies the item properties and content to include in a SyncFolderItems response.</span></span> <span data-ttu-id="db9b1-115">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="db9b1-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="db9b1-116">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="db9b1-116">SyncFolderId</span></span>](syncfolderid.md) <br/> |<span data-ttu-id="db9b1-117">Representa la carpeta que contiene los elementos que se van a sincronizar.</span><span class="sxs-lookup"><span data-stu-id="db9b1-117">Represents the folder that contains the items to synchronize.</span></span> <span data-ttu-id="db9b1-118">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="db9b1-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="db9b1-119">SyncState</span><span class="sxs-lookup"><span data-stu-id="db9b1-119">SyncState</span></span>](syncstate-ex15websvcsotherref.md) <br/> |<span data-ttu-id="db9b1-120">Contiene una forma codificada en Base64 de los datos de sincronización que se actualizan después de cada solicitud correcta.</span><span class="sxs-lookup"><span data-stu-id="db9b1-120">Contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="db9b1-121">Se usa para identificar el estado de sincronización.</span><span class="sxs-lookup"><span data-stu-id="db9b1-121">This is used to identify the synchronization state.</span></span> <span data-ttu-id="db9b1-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="db9b1-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="db9b1-123">Ignore</span><span class="sxs-lookup"><span data-stu-id="db9b1-123">Ignore</span></span>](ignore.md) <br/> |<span data-ttu-id="db9b1-124">Identifica los elementos que se deben omitir durante la sincronización.</span><span class="sxs-lookup"><span data-stu-id="db9b1-124">Identifies items to skip during synchronization.</span></span> <span data-ttu-id="db9b1-125">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="db9b1-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="db9b1-126">MaxChangesReturned</span><span class="sxs-lookup"><span data-stu-id="db9b1-126">MaxChangesReturned</span></span>](maxchangesreturned.md) <br/> |<span data-ttu-id="db9b1-127">Describe el número máximo de cambios que se pueden devolver en una respuesta de sincronización.</span><span class="sxs-lookup"><span data-stu-id="db9b1-127">Describes the maximum number of changes that can be returned in a synchronization response.</span></span> <span data-ttu-id="db9b1-128">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="db9b1-128">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="db9b1-129">SyncScope</span><span class="sxs-lookup"><span data-stu-id="db9b1-129">SyncScope</span></span>](syncscope.md) <br/> |<span data-ttu-id="db9b1-130">Especifica si solo los elementos o elementos y la información asociada a la carpeta se devuelven en una respuesta de sincronización.</span><span class="sxs-lookup"><span data-stu-id="db9b1-130">Specifies whether just items or items and folder associated information are returned in a synchronization response.</span></span> <span data-ttu-id="db9b1-131">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="db9b1-131">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="db9b1-132">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="db9b1-132">Parent elements</span></span>

<span data-ttu-id="db9b1-133">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="db9b1-133">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="db9b1-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="db9b1-134">Remarks</span></span>

<span data-ttu-id="db9b1-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="db9b1-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="db9b1-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="db9b1-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db9b1-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="db9b1-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="db9b1-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="db9b1-138">Schema name</span></span>  <br/> |<span data-ttu-id="db9b1-139">esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="db9b1-139">messages schema</span></span>  <br/> |
|<span data-ttu-id="db9b1-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="db9b1-140">Validation file</span></span>  <br/> |<span data-ttu-id="db9b1-141">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="db9b1-141">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="db9b1-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="db9b1-142">Can be empty</span></span>  <br/> |<span data-ttu-id="db9b1-143">Falso</span><span class="sxs-lookup"><span data-stu-id="db9b1-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="db9b1-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="db9b1-144">See also</span></span>



[<span data-ttu-id="db9b1-145">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="db9b1-145">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="db9b1-146">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="db9b1-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

