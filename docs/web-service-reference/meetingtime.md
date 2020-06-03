---
title: MeetingTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingTime
api_type:
- schema
ms.assetid: 6e6d2d8b-e8a2-43e6-a715-0fc7d6dd44b9
description: El elemento MeetingTime representa una hora de reunión sugerida.
ms.openlocfilehash: 3a7031e70eb8b22adc8030c1cec09d33399332ee
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530453"
---
# <a name="meetingtime"></a><span data-ttu-id="1338a-103">MeetingTime</span><span class="sxs-lookup"><span data-stu-id="1338a-103">MeetingTime</span></span>

<span data-ttu-id="1338a-104">El elemento **MeetingTime** representa una hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="1338a-104">The **MeetingTime** element represents a suggested meeting time.</span></span> 
  
[<span data-ttu-id="1338a-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1338a-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="1338a-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="1338a-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="1338a-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="1338a-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="1338a-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="1338a-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="1338a-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="1338a-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="1338a-110">Alguna</span><span class="sxs-lookup"><span data-stu-id="1338a-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="1338a-111">MeetingTime</span><span class="sxs-lookup"><span data-stu-id="1338a-111">MeetingTime</span></span>](meetingtime.md)
  
```xml
<MeetingTime>...</MeetingTime
```

 <span data-ttu-id="1338a-112">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="1338a-112">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1338a-113">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1338a-113">Attributes and elements</span></span>

<span data-ttu-id="1338a-114">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1338a-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1338a-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="1338a-115">Attributes</span></span>

<span data-ttu-id="1338a-116">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1338a-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1338a-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1338a-117">Child elements</span></span>

<span data-ttu-id="1338a-118">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1338a-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1338a-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1338a-119">Parent elements</span></span>

|<span data-ttu-id="1338a-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1338a-120">**Element**</span></span>|<span data-ttu-id="1338a-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1338a-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1338a-122">Alguna</span><span class="sxs-lookup"><span data-stu-id="1338a-122">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="1338a-123">Representa una sugerencia de hora de reunión única.</span><span class="sxs-lookup"><span data-stu-id="1338a-123">Represents a single meeting time suggestion.</span></span>  <br/> <span data-ttu-id="1338a-124">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="1338a-124">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1338a-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1338a-125">Text value</span></span>

<span data-ttu-id="1338a-126">Es necesario un valor de texto que representa un valor de **fecha y hora** .</span><span class="sxs-lookup"><span data-stu-id="1338a-126">A text value that represents a **dateTime** value is required.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1338a-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1338a-127">Remarks</span></span>

<span data-ttu-id="1338a-128">El elemento [MeetingTime](meetingtime.md) es un elemento secundario necesario del elemento de [sugerencia](suggestion.md) .</span><span class="sxs-lookup"><span data-stu-id="1338a-128">The [MeetingTime](meetingtime.md) element is a required child element of the [Suggestion](suggestion.md) element.</span></span> 
  
<span data-ttu-id="1338a-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="1338a-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1338a-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1338a-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1338a-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="1338a-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1338a-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1338a-132">Schema Name</span></span>  <br/> |<span data-ttu-id="1338a-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1338a-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="1338a-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1338a-134">Validation File</span></span>  <br/> |<span data-ttu-id="1338a-135">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1338a-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1338a-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1338a-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="1338a-137">Falso</span><span class="sxs-lookup"><span data-stu-id="1338a-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1338a-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="1338a-138">See also</span></span>



[<span data-ttu-id="1338a-139">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="1338a-139">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="1338a-140">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1338a-140">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="1338a-141">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="1338a-141">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

