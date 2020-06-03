---
title: ConvertId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConvertId
api_type:
- schema
ms.assetid: 9684c22c-29d4-4f7f-befc-8cd41da56d38
description: El elemento ConvertId define una solicitud para convertir los identificadores de elemento y carpeta entre los formatos de Exchange admitidos. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: d421baf1f29fb59a8c6eb2b09e1fa0e8a38ffaa4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452541"
---
# <a name="convertid"></a><span data-ttu-id="c6fe8-104">ConvertId</span><span class="sxs-lookup"><span data-stu-id="c6fe8-104">ConvertId</span></span>

<span data-ttu-id="c6fe8-105">El elemento **ConvertId** define una solicitud para convertir los identificadores de elemento y carpeta entre los formatos de Exchange admitidos.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-105">The **ConvertId** element defines a request to convert item and folder identifiers between supported Exchange formats.</span></span> <span data-ttu-id="c6fe8-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c6fe8-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ConvertId DestinationFormat="">
   <SourceIds/>
</ConvertId>
```

 <span data-ttu-id="c6fe8-107">**ConvertIdType**</span><span class="sxs-lookup"><span data-stu-id="c6fe8-107">**ConvertIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c6fe8-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c6fe8-108">Attributes and elements</span></span>

<span data-ttu-id="c6fe8-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c6fe8-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="c6fe8-110">Attributes</span></span>

|<span data-ttu-id="c6fe8-111">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c6fe8-111">**Attribute**</span></span>|<span data-ttu-id="c6fe8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c6fe8-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c6fe8-113">**DestinationFormat**</span><span class="sxs-lookup"><span data-stu-id="c6fe8-113">**DestinationFormat**</span></span> <br/> |<span data-ttu-id="c6fe8-114">Describe el formato de identificador que se devolverá para todos los identificadores convertidos.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-114">Describes the identifier format that will be returned for all the converted identifiers.</span></span> <span data-ttu-id="c6fe8-115">La DestinationFormat se describe mediante el IdFormatType.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-115">The DestinationFormat is described by the IdFormatType.</span></span>  <br/> |
   
#### <a name="destinationformat-attribute"></a><span data-ttu-id="c6fe8-116">Atributo DestinationFormat</span><span class="sxs-lookup"><span data-stu-id="c6fe8-116">DestinationFormat Attribute</span></span>

|<span data-ttu-id="c6fe8-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c6fe8-117">**Value**</span></span>|<span data-ttu-id="c6fe8-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c6fe8-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c6fe8-119">**EwsLegacyId**</span><span class="sxs-lookup"><span data-stu-id="c6fe8-119">**EwsLegacyId**</span></span> <br/> |<span data-ttu-id="c6fe8-120">Representa el formato de identificador que se usa para los identificadores de servicios Web de Exchange que se proporcionan en la versión de lanzamiento inicial de Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-120">Represents the identifier format that is used for Exchange Web Services identifiers that are provided in the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="c6fe8-121">**EwsId**</span><span class="sxs-lookup"><span data-stu-id="c6fe8-121">**EwsId**</span></span> <br/> |<span data-ttu-id="c6fe8-122">Representa el formato de identificador que se usa para los identificadores de servicios Web de Exchange que comienzan con Exchange Server 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-122">Represents the identifier format that is used for Exchange Web Services identifiers starting with Exchange Server 2007 SP1.</span></span>  <br/> |
|<span data-ttu-id="c6fe8-123">**EntryId**</span><span class="sxs-lookup"><span data-stu-id="c6fe8-123">**EntryId**</span></span> <br/> |<span data-ttu-id="c6fe8-124">Representa el identificador de MAPI, como en la propiedad PR_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-124">Represents the MAPI identifier, as in the PR_ENTRYID property.</span></span>  <br/> |
|<span data-ttu-id="c6fe8-125">**HexEntryId**</span><span class="sxs-lookup"><span data-stu-id="c6fe8-125">**HexEntryId**</span></span> <br/> |<span data-ttu-id="c6fe8-126">Representa el identificador de evento del calendario de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-126">Represents the availability calendar event identifier.</span></span> <span data-ttu-id="c6fe8-127">Se trata de una representación codificada en hexadecimal de la propiedad PR_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-127">This is a hexadecimal-encoded representation of the PR_ENTRYID property.</span></span>  <br/> |
|<span data-ttu-id="c6fe8-128">**StoreId**</span><span class="sxs-lookup"><span data-stu-id="c6fe8-128">**StoreId**</span></span> <br/> |<span data-ttu-id="c6fe8-129">Representa el identificador del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-129">Represents the Exchange store identifier.</span></span>  <br/> |
|<span data-ttu-id="c6fe8-130">**OwaId**</span><span class="sxs-lookup"><span data-stu-id="c6fe8-130">**OwaId**</span></span> <br/> |<span data-ttu-id="c6fe8-131">Representa el formato de identificador de Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-131">Represents the Outlook Web Access identifier format.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c6fe8-132">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c6fe8-132">Child elements</span></span>

|<span data-ttu-id="c6fe8-133">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c6fe8-133">**Element**</span></span>|<span data-ttu-id="c6fe8-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c6fe8-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c6fe8-135">SourceIds</span><span class="sxs-lookup"><span data-stu-id="c6fe8-135">SourceIds</span></span>](sourceids.md) <br/> |<span data-ttu-id="c6fe8-136">Contiene los identificadores de origen que se van a convertir.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-136">Contains the source identifiers to convert.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c6fe8-137">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c6fe8-137">Parent elements</span></span>

<span data-ttu-id="c6fe8-138">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-138">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c6fe8-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c6fe8-139">Remarks</span></span>

<span data-ttu-id="c6fe8-140">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="c6fe8-140">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c6fe8-141">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c6fe8-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c6fe8-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="c6fe8-142">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c6fe8-143">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c6fe8-143">Schema Name</span></span>  <br/> |<span data-ttu-id="c6fe8-144">esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c6fe8-144">messages schema</span></span>  <br/> |
|<span data-ttu-id="c6fe8-145">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c6fe8-145">Validation File</span></span>  <br/> |<span data-ttu-id="c6fe8-146">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c6fe8-146">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c6fe8-147">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c6fe8-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="c6fe8-148">Falso</span><span class="sxs-lookup"><span data-stu-id="c6fe8-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c6fe8-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6fe8-149">See also</span></span>



[<span data-ttu-id="c6fe8-150">Operación ConvertId</span><span class="sxs-lookup"><span data-stu-id="c6fe8-150">ConvertId operation</span></span>](convertid-operation.md)


- [<span data-ttu-id="c6fe8-151">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c6fe8-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="c6fe8-152">Convertir identificadores</span><span class="sxs-lookup"><span data-stu-id="c6fe8-152">Converting Identifiers</span></span>](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

