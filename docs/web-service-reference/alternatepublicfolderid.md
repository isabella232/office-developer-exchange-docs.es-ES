---
title: AlternatePublicFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AlternatePublicFolderId
api_type:
- schema
ms.assetid: 0a4dc1cc-959e-4b93-aa3a-3020ca8b8a02
description: El elemento AlternatePublicFolderId describe un identificador de la carpeta pública para convertir a otro formato de identificador. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 32e6e75eb381e479baf5fdb5ad0a40b32c1b02a9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763435"
---
# <a name="alternatepublicfolderid"></a><span data-ttu-id="58d66-104">AlternatePublicFolderId</span><span class="sxs-lookup"><span data-stu-id="58d66-104">AlternatePublicFolderId</span></span>

<span data-ttu-id="58d66-105">El elemento **AlternatePublicFolderId** describe un identificador de la carpeta pública para convertir a otro formato de identificador.</span><span class="sxs-lookup"><span data-stu-id="58d66-105">The **AlternatePublicFolderId** element describes a public folder identifier to convert to another identifier format.</span></span> <span data-ttu-id="58d66-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="58d66-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
- [<span data-ttu-id="58d66-107">ConvertId</span><span class="sxs-lookup"><span data-stu-id="58d66-107">ConvertId</span></span>](convertid.md)
  
- [<span data-ttu-id="58d66-108">SourceIds</span><span class="sxs-lookup"><span data-stu-id="58d66-108">SourceIds</span></span>](sourceids.md)
  
- [<span data-ttu-id="58d66-109">AlternatePublicFolderId</span><span class="sxs-lookup"><span data-stu-id="58d66-109">AlternatePublicFolderId</span></span>](alternatepublicfolderid.md)
  
```xml
<AlternatePublicFolderId FolderId="" Format="" />
```

 <span data-ttu-id="58d66-110">**AlternatePublicFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="58d66-110">**AlternatePublicFolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="58d66-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="58d66-111">Attributes and elements</span></span>

<span data-ttu-id="58d66-112">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="58d66-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="58d66-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="58d66-113">Attributes</span></span>

|<span data-ttu-id="58d66-114">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="58d66-114">**Attribute**</span></span>|<span data-ttu-id="58d66-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="58d66-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="58d66-116">FolderId</span><span class="sxs-lookup"><span data-stu-id="58d66-116">FolderId</span></span>  <br/> |<span data-ttu-id="58d66-117">Contiene el identificador de la carpeta pública para convertir.</span><span class="sxs-lookup"><span data-stu-id="58d66-117">Contains the public folder identifier to convert.</span></span> <span data-ttu-id="58d66-118">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="58d66-118">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="58d66-119">Format</span><span class="sxs-lookup"><span data-stu-id="58d66-119">Format</span></span>  <br/> |<span data-ttu-id="58d66-120">Identifica el formato que describe el identificador de carpeta pública para convertir.</span><span class="sxs-lookup"><span data-stu-id="58d66-120">Identifies the format that describes the public folder identifier to convert.</span></span> <span data-ttu-id="58d66-121">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="58d66-121">This attribute is required.</span></span>  <br/> |
   
#### <a name="format-attribute"></a><span data-ttu-id="58d66-122">Atributo de formato</span><span class="sxs-lookup"><span data-stu-id="58d66-122">Format attribute</span></span>

|<span data-ttu-id="58d66-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="58d66-123">**Value**</span></span>|<span data-ttu-id="58d66-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="58d66-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="58d66-125">EwsLegacyId</span><span class="sxs-lookup"><span data-stu-id="58d66-125">EwsLegacyId</span></span>  <br/> |<span data-ttu-id="58d66-126">Describe identificadores producidos por servicios Web de Exchange en la versión inicial de Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="58d66-126">Describes identifiers that are produced by Exchange Web Services in the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="58d66-127">EwsId</span><span class="sxs-lookup"><span data-stu-id="58d66-127">EwsId</span></span>  <br/> |<span data-ttu-id="58d66-128">Describe identificadores producidos por los servicios Web Exchange comenzando con Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="58d66-128">Describes identifiers that are produced by Exchange Web Services starting with Exchange 2007 SP1.</span></span>  <br/> |
|<span data-ttu-id="58d66-129">Propiedad EntryId</span><span class="sxs-lookup"><span data-stu-id="58d66-129">EntryId</span></span>  <br/> |<span data-ttu-id="58d66-130">Describe identificadores de MAPI, como se muestra en la propiedad de entrada del objeto.</span><span class="sxs-lookup"><span data-stu-id="58d66-130">Describes MAPI identifiers, as in the PR_ENTRYID property.</span></span>  <br/> |
|<span data-ttu-id="58d66-131">HexEntryId</span><span class="sxs-lookup"><span data-stu-id="58d66-131">HexEntryId</span></span>  <br/> |<span data-ttu-id="58d66-132">Describe una representación codificada en hexadecimal de la propiedad de entrada del objeto.</span><span class="sxs-lookup"><span data-stu-id="58d66-132">Describes a hexadecimal-encoded representation of the PR_ENTRYID property.</span></span> <span data-ttu-id="58d66-133">Éste es el formato de los identificadores de eventos de calendario de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="58d66-133">This is the format of availability calendar event identifiers.</span></span>  <br/> |
|<span data-ttu-id="58d66-134">StoreId</span><span class="sxs-lookup"><span data-stu-id="58d66-134">StoreId</span></span>  <br/> |<span data-ttu-id="58d66-135">Describe identificadores de almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="58d66-135">Describes Exchange store identifiers.</span></span>  <br/> |
|<span data-ttu-id="58d66-136">OwaId</span><span class="sxs-lookup"><span data-stu-id="58d66-136">OwaId</span></span>  <br/> |<span data-ttu-id="58d66-137">Se describe un identificador de Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="58d66-137">Describes an Outlook Web Access identifier.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="58d66-138">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="58d66-138">Child elements</span></span>

<span data-ttu-id="58d66-139">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="58d66-139">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="58d66-140">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="58d66-140">Parent elements</span></span>

|<span data-ttu-id="58d66-141">**Element**</span><span class="sxs-lookup"><span data-stu-id="58d66-141">**Element**</span></span>|<span data-ttu-id="58d66-142">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="58d66-142">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="58d66-143">SourceIds</span><span class="sxs-lookup"><span data-stu-id="58d66-143">SourceIds</span></span>](sourceids.md) <br/> |<span data-ttu-id="58d66-144">Contiene los identificadores de origen para convertir.</span><span class="sxs-lookup"><span data-stu-id="58d66-144">Contains the source identifiers to convert.</span></span> <span data-ttu-id="58d66-145">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="58d66-145">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="58d66-146">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="58d66-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58d66-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="58d66-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="58d66-148">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="58d66-148">Schema Name</span></span>  <br/> |<span data-ttu-id="58d66-149">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="58d66-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="58d66-150">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="58d66-150">Validation File</span></span>  <br/> |<span data-ttu-id="58d66-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="58d66-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="58d66-152">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="58d66-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="58d66-153">Verdadero</span><span class="sxs-lookup"><span data-stu-id="58d66-153">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="58d66-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="58d66-154">See also</span></span>

- [<span data-ttu-id="58d66-155">Operación ConvertId</span><span class="sxs-lookup"><span data-stu-id="58d66-155">ConvertId operation</span></span>](convertid-operation.md)
- [<span data-ttu-id="58d66-156">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="58d66-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="58d66-157">Convertir identificadores</span><span class="sxs-lookup"><span data-stu-id="58d66-157">Converting Identifiers</span></span>](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

