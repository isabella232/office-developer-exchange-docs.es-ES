---
title: SuggestionsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionsResponse
api_type:
- schema
ms.assetid: d25ca143-f80c-4458-b669-346fda29a5a7
description: El elemento SuggestionsResponse contiene los datos de sugerencia y la información de estado en respuesta de sugerencias de reunión solicitada.
ms.openlocfilehash: 614b58a1df8e340c6be468ccddd3b37537d32591
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840602"
---
# <a name="suggestionsresponse"></a><span data-ttu-id="2425e-103">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="2425e-103">SuggestionsResponse</span></span>

<span data-ttu-id="2425e-104">El elemento **SuggestionsResponse** contiene los datos de sugerencia y la información de estado en respuesta de sugerencias de reunión solicitada.</span><span class="sxs-lookup"><span data-stu-id="2425e-104">The **SuggestionsResponse** element contains response status information and suggestion data for requested meeting suggestions.</span></span> 
  
[<span data-ttu-id="2425e-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="2425e-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="2425e-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="2425e-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
```xml
<SuggestionsResponse>
   <ResponseMessage>...</ResponseMessage>
   <SuggestionDayResultArray>...</SuggestionDayResultArray>
</SuggestionsResponse>
```

 <span data-ttu-id="2425e-107">**SuggestionsResponseType**</span><span class="sxs-lookup"><span data-stu-id="2425e-107">**SuggestionsResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2425e-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2425e-108">Attributes and elements</span></span>

<span data-ttu-id="2425e-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2425e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2425e-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="2425e-110">Attributes</span></span>

<span data-ttu-id="2425e-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2425e-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2425e-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2425e-112">Child elements</span></span>

|<span data-ttu-id="2425e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2425e-113">**Element**</span></span>|<span data-ttu-id="2425e-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2425e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2425e-115">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2425e-115">ResponseMessage</span></span>](responsemessage.md) <br/> |<span data-ttu-id="2425e-116">Proporciona información descriptiva sobre el estado de respuesta.</span><span class="sxs-lookup"><span data-stu-id="2425e-116">Provides descriptive information about the response status.</span></span>  <br/> |
|[<span data-ttu-id="2425e-117">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="2425e-117">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md) <br/> |<span data-ttu-id="2425e-118">Contiene una matriz de sugerencias organizadas por fecha de reunión.</span><span class="sxs-lookup"><span data-stu-id="2425e-118">Contains an array of meeting suggestions organized by date.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2425e-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2425e-119">Parent elements</span></span>

|<span data-ttu-id="2425e-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="2425e-120">**Element**</span></span>|<span data-ttu-id="2425e-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2425e-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2425e-122">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="2425e-122">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md) <br/> |<span data-ttu-id="2425e-123">Contiene información sobre la disponibilidad de los usuarios solicitado.</span><span class="sxs-lookup"><span data-stu-id="2425e-123">Contains the requested users' availability information.</span></span>  <br/> <span data-ttu-id="2425e-124">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="2425e-124">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2425e-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2425e-125">Remarks</span></span>

<span data-ttu-id="2425e-126">Este elemento no está incluido en una respuesta GetUserAvailability si [SuggestionsViewOptions](suggestionsviewoptions.md) no está establecida en el mensaje de solicitud de GetUserAvailability.</span><span class="sxs-lookup"><span data-stu-id="2425e-126">This element is not included in a GetUserAvailability response if [SuggestionsViewOptions](suggestionsviewoptions.md) is not set in the GetUserAvailability request message.</span></span> 
  
<span data-ttu-id="2425e-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="2425e-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2425e-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2425e-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2425e-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2425e-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2425e-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2425e-130">Schema Name</span></span>  <br/> |<span data-ttu-id="2425e-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="2425e-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2425e-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2425e-132">Validation File</span></span>  <br/> |<span data-ttu-id="2425e-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2425e-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2425e-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2425e-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="2425e-135">False</span><span class="sxs-lookup"><span data-stu-id="2425e-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2425e-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="2425e-136">See also</span></span>



[<span data-ttu-id="2425e-137">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="2425e-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="2425e-138">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="2425e-138">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="2425e-139">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="2425e-139">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

