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
description: El elemento MaximumResultsByDay especifica el número de horas de reunión sugeridas por un día devuelto en la respuesta.
ms.openlocfilehash: 46d5c35a83034b8b968901fbc4ee57d046b6c164
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468421"
---
# <a name="maximumresultsbyday"></a><span data-ttu-id="a94df-103">MaximumResultsByDay</span><span class="sxs-lookup"><span data-stu-id="a94df-103">MaximumResultsByDay</span></span>

<span data-ttu-id="a94df-104">El elemento **MaximumResultsByDay** especifica el número de horas de reunión sugeridas por un día devuelto en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a94df-104">The **MaximumResultsByDay** element specifies the number of suggested meeting times per a day returned in the response.</span></span> 
  
[<span data-ttu-id="a94df-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="a94df-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="a94df-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="a94df-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="a94df-107">MaximumResultsByDay</span><span class="sxs-lookup"><span data-stu-id="a94df-107">MaximumResultsByDay</span></span>](maximumresultsbyday.md)
  
```xml
<MaximumResultsByDay>...</MaximumResultsByDay>
```

<span data-ttu-id="a94df-108">**int**</span><span class="sxs-lookup"><span data-stu-id="a94df-108">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a94df-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a94df-109">Attributes and elements</span></span>

<span data-ttu-id="a94df-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a94df-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a94df-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="a94df-111">Attributes</span></span>

<span data-ttu-id="a94df-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a94df-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a94df-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a94df-113">Child elements</span></span>

<span data-ttu-id="a94df-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a94df-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a94df-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a94df-115">Parent elements</span></span>

|<span data-ttu-id="a94df-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a94df-116">**Element**</span></span>|<span data-ttu-id="a94df-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a94df-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a94df-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="a94df-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="a94df-119">Contiene las opciones para obtener información sobre las sugerencias de la reunión.</span><span class="sxs-lookup"><span data-stu-id="a94df-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="a94df-120">A continuación se encuentra la expresión XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="a94df-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a94df-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a94df-121">Text value</span></span>

<span data-ttu-id="a94df-122">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="a94df-122">A text value is required.</span></span> <span data-ttu-id="a94df-123">El valor de texto representa un número entero.</span><span class="sxs-lookup"><span data-stu-id="a94df-123">The text value represents an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a94df-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a94df-124">Remarks</span></span>

<span data-ttu-id="a94df-125">Este elemento es obligatorio si se usa el elemento [SuggestionsViewOptions](suggestionsviewoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="a94df-125">This element is required if the [SuggestionsViewOptions](suggestionsviewoptions.md) element is used.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a94df-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft® Exchange Server 2007 que tenga instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="a94df-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft® Exchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="a94df-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a94df-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a94df-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="a94df-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a94df-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a94df-129">Schema Name</span></span>  <br/> |<span data-ttu-id="a94df-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a94df-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="a94df-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a94df-131">Validation File</span></span>  <br/> |<span data-ttu-id="a94df-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a94df-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a94df-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a94df-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="a94df-134">Falso</span><span class="sxs-lookup"><span data-stu-id="a94df-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a94df-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="a94df-135">See also</span></span>

- [<span data-ttu-id="a94df-136">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="a94df-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="a94df-137">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="a94df-137">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

