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
description: El elemento SuggestionDayResultArray contiene una matriz de sugerencias de reunión organizadas por fecha.
ms.openlocfilehash: 277d4cf71c31aba26cbff6f598eaa62769cae552
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457987"
---
# <a name="suggestiondayresultarray"></a><span data-ttu-id="001e2-103">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="001e2-103">SuggestionDayResultArray</span></span>

<span data-ttu-id="001e2-104">El elemento **SuggestionDayResultArray** contiene una matriz de sugerencias de reunión organizadas por fecha.</span><span class="sxs-lookup"><span data-stu-id="001e2-104">The **SuggestionDayResultArray** element contains an array of meeting suggestions organized by date.</span></span> 
  
[<span data-ttu-id="001e2-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="001e2-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="001e2-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="001e2-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="001e2-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="001e2-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
```xml
<SuggestionDayResultArray>
   <SuggestionDayResult>...</SuggestionDayResult>
</SuggestionDayResultArray>
```

 <span data-ttu-id="001e2-108">**ArrayOfSuggestionDayResult**</span><span class="sxs-lookup"><span data-stu-id="001e2-108">**ArrayOfSuggestionDayResult**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="001e2-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="001e2-109">Attributes and elements</span></span>

<span data-ttu-id="001e2-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="001e2-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="001e2-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="001e2-111">Attributes</span></span>

<span data-ttu-id="001e2-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="001e2-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="001e2-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="001e2-113">Child elements</span></span>

|<span data-ttu-id="001e2-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="001e2-114">**Element**</span></span>|<span data-ttu-id="001e2-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="001e2-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="001e2-116">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="001e2-116">SuggestionDayResult</span></span>](suggestiondayresult.md) <br/> |<span data-ttu-id="001e2-117">Representa un solo día que contiene las horas de reunión sugeridas.</span><span class="sxs-lookup"><span data-stu-id="001e2-117">Represents a single day that contains suggested meeting times.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="001e2-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="001e2-118">Parent elements</span></span>

|<span data-ttu-id="001e2-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="001e2-119">**Element**</span></span>|<span data-ttu-id="001e2-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="001e2-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="001e2-121">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="001e2-121">SuggestionsResponse</span></span>](suggestionsresponse.md) <br/> |<span data-ttu-id="001e2-122">Contiene información de respuesta y datos de sugerencias para las sugerencias de reunión solicitadas</span><span class="sxs-lookup"><span data-stu-id="001e2-122">Contains response information and suggestion data for requested meeting suggestions</span></span>  <br/> <span data-ttu-id="001e2-123">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="001e2-123">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="001e2-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="001e2-124">Remarks</span></span>

<span data-ttu-id="001e2-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="001e2-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="001e2-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="001e2-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="001e2-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="001e2-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="001e2-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="001e2-128">Schema Name</span></span>  <br/> |<span data-ttu-id="001e2-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="001e2-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="001e2-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="001e2-130">Validation File</span></span>  <br/> |<span data-ttu-id="001e2-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="001e2-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="001e2-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="001e2-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="001e2-133">Falso</span><span class="sxs-lookup"><span data-stu-id="001e2-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="001e2-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="001e2-134">See also</span></span>



[<span data-ttu-id="001e2-135">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="001e2-135">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="001e2-136">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="001e2-136">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="001e2-137">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="001e2-137">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

