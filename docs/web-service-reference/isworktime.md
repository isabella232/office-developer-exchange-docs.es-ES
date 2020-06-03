---
title: IsWorkTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsWorkTime
api_type:
- schema
ms.assetid: 5243dd19-3593-4a81-bb2d-90496e04cb98
description: El elemento IsWorkTime representa si la hora de reunión sugerida se produce durante las horas laborables programadas.
ms.openlocfilehash: a3f3c73d585bee6f73863e2be64eea245be674f4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467581"
---
# <a name="isworktime"></a><span data-ttu-id="bae2f-103">IsWorkTime</span><span class="sxs-lookup"><span data-stu-id="bae2f-103">IsWorkTime</span></span>

<span data-ttu-id="bae2f-104">El elemento **IsWorkTime** representa si la hora de reunión sugerida se produce durante las horas laborables programadas.</span><span class="sxs-lookup"><span data-stu-id="bae2f-104">The **IsWorkTime** element represents whether the suggested meeting time occurs during scheduled work hours.</span></span> 
  
[<span data-ttu-id="bae2f-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="bae2f-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="bae2f-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="bae2f-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="bae2f-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="bae2f-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="bae2f-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="bae2f-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="bae2f-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="bae2f-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="bae2f-110">Alguna</span><span class="sxs-lookup"><span data-stu-id="bae2f-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="bae2f-111">IsWorkTime</span><span class="sxs-lookup"><span data-stu-id="bae2f-111">IsWorkTime</span></span>](isworktime.md)
  
```xml
<IsWorkTime>true or false</IsWorkTime>
```

 <span data-ttu-id="bae2f-112">**boolean**</span><span class="sxs-lookup"><span data-stu-id="bae2f-112">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bae2f-113">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bae2f-113">Attributes and elements</span></span>

<span data-ttu-id="bae2f-114">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bae2f-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bae2f-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="bae2f-115">Attributes</span></span>

<span data-ttu-id="bae2f-116">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="bae2f-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bae2f-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bae2f-117">Child elements</span></span>

<span data-ttu-id="bae2f-118">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="bae2f-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bae2f-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bae2f-119">Parent elements</span></span>

|<span data-ttu-id="bae2f-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bae2f-120">**Element**</span></span>|<span data-ttu-id="bae2f-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bae2f-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bae2f-122">Alguna</span><span class="sxs-lookup"><span data-stu-id="bae2f-122">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="bae2f-123">Representa una sugerencia de hora de reunión única.</span><span class="sxs-lookup"><span data-stu-id="bae2f-123">Represents a single meeting time suggestion.</span></span>  <br/> <span data-ttu-id="bae2f-124">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="bae2f-124">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bae2f-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="bae2f-125">Text value</span></span>

<span data-ttu-id="bae2f-126">Se requiere un valor de texto que representa un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="bae2f-126">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bae2f-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bae2f-127">Remarks</span></span>

<span data-ttu-id="bae2f-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="bae2f-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bae2f-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bae2f-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bae2f-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="bae2f-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bae2f-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="bae2f-131">Schema Name</span></span>  <br/> |<span data-ttu-id="bae2f-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="bae2f-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="bae2f-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="bae2f-133">Validation File</span></span>  <br/> |<span data-ttu-id="bae2f-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="bae2f-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bae2f-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="bae2f-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="bae2f-136">Falso</span><span class="sxs-lookup"><span data-stu-id="bae2f-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bae2f-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="bae2f-137">See also</span></span>



[<span data-ttu-id="bae2f-138">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="bae2f-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="bae2f-139">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="bae2f-139">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="bae2f-140">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="bae2f-140">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

