---
title: DetailedSuggestionsWindow
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DetailedSuggestionsWindow
api_type:
- schema
ms.assetid: 7b348d63-6a7d-45f4-9562-5c42243d63a5
description: El elemento DetailedSuggestionsWindow identifica el intervalo de tiempo que se consulta para obtener información detallada acerca de las horas de reunión sugerida.
ms.openlocfilehash: 8a3af0178d0c96b50f4dd641716a9f7a7be8f7a2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764140"
---
# <a name="detailedsuggestionswindow"></a><span data-ttu-id="fd0eb-103">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="fd0eb-103">DetailedSuggestionsWindow</span></span>

<span data-ttu-id="fd0eb-104">El elemento **DetailedSuggestionsWindow** identifica el intervalo de tiempo que se consulta para obtener información detallada acerca de las horas de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="fd0eb-104">The **DetailedSuggestionsWindow** element identifies the time span that is queried for detailed information about suggested meeting times.</span></span> 
  
- [<span data-ttu-id="fd0eb-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="fd0eb-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) 
- [<span data-ttu-id="fd0eb-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="fd0eb-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) 
- [<span data-ttu-id="fd0eb-107">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="fd0eb-107">DetailedSuggestionsWindow</span></span>](detailedsuggestionswindow.md)
  
```xml
<DetailedSuggestionsWindow>
   <StartTime>...</StartTime>
   <EndTime>...</EndTime>
</DetailedSuggestionsWindow>
```

 <span data-ttu-id="fd0eb-108">**Duration**</span><span class="sxs-lookup"><span data-stu-id="fd0eb-108">**Duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fd0eb-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fd0eb-109">Attributes and elements</span></span>

<span data-ttu-id="fd0eb-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fd0eb-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fd0eb-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="fd0eb-111">Attributes</span></span>

<span data-ttu-id="fd0eb-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fd0eb-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fd0eb-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fd0eb-113">Child elements</span></span>

|<span data-ttu-id="fd0eb-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="fd0eb-114">**Element**</span></span>|<span data-ttu-id="fd0eb-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fd0eb-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fd0eb-116">StartTime</span><span class="sxs-lookup"><span data-stu-id="fd0eb-116">StartTime</span></span>](starttime.md) <br/> |<span data-ttu-id="fd0eb-117">Representa el inicio de un período de tiempo de consulta para obtener información detallada acerca de las horas de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="fd0eb-117">Represents the start of the time span queried for detailed information about suggested meeting times.</span></span>  <br/> |
|[<span data-ttu-id="fd0eb-118">Hora de finalización</span><span class="sxs-lookup"><span data-stu-id="fd0eb-118">EndTime</span></span>](endtime.md) <br/> |<span data-ttu-id="fd0eb-119">Representa el final de un período de tiempo de consulta para obtener información detallada acerca de las horas de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="fd0eb-119">Represents the end of the time span queried for detailed information about suggested meeting times.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fd0eb-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fd0eb-120">Parent elements</span></span>

|<span data-ttu-id="fd0eb-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="fd0eb-121">**Element**</span></span>|<span data-ttu-id="fd0eb-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fd0eb-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fd0eb-123">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="fd0eb-123">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="fd0eb-124">Contiene las opciones para obtener información de la sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="fd0eb-124">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="fd0eb-125">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="fd0eb-125">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd0eb-126">Notas</span><span class="sxs-lookup"><span data-stu-id="fd0eb-126">Remarks</span></span>

<span data-ttu-id="fd0eb-127">Este elemento no es necesario.</span><span class="sxs-lookup"><span data-stu-id="fd0eb-127">This element is not required.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fd0eb-128">El esquema que describe este elemento se encuentra en el directorio /EWS/ del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="fd0eb-128">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="fd0eb-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fd0eb-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fd0eb-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fd0eb-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fd0eb-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fd0eb-131">Schema Name</span></span>  <br/> |<span data-ttu-id="fd0eb-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="fd0eb-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="fd0eb-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fd0eb-133">Validation File</span></span>  <br/> |<span data-ttu-id="fd0eb-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fd0eb-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fd0eb-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fd0eb-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="fd0eb-136">False</span><span class="sxs-lookup"><span data-stu-id="fd0eb-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fd0eb-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="fd0eb-137">See also</span></span>

- [<span data-ttu-id="fd0eb-138">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="fd0eb-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="fd0eb-139">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="fd0eb-139">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

