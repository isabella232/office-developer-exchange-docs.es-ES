---
title: Suceda
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Occurrence
api_type:
- schema
ms.assetid: d292b99c-b896-40b7-be5d-2cb314c9481f
description: El elemento Representation representa una única ocurrencia modificada de un elemento de calendario periódico.
ms.openlocfilehash: c3a6bcce23f0bb1125dbd2a5bb86e9b20039a4e1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466321"
---
# <a name="occurrence"></a><span data-ttu-id="7d14f-103">Suceda</span><span class="sxs-lookup"><span data-stu-id="7d14f-103">Occurrence</span></span>

<span data-ttu-id="7d14f-104">El **elemento** Representation representa una única ocurrencia modificada de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="7d14f-104">The **Occurrence** element represents a single modified occurrence of a recurring calendar item.</span></span> 
  
```xml
<Occurrence>
   <ItemId/>
   <Start/>
   <End/>
   <OriginalStart/>
</Occurrence>
```

<span data-ttu-id="7d14f-105">**OccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="7d14f-105">**OccurrenceInfoType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="7d14f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7d14f-106">Attributes and elements</span></span>

<span data-ttu-id="7d14f-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7d14f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7d14f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7d14f-108">Attributes</span></span>

<span data-ttu-id="7d14f-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7d14f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7d14f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7d14f-110">Child elements</span></span>

|<span data-ttu-id="7d14f-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7d14f-111">**Element**</span></span>|<span data-ttu-id="7d14f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7d14f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7d14f-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="7d14f-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="7d14f-114">Contiene el identificador único y la clave de cambio de una repetición modificada de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="7d14f-114">Contains the unique identifier and change key of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="7d14f-115">Start</span><span class="sxs-lookup"><span data-stu-id="7d14f-115">Start</span></span>](start.md) <br/> |<span data-ttu-id="7d14f-116">Representa la hora de inicio de una repetición modificada de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="7d14f-116">Represents the start time of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="7d14f-117">Centraliza</span><span class="sxs-lookup"><span data-stu-id="7d14f-117">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="7d14f-118">Representa la hora de finalización de una repetición modificada de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="7d14f-118">Represents the end time of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="7d14f-119">OriginalStart</span><span class="sxs-lookup"><span data-stu-id="7d14f-119">OriginalStart</span></span>](originalstart.md) <br/> |<span data-ttu-id="7d14f-120">Representa la hora de inicio original de una repetición modificada de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="7d14f-120">Represents the original start time of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7d14f-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7d14f-121">Parent elements</span></span>

|<span data-ttu-id="7d14f-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7d14f-122">**Element**</span></span>|<span data-ttu-id="7d14f-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7d14f-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7d14f-124">ModifiedOccurrences</span><span class="sxs-lookup"><span data-stu-id="7d14f-124">ModifiedOccurrences</span></span>](modifiedoccurrences.md) <br/> |<span data-ttu-id="7d14f-125">Contiene una colección de repeticiones de elementos de calendario periódicas que se han modificado para que sean diferentes del elemento principal de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="7d14f-125">Contains a collection of recurring calendar item occurrences that have been modified so that they are different than the recurrence master item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d14f-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7d14f-126">Remarks</span></span>

<span data-ttu-id="7d14f-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="7d14f-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7d14f-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7d14f-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d14f-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="7d14f-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7d14f-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7d14f-130">Schema name</span></span>  <br/> |<span data-ttu-id="7d14f-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="7d14f-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="7d14f-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7d14f-132">Validation file</span></span>  <br/> |<span data-ttu-id="7d14f-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="7d14f-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7d14f-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7d14f-134">Can be empty</span></span>  <br/> |<span data-ttu-id="7d14f-135">Falso</span><span class="sxs-lookup"><span data-stu-id="7d14f-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7d14f-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d14f-136">See also</span></span>

- [<span data-ttu-id="7d14f-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="7d14f-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

