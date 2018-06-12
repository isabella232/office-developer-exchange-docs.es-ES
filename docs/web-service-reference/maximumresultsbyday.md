---
title: MaximumResultsByDay
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MaximumResultsByDay
api_type:
- schema
ms.assetid: d581a12a-2b8e-4960-ae14-c8c4aa0b1849
description: El elemento MaximumResultsByDay especifica el número de veces que la reunión sugerida por un día devuelto en la respuesta.
ms.openlocfilehash: 69ab4e0b23f85e5b8786ba2dd934850cadc88f0e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836381"
---
# <a name="maximumresultsbyday"></a><span data-ttu-id="f8ce5-103">MaximumResultsByDay</span><span class="sxs-lookup"><span data-stu-id="f8ce5-103">MaximumResultsByDay</span></span>

<span data-ttu-id="f8ce5-104">El elemento **MaximumResultsByDay** especifica el número de veces que la reunión sugerida por un día devuelto en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f8ce5-104">The **MaximumResultsByDay** element specifies the number of suggested meeting times per a day returned in the response.</span></span> 
  
[<span data-ttu-id="f8ce5-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="f8ce5-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="f8ce5-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="f8ce5-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="f8ce5-107">MaximumResultsByDay</span><span class="sxs-lookup"><span data-stu-id="f8ce5-107">MaximumResultsByDay</span></span>](maximumresultsbyday.md)
  
```xml
<MaximumResultsByDay>...</MaximumResultsByDay>
```

<span data-ttu-id="f8ce5-108">**int**</span><span class="sxs-lookup"><span data-stu-id="f8ce5-108">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f8ce5-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f8ce5-109">Attributes and elements</span></span>

<span data-ttu-id="f8ce5-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f8ce5-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f8ce5-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="f8ce5-111">Attributes</span></span>

<span data-ttu-id="f8ce5-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f8ce5-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f8ce5-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f8ce5-113">Child elements</span></span>

<span data-ttu-id="f8ce5-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f8ce5-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f8ce5-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f8ce5-115">Parent elements</span></span>

|<span data-ttu-id="f8ce5-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f8ce5-116">**Element**</span></span>|<span data-ttu-id="f8ce5-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f8ce5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f8ce5-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="f8ce5-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="f8ce5-119">Contiene las opciones para obtener información de la sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="f8ce5-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="f8ce5-120">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="f8ce5-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f8ce5-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f8ce5-121">Text value</span></span>

<span data-ttu-id="f8ce5-122">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="f8ce5-122">A text value is required.</span></span> <span data-ttu-id="f8ce5-123">El valor de texto representa un número entero.</span><span class="sxs-lookup"><span data-stu-id="f8ce5-123">The text value represents an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f8ce5-124">Notas</span><span class="sxs-lookup"><span data-stu-id="f8ce5-124">Remarks</span></span>

<span data-ttu-id="f8ce5-125">Este elemento es necesario si se usa el elemento [SuggestionsViewOptions](suggestionsviewoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="f8ce5-125">This element is required if the [SuggestionsViewOptions](suggestionsviewoptions.md) element is used.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f8ce5-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft® Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="f8ce5-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft® Exchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="f8ce5-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f8ce5-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f8ce5-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f8ce5-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f8ce5-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f8ce5-129">Schema Name</span></span>  <br/> |<span data-ttu-id="f8ce5-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f8ce5-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="f8ce5-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f8ce5-131">Validation File</span></span>  <br/> |<span data-ttu-id="f8ce5-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f8ce5-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f8ce5-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f8ce5-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="f8ce5-134">False</span><span class="sxs-lookup"><span data-stu-id="f8ce5-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f8ce5-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="f8ce5-135">See also</span></span>

- [<span data-ttu-id="f8ce5-136">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="f8ce5-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="f8ce5-137">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="f8ce5-137">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

