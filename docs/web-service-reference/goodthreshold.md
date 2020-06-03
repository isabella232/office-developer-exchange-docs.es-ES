---
title: GoodThreshold
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GoodThreshold
api_type:
- schema
ms.assetid: 68f607f5-7271-46a6-8ffc-91878185a683
description: El elemento GoodThreshold especifica el porcentaje de asistentes que deben tener el período de tiempo abierto para que el período de tiempo se califique como una buena hora de reunión.
ms.openlocfilehash: 34ea433ad7315d61df8cf8e22bae1166d3210af3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457315"
---
# <a name="goodthreshold"></a><span data-ttu-id="4c3fd-103">GoodThreshold</span><span class="sxs-lookup"><span data-stu-id="4c3fd-103">GoodThreshold</span></span>

<span data-ttu-id="4c3fd-104">El elemento **GoodThreshold** especifica el porcentaje de asistentes que deben tener el período de tiempo abierto para que el período de tiempo se califique como una buena hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="4c3fd-104">The **GoodThreshold** element specifies the percentage of attendees that must have the time period open in order for the time period to qualify as a Good suggested meeting time.</span></span> 
  
[<span data-ttu-id="4c3fd-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="4c3fd-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="4c3fd-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="4c3fd-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="4c3fd-107">GoodThreshold</span><span class="sxs-lookup"><span data-stu-id="4c3fd-107">GoodThreshold</span></span>](goodthreshold.md)
  
```xml
<GoodThreshold>...</GoodThreshold>
```

 <span data-ttu-id="4c3fd-108">**int**</span><span class="sxs-lookup"><span data-stu-id="4c3fd-108">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4c3fd-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4c3fd-109">Attributes and elements</span></span>

<span data-ttu-id="4c3fd-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4c3fd-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4c3fd-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="4c3fd-111">Attributes</span></span>

<span data-ttu-id="4c3fd-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4c3fd-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4c3fd-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4c3fd-113">Child elements</span></span>

<span data-ttu-id="4c3fd-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4c3fd-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4c3fd-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4c3fd-115">Parent elements</span></span>

|<span data-ttu-id="4c3fd-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4c3fd-116">**Element**</span></span>|<span data-ttu-id="4c3fd-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4c3fd-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4c3fd-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="4c3fd-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="4c3fd-119">Contiene las opciones para obtener información sobre las sugerencias de la reunión.</span><span class="sxs-lookup"><span data-stu-id="4c3fd-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="4c3fd-120">A continuación se encuentra la expresión XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="4c3fd-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4c3fd-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4c3fd-121">Text value</span></span>

<span data-ttu-id="4c3fd-122">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="4c3fd-122">A text value is required.</span></span> <span data-ttu-id="4c3fd-123">Los valores enteros esperados están entre 0 y 50.</span><span class="sxs-lookup"><span data-stu-id="4c3fd-123">The expected integer values are between 0 and 50.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4c3fd-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4c3fd-124">Remarks</span></span>

<span data-ttu-id="4c3fd-125">Este elemento es obligatorio si se usa el elemento [SuggestionsViewOptions](suggestionsviewoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="4c3fd-125">This element is required if the [SuggestionsViewOptions](suggestionsviewoptions.md) element is used.</span></span> <span data-ttu-id="4c3fd-126">El elemento **GoodThreshold** también determina qué reuniones se consideran justas.</span><span class="sxs-lookup"><span data-stu-id="4c3fd-126">The **GoodThreshold** element also determines what meetings are considered Fair.</span></span> <span data-ttu-id="4c3fd-127">El porcentaje de los asistentes con conflictos es menor que el umbral correcto y supera el 50 por ciento, la hora de reunión sugerida se califica como justa.</span><span class="sxs-lookup"><span data-stu-id="4c3fd-127">It the percentage of attendees with conflicts is less than the Good Threshold and higher than 50 percent, the suggested meeting time qualifies as Fair.</span></span> <span data-ttu-id="4c3fd-128">El umbral bueno más 50 equivale al porcentaje que define el umbral adecuado/equitativo.</span><span class="sxs-lookup"><span data-stu-id="4c3fd-128">The Good Threshold plus 50 equals the percentage that defines the Good/Fair threshold.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4c3fd-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="4c3fd-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="4c3fd-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4c3fd-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c3fd-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="4c3fd-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4c3fd-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4c3fd-132">Schema Name</span></span>  <br/> |<span data-ttu-id="4c3fd-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4c3fd-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="4c3fd-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4c3fd-134">Validation File</span></span>  <br/> |<span data-ttu-id="4c3fd-135">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="4c3fd-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4c3fd-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4c3fd-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="4c3fd-137">Falso</span><span class="sxs-lookup"><span data-stu-id="4c3fd-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4c3fd-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c3fd-138">See also</span></span>



[<span data-ttu-id="4c3fd-139">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="4c3fd-139">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="4c3fd-140">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="4c3fd-140">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

