---
title: Estado de sincronización
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
description: El elemento de estado de sincronización contiene un formulario con codificación base64 de los datos de sincronización que se actualizan después de cada solicitud realizada correctamente. Esto se usa para identificar el estado de sincronización.
ms.openlocfilehash: 3c600dde09fd813dcfb1f6e74671ebe9004701a1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840619"
---
# <a name="syncstate"></a><span data-ttu-id="e34c9-104">Estado de sincronización</span><span class="sxs-lookup"><span data-stu-id="e34c9-104">SyncState</span></span>

<span data-ttu-id="e34c9-105">El elemento de **estado de sincronización** contiene un formulario con codificación base64 de los datos de sincronización que se actualizan después de cada solicitud realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="e34c9-105">The **SyncState** element contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="e34c9-106">Esto se usa para identificar el estado de sincronización.</span><span class="sxs-lookup"><span data-stu-id="e34c9-106">This is used to identify the synchronization state.</span></span> 
  
```xml
<SyncState/>
```

 <span data-ttu-id="e34c9-107">**String**</span><span class="sxs-lookup"><span data-stu-id="e34c9-107">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e34c9-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e34c9-108">Attributes and elements</span></span>

<span data-ttu-id="e34c9-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e34c9-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e34c9-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="e34c9-110">Attributes</span></span>

<span data-ttu-id="e34c9-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e34c9-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e34c9-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e34c9-112">Child elements</span></span>

<span data-ttu-id="e34c9-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e34c9-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e34c9-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e34c9-114">Parent elements</span></span>

|<span data-ttu-id="e34c9-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="e34c9-115">**Element**</span></span>|<span data-ttu-id="e34c9-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e34c9-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e34c9-117">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="e34c9-117">SyncFolderHierarchy</span></span>](syncfolderhierarchy.md) <br/> |<span data-ttu-id="e34c9-118">Define una solicitud para sincronizar una jerarquía de carpetas en un cliente.</span><span class="sxs-lookup"><span data-stu-id="e34c9-118">Defines a request to synchronize a folder hierarchy on a client.</span></span>  <br/> |
|[<span data-ttu-id="e34c9-119">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e34c9-119">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md) <br/> |<span data-ttu-id="e34c9-120">Contiene el estado y el resultado de una solicitud de SyncFolderHierarchy.</span><span class="sxs-lookup"><span data-stu-id="e34c9-120">Contains the status and result of a SyncFolderHierarchy request.</span></span>  <br/> |
|[<span data-ttu-id="e34c9-121">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="e34c9-121">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="e34c9-122">Define una solicitud para sincronizar los elementos en una carpeta de almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e34c9-122">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> |
|[<span data-ttu-id="e34c9-123">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e34c9-123">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md) <br/> |<span data-ttu-id="e34c9-124">Contiene el estado y el resultado de una solicitud de SyncFolderItems.</span><span class="sxs-lookup"><span data-stu-id="e34c9-124">Contains the status and result of a SyncFolderItems request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e34c9-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e34c9-125">Text value</span></span>

<span data-ttu-id="e34c9-126">Cuando se usa este elemento, es necesario un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="e34c9-126">A text value is required when this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e34c9-127">Notas</span><span class="sxs-lookup"><span data-stu-id="e34c9-127">Remarks</span></span>

<span data-ttu-id="e34c9-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="e34c9-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e34c9-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e34c9-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e34c9-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e34c9-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e34c9-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e34c9-131">Schema name</span></span>  <br/> |<span data-ttu-id="e34c9-132">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="e34c9-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e34c9-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e34c9-133">Validation file</span></span>  <br/> |<span data-ttu-id="e34c9-134">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e34c9-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e34c9-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e34c9-135">Can be empty</span></span>  <br/> |<span data-ttu-id="e34c9-136">False</span><span class="sxs-lookup"><span data-stu-id="e34c9-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e34c9-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="e34c9-137">See also</span></span>



[<span data-ttu-id="e34c9-138">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="e34c9-138">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
  
[<span data-ttu-id="e34c9-139">Operación SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="e34c9-139">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)


- [<span data-ttu-id="e34c9-140">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e34c9-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

