---
title: Eliminar (FolderSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Delete
api_type:
- schema
ms.assetid: c4397d91-43ef-40a9-a80e-d31501a33caa
description: El elemento Eliminar identifica una sola carpeta para eliminar en el almacén de cliente local.
ms.openlocfilehash: 5cad36c6fcff782195fdb285e2d3c4f3c5ec0f1e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764073"
---
# <a name="delete-foldersync"></a><span data-ttu-id="4db55-103">Eliminar (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="4db55-103">Delete (FolderSync)</span></span>

<span data-ttu-id="4db55-104">El elemento **Eliminar** identifica una sola carpeta para eliminar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="4db55-104">The **Delete** element identifies a single folder to delete in the local client store.</span></span> 
  
- [<span data-ttu-id="4db55-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="4db55-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)  
- [<span data-ttu-id="4db55-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4db55-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="4db55-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4db55-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)  
- [<span data-ttu-id="4db55-108">Cambios (jerarquía)</span><span class="sxs-lookup"><span data-stu-id="4db55-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md)  
- [<span data-ttu-id="4db55-109">Eliminar (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="4db55-109">Delete (FolderSync)</span></span>](delete-foldersync.md)
  
```xml
<Delete>
   <FolderId/>
</Delete>
```

<span data-ttu-id="4db55-110">**SyncFolderHierarchyDeleteType**</span><span class="sxs-lookup"><span data-stu-id="4db55-110">**SyncFolderHierarchyDeleteType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="4db55-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4db55-111">Attributes and elements</span></span>

<span data-ttu-id="4db55-112">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4db55-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4db55-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="4db55-113">Attributes</span></span>

<span data-ttu-id="4db55-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4db55-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4db55-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4db55-115">Child elements</span></span>

|<span data-ttu-id="4db55-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="4db55-116">**Element**</span></span>|<span data-ttu-id="4db55-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4db55-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4db55-118">FolderId</span><span class="sxs-lookup"><span data-stu-id="4db55-118">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="4db55-119">Contiene el identificador y cambiar la clave de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="4db55-119">Contains the identifier and change key of a folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4db55-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4db55-120">Parent elements</span></span>

|<span data-ttu-id="4db55-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="4db55-121">**Element**</span></span>|<span data-ttu-id="4db55-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4db55-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4db55-123">Cambios (jerarquía)</span><span class="sxs-lookup"><span data-stu-id="4db55-123">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="4db55-124">Contiene una matriz de tipos de cambio que representan el tipo de las diferencias entre las carpetas en el cliente y las carpetas en el equipo que ejecuta Microsoft Exchange Server 2007 secuenciada.</span><span class="sxs-lookup"><span data-stu-id="4db55-124">Contains a sequenced array of change types that represent the type of differences between the folders on the client and the folders on the computer that is running Microsoft Exchange Server 2007.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4db55-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4db55-125">Remarks</span></span>

<span data-ttu-id="4db55-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo de Exchange 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4db55-126">The schema that describes this element is located in the EWS virtual directory of the Exchange 2007 computer that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4db55-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4db55-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4db55-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4db55-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4db55-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4db55-129">Schema name</span></span>  <br/> |<span data-ttu-id="4db55-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4db55-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="4db55-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4db55-131">Validation file</span></span>  <br/> |<span data-ttu-id="4db55-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4db55-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4db55-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4db55-133">Can be empty</span></span>  <br/> |<span data-ttu-id="4db55-134">False</span><span class="sxs-lookup"><span data-stu-id="4db55-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4db55-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="4db55-135">See also</span></span>

- [<span data-ttu-id="4db55-136">Operación SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="4db55-136">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)
- [<span data-ttu-id="4db55-137">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="4db55-137">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="4db55-138">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="4db55-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

