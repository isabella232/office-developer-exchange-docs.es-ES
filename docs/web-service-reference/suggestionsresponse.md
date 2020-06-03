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
description: El elemento SuggestionsResponse contiene información del estado de respuesta y datos de sugerencia para las sugerencias de reunión solicitadas.
ms.openlocfilehash: cba344f3f97777580c2cc6d296f110f20b550063
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466657"
---
# <a name="suggestionsresponse"></a><span data-ttu-id="7b9c2-103">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="7b9c2-103">SuggestionsResponse</span></span>

<span data-ttu-id="7b9c2-104">El elemento **SuggestionsResponse** contiene información del estado de respuesta y datos de sugerencia para las sugerencias de reunión solicitadas.</span><span class="sxs-lookup"><span data-stu-id="7b9c2-104">The **SuggestionsResponse** element contains response status information and suggestion data for requested meeting suggestions.</span></span> 
  
[<span data-ttu-id="7b9c2-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="7b9c2-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="7b9c2-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="7b9c2-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
```xml
<SuggestionsResponse>
   <ResponseMessage>...</ResponseMessage>
   <SuggestionDayResultArray>...</SuggestionDayResultArray>
</SuggestionsResponse>
```

 <span data-ttu-id="7b9c2-107">**SuggestionsResponseType**</span><span class="sxs-lookup"><span data-stu-id="7b9c2-107">**SuggestionsResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7b9c2-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7b9c2-108">Attributes and elements</span></span>

<span data-ttu-id="7b9c2-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7b9c2-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7b9c2-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="7b9c2-110">Attributes</span></span>

<span data-ttu-id="7b9c2-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7b9c2-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7b9c2-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7b9c2-112">Child elements</span></span>

|<span data-ttu-id="7b9c2-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7b9c2-113">**Element**</span></span>|<span data-ttu-id="7b9c2-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7b9c2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b9c2-115">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7b9c2-115">ResponseMessage</span></span>](responsemessage.md) <br/> |<span data-ttu-id="7b9c2-116">Proporciona información descriptiva sobre el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b9c2-116">Provides descriptive information about the response status.</span></span>  <br/> |
|[<span data-ttu-id="7b9c2-117">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="7b9c2-117">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md) <br/> |<span data-ttu-id="7b9c2-118">Contiene una matriz de sugerencias de reunión organizadas por fecha.</span><span class="sxs-lookup"><span data-stu-id="7b9c2-118">Contains an array of meeting suggestions organized by date.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7b9c2-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7b9c2-119">Parent elements</span></span>

|<span data-ttu-id="7b9c2-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7b9c2-120">**Element**</span></span>|<span data-ttu-id="7b9c2-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7b9c2-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b9c2-122">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="7b9c2-122">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md) <br/> |<span data-ttu-id="7b9c2-123">Contiene la información de disponibilidad de los usuarios solicitados.</span><span class="sxs-lookup"><span data-stu-id="7b9c2-123">Contains the requested users' availability information.</span></span>  <br/> <span data-ttu-id="7b9c2-124">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="7b9c2-124">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b9c2-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7b9c2-125">Remarks</span></span>

<span data-ttu-id="7b9c2-126">Este elemento no se incluye en una respuesta GetUserAvailability si [SuggestionsViewOptions](suggestionsviewoptions.md) no se establece en el mensaje de solicitud GetUserAvailability.</span><span class="sxs-lookup"><span data-stu-id="7b9c2-126">This element is not included in a GetUserAvailability response if [SuggestionsViewOptions](suggestionsviewoptions.md) is not set in the GetUserAvailability request message.</span></span> 
  
<span data-ttu-id="7b9c2-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="7b9c2-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7b9c2-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7b9c2-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b9c2-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="7b9c2-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7b9c2-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7b9c2-130">Schema Name</span></span>  <br/> |<span data-ttu-id="7b9c2-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="7b9c2-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7b9c2-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7b9c2-132">Validation File</span></span>  <br/> |<span data-ttu-id="7b9c2-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="7b9c2-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7b9c2-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7b9c2-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="7b9c2-135">Falso</span><span class="sxs-lookup"><span data-stu-id="7b9c2-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b9c2-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b9c2-136">See also</span></span>



[<span data-ttu-id="7b9c2-137">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="7b9c2-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="7b9c2-138">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="7b9c2-138">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="7b9c2-139">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="7b9c2-139">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

