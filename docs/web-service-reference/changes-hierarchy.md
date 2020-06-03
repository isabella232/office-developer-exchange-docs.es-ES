---
title: Cambios (jerarquía)
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
ms.assetid: 918a0d1f-90a5-4eef-9592-07e15bef94e6
description: El elemento Changes contiene una matriz secuenciada de tipos de cambio que representan el tipo de diferencias entre las carpetas en el cliente y las carpetas en el equipo que ejecuta Microsoft Exchange Server 2007.
ms.openlocfilehash: a296d87f23e85d42b4c8c858e92eddfb586a8324
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463275"
---
# <a name="changes-hierarchy"></a><span data-ttu-id="cdbca-103">Cambios (jerarquía)</span><span class="sxs-lookup"><span data-stu-id="cdbca-103">Changes (Hierarchy)</span></span>

<span data-ttu-id="cdbca-104">El elemento **Changes** contiene una matriz secuenciada de tipos de cambio que representan el tipo de diferencias entre las carpetas en el cliente y las carpetas en el equipo que ejecuta Microsoft Exchange Server 2007.</span><span class="sxs-lookup"><span data-stu-id="cdbca-104">The **Changes** element contains a sequenced array of change types that represent the type of differences between the folders on the client and the folders on the computer that is running Microsoft Exchange Server 2007.</span></span> 
  
[<span data-ttu-id="cdbca-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="cdbca-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
  
[<span data-ttu-id="cdbca-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="cdbca-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="cdbca-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="cdbca-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
  
[<span data-ttu-id="cdbca-108">Cambios (jerarquía)</span><span class="sxs-lookup"><span data-stu-id="cdbca-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md)
  
```xml
<Changes>
   <Create/>
   <Update/>
   <Delete/>
</Changes>
```

 <span data-ttu-id="cdbca-109">**SyncFolderHierarchyChangesType**</span><span class="sxs-lookup"><span data-stu-id="cdbca-109">**SyncFolderHierarchyChangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cdbca-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cdbca-110">Attributes and elements</span></span>

<span data-ttu-id="cdbca-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cdbca-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cdbca-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="cdbca-112">Attributes</span></span>

<span data-ttu-id="cdbca-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cdbca-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cdbca-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cdbca-114">Child elements</span></span>

|<span data-ttu-id="cdbca-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cdbca-115">**Element**</span></span>|<span data-ttu-id="cdbca-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cdbca-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cdbca-117">Crear (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="cdbca-117">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="cdbca-118">Identifica una única carpeta que se va a crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="cdbca-118">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="cdbca-119">Actualización (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="cdbca-119">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="cdbca-120">Identifica una única carpeta para actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="cdbca-120">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="cdbca-121">Eliminar (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="cdbca-121">Delete (FolderSync)</span></span>](delete-foldersync.md) <br/> |<span data-ttu-id="cdbca-122">Identifica una única carpeta que se va a eliminar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="cdbca-122">Identifies a single folder to delete in the local client store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cdbca-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cdbca-123">Parent elements</span></span>

|<span data-ttu-id="cdbca-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cdbca-124">**Element**</span></span>|<span data-ttu-id="cdbca-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cdbca-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cdbca-126">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="cdbca-126">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md) <br/> |<span data-ttu-id="cdbca-127">Contiene el estado y el resultado de una solicitud SyncFolderHierarchy.</span><span class="sxs-lookup"><span data-stu-id="cdbca-127">Contains the status and result of a SyncFolderHierarchy request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cdbca-128">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="cdbca-128">Text value</span></span>

<span data-ttu-id="cdbca-129">Se requiere un valor de texto que representa un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="cdbca-129">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cdbca-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cdbca-130">Remarks</span></span>

<span data-ttu-id="cdbca-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo de Exchange 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="cdbca-131">The schema that describes this element is located in the EWS virtual directory of the Exchange 2007 computer that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cdbca-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cdbca-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cdbca-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="cdbca-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cdbca-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cdbca-134">Schema name</span></span>  <br/> |<span data-ttu-id="cdbca-135">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="cdbca-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cdbca-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cdbca-136">Validation file</span></span>  <br/> |<span data-ttu-id="cdbca-137">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="cdbca-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cdbca-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cdbca-138">Can be empty</span></span>  <br/> |<span data-ttu-id="cdbca-139">Falso</span><span class="sxs-lookup"><span data-stu-id="cdbca-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cdbca-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="cdbca-140">See also</span></span>



[<span data-ttu-id="cdbca-141">Operación SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="cdbca-141">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)


[<span data-ttu-id="cdbca-142">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="cdbca-142">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
  
- [<span data-ttu-id="cdbca-143">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="cdbca-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

