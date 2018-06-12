---
title: MaximumNonWorkHourResultsByDay
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MaximumNonWorkHourResultsByDay
api_type:
- schema
ms.assetid: 9fb7314d-779c-4b1f-9d7c-b5cb092ed134
description: El elemento MaximumNonWorkHourResultsByDay especifica el número de resultados sugeridos para horas fuera del horario normal de trabajo por día de la reunión.
ms.openlocfilehash: f931dcaabda222e1579a0a4c0e0e6e49d88c6342
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836382"
---
# <a name="maximumnonworkhourresultsbyday"></a><span data-ttu-id="fa6a3-103">MaximumNonWorkHourResultsByDay</span><span class="sxs-lookup"><span data-stu-id="fa6a3-103">MaximumNonWorkHourResultsByDay</span></span>

<span data-ttu-id="fa6a3-104">El elemento **MaximumNonWorkHourResultsByDay** especifica el número de resultados sugeridos para horas fuera del horario normal de trabajo por día de la reunión.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-104">The **MaximumNonWorkHourResultsByDay** element specifies the number of suggested results for meeting times outside regular working hours per day.</span></span> 
  
[<span data-ttu-id="fa6a3-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="fa6a3-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="fa6a3-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="fa6a3-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="fa6a3-107">MaximumNonWorkHourResultsByDay</span><span class="sxs-lookup"><span data-stu-id="fa6a3-107">MaximumNonWorkHourResultsByDay</span></span>](maximumnonworkhourresultsbyday.md)
  
```xml
<MaximumNonWorkHourResultsByDay>...</MaximumNonWorkHourResultsByDay>
```

 <span data-ttu-id="fa6a3-108">**int**</span><span class="sxs-lookup"><span data-stu-id="fa6a3-108">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa6a3-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fa6a3-109">Attributes and elements</span></span>

<span data-ttu-id="fa6a3-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa6a3-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="fa6a3-111">Attributes</span></span>

<span data-ttu-id="fa6a3-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa6a3-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fa6a3-113">Child elements</span></span>

<span data-ttu-id="fa6a3-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fa6a3-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fa6a3-115">Parent elements</span></span>

|<span data-ttu-id="fa6a3-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="fa6a3-116">**Element**</span></span>|<span data-ttu-id="fa6a3-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fa6a3-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa6a3-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="fa6a3-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="fa6a3-119">Contiene las opciones para obtener información de la sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="fa6a3-120">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="fa6a3-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fa6a3-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fa6a3-121">Text value</span></span>

<span data-ttu-id="fa6a3-122">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-122">A text value is required.</span></span> <span data-ttu-id="fa6a3-123">El valor de texto representa un número entero.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-123">The text value represents an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fa6a3-124">Notas</span><span class="sxs-lookup"><span data-stu-id="fa6a3-124">Remarks</span></span>

<span data-ttu-id="fa6a3-125">Este elemento es necesario si se usa el elemento [SuggestionsViewOptions](suggestionsviewoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="fa6a3-125">This element is required if the [SuggestionsViewOptions](suggestionsviewoptions.md) element is used.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fa6a3-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="fa6a3-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fa6a3-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa6a3-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fa6a3-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fa6a3-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fa6a3-129">Schema Name</span></span>  <br/> |<span data-ttu-id="fa6a3-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="fa6a3-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="fa6a3-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fa6a3-131">Validation File</span></span>  <br/> |<span data-ttu-id="fa6a3-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fa6a3-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fa6a3-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fa6a3-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="fa6a3-134">False</span><span class="sxs-lookup"><span data-stu-id="fa6a3-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa6a3-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="fa6a3-135">See also</span></span>



[<span data-ttu-id="fa6a3-136">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="fa6a3-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="fa6a3-137">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="fa6a3-137">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

