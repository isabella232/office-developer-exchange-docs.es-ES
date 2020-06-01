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
description: El elemento CurrentMeetingTime representa la hora de inicio de una reunión que desea actualizar con una hora de reunión propuesta por un asistente de la reunión.
ms.openlocfilehash: e79616fd735cbf6410e85450bd75c1276923f171
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458778"
---
# <a name="currentmeetingtime"></a><span data-ttu-id="150b3-103">CurrentMeetingTime</span><span class="sxs-lookup"><span data-stu-id="150b3-103">CurrentMeetingTime</span></span>

<span data-ttu-id="150b3-104">El elemento **CurrentMeetingTime** representa la hora de inicio de una reunión que desea actualizar con una hora de reunión propuesta por un asistente de la reunión.</span><span class="sxs-lookup"><span data-stu-id="150b3-104">The **CurrentMeetingTime** element represents the start time of a meeting that you want to update with a meeting time proposed by a meeting attendee.</span></span> 
  
[<span data-ttu-id="150b3-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="150b3-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="150b3-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="150b3-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="150b3-107">CurrentMeetingTime</span><span class="sxs-lookup"><span data-stu-id="150b3-107">CurrentMeetingTime</span></span>](currentmeetingtime.md)
  
```xml
<CurrentMeetingTime>...</CurrentMeetingTime>
```

 <span data-ttu-id="150b3-108">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="150b3-108">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="150b3-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="150b3-109">Attributes and elements</span></span>

<span data-ttu-id="150b3-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="150b3-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="150b3-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="150b3-111">Attributes</span></span>

<span data-ttu-id="150b3-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="150b3-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="150b3-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="150b3-113">Child elements</span></span>

<span data-ttu-id="150b3-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="150b3-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="150b3-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="150b3-115">Parent elements</span></span>

|<span data-ttu-id="150b3-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="150b3-116">**Element**</span></span>|<span data-ttu-id="150b3-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="150b3-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="150b3-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="150b3-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="150b3-119">Contiene las opciones para obtener información sobre las sugerencias de la reunión.</span><span class="sxs-lookup"><span data-stu-id="150b3-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="150b3-120">A continuación se encuentra la expresión XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="150b3-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="150b3-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="150b3-121">Remarks</span></span>

<span data-ttu-id="150b3-122">Este elemento no es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="150b3-122">This element is not required.</span></span>
  
> [!NOTE]
> <span data-ttu-id="150b3-123">El esquema que describe este elemento se encuentra en el directorio/EWS/del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="150b3-123">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="150b3-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="150b3-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="150b3-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="150b3-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="150b3-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="150b3-126">Schema Name</span></span>  <br/> |<span data-ttu-id="150b3-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="150b3-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="150b3-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="150b3-128">Validation File</span></span>  <br/> |<span data-ttu-id="150b3-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="150b3-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="150b3-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="150b3-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="150b3-131">Falso</span><span class="sxs-lookup"><span data-stu-id="150b3-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="150b3-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="150b3-132">See also</span></span>



[<span data-ttu-id="150b3-133">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="150b3-133">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="150b3-134">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="150b3-134">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

