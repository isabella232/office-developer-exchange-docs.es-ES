---
title: SuggestionDayResultArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionDayResultArray
api_type:
- schema
ms.assetid: eeba9eff-5eca-4002-b5a5-8fb794feaba1
description: El elemento SuggestionDayResultArray contiene una matriz de sugerencias organizadas por fecha de reunión.
ms.openlocfilehash: c208104356606a5d9961461ad8743a772d2410d8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840601"
---
# <a name="suggestiondayresultarray"></a><span data-ttu-id="8958c-103">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="8958c-103">SuggestionDayResultArray</span></span>

<span data-ttu-id="8958c-104">El elemento **SuggestionDayResultArray** contiene una matriz de sugerencias organizadas por fecha de reunión.</span><span class="sxs-lookup"><span data-stu-id="8958c-104">The **SuggestionDayResultArray** element contains an array of meeting suggestions organized by date.</span></span> 
  
[<span data-ttu-id="8958c-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="8958c-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="8958c-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="8958c-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="8958c-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="8958c-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
```xml
<SuggestionDayResultArray>
   <SuggestionDayResult>...</SuggestionDayResult>
</SuggestionDayResultArray>
```

 <span data-ttu-id="8958c-108">**ArrayOfSuggestionDayResult**</span><span class="sxs-lookup"><span data-stu-id="8958c-108">**ArrayOfSuggestionDayResult**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8958c-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8958c-109">Attributes and elements</span></span>

<span data-ttu-id="8958c-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8958c-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8958c-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="8958c-111">Attributes</span></span>

<span data-ttu-id="8958c-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8958c-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8958c-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8958c-113">Child elements</span></span>

|<span data-ttu-id="8958c-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="8958c-114">**Element**</span></span>|<span data-ttu-id="8958c-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8958c-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8958c-116">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="8958c-116">SuggestionDayResult</span></span>](suggestiondayresult.md) <br/> |<span data-ttu-id="8958c-117">Representa un solo día que contiene las horas de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="8958c-117">Represents a single day that contains suggested meeting times.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8958c-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8958c-118">Parent elements</span></span>

|<span data-ttu-id="8958c-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="8958c-119">**Element**</span></span>|<span data-ttu-id="8958c-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8958c-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8958c-121">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="8958c-121">SuggestionsResponse</span></span>](suggestionsresponse.md) <br/> |<span data-ttu-id="8958c-122">Contiene los datos de información y sugerencia de la respuesta para solicitado sugerencias de reunión</span><span class="sxs-lookup"><span data-stu-id="8958c-122">Contains response information and suggestion data for requested meeting suggestions</span></span>  <br/> <span data-ttu-id="8958c-123">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="8958c-123">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8958c-124">Notas</span><span class="sxs-lookup"><span data-stu-id="8958c-124">Remarks</span></span>

<span data-ttu-id="8958c-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="8958c-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8958c-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8958c-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8958c-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8958c-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8958c-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8958c-128">Schema Name</span></span>  <br/> |<span data-ttu-id="8958c-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="8958c-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8958c-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8958c-130">Validation File</span></span>  <br/> |<span data-ttu-id="8958c-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8958c-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8958c-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8958c-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="8958c-133">False</span><span class="sxs-lookup"><span data-stu-id="8958c-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8958c-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="8958c-134">See also</span></span>



[<span data-ttu-id="8958c-135">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="8958c-135">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="8958c-136">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="8958c-136">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="8958c-137">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="8958c-137">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

