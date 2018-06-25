---
title: Repetición
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
description: El elemento de repetición representa una sola aparición de modificación de un elemento periódico del calendario.
ms.openlocfilehash: 5a40faa9b885a235d30e7f41830d1eefe2ed23c3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836653"
---
# <a name="occurrence"></a><span data-ttu-id="292dc-103">Repetición</span><span class="sxs-lookup"><span data-stu-id="292dc-103">Occurrence</span></span>

<span data-ttu-id="292dc-104">El elemento de **repetición** representa una sola aparición de modificación de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="292dc-104">The **Occurrence** element represents a single modified occurrence of a recurring calendar item.</span></span> 
  
```xml
<Occurrence>
   <ItemId/>
   <Start/>
   <End/>
   <OriginalStart/>
</Occurrence>
```

<span data-ttu-id="292dc-105">**OccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="292dc-105">**OccurrenceInfoType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="292dc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="292dc-106">Attributes and elements</span></span>

<span data-ttu-id="292dc-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="292dc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="292dc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="292dc-108">Attributes</span></span>

<span data-ttu-id="292dc-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="292dc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="292dc-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="292dc-110">Child elements</span></span>

|<span data-ttu-id="292dc-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="292dc-111">**Element**</span></span>|<span data-ttu-id="292dc-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="292dc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="292dc-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="292dc-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="292dc-114">Contiene la clave exclusiva de identificador y el cambio de una ocurrencia modificada de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="292dc-114">Contains the unique identifier and change key of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="292dc-115">Start</span><span class="sxs-lookup"><span data-stu-id="292dc-115">Start</span></span>](start.md) <br/> |<span data-ttu-id="292dc-116">Representa la hora de inicio de una repetición modificada de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="292dc-116">Represents the start time of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="292dc-117">End</span><span class="sxs-lookup"><span data-stu-id="292dc-117">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="292dc-118">Representa la hora de finalización de una ocurrencia modificada de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="292dc-118">Represents the end time of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="292dc-119">OriginalStart</span><span class="sxs-lookup"><span data-stu-id="292dc-119">OriginalStart</span></span>](originalstart.md) <br/> |<span data-ttu-id="292dc-120">Representa la hora de inicio original de una ocurrencia modificada de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="292dc-120">Represents the original start time of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="292dc-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="292dc-121">Parent elements</span></span>

|<span data-ttu-id="292dc-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="292dc-122">**Element**</span></span>|<span data-ttu-id="292dc-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="292dc-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="292dc-124">ModifiedOccurrences</span><span class="sxs-lookup"><span data-stu-id="292dc-124">ModifiedOccurrences</span></span>](modifiedoccurrences.md) <br/> |<span data-ttu-id="292dc-125">Contiene una colección de periódica repeticiones del elemento de calendario que se han modificado para que sean diferentes que el elemento de patrón de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="292dc-125">Contains a collection of recurring calendar item occurrences that have been modified so that they are different than the recurrence master item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="292dc-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="292dc-126">Remarks</span></span>

<span data-ttu-id="292dc-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="292dc-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="292dc-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="292dc-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="292dc-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="292dc-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="292dc-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="292dc-130">Schema name</span></span>  <br/> |<span data-ttu-id="292dc-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="292dc-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="292dc-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="292dc-132">Validation file</span></span>  <br/> |<span data-ttu-id="292dc-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="292dc-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="292dc-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="292dc-134">Can be empty</span></span>  <br/> |<span data-ttu-id="292dc-135">False</span><span class="sxs-lookup"><span data-stu-id="292dc-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="292dc-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="292dc-136">See also</span></span>

- [<span data-ttu-id="292dc-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="292dc-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

