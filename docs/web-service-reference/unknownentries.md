---
title: UnknownEntries
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnknownEntries
api_type:
- schema
ms.assetid: 107ec73e-083a-4956-9d37-33d4734cc157
description: El elemento UnknownEntries contiene una matriz de las entradas de permiso desconocido que no se puede resolver con el servicio de directorio de Active Directory. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 306e5f226a56694bb1ff32362f77e7dff80865ad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840784"
---
# <a name="unknownentries"></a><span data-ttu-id="ba226-104">UnknownEntries</span><span class="sxs-lookup"><span data-stu-id="ba226-104">UnknownEntries</span></span>

<span data-ttu-id="ba226-105">El elemento **UnknownEntries** contiene una matriz de las entradas de permiso desconocido que no se puede resolver con el servicio de directorio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ba226-105">The **UnknownEntries** element contains an array of unknown permission entries that cannot be resolved against the Active Directory directory service.</span></span> <span data-ttu-id="ba226-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ba226-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<UnknownEntries>
   <UnknownEntry/>
</UnknownEntries>
```

 <span data-ttu-id="ba226-107">**ArrayOfUnknownEntriesType**</span><span class="sxs-lookup"><span data-stu-id="ba226-107">**ArrayOfUnknownEntriesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ba226-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ba226-108">Attributes and elements</span></span>

<span data-ttu-id="ba226-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ba226-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba226-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="ba226-110">Attributes</span></span>

<span data-ttu-id="ba226-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ba226-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ba226-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ba226-112">Child elements</span></span>

|<span data-ttu-id="ba226-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ba226-113">**Element**</span></span>|<span data-ttu-id="ba226-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ba226-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba226-115">UnknownEntry</span><span class="sxs-lookup"><span data-stu-id="ba226-115">UnknownEntry</span></span>](unknownentry.md) <br/> |<span data-ttu-id="ba226-116">Representa una entrada de permiso desconocido único que no se puede resolver en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ba226-116">Represents a single unknown permission entry that cannot be resolved against Active Directory.</span></span> <span data-ttu-id="ba226-117">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="ba226-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ba226-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ba226-118">Parent elements</span></span>

|<span data-ttu-id="ba226-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="ba226-119">**Element**</span></span>|<span data-ttu-id="ba226-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ba226-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba226-121">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="ba226-121">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="ba226-122">Contiene todos los permisos que están configurados para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="ba226-122">Contains all the permissions that are configured for a folder.</span></span> <span data-ttu-id="ba226-123">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="ba226-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="ba226-124">PermissionSet (CalendarPermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="ba226-124">PermissionSet (CalendarPermissionSetType)</span></span>](permissionset-calendarpermissionsettype.md) <br/> |<span data-ttu-id="ba226-125">Contiene todos los permisos que están configurados para una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="ba226-125">Contains all the permissions that are configured for a calendar folder.</span></span> <span data-ttu-id="ba226-126">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="ba226-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba226-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ba226-127">Remarks</span></span>

<span data-ttu-id="ba226-128">Puede eliminar entradas desconocidas de una carpeta mediante el uso de la operación UpdateFolder con el elemento [SetFolderField](setfolderfield.md) .</span><span class="sxs-lookup"><span data-stu-id="ba226-128">You can delete unknown entries from a folder by using the UpdateFolder operation with the [SetFolderField](setfolderfield.md) element.</span></span> <span data-ttu-id="ba226-129">Cuando se restablece el conjunto de permisos mediante la opción SetFolderField de la operación UpdateFolder, se eliminan las entradas desconocidas.</span><span class="sxs-lookup"><span data-stu-id="ba226-129">The unknown entries are deleted when you reset the PermissionSet by using the SetFolderField option of the UpdateFolder operation.</span></span> <span data-ttu-id="ba226-130">Servicios Web de Exchange no es compatible con la eliminación de entradas individuales.</span><span class="sxs-lookup"><span data-stu-id="ba226-130">Exchange Web Services does not support the deletion of individual entries.</span></span> 
  
<span data-ttu-id="ba226-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="ba226-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba226-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ba226-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba226-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ba226-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ba226-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ba226-134">Schema Name</span></span>  <br/> |<span data-ttu-id="ba226-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ba226-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="ba226-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ba226-136">Validation File</span></span>  <br/> |<span data-ttu-id="ba226-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ba226-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ba226-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ba226-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="ba226-139">False</span><span class="sxs-lookup"><span data-stu-id="ba226-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba226-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba226-140">See also</span></span>



[<span data-ttu-id="ba226-141">Operación UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="ba226-141">UpdateFolder operation</span></span>](updatefolder-operation.md)


- [<span data-ttu-id="ba226-142">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="ba226-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="ba226-143">Establecimiento de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="ba226-143">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

