---
title: StartDate (periodicidad)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StartDate
api_type:
- schema
ms.assetid: bd65ac06-b3ac-4c9b-9568-3e4dc94378e7
description: El elemento StartDate representa la fecha de comienzo de una tarea periódica o elemento de calendario.
ms.openlocfilehash: 6a38e63bbcf010ab6dca8f66440a2b0a559cf88d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837551"
---
# <a name="startdate-recurrence"></a><span data-ttu-id="40e6a-103">StartDate (periodicidad)</span><span class="sxs-lookup"><span data-stu-id="40e6a-103">StartDate (Recurrence)</span></span>

<span data-ttu-id="40e6a-104">El elemento **StartDate** representa la fecha de comienzo de una tarea periódica o elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="40e6a-104">The **StartDate** element represents the start date of a recurring task or calendar item.</span></span> 
  
```xml
<StartDate/>
```

<span data-ttu-id="40e6a-105">**Date**</span><span class="sxs-lookup"><span data-stu-id="40e6a-105">**Date**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="40e6a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="40e6a-106">Attributes and elements</span></span>

<span data-ttu-id="40e6a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="40e6a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="40e6a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="40e6a-108">Attributes</span></span>

<span data-ttu-id="40e6a-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="40e6a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="40e6a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="40e6a-110">Child elements</span></span>

<span data-ttu-id="40e6a-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="40e6a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="40e6a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="40e6a-112">Parent elements</span></span>

|<span data-ttu-id="40e6a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="40e6a-113">**Element**</span></span>|<span data-ttu-id="40e6a-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="40e6a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="40e6a-115">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="40e6a-115">EndDateRecurrence</span></span>](enddaterecurrence.md) <br/> |<span data-ttu-id="40e6a-116">Describe la fecha de inicio y la fecha de finalización de un patrón de periodicidad de elemento.</span><span class="sxs-lookup"><span data-stu-id="40e6a-116">Describes the start date and the end date of an item recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="40e6a-117">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="40e6a-117">NoEndRecurrence</span></span>](noendrecurrence.md) <br/> |<span data-ttu-id="40e6a-118">Describe la fecha de inicio de un patrón de periodicidad de elemento que no tiene una fecha de finalización definidas.</span><span class="sxs-lookup"><span data-stu-id="40e6a-118">Describes the start date of an item recurrence pattern that does not have a defined end date.</span></span>  <br/> |
|[<span data-ttu-id="40e6a-119">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="40e6a-119">NumberedRecurrence</span></span>](numberedrecurrence.md) <br/> |<span data-ttu-id="40e6a-120">Describe la fecha de inicio y el número de repeticiones de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="40e6a-120">Describes the start date and the number of occurrences of a recurring item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="40e6a-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="40e6a-121">Text value</span></span>

<span data-ttu-id="40e6a-122">Si se usa este elemento, es necesario un valor de texto que representa una fecha.</span><span class="sxs-lookup"><span data-stu-id="40e6a-122">A text value that represents a date is required if this element is used.</span></span> <span data-ttu-id="40e6a-123">El valor no puede ser menor que 1 de abril de 1601 00:00:00.</span><span class="sxs-lookup"><span data-stu-id="40e6a-123">The value cannot be less than Apr, 1, 1601 00:00:00.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="40e6a-124">Notas</span><span class="sxs-lookup"><span data-stu-id="40e6a-124">Remarks</span></span>

<span data-ttu-id="40e6a-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="40e6a-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="40e6a-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="40e6a-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40e6a-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="40e6a-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="40e6a-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="40e6a-128">Schema name</span></span>  <br/> |<span data-ttu-id="40e6a-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="40e6a-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="40e6a-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="40e6a-130">Validation file</span></span>  <br/> |<span data-ttu-id="40e6a-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="40e6a-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="40e6a-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="40e6a-132">Can be empty</span></span>  <br/> |<span data-ttu-id="40e6a-133">False</span><span class="sxs-lookup"><span data-stu-id="40e6a-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="40e6a-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="40e6a-134">See also</span></span>

- [<span data-ttu-id="40e6a-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="40e6a-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

