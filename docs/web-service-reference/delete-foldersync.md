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
description: El elemento Delete identifica una única carpeta que se va a eliminar en el almacén de cliente local.
ms.openlocfilehash: 68f8687b8cf0723d7fd63a3d55da8ef7c2f98f8e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44454984"
---
# <a name="delete-foldersync"></a><span data-ttu-id="a8f4f-103">Eliminar (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="a8f4f-103">Delete (FolderSync)</span></span>

<span data-ttu-id="a8f4f-104">El elemento **Delete** identifica una única carpeta que se va a eliminar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="a8f4f-104">The **Delete** element identifies a single folder to delete in the local client store.</span></span> 
  
- [<span data-ttu-id="a8f4f-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="a8f4f-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)  
- [<span data-ttu-id="a8f4f-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a8f4f-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="a8f4f-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a8f4f-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)  
- [<span data-ttu-id="a8f4f-108">Cambios (jerarquía)</span><span class="sxs-lookup"><span data-stu-id="a8f4f-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md)  
- [<span data-ttu-id="a8f4f-109">Eliminar (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="a8f4f-109">Delete (FolderSync)</span></span>](delete-foldersync.md)
  
```xml
<Delete>
   <FolderId/>
</Delete>
```

<span data-ttu-id="a8f4f-110">**SyncFolderHierarchyDeleteType**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-110">**SyncFolderHierarchyDeleteType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a8f4f-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a8f4f-111">Attributes and elements</span></span>

<span data-ttu-id="a8f4f-112">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a8f4f-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a8f4f-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="a8f4f-113">Attributes</span></span>

<span data-ttu-id="a8f4f-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a8f4f-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a8f4f-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a8f4f-115">Child elements</span></span>

|<span data-ttu-id="a8f4f-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-116">**Element**</span></span>|<span data-ttu-id="a8f4f-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a8f4f-118">FolderId</span><span class="sxs-lookup"><span data-stu-id="a8f4f-118">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="a8f4f-119">Contiene el identificador y la clave de cambio de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="a8f4f-119">Contains the identifier and change key of a folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a8f4f-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a8f4f-120">Parent elements</span></span>

|<span data-ttu-id="a8f4f-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-121">**Element**</span></span>|<span data-ttu-id="a8f4f-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a8f4f-123">Cambios (jerarquía)</span><span class="sxs-lookup"><span data-stu-id="a8f4f-123">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="a8f4f-124">Contiene una matriz secuenciada de tipos de cambio que representan el tipo de diferencias entre las carpetas en el cliente y las carpetas en el equipo que ejecuta Microsoft Exchange Server 2007.</span><span class="sxs-lookup"><span data-stu-id="a8f4f-124">Contains a sequenced array of change types that represent the type of differences between the folders on the client and the folders on the computer that is running Microsoft Exchange Server 2007.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8f4f-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a8f4f-125">Remarks</span></span>

<span data-ttu-id="a8f4f-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo de Exchange 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="a8f4f-126">The schema that describes this element is located in the EWS virtual directory of the Exchange 2007 computer that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a8f4f-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a8f4f-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8f4f-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8f4f-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a8f4f-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a8f4f-129">Schema name</span></span>  <br/> |<span data-ttu-id="a8f4f-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a8f4f-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="a8f4f-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a8f4f-131">Validation file</span></span>  <br/> |<span data-ttu-id="a8f4f-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a8f4f-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a8f4f-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a8f4f-133">Can be empty</span></span>  <br/> |<span data-ttu-id="a8f4f-134">Falso</span><span class="sxs-lookup"><span data-stu-id="a8f4f-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a8f4f-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8f4f-135">See also</span></span>

- [<span data-ttu-id="a8f4f-136">Operación SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="a8f4f-136">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)
- [<span data-ttu-id="a8f4f-137">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="a8f4f-137">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="a8f4f-138">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a8f4f-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

