---
title: MeetingDurationInMinutes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingDurationInMinutes
api_type:
- schema
ms.assetid: bb86b275-9c29-4daf-8196-8d505b87a4f4
description: El elemento MeetingDurationInMinutes especifica la duración de la reunión que se va a sugerir.
ms.openlocfilehash: b41e234be40c2ad8b28047ae2e812edfd66af644
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467490"
---
# <a name="meetingdurationinminutes"></a><span data-ttu-id="9fb70-103">MeetingDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="9fb70-103">MeetingDurationInMinutes</span></span>

<span data-ttu-id="9fb70-104">El elemento **MeetingDurationInMinutes** especifica la duración de la reunión que se va a sugerir.</span><span class="sxs-lookup"><span data-stu-id="9fb70-104">The **MeetingDurationInMinutes** element specifies the duration of the meeting to be suggested.</span></span> 
  
[<span data-ttu-id="9fb70-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="9fb70-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="9fb70-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="9fb70-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="9fb70-107">MeetingDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="9fb70-107">MeetingDurationInMinutes</span></span>](meetingdurationinminutes.md)
  
```xml
<MeetingDurationInMinutes>...</MeetingDurationInMinutes>
```

 <span data-ttu-id="9fb70-108">**int**</span><span class="sxs-lookup"><span data-stu-id="9fb70-108">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9fb70-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9fb70-109">Attributes and elements</span></span>

<span data-ttu-id="9fb70-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9fb70-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9fb70-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="9fb70-111">Attributes</span></span>

<span data-ttu-id="9fb70-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9fb70-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9fb70-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9fb70-113">Child elements</span></span>

<span data-ttu-id="9fb70-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9fb70-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9fb70-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9fb70-115">Parent elements</span></span>

|<span data-ttu-id="9fb70-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9fb70-116">**Element**</span></span>|<span data-ttu-id="9fb70-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9fb70-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9fb70-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="9fb70-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="9fb70-119">Contiene las opciones para obtener información sobre las sugerencias de la reunión.</span><span class="sxs-lookup"><span data-stu-id="9fb70-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="9fb70-120">A continuación se encuentra la expresión XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="9fb70-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9fb70-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="9fb70-121">Text value</span></span>

<span data-ttu-id="9fb70-122">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="9fb70-122">A text value is required.</span></span> <span data-ttu-id="9fb70-123">El valor de texto representa un número entero.</span><span class="sxs-lookup"><span data-stu-id="9fb70-123">The text value represents an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9fb70-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9fb70-124">Remarks</span></span>

<span data-ttu-id="9fb70-125">Este elemento es obligatorio si se usa el elemento [SuggestionsViewOptions](suggestionsviewoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="9fb70-125">This element is required if the [SuggestionsViewOptions](suggestionsviewoptions.md) element is used.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9fb70-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="9fb70-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="9fb70-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9fb70-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fb70-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="9fb70-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9fb70-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9fb70-129">Schema Name</span></span>  <br/> |<span data-ttu-id="9fb70-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="9fb70-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="9fb70-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9fb70-131">Validation File</span></span>  <br/> |<span data-ttu-id="9fb70-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="9fb70-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9fb70-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9fb70-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="9fb70-134">Falso</span><span class="sxs-lookup"><span data-stu-id="9fb70-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9fb70-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fb70-135">See also</span></span>



[<span data-ttu-id="9fb70-136">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="9fb70-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="9fb70-137">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="9fb70-137">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

