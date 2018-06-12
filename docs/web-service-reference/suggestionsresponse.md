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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840602"
---
# <a name="suggestionsresponse"></a><span data-ttu-id="1aefd-103">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="1aefd-103">SuggestionsResponse</span></span>

<span data-ttu-id="1aefd-104">El elemento **SuggestionsResponse** contiene los datos de sugerencia y la información de estado en respuesta de sugerencias de reunión solicitada.</span><span class="sxs-lookup"><span data-stu-id="1aefd-104">The **SuggestionsResponse** element contains response status information and suggestion data for requested meeting suggestions.</span></span> 
  
[<span data-ttu-id="1aefd-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1aefd-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="1aefd-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="1aefd-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
```xml
<SuggestionsResponse>
   <ResponseMessage>...</ResponseMessage>
   <SuggestionDayResultArray>...</SuggestionDayResultArray>
</SuggestionsResponse>
```

 <span data-ttu-id="1aefd-107">**SuggestionsResponseType**</span><span class="sxs-lookup"><span data-stu-id="1aefd-107">**SuggestionsResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1aefd-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1aefd-108">Attributes and elements</span></span>

<span data-ttu-id="1aefd-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1aefd-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1aefd-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="1aefd-110">Attributes</span></span>

<span data-ttu-id="1aefd-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1aefd-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1aefd-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1aefd-112">Child elements</span></span>

|<span data-ttu-id="1aefd-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1aefd-113">**Element**</span></span>|<span data-ttu-id="1aefd-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1aefd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1aefd-115">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1aefd-115">ResponseMessage</span></span>](responsemessage.md) <br/> |<span data-ttu-id="1aefd-116">Proporciona información descriptiva sobre el estado de respuesta.</span><span class="sxs-lookup"><span data-stu-id="1aefd-116">Provides descriptive information about the response status.</span></span>  <br/> |
|[<span data-ttu-id="1aefd-117">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="1aefd-117">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md) <br/> |<span data-ttu-id="1aefd-118">Contiene una matriz de sugerencias organizadas por fecha de reunión.</span><span class="sxs-lookup"><span data-stu-id="1aefd-118">Contains an array of meeting suggestions organized by date.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1aefd-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1aefd-119">Parent elements</span></span>

|<span data-ttu-id="1aefd-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="1aefd-120">**Element**</span></span>|<span data-ttu-id="1aefd-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1aefd-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1aefd-122">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1aefd-122">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md) <br/> |<span data-ttu-id="1aefd-123">Contiene información sobre la disponibilidad de los usuarios solicitado.</span><span class="sxs-lookup"><span data-stu-id="1aefd-123">Contains the requested users' availability information.</span></span>  <br/> <span data-ttu-id="1aefd-124">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="1aefd-124">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1aefd-125">Notas</span><span class="sxs-lookup"><span data-stu-id="1aefd-125">Remarks</span></span>

<span data-ttu-id="1aefd-126">Este elemento no está incluido en una respuesta GetUserAvailability si [SuggestionsViewOptions](suggestionsviewoptions.md) no está establecida en el mensaje de solicitud de GetUserAvailability.</span><span class="sxs-lookup"><span data-stu-id="1aefd-126">This element is not included in a GetUserAvailability response if [SuggestionsViewOptions](suggestionsviewoptions.md) is not set in the GetUserAvailability request message.</span></span> 
  
<span data-ttu-id="1aefd-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="1aefd-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1aefd-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1aefd-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1aefd-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1aefd-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1aefd-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1aefd-130">Schema Name</span></span>  <br/> |<span data-ttu-id="1aefd-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="1aefd-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1aefd-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1aefd-132">Validation File</span></span>  <br/> |<span data-ttu-id="1aefd-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1aefd-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1aefd-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1aefd-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="1aefd-135">False</span><span class="sxs-lookup"><span data-stu-id="1aefd-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1aefd-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="1aefd-136">See also</span></span>



[<span data-ttu-id="1aefd-137">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="1aefd-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="1aefd-138">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1aefd-138">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="1aefd-139">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="1aefd-139">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

