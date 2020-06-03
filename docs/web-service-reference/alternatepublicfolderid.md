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
description: El elemento AlternatePublicFolderId describe un identificador de carpeta pública para convertir a otro formato de identificador. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 54ad663117839222ea1174cd1c25600f31aa6b43
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464801"
---
# <a name="alternatepublicfolderid"></a><span data-ttu-id="63a4f-104">AlternatePublicFolderId</span><span class="sxs-lookup"><span data-stu-id="63a4f-104">AlternatePublicFolderId</span></span>

<span data-ttu-id="63a4f-105">El elemento **AlternatePublicFolderId** describe un identificador de carpeta pública para convertir a otro formato de identificador.</span><span class="sxs-lookup"><span data-stu-id="63a4f-105">The **AlternatePublicFolderId** element describes a public folder identifier to convert to another identifier format.</span></span> <span data-ttu-id="63a4f-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="63a4f-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
- [<span data-ttu-id="63a4f-107">ConvertId</span><span class="sxs-lookup"><span data-stu-id="63a4f-107">ConvertId</span></span>](convertid.md)
  
- [<span data-ttu-id="63a4f-108">SourceIds</span><span class="sxs-lookup"><span data-stu-id="63a4f-108">SourceIds</span></span>](sourceids.md)
  
- [<span data-ttu-id="63a4f-109">AlternatePublicFolderId</span><span class="sxs-lookup"><span data-stu-id="63a4f-109">AlternatePublicFolderId</span></span>](alternatepublicfolderid.md)
  
```xml
<AlternatePublicFolderId FolderId="" Format="" />
```

 <span data-ttu-id="63a4f-110">**AlternatePublicFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="63a4f-110">**AlternatePublicFolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="63a4f-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="63a4f-111">Attributes and elements</span></span>

<span data-ttu-id="63a4f-112">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="63a4f-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="63a4f-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="63a4f-113">Attributes</span></span>

|<span data-ttu-id="63a4f-114">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="63a4f-114">**Attribute**</span></span>|<span data-ttu-id="63a4f-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="63a4f-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="63a4f-116">FolderId</span><span class="sxs-lookup"><span data-stu-id="63a4f-116">FolderId</span></span>  <br/> |<span data-ttu-id="63a4f-117">Contiene el identificador de la carpeta pública que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="63a4f-117">Contains the public folder identifier to convert.</span></span> <span data-ttu-id="63a4f-118">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="63a4f-118">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="63a4f-119">Formato</span><span class="sxs-lookup"><span data-stu-id="63a4f-119">Format</span></span>  <br/> |<span data-ttu-id="63a4f-120">Identifica el formato que describe el identificador de carpeta pública que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="63a4f-120">Identifies the format that describes the public folder identifier to convert.</span></span> <span data-ttu-id="63a4f-121">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="63a4f-121">This attribute is required.</span></span>  <br/> |
   
#### <a name="format-attribute"></a><span data-ttu-id="63a4f-122">Atributo Format</span><span class="sxs-lookup"><span data-stu-id="63a4f-122">Format attribute</span></span>

|<span data-ttu-id="63a4f-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="63a4f-123">**Value**</span></span>|<span data-ttu-id="63a4f-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="63a4f-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="63a4f-125">EwsLegacyId</span><span class="sxs-lookup"><span data-stu-id="63a4f-125">EwsLegacyId</span></span>  <br/> |<span data-ttu-id="63a4f-126">Describe los identificadores producidos por los servicios Web de Exchange en la versión de lanzamiento inicial de Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="63a4f-126">Describes identifiers that are produced by Exchange Web Services in the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="63a4f-127">EwsId</span><span class="sxs-lookup"><span data-stu-id="63a4f-127">EwsId</span></span>  <br/> |<span data-ttu-id="63a4f-128">Describe los identificadores que crean los servicios Web de Exchange a partir de Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="63a4f-128">Describes identifiers that are produced by Exchange Web Services starting with Exchange 2007 SP1.</span></span>  <br/> |
|<span data-ttu-id="63a4f-129">EntryId</span><span class="sxs-lookup"><span data-stu-id="63a4f-129">EntryId</span></span>  <br/> |<span data-ttu-id="63a4f-130">Describe los identificadores de MAPI, como en la propiedad PR_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="63a4f-130">Describes MAPI identifiers, as in the PR_ENTRYID property.</span></span>  <br/> |
|<span data-ttu-id="63a4f-131">HexEntryId</span><span class="sxs-lookup"><span data-stu-id="63a4f-131">HexEntryId</span></span>  <br/> |<span data-ttu-id="63a4f-132">Describe una representación codificada en hexadecimal de la propiedad PR_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="63a4f-132">Describes a hexadecimal-encoded representation of the PR_ENTRYID property.</span></span> <span data-ttu-id="63a4f-133">Este es el formato de los identificadores de evento de calendario de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="63a4f-133">This is the format of availability calendar event identifiers.</span></span>  <br/> |
|<span data-ttu-id="63a4f-134">StoreId</span><span class="sxs-lookup"><span data-stu-id="63a4f-134">StoreId</span></span>  <br/> |<span data-ttu-id="63a4f-135">Describe los identificadores de almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="63a4f-135">Describes Exchange store identifiers.</span></span>  <br/> |
|<span data-ttu-id="63a4f-136">OwaId</span><span class="sxs-lookup"><span data-stu-id="63a4f-136">OwaId</span></span>  <br/> |<span data-ttu-id="63a4f-137">Describe un identificador de Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="63a4f-137">Describes an Outlook Web Access identifier.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="63a4f-138">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="63a4f-138">Child elements</span></span>

<span data-ttu-id="63a4f-139">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="63a4f-139">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="63a4f-140">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="63a4f-140">Parent elements</span></span>

|<span data-ttu-id="63a4f-141">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="63a4f-141">**Element**</span></span>|<span data-ttu-id="63a4f-142">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="63a4f-142">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="63a4f-143">SourceIds</span><span class="sxs-lookup"><span data-stu-id="63a4f-143">SourceIds</span></span>](sourceids.md) <br/> |<span data-ttu-id="63a4f-144">Contiene los identificadores de origen que se van a convertir.</span><span class="sxs-lookup"><span data-stu-id="63a4f-144">Contains the source identifiers to convert.</span></span> <span data-ttu-id="63a4f-145">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="63a4f-145">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="63a4f-146">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="63a4f-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63a4f-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="63a4f-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="63a4f-148">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="63a4f-148">Schema Name</span></span>  <br/> |<span data-ttu-id="63a4f-149">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="63a4f-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="63a4f-150">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="63a4f-150">Validation File</span></span>  <br/> |<span data-ttu-id="63a4f-151">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="63a4f-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="63a4f-152">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="63a4f-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="63a4f-153">Verdadero</span><span class="sxs-lookup"><span data-stu-id="63a4f-153">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="63a4f-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="63a4f-154">See also</span></span>

- [<span data-ttu-id="63a4f-155">Operación ConvertId</span><span class="sxs-lookup"><span data-stu-id="63a4f-155">ConvertId operation</span></span>](convertid-operation.md)
- [<span data-ttu-id="63a4f-156">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="63a4f-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="63a4f-157">Convertir identificadores</span><span class="sxs-lookup"><span data-stu-id="63a4f-157">Converting Identifiers</span></span>](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

