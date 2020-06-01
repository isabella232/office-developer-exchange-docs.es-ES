---
title: AlternatePublicFolderItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AlternatePublicFolderItemId
api_type:
- schema
ms.assetid: a67df9b9-8fdb-42de-b9c5-8377b71fa3d9
description: El elemento AlternatePublicFolderItemId describe un identificador de elemento de carpeta pública para convertir a otro formato de identificador. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 11a9fafec78a9bd14e4d98982fd38954d45e4d1a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464773"
---
# <a name="alternatepublicfolderitemid"></a><span data-ttu-id="ebdca-104">AlternatePublicFolderItemId</span><span class="sxs-lookup"><span data-stu-id="ebdca-104">AlternatePublicFolderItemId</span></span>

<span data-ttu-id="ebdca-105">El elemento **AlternatePublicFolderItemId** describe un identificador de elemento de carpeta pública para convertir a otro formato de identificador.</span><span class="sxs-lookup"><span data-stu-id="ebdca-105">The **AlternatePublicFolderItemId** element describes a public folder item identifier to convert to another identifier format.</span></span> <span data-ttu-id="ebdca-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ebdca-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
- [<span data-ttu-id="ebdca-107">ConvertId</span><span class="sxs-lookup"><span data-stu-id="ebdca-107">ConvertId</span></span>](convertid.md)
  
- [<span data-ttu-id="ebdca-108">SourceIds</span><span class="sxs-lookup"><span data-stu-id="ebdca-108">SourceIds</span></span>](sourceids.md)
  
- [<span data-ttu-id="ebdca-109">AlternatePublicFolderItemId</span><span class="sxs-lookup"><span data-stu-id="ebdca-109">AlternatePublicFolderItemId</span></span>](alternatepublicfolderitemid.md)
  
```xml
<AlternatePublicFolderItemId FolderId="" Format="" ItemId=""/>
```

 <span data-ttu-id="ebdca-110">**AlternatePublicFolderItemIdType**</span><span class="sxs-lookup"><span data-stu-id="ebdca-110">**AlternatePublicFolderItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ebdca-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ebdca-111">Attributes and elements</span></span>

<span data-ttu-id="ebdca-112">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ebdca-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ebdca-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="ebdca-113">Attributes</span></span>

|<span data-ttu-id="ebdca-114">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ebdca-114">**Attribute**</span></span>|<span data-ttu-id="ebdca-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ebdca-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ebdca-116">FolderId</span><span class="sxs-lookup"><span data-stu-id="ebdca-116">FolderId</span></span>  <br/> |<span data-ttu-id="ebdca-117">Identifica la carpeta pública que contiene el elemento de carpeta pública.</span><span class="sxs-lookup"><span data-stu-id="ebdca-117">Identifies the public folder that contains the public folder item.</span></span> <span data-ttu-id="ebdca-118">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ebdca-118">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="ebdca-119">Formato</span><span class="sxs-lookup"><span data-stu-id="ebdca-119">Format</span></span>  <br/> |<span data-ttu-id="ebdca-120">Identifica el formato que describe el identificador de elemento de carpeta pública que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="ebdca-120">Identifies the format that describes the public folder item identifier to convert.</span></span> <span data-ttu-id="ebdca-121">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ebdca-121">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="ebdca-122">ItemId</span><span class="sxs-lookup"><span data-stu-id="ebdca-122">ItemId</span></span>  <br/> |<span data-ttu-id="ebdca-123">Identificador el elemento de carpeta pública que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="ebdca-123">Identifier the public folder item to convert.</span></span> <span data-ttu-id="ebdca-124">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ebdca-124">This attribute is required.</span></span>  <br/> |
   
#### <a name="format-attribute-values"></a><span data-ttu-id="ebdca-125">Valores de atributo de formato</span><span class="sxs-lookup"><span data-stu-id="ebdca-125">Format attribute values</span></span>

|<span data-ttu-id="ebdca-126">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ebdca-126">**Value**</span></span>|<span data-ttu-id="ebdca-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ebdca-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ebdca-128">EwsLegacyId</span><span class="sxs-lookup"><span data-stu-id="ebdca-128">EwsLegacyId</span></span>  <br/> |<span data-ttu-id="ebdca-129">Describe los identificadores producidos por los servicios Web de Exchange en la versión de lanzamiento inicial de Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="ebdca-129">Describes identifiers that are produced by Exchange Web Services in the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="ebdca-130">EwsId</span><span class="sxs-lookup"><span data-stu-id="ebdca-130">EwsId</span></span>  <br/> |<span data-ttu-id="ebdca-131">Describe los identificadores que crean los servicios Web de Exchange a partir de Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="ebdca-131">Describes identifiers that are produced by Exchange Web Services starting with Exchange 2007 SP1.</span></span>  <br/> |
|<span data-ttu-id="ebdca-132">EntryId</span><span class="sxs-lookup"><span data-stu-id="ebdca-132">EntryId</span></span>  <br/> |<span data-ttu-id="ebdca-133">Describe los identificadores de MAPI, como en la propiedad PR_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="ebdca-133">Describes MAPI identifiers, as in the PR_ENTRYID property.</span></span>  <br/> |
|<span data-ttu-id="ebdca-134">HexEntryId</span><span class="sxs-lookup"><span data-stu-id="ebdca-134">HexEntryId</span></span>  <br/> |<span data-ttu-id="ebdca-135">Describe una representación codificada en hexadecimal de la propiedad PR_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="ebdca-135">Describes a hexadecimal-encoded representation of the PR_ENTRYID property.</span></span> <span data-ttu-id="ebdca-136">Este es el formato de los identificadores de evento de calendario de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="ebdca-136">This is the format of availability calendar event identifiers.</span></span>  <br/> |
|<span data-ttu-id="ebdca-137">StoreId</span><span class="sxs-lookup"><span data-stu-id="ebdca-137">StoreId</span></span>  <br/> |<span data-ttu-id="ebdca-138">Describe los identificadores de almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ebdca-138">Describes Exchange store identifiers.</span></span>  <br/> |
|<span data-ttu-id="ebdca-139">OwaId</span><span class="sxs-lookup"><span data-stu-id="ebdca-139">OwaId</span></span>  <br/> |<span data-ttu-id="ebdca-140">Describe un identificador de Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="ebdca-140">Describes an Outlook Web Access identifier.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ebdca-141">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ebdca-141">Child elements</span></span>

<span data-ttu-id="ebdca-142">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ebdca-142">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ebdca-143">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ebdca-143">Parent elements</span></span>

|<span data-ttu-id="ebdca-144">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ebdca-144">**Element**</span></span>|<span data-ttu-id="ebdca-145">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ebdca-145">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ebdca-146">SourceIds</span><span class="sxs-lookup"><span data-stu-id="ebdca-146">SourceIds</span></span>](sourceids.md) <br/> |<span data-ttu-id="ebdca-147">Contiene los identificadores de origen que se van a convertir.</span><span class="sxs-lookup"><span data-stu-id="ebdca-147">Contains the source identifiers to convert.</span></span> <span data-ttu-id="ebdca-148">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="ebdca-148">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ebdca-149">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ebdca-149">Remarks</span></span>

<span data-ttu-id="ebdca-150">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="ebdca-150">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ebdca-151">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ebdca-151">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ebdca-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="ebdca-152">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ebdca-153">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ebdca-153">Schema Name</span></span>  <br/> |<span data-ttu-id="ebdca-154">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ebdca-154">Types schema</span></span>  <br/> |
|<span data-ttu-id="ebdca-155">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ebdca-155">Validation File</span></span>  <br/> |<span data-ttu-id="ebdca-156">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ebdca-156">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ebdca-157">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ebdca-157">Can be Empty</span></span>  <br/> |<span data-ttu-id="ebdca-158">Verdadero</span><span class="sxs-lookup"><span data-stu-id="ebdca-158">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ebdca-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="ebdca-159">See also</span></span>

- [<span data-ttu-id="ebdca-160">Operación ConvertId</span><span class="sxs-lookup"><span data-stu-id="ebdca-160">ConvertId operation</span></span>](convertid-operation.md)
- [<span data-ttu-id="ebdca-161">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ebdca-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="ebdca-162">Convertir identificadores</span><span class="sxs-lookup"><span data-stu-id="ebdca-162">Converting Identifiers</span></span>](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

