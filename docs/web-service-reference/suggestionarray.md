---
title: SuggestionArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionArray
api_type:
- schema
ms.assetid: c1c26008-7b14-4563-8db5-bceb0f475b1b
description: El elemento SuggestionArray contiene una matriz de sugerencias de reunión.
ms.openlocfilehash: ec982417c39569820beef82ae837eacbe316740c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466678"
---
# <a name="suggestionarray"></a><span data-ttu-id="dca11-103">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="dca11-103">SuggestionArray</span></span>

<span data-ttu-id="dca11-104">El elemento **SuggestionArray** contiene una matriz de sugerencias de reunión.</span><span class="sxs-lookup"><span data-stu-id="dca11-104">The **SuggestionArray** element contains an array of meeting suggestions.</span></span> 
  
[<span data-ttu-id="dca11-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="dca11-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="dca11-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="dca11-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="dca11-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="dca11-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="dca11-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="dca11-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="dca11-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="dca11-109">SuggestionArray</span></span>](suggestionarray.md)
  
```xml
<SuggestionArray>
   <Suggestion>...</Suggestion>
</SuggestionArray>
```

 <span data-ttu-id="dca11-110">**ArrayOfSuggestion**</span><span class="sxs-lookup"><span data-stu-id="dca11-110">**ArrayOfSuggestion**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dca11-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="dca11-111">Attributes and elements</span></span>

<span data-ttu-id="dca11-112">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="dca11-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dca11-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="dca11-113">Attributes</span></span>

<span data-ttu-id="dca11-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="dca11-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dca11-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dca11-115">Child elements</span></span>

|<span data-ttu-id="dca11-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="dca11-116">**Element**</span></span>|<span data-ttu-id="dca11-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dca11-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dca11-118">Alguna</span><span class="sxs-lookup"><span data-stu-id="dca11-118">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="dca11-119">Representa una sugerencia de reunión única.</span><span class="sxs-lookup"><span data-stu-id="dca11-119">Represents a single meeting suggestion.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dca11-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="dca11-120">Parent elements</span></span>

|<span data-ttu-id="dca11-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="dca11-121">**Element**</span></span>|<span data-ttu-id="dca11-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dca11-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dca11-123">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="dca11-123">SuggestionDayResult</span></span>](suggestiondayresult.md) <br/> |<span data-ttu-id="dca11-124">Representa un solo día que contiene las horas de reunión sugeridas.</span><span class="sxs-lookup"><span data-stu-id="dca11-124">Represents a single day that contains suggested meeting times.</span></span>  <br/> <span data-ttu-id="dca11-125">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="dca11-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dca11-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dca11-126">Remarks</span></span>

<span data-ttu-id="dca11-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="dca11-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dca11-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="dca11-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dca11-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="dca11-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dca11-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="dca11-130">Schema Name</span></span>  <br/> |<span data-ttu-id="dca11-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="dca11-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="dca11-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="dca11-132">Validation File</span></span>  <br/> |<span data-ttu-id="dca11-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="dca11-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dca11-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="dca11-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="dca11-135">Falso</span><span class="sxs-lookup"><span data-stu-id="dca11-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dca11-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="dca11-136">See also</span></span>



[<span data-ttu-id="dca11-137">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="dca11-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="dca11-138">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="dca11-138">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="dca11-139">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="dca11-139">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

