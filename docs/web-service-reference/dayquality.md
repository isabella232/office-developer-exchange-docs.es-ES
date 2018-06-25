---
title: DayQuality
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayQuality
api_type:
- schema
ms.assetid: cd0eb239-6e7f-4a5a-b245-659f170550b7
description: El elemento DayQuality representa la calidad del día para que contiene las horas de reunión sugerida de calidad.
ms.openlocfilehash: 156d5bc58d481c9c812793da4722272ac76adaad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764059"
---
# <a name="dayquality"></a><span data-ttu-id="39a28-103">DayQuality</span><span class="sxs-lookup"><span data-stu-id="39a28-103">DayQuality</span></span>

<span data-ttu-id="39a28-104">El elemento **DayQuality** representa la calidad del día para que contiene la calidad sugerida tiempos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="39a28-104">The **DayQuality** element represents the quality of the day for containing quality suggested meeting times.</span></span> 
  
- [<span data-ttu-id="39a28-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="39a28-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)  
- [<span data-ttu-id="39a28-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="39a28-106">SuggestionsResponse</span></span>](suggestionsresponse.md) 
- [<span data-ttu-id="39a28-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="39a28-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)  
- [<span data-ttu-id="39a28-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="39a28-108">SuggestionDayResult</span></span>](suggestiondayresult.md) 
- [<span data-ttu-id="39a28-109">DayQuality</span><span class="sxs-lookup"><span data-stu-id="39a28-109">DayQuality</span></span>](dayquality.md)
  
```xml
<DayQuality>Excellent or Good or Fair or Poor</DayQuality>
```

<span data-ttu-id="39a28-110">**SuggestionQuality**</span><span class="sxs-lookup"><span data-stu-id="39a28-110">**SuggestionQuality**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="39a28-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="39a28-111">Attributes and elements</span></span>

<span data-ttu-id="39a28-112">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="39a28-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="39a28-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="39a28-113">Attributes</span></span>

<span data-ttu-id="39a28-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="39a28-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="39a28-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="39a28-115">Child elements</span></span>

<span data-ttu-id="39a28-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="39a28-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="39a28-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="39a28-117">Parent elements</span></span>

|<span data-ttu-id="39a28-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="39a28-118">**Element**</span></span>|<span data-ttu-id="39a28-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="39a28-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39a28-120">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="39a28-120">SuggestionDayResult</span></span>](suggestiondayresult.md) <br/> |<span data-ttu-id="39a28-121">Representa un solo día que contiene las horas de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="39a28-121">Represents a single day that contains suggested meeting times.</span></span>  <br/><br/><span data-ttu-id="39a28-122">La siguiente es la expresión de XPath 2.0 para este elemento:</span><span class="sxs-lookup"><span data-stu-id="39a28-122">The following is the XPath 2.0 expression to this element:</span></span><br/><br/>`/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="39a28-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="39a28-123">Text value</span></span>

<span data-ttu-id="39a28-124">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="39a28-124">A text value is required.</span></span> <span data-ttu-id="39a28-125">Los siguientes son los valores posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="39a28-125">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="39a28-126">**Excelente**</span><span class="sxs-lookup"><span data-stu-id="39a28-126">**Excellent**</span></span>   
- <span data-ttu-id="39a28-127">**Buena**</span><span class="sxs-lookup"><span data-stu-id="39a28-127">**Good**</span></span>    
- <span data-ttu-id="39a28-128">**Razonable**</span><span class="sxs-lookup"><span data-stu-id="39a28-128">**Fair**</span></span>    
- <span data-ttu-id="39a28-129">**Deficiente**</span><span class="sxs-lookup"><span data-stu-id="39a28-129">**Poor**</span></span>
    
## <a name="remarks"></a><span data-ttu-id="39a28-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="39a28-130">Remarks</span></span>

<span data-ttu-id="39a28-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="39a28-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="39a28-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="39a28-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39a28-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="39a28-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="39a28-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="39a28-134">Schema Name</span></span>  <br/> |<span data-ttu-id="39a28-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="39a28-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="39a28-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="39a28-136">Validation File</span></span>  <br/> |<span data-ttu-id="39a28-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="39a28-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="39a28-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="39a28-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="39a28-139">False</span><span class="sxs-lookup"><span data-stu-id="39a28-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="39a28-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="39a28-140">See also</span></span>

- [<span data-ttu-id="39a28-141">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="39a28-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="39a28-142">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="39a28-142">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="39a28-143">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="39a28-143">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

