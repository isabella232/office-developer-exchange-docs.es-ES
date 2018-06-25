---
title: CurrentMeetingTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CurrentMeetingTime
api_type:
- schema
ms.assetid: 1ff68154-24b5-465a-a31c-3d3bab0d491e
description: El elemento CurrentMeetingTime representa la hora de inicio de una reunión que desea actualizar con una hora de reunión propuesta por un asistente a la reunión.
ms.openlocfilehash: 88adbe566270d759986e9b55afd4827c0513ca43
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763998"
---
# <a name="currentmeetingtime"></a><span data-ttu-id="ae440-103">CurrentMeetingTime</span><span class="sxs-lookup"><span data-stu-id="ae440-103">CurrentMeetingTime</span></span>

<span data-ttu-id="ae440-104">El elemento **CurrentMeetingTime** representa la hora de inicio de una reunión que desea actualizar con una hora de reunión propuesta por un asistente a la reunión.</span><span class="sxs-lookup"><span data-stu-id="ae440-104">The **CurrentMeetingTime** element represents the start time of a meeting that you want to update with a meeting time proposed by a meeting attendee.</span></span> 
  
[<span data-ttu-id="ae440-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="ae440-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="ae440-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="ae440-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="ae440-107">CurrentMeetingTime</span><span class="sxs-lookup"><span data-stu-id="ae440-107">CurrentMeetingTime</span></span>](currentmeetingtime.md)
  
```xml
<CurrentMeetingTime>...</CurrentMeetingTime>
```

 <span data-ttu-id="ae440-108">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="ae440-108">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ae440-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ae440-109">Attributes and elements</span></span>

<span data-ttu-id="ae440-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ae440-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae440-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="ae440-111">Attributes</span></span>

<span data-ttu-id="ae440-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ae440-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ae440-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ae440-113">Child elements</span></span>

<span data-ttu-id="ae440-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ae440-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ae440-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ae440-115">Parent elements</span></span>

|<span data-ttu-id="ae440-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="ae440-116">**Element**</span></span>|<span data-ttu-id="ae440-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ae440-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae440-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="ae440-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="ae440-119">Contiene las opciones para obtener información de la sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="ae440-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="ae440-120">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="ae440-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae440-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ae440-121">Remarks</span></span>

<span data-ttu-id="ae440-122">Este elemento no es necesario.</span><span class="sxs-lookup"><span data-stu-id="ae440-122">This element is not required.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ae440-123">El esquema que describe este elemento se encuentra en el directorio /EWS/ del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="ae440-123">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="ae440-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ae440-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae440-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ae440-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ae440-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ae440-126">Schema Name</span></span>  <br/> |<span data-ttu-id="ae440-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ae440-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="ae440-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ae440-128">Validation File</span></span>  <br/> |<span data-ttu-id="ae440-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ae440-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ae440-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ae440-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="ae440-131">False</span><span class="sxs-lookup"><span data-stu-id="ae440-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ae440-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae440-132">See also</span></span>



[<span data-ttu-id="ae440-133">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="ae440-133">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="ae440-134">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="ae440-134">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

