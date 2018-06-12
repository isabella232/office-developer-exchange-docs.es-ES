---
title: SyncFolderHierarchy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderHierarchy
api_type:
- schema
ms.assetid: 55df4d01-e48e-4263-a851-78a66ad1093a
description: El elemento SyncFolderHierarchy define una solicitud para sincronizar una jerarquía de carpetas en un cliente.
ms.openlocfilehash: f72640e5605dd83e92cd323cb00e4d2f64406245
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840610"
---
# <a name="syncfolderhierarchy"></a><span data-ttu-id="0dbf6-103">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="0dbf6-103">SyncFolderHierarchy</span></span>

<span data-ttu-id="0dbf6-104">El elemento **SyncFolderHierarchy** define una solicitud para sincronizar una jerarquía de carpetas en un cliente.</span><span class="sxs-lookup"><span data-stu-id="0dbf6-104">The **SyncFolderHierarchy** element defines a request to synchronize a folder hierarchy on a client.</span></span> 
  
```xml
<SyncFolderHierarchy>
   <FolderShape/>   <SyncFolderId/>
   <SyncState/>
</SyncFolderHierarchy>
```

 <span data-ttu-id="0dbf6-105">**SyncFolderHierarchyType**</span><span class="sxs-lookup"><span data-stu-id="0dbf6-105">**SyncFolderHierarchyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0dbf6-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0dbf6-106">Attributes and elements</span></span>

<span data-ttu-id="0dbf6-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0dbf6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0dbf6-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0dbf6-108">Attributes</span></span>

<span data-ttu-id="0dbf6-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0dbf6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0dbf6-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0dbf6-110">Child elements</span></span>

|<span data-ttu-id="0dbf6-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="0dbf6-111">**Element**</span></span>|<span data-ttu-id="0dbf6-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0dbf6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0dbf6-113">FolderShape</span><span class="sxs-lookup"><span data-stu-id="0dbf6-113">FolderShape</span></span>](foldershape.md) <br/> |<span data-ttu-id="0dbf6-114">Identifica las propiedades de carpeta para incluir en una respuesta [SyncFolderHierarchy](syncfolderhierarchy.md) .</span><span class="sxs-lookup"><span data-stu-id="0dbf6-114">Identifies the folder properties to include in a [SyncFolderHierarchy](syncfolderhierarchy.md) response.</span></span>  <br/> |
|[<span data-ttu-id="0dbf6-115">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="0dbf6-115">SyncFolderId</span></span>](syncfolderid.md) <br/> |<span data-ttu-id="0dbf6-116">Representa la carpeta que contiene los elementos para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="0dbf6-116">Represents the folder that contains the items to synchronize.</span></span> <span data-ttu-id="0dbf6-117">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="0dbf6-117">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="0dbf6-118">Estado de sincronización</span><span class="sxs-lookup"><span data-stu-id="0dbf6-118">SyncState</span></span>](syncstate-ex15websvcsotherref.md) <br/> |<span data-ttu-id="0dbf6-119">Contiene un formulario con codificación base64 de los datos de sincronización que se actualizan después de cada solicitud realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="0dbf6-119">Contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="0dbf6-120">Esto se usa para identificar el estado de sincronización.</span><span class="sxs-lookup"><span data-stu-id="0dbf6-120">This is used to identify the synchronization state.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0dbf6-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0dbf6-121">Parent elements</span></span>

<span data-ttu-id="0dbf6-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0dbf6-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0dbf6-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0dbf6-123">Remarks</span></span>

<span data-ttu-id="0dbf6-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="0dbf6-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0dbf6-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0dbf6-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0dbf6-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0dbf6-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0dbf6-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0dbf6-127">Schema name</span></span>  <br/> |<span data-ttu-id="0dbf6-128">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="0dbf6-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0dbf6-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0dbf6-129">Validation file</span></span>  <br/> |<span data-ttu-id="0dbf6-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0dbf6-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0dbf6-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0dbf6-131">Can be empty</span></span>  <br/> |<span data-ttu-id="0dbf6-132">False</span><span class="sxs-lookup"><span data-stu-id="0dbf6-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0dbf6-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="0dbf6-133">See also</span></span>



[<span data-ttu-id="0dbf6-134">Operación SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="0dbf6-134">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)


- [<span data-ttu-id="0dbf6-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0dbf6-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

