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
description: El elemento AlternatePublicFolderItemId describe un identificador de elemento de la carpeta pública para convertir a otro formato de identificador. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 2240f3ff80c2c5b705611c3cf9286faa62d204cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763434"
---
# <a name="alternatepublicfolderitemid"></a><span data-ttu-id="5c578-104">AlternatePublicFolderItemId</span><span class="sxs-lookup"><span data-stu-id="5c578-104">AlternatePublicFolderItemId</span></span>

<span data-ttu-id="5c578-105">El elemento **AlternatePublicFolderItemId** describe un identificador de elemento de la carpeta pública para convertir a otro formato de identificador.</span><span class="sxs-lookup"><span data-stu-id="5c578-105">The **AlternatePublicFolderItemId** element describes a public folder item identifier to convert to another identifier format.</span></span> <span data-ttu-id="5c578-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="5c578-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
- [<span data-ttu-id="5c578-107">ConvertId</span><span class="sxs-lookup"><span data-stu-id="5c578-107">ConvertId</span></span>](convertid.md)
  
- [<span data-ttu-id="5c578-108">SourceIds</span><span class="sxs-lookup"><span data-stu-id="5c578-108">SourceIds</span></span>](sourceids.md)
  
- [<span data-ttu-id="5c578-109">AlternatePublicFolderItemId</span><span class="sxs-lookup"><span data-stu-id="5c578-109">AlternatePublicFolderItemId</span></span>](alternatepublicfolderitemid.md)
  
```xml
<AlternatePublicFolderItemId FolderId="" Format="" ItemId=""/>
```

 <span data-ttu-id="5c578-110">**AlternatePublicFolderItemIdType**</span><span class="sxs-lookup"><span data-stu-id="5c578-110">**AlternatePublicFolderItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5c578-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5c578-111">Attributes and elements</span></span>

<span data-ttu-id="5c578-112">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5c578-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5c578-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="5c578-113">Attributes</span></span>

|<span data-ttu-id="5c578-114">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="5c578-114">**Attribute**</span></span>|<span data-ttu-id="5c578-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5c578-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5c578-116">FolderId</span><span class="sxs-lookup"><span data-stu-id="5c578-116">FolderId</span></span>  <br/> |<span data-ttu-id="5c578-117">Identifica la carpeta pública que contiene el elemento de la carpeta pública.</span><span class="sxs-lookup"><span data-stu-id="5c578-117">Identifies the public folder that contains the public folder item.</span></span> <span data-ttu-id="5c578-118">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="5c578-118">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="5c578-119">Format</span><span class="sxs-lookup"><span data-stu-id="5c578-119">Format</span></span>  <br/> |<span data-ttu-id="5c578-120">Identifica el formato que se describe el identificador de elemento de la carpeta pública para convertir.</span><span class="sxs-lookup"><span data-stu-id="5c578-120">Identifies the format that describes the public folder item identifier to convert.</span></span> <span data-ttu-id="5c578-121">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="5c578-121">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="5c578-122">ItemId</span><span class="sxs-lookup"><span data-stu-id="5c578-122">ItemId</span></span>  <br/> |<span data-ttu-id="5c578-123">Identificador de elemento de carpetas públicas que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="5c578-123">Identifier the public folder item to convert.</span></span> <span data-ttu-id="5c578-124">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="5c578-124">This attribute is required.</span></span>  <br/> |
   
#### <a name="format-attribute-values"></a><span data-ttu-id="5c578-125">Valores de atributos de formato</span><span class="sxs-lookup"><span data-stu-id="5c578-125">Format attribute values</span></span>

|<span data-ttu-id="5c578-126">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5c578-126">**Value**</span></span>|<span data-ttu-id="5c578-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5c578-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5c578-128">EwsLegacyId</span><span class="sxs-lookup"><span data-stu-id="5c578-128">EwsLegacyId</span></span>  <br/> |<span data-ttu-id="5c578-129">Describe identificadores producidos por servicios Web de Exchange en la versión inicial de Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="5c578-129">Describes identifiers that are produced by Exchange Web Services in the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="5c578-130">EwsId</span><span class="sxs-lookup"><span data-stu-id="5c578-130">EwsId</span></span>  <br/> |<span data-ttu-id="5c578-131">Describe identificadores producidos por los servicios Web Exchange comenzando con Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="5c578-131">Describes identifiers that are produced by Exchange Web Services starting with Exchange 2007 SP1.</span></span>  <br/> |
|<span data-ttu-id="5c578-132">Propiedad EntryId</span><span class="sxs-lookup"><span data-stu-id="5c578-132">EntryId</span></span>  <br/> |<span data-ttu-id="5c578-133">Describe identificadores de MAPI, como se muestra en la propiedad de entrada del objeto.</span><span class="sxs-lookup"><span data-stu-id="5c578-133">Describes MAPI identifiers, as in the PR_ENTRYID property.</span></span>  <br/> |
|<span data-ttu-id="5c578-134">HexEntryId</span><span class="sxs-lookup"><span data-stu-id="5c578-134">HexEntryId</span></span>  <br/> |<span data-ttu-id="5c578-135">Describe una representación codificada en hexadecimal de la propiedad de entrada del objeto.</span><span class="sxs-lookup"><span data-stu-id="5c578-135">Describes a hexadecimal-encoded representation of the PR_ENTRYID property.</span></span> <span data-ttu-id="5c578-136">Éste es el formato de los identificadores de eventos de calendario de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="5c578-136">This is the format of availability calendar event identifiers.</span></span>  <br/> |
|<span data-ttu-id="5c578-137">StoreId</span><span class="sxs-lookup"><span data-stu-id="5c578-137">StoreId</span></span>  <br/> |<span data-ttu-id="5c578-138">Describe identificadores de almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5c578-138">Describes Exchange store identifiers.</span></span>  <br/> |
|<span data-ttu-id="5c578-139">OwaId</span><span class="sxs-lookup"><span data-stu-id="5c578-139">OwaId</span></span>  <br/> |<span data-ttu-id="5c578-140">Se describe un identificador de Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="5c578-140">Describes an Outlook Web Access identifier.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5c578-141">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5c578-141">Child elements</span></span>

<span data-ttu-id="5c578-142">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5c578-142">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5c578-143">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5c578-143">Parent elements</span></span>

|<span data-ttu-id="5c578-144">**Element**</span><span class="sxs-lookup"><span data-stu-id="5c578-144">**Element**</span></span>|<span data-ttu-id="5c578-145">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5c578-145">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5c578-146">SourceIds</span><span class="sxs-lookup"><span data-stu-id="5c578-146">SourceIds</span></span>](sourceids.md) <br/> |<span data-ttu-id="5c578-147">Contiene los identificadores de origen para convertir.</span><span class="sxs-lookup"><span data-stu-id="5c578-147">Contains the source identifiers to convert.</span></span> <span data-ttu-id="5c578-148">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="5c578-148">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c578-149">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5c578-149">Remarks</span></span>

<span data-ttu-id="5c578-150">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="5c578-150">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5c578-151">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5c578-151">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c578-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5c578-152">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5c578-153">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5c578-153">Schema Name</span></span>  <br/> |<span data-ttu-id="5c578-154">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5c578-154">Types schema</span></span>  <br/> |
|<span data-ttu-id="5c578-155">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5c578-155">Validation File</span></span>  <br/> |<span data-ttu-id="5c578-156">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5c578-156">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5c578-157">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5c578-157">Can be Empty</span></span>  <br/> |<span data-ttu-id="5c578-158">Verdadero</span><span class="sxs-lookup"><span data-stu-id="5c578-158">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5c578-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c578-159">See also</span></span>

- [<span data-ttu-id="5c578-160">Operación ConvertId</span><span class="sxs-lookup"><span data-stu-id="5c578-160">ConvertId operation</span></span>](convertid-operation.md)
- [<span data-ttu-id="5c578-161">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="5c578-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="5c578-162">Convertir identificadores</span><span class="sxs-lookup"><span data-stu-id="5c578-162">Converting Identifiers</span></span>](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

