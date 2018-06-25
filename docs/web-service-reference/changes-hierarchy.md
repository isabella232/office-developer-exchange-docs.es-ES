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
description: El elemento de cambios contiene una matriz de tipos de cambio que representan el tipo de las diferencias entre las carpetas en el cliente y las carpetas en el equipo que ejecuta Microsoft Exchange Server 2007 secuenciada.
ms.openlocfilehash: 15e4f9f37c5e4a4083260dcf379a49beb2260030
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763739"
---
# <a name="changes-hierarchy"></a><span data-ttu-id="697cf-103">Cambios (jerarquía)</span><span class="sxs-lookup"><span data-stu-id="697cf-103">Changes (Hierarchy)</span></span>

<span data-ttu-id="697cf-104">El elemento de **cambios** contiene una matriz de tipos de cambio que representan el tipo de las diferencias entre las carpetas en el cliente y las carpetas en el equipo que ejecuta Microsoft Exchange Server 2007 secuenciada.</span><span class="sxs-lookup"><span data-stu-id="697cf-104">The **Changes** element contains a sequenced array of change types that represent the type of differences between the folders on the client and the folders on the computer that is running Microsoft Exchange Server 2007.</span></span> 
  
[<span data-ttu-id="697cf-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="697cf-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
  
[<span data-ttu-id="697cf-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="697cf-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="697cf-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="697cf-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
  
[<span data-ttu-id="697cf-108">Cambios (jerarquía)</span><span class="sxs-lookup"><span data-stu-id="697cf-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md)
  
```xml
<Changes>
   <Create/>
   <Update/>
   <Delete/>
</Changes>
```

 <span data-ttu-id="697cf-109">**SyncFolderHierarchyChangesType**</span><span class="sxs-lookup"><span data-stu-id="697cf-109">**SyncFolderHierarchyChangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="697cf-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="697cf-110">Attributes and elements</span></span>

<span data-ttu-id="697cf-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="697cf-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="697cf-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="697cf-112">Attributes</span></span>

<span data-ttu-id="697cf-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="697cf-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="697cf-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="697cf-114">Child elements</span></span>

|<span data-ttu-id="697cf-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="697cf-115">**Element**</span></span>|<span data-ttu-id="697cf-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="697cf-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="697cf-117">Crear (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="697cf-117">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="697cf-118">Identifica una sola carpeta para crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="697cf-118">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="697cf-119">Actualización (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="697cf-119">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="697cf-120">Identifica una sola carpeta para actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="697cf-120">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="697cf-121">Eliminar (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="697cf-121">Delete (FolderSync)</span></span>](delete-foldersync.md) <br/> |<span data-ttu-id="697cf-122">Identifica una sola carpeta para eliminar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="697cf-122">Identifies a single folder to delete in the local client store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="697cf-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="697cf-123">Parent elements</span></span>

|<span data-ttu-id="697cf-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="697cf-124">**Element**</span></span>|<span data-ttu-id="697cf-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="697cf-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="697cf-126">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="697cf-126">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md) <br/> |<span data-ttu-id="697cf-127">Contiene el estado y el resultado de una solicitud de SyncFolderHierarchy.</span><span class="sxs-lookup"><span data-stu-id="697cf-127">Contains the status and result of a SyncFolderHierarchy request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="697cf-128">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="697cf-128">Text value</span></span>

<span data-ttu-id="697cf-129">Se requiere un valor de texto que representa un valor de tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="697cf-129">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="697cf-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="697cf-130">Remarks</span></span>

<span data-ttu-id="697cf-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo de Exchange 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="697cf-131">The schema that describes this element is located in the EWS virtual directory of the Exchange 2007 computer that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="697cf-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="697cf-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="697cf-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="697cf-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="697cf-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="697cf-134">Schema name</span></span>  <br/> |<span data-ttu-id="697cf-135">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="697cf-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="697cf-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="697cf-136">Validation file</span></span>  <br/> |<span data-ttu-id="697cf-137">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="697cf-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="697cf-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="697cf-138">Can be empty</span></span>  <br/> |<span data-ttu-id="697cf-139">False</span><span class="sxs-lookup"><span data-stu-id="697cf-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="697cf-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="697cf-140">See also</span></span>



[<span data-ttu-id="697cf-141">Operación SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="697cf-141">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)


[<span data-ttu-id="697cf-142">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="697cf-142">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
  
- [<span data-ttu-id="697cf-143">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="697cf-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

