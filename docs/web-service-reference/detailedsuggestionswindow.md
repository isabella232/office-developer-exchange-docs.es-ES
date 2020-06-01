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
description: El elemento DetailedSuggestionsWindow identifica el intervalo de tiempo que se consulta para obtener información detallada sobre las horas de reunión sugeridas.
ms.openlocfilehash: 45d582f2642c0e3d8f6330b09946230c8842618d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467847"
---
# <a name="detailedsuggestionswindow"></a><span data-ttu-id="48a81-103">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="48a81-103">DetailedSuggestionsWindow</span></span>

<span data-ttu-id="48a81-104">El elemento **DetailedSuggestionsWindow** identifica el intervalo de tiempo que se consulta para obtener información detallada sobre las horas de reunión sugeridas.</span><span class="sxs-lookup"><span data-stu-id="48a81-104">The **DetailedSuggestionsWindow** element identifies the time span that is queried for detailed information about suggested meeting times.</span></span> 
  
- [<span data-ttu-id="48a81-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="48a81-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) 
- [<span data-ttu-id="48a81-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="48a81-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) 
- [<span data-ttu-id="48a81-107">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="48a81-107">DetailedSuggestionsWindow</span></span>](detailedsuggestionswindow.md)
  
```xml
<DetailedSuggestionsWindow>
   <StartTime>...</StartTime>
   <EndTime>...</EndTime>
</DetailedSuggestionsWindow>
```

 <span data-ttu-id="48a81-108">**Duración**</span><span class="sxs-lookup"><span data-stu-id="48a81-108">**Duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="48a81-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="48a81-109">Attributes and elements</span></span>

<span data-ttu-id="48a81-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="48a81-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="48a81-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="48a81-111">Attributes</span></span>

<span data-ttu-id="48a81-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="48a81-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="48a81-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="48a81-113">Child elements</span></span>

|<span data-ttu-id="48a81-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="48a81-114">**Element**</span></span>|<span data-ttu-id="48a81-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="48a81-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="48a81-116">StartTime</span><span class="sxs-lookup"><span data-stu-id="48a81-116">StartTime</span></span>](starttime.md) <br/> |<span data-ttu-id="48a81-117">Representa el inicio del intervalo de tiempo consultado para obtener información detallada sobre las horas de reunión sugeridas.</span><span class="sxs-lookup"><span data-stu-id="48a81-117">Represents the start of the time span queried for detailed information about suggested meeting times.</span></span>  <br/> |
|[<span data-ttu-id="48a81-118">EndTime</span><span class="sxs-lookup"><span data-stu-id="48a81-118">EndTime</span></span>](endtime.md) <br/> |<span data-ttu-id="48a81-119">Representa el final del intervalo de tiempo consultado para obtener información detallada sobre las horas de reunión sugeridas.</span><span class="sxs-lookup"><span data-stu-id="48a81-119">Represents the end of the time span queried for detailed information about suggested meeting times.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="48a81-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="48a81-120">Parent elements</span></span>

|<span data-ttu-id="48a81-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="48a81-121">**Element**</span></span>|<span data-ttu-id="48a81-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="48a81-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="48a81-123">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="48a81-123">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="48a81-124">Contiene las opciones para obtener información sobre las sugerencias de la reunión.</span><span class="sxs-lookup"><span data-stu-id="48a81-124">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="48a81-125">A continuación se encuentra la expresión XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="48a81-125">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48a81-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="48a81-126">Remarks</span></span>

<span data-ttu-id="48a81-127">Este elemento no es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="48a81-127">This element is not required.</span></span>
  
> [!NOTE]
> <span data-ttu-id="48a81-128">El esquema que describe este elemento se encuentra en el directorio/EWS/del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="48a81-128">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="48a81-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="48a81-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="48a81-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="48a81-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="48a81-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="48a81-131">Schema Name</span></span>  <br/> |<span data-ttu-id="48a81-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="48a81-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="48a81-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="48a81-133">Validation File</span></span>  <br/> |<span data-ttu-id="48a81-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="48a81-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="48a81-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="48a81-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="48a81-136">Falso</span><span class="sxs-lookup"><span data-stu-id="48a81-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="48a81-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="48a81-137">See also</span></span>

- [<span data-ttu-id="48a81-138">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="48a81-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="48a81-139">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="48a81-139">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

