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
description: El elemento ConvertId define una solicitud para convertir los identificadores de elemento y carpeta entre formatos compatibles con Exchange. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 956f6464fd9013f9e72d2915f21c3b011d0add5b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763883"
---
# <a name="convertid"></a><span data-ttu-id="4d9f9-104">ConvertId</span><span class="sxs-lookup"><span data-stu-id="4d9f9-104">ConvertId</span></span>

<span data-ttu-id="4d9f9-105">El elemento **ConvertId** define una solicitud para convertir los identificadores de elemento y carpeta entre formatos compatibles con Exchange.</span><span class="sxs-lookup"><span data-stu-id="4d9f9-105">The **ConvertId** element defines a request to convert item and folder identifiers between supported Exchange formats.</span></span> <span data-ttu-id="4d9f9-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4d9f9-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ConvertId DestinationFormat="">
   <SourceIds/>
</ConvertId>
```

 <span data-ttu-id="4d9f9-107">**ConvertIdType**</span><span class="sxs-lookup"><span data-stu-id="4d9f9-107">**ConvertIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4d9f9-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4d9f9-108">Attributes and elements</span></span>

<span data-ttu-id="4d9f9-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4d9f9-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4d9f9-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="4d9f9-110">Attributes</span></span>

|<span data-ttu-id="4d9f9-111">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="4d9f9-111">**Attribute**</span></span>|<span data-ttu-id="4d9f9-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4d9f9-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4d9f9-113">**DestinationFormat**</span><span class="sxs-lookup"><span data-stu-id="4d9f9-113">**DestinationFormat**</span></span> <br/> |<span data-ttu-id="4d9f9-114">Describe el formato de identificador que se devolverán para todos los identificadores de convertidos.</span><span class="sxs-lookup"><span data-stu-id="4d9f9-114">Describes the identifier format that will be returned for all the converted identifiers.</span></span> <span data-ttu-id="4d9f9-115">Se describe la DestinationFormat por la IdFormatType.</span><span class="sxs-lookup"><span data-stu-id="4d9f9-115">The DestinationFormat is described by the IdFormatType.</span></span>  <br/> |
   
#### <a name="destinationformat-attribute"></a><span data-ttu-id="4d9f9-116">Atributo DestinationFormat</span><span class="sxs-lookup"><span data-stu-id="4d9f9-116">DestinationFormat Attribute</span></span>

|<span data-ttu-id="4d9f9-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4d9f9-117">**Value**</span></span>|<span data-ttu-id="4d9f9-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4d9f9-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4d9f9-119">**EwsLegacyId**</span><span class="sxs-lookup"><span data-stu-id="4d9f9-119">**EwsLegacyId**</span></span> <br/> |<span data-ttu-id="4d9f9-120">Representa el formato de identificador que se usa para los identificadores de servicios Web de Exchange que se proporcionan en la versión inicial de Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="4d9f9-120">Represents the identifier format that is used for Exchange Web Services identifiers that are provided in the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="4d9f9-121">**EwsId**</span><span class="sxs-lookup"><span data-stu-id="4d9f9-121">**EwsId**</span></span> <br/> |<span data-ttu-id="4d9f9-122">Representa el formato de identificador que se usa para los identificadores de los servicios Web Exchange empezando con Exchange Server 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="4d9f9-122">Represents the identifier format that is used for Exchange Web Services identifiers starting with Exchange Server 2007 SP1.</span></span>  <br/> |
|<span data-ttu-id="4d9f9-123">**Propiedad EntryId**</span><span class="sxs-lookup"><span data-stu-id="4d9f9-123">**EntryId**</span></span> <br/> |<span data-ttu-id="4d9f9-124">Representa el identificador MAPI, como se muestra en la propiedad de entrada del objeto.</span><span class="sxs-lookup"><span data-stu-id="4d9f9-124">Represents the MAPI identifier, as in the PR_ENTRYID property.</span></span>  <br/> |
|<span data-ttu-id="4d9f9-125">**HexEntryId**</span><span class="sxs-lookup"><span data-stu-id="4d9f9-125">**HexEntryId**</span></span> <br/> |<span data-ttu-id="4d9f9-126">Representa el identificador de evento del calendario de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="4d9f9-126">Represents the availability calendar event identifier.</span></span> <span data-ttu-id="4d9f9-127">Ésta es una representación codificada en hexadecimal de la propiedad de entrada del objeto.</span><span class="sxs-lookup"><span data-stu-id="4d9f9-127">This is a hexadecimal-encoded representation of the PR_ENTRYID property.</span></span>  <br/> |
|<span data-ttu-id="4d9f9-128">**StoreId**</span><span class="sxs-lookup"><span data-stu-id="4d9f9-128">**StoreId**</span></span> <br/> |<span data-ttu-id="4d9f9-129">Representa el identificador de almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4d9f9-129">Represents the Exchange store identifier.</span></span>  <br/> |
|<span data-ttu-id="4d9f9-130">**OwaId**</span><span class="sxs-lookup"><span data-stu-id="4d9f9-130">**OwaId**</span></span> <br/> |<span data-ttu-id="4d9f9-131">Representa el formato de identificador de Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="4d9f9-131">Represents the Outlook Web Access identifier format.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4d9f9-132">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4d9f9-132">Child elements</span></span>

|<span data-ttu-id="4d9f9-133">**Element**</span><span class="sxs-lookup"><span data-stu-id="4d9f9-133">**Element**</span></span>|<span data-ttu-id="4d9f9-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4d9f9-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4d9f9-135">SourceIds</span><span class="sxs-lookup"><span data-stu-id="4d9f9-135">SourceIds</span></span>](sourceids.md) <br/> |<span data-ttu-id="4d9f9-136">Contiene los identificadores de origen para convertir.</span><span class="sxs-lookup"><span data-stu-id="4d9f9-136">Contains the source identifiers to convert.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4d9f9-137">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4d9f9-137">Parent elements</span></span>

<span data-ttu-id="4d9f9-138">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4d9f9-138">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4d9f9-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4d9f9-139">Remarks</span></span>

<span data-ttu-id="4d9f9-140">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4d9f9-140">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4d9f9-141">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4d9f9-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4d9f9-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4d9f9-142">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4d9f9-143">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4d9f9-143">Schema Name</span></span>  <br/> |<span data-ttu-id="4d9f9-144">esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="4d9f9-144">messages schema</span></span>  <br/> |
|<span data-ttu-id="4d9f9-145">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4d9f9-145">Validation File</span></span>  <br/> |<span data-ttu-id="4d9f9-146">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4d9f9-146">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4d9f9-147">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4d9f9-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="4d9f9-148">False</span><span class="sxs-lookup"><span data-stu-id="4d9f9-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4d9f9-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d9f9-149">See also</span></span>



[<span data-ttu-id="4d9f9-150">Operación ConvertId</span><span class="sxs-lookup"><span data-stu-id="4d9f9-150">ConvertId operation</span></span>](convertid-operation.md)


- [<span data-ttu-id="4d9f9-151">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="4d9f9-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="4d9f9-152">Convertir identificadores</span><span class="sxs-lookup"><span data-stu-id="4d9f9-152">Converting Identifiers</span></span>](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

