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
description: El elemento DayQuality representa la calidad del día para contener horas de reunión sugeridas de calidad.
ms.openlocfilehash: 41cc8313dccb1a5172fefc167e6ed90a21109ec5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455117"
---
# <a name="dayquality"></a><span data-ttu-id="49288-103">DayQuality</span><span class="sxs-lookup"><span data-stu-id="49288-103">DayQuality</span></span>

<span data-ttu-id="49288-104">El elemento **DayQuality** representa la calidad del día para contener horas de reunión sugeridas de calidad.</span><span class="sxs-lookup"><span data-stu-id="49288-104">The **DayQuality** element represents the quality of the day for containing quality suggested meeting times.</span></span> 
  
- [<span data-ttu-id="49288-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="49288-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)  
- [<span data-ttu-id="49288-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="49288-106">SuggestionsResponse</span></span>](suggestionsresponse.md) 
- [<span data-ttu-id="49288-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="49288-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)  
- [<span data-ttu-id="49288-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="49288-108">SuggestionDayResult</span></span>](suggestiondayresult.md) 
- [<span data-ttu-id="49288-109">DayQuality</span><span class="sxs-lookup"><span data-stu-id="49288-109">DayQuality</span></span>](dayquality.md)
  
```xml
<DayQuality>Excellent or Good or Fair or Poor</DayQuality>
```

<span data-ttu-id="49288-110">**SuggestionQuality**</span><span class="sxs-lookup"><span data-stu-id="49288-110">**SuggestionQuality**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="49288-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="49288-111">Attributes and elements</span></span>

<span data-ttu-id="49288-112">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="49288-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="49288-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="49288-113">Attributes</span></span>

<span data-ttu-id="49288-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="49288-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="49288-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="49288-115">Child elements</span></span>

<span data-ttu-id="49288-116">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="49288-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="49288-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="49288-117">Parent elements</span></span>

|<span data-ttu-id="49288-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="49288-118">**Element**</span></span>|<span data-ttu-id="49288-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="49288-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="49288-120">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="49288-120">SuggestionDayResult</span></span>](suggestiondayresult.md) <br/> |<span data-ttu-id="49288-121">Representa un solo día que contiene las horas de reunión sugeridas.</span><span class="sxs-lookup"><span data-stu-id="49288-121">Represents a single day that contains suggested meeting times.</span></span>  <br/><br/><span data-ttu-id="49288-122">La siguiente es la expresión XPath 2,0 a este elemento:</span><span class="sxs-lookup"><span data-stu-id="49288-122">The following is the XPath 2.0 expression to this element:</span></span><br/><br/>`/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="49288-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="49288-123">Text value</span></span>

<span data-ttu-id="49288-124">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="49288-124">A text value is required.</span></span> <span data-ttu-id="49288-125">A continuación se muestran los valores posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="49288-125">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="49288-126">**Excelente**</span><span class="sxs-lookup"><span data-stu-id="49288-126">**Excellent**</span></span>   
- <span data-ttu-id="49288-127">**Good**</span><span class="sxs-lookup"><span data-stu-id="49288-127">**Good**</span></span>    
- <span data-ttu-id="49288-128">**Imparcial**</span><span class="sxs-lookup"><span data-stu-id="49288-128">**Fair**</span></span>    
- <span data-ttu-id="49288-129">**Deficiente**</span><span class="sxs-lookup"><span data-stu-id="49288-129">**Poor**</span></span>
    
## <a name="remarks"></a><span data-ttu-id="49288-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="49288-130">Remarks</span></span>

<span data-ttu-id="49288-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="49288-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="49288-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="49288-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="49288-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="49288-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="49288-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="49288-134">Schema Name</span></span>  <br/> |<span data-ttu-id="49288-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="49288-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="49288-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="49288-136">Validation File</span></span>  <br/> |<span data-ttu-id="49288-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="49288-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="49288-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="49288-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="49288-139">Falso</span><span class="sxs-lookup"><span data-stu-id="49288-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="49288-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="49288-140">See also</span></span>

- [<span data-ttu-id="49288-141">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="49288-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="49288-142">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="49288-142">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="49288-143">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="49288-143">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

