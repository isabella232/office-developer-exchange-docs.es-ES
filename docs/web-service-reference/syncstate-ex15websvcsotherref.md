---
title: SyncState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncState
api_type:
- schema
ms.assetid: e5ebaae3-0f07-481d-ac67-d9687a3c7ac3
description: El elemento SyncState contiene una forma codificada en Base64 de los datos de sincronización que se actualizan después de cada solicitud correcta. Se usa para identificar el estado de sincronización.
ms.openlocfilehash: 8e2d9a633cdad0a124b87e4e794399c06d3b5445
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458967"
---
# <a name="syncstate"></a><span data-ttu-id="69d0d-104">SyncState</span><span class="sxs-lookup"><span data-stu-id="69d0d-104">SyncState</span></span>

<span data-ttu-id="69d0d-105">El elemento **SyncState** contiene una forma codificada en Base64 de los datos de sincronización que se actualizan después de cada solicitud correcta.</span><span class="sxs-lookup"><span data-stu-id="69d0d-105">The **SyncState** element contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="69d0d-106">Se usa para identificar el estado de sincronización.</span><span class="sxs-lookup"><span data-stu-id="69d0d-106">This is used to identify the synchronization state.</span></span> 
  
```xml
<SyncState/>
```

 <span data-ttu-id="69d0d-107">**String**</span><span class="sxs-lookup"><span data-stu-id="69d0d-107">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="69d0d-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="69d0d-108">Attributes and elements</span></span>

<span data-ttu-id="69d0d-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="69d0d-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="69d0d-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="69d0d-110">Attributes</span></span>

<span data-ttu-id="69d0d-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="69d0d-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="69d0d-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="69d0d-112">Child elements</span></span>

<span data-ttu-id="69d0d-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="69d0d-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="69d0d-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="69d0d-114">Parent elements</span></span>

|<span data-ttu-id="69d0d-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="69d0d-115">**Element**</span></span>|<span data-ttu-id="69d0d-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="69d0d-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69d0d-117">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="69d0d-117">SyncFolderHierarchy</span></span>](syncfolderhierarchy.md) <br/> |<span data-ttu-id="69d0d-118">Define una solicitud para sincronizar una jerarquía de carpetas en un cliente.</span><span class="sxs-lookup"><span data-stu-id="69d0d-118">Defines a request to synchronize a folder hierarchy on a client.</span></span>  <br/> |
|[<span data-ttu-id="69d0d-119">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="69d0d-119">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md) <br/> |<span data-ttu-id="69d0d-120">Contiene el estado y el resultado de una solicitud SyncFolderHierarchy.</span><span class="sxs-lookup"><span data-stu-id="69d0d-120">Contains the status and result of a SyncFolderHierarchy request.</span></span>  <br/> |
|[<span data-ttu-id="69d0d-121">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="69d0d-121">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="69d0d-122">Define una solicitud para sincronizar elementos en una carpeta de almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="69d0d-122">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> |
|[<span data-ttu-id="69d0d-123">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="69d0d-123">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md) <br/> |<span data-ttu-id="69d0d-124">Contiene el estado y el resultado de una solicitud SyncFolderItems.</span><span class="sxs-lookup"><span data-stu-id="69d0d-124">Contains the status and result of a SyncFolderItems request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="69d0d-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="69d0d-125">Text value</span></span>

<span data-ttu-id="69d0d-126">Es necesario un valor de texto cuando se usa este elemento.</span><span class="sxs-lookup"><span data-stu-id="69d0d-126">A text value is required when this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="69d0d-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="69d0d-127">Remarks</span></span>

<span data-ttu-id="69d0d-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="69d0d-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="69d0d-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="69d0d-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69d0d-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="69d0d-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="69d0d-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="69d0d-131">Schema name</span></span>  <br/> |<span data-ttu-id="69d0d-132">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="69d0d-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="69d0d-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="69d0d-133">Validation file</span></span>  <br/> |<span data-ttu-id="69d0d-134">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="69d0d-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="69d0d-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="69d0d-135">Can be empty</span></span>  <br/> |<span data-ttu-id="69d0d-136">Falso</span><span class="sxs-lookup"><span data-stu-id="69d0d-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="69d0d-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="69d0d-137">See also</span></span>



[<span data-ttu-id="69d0d-138">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="69d0d-138">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
  
[<span data-ttu-id="69d0d-139">Operación SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="69d0d-139">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)


- [<span data-ttu-id="69d0d-140">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="69d0d-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

