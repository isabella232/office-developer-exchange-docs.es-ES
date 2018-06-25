---
title: MergedFreeBusyIntervalInMinutes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MergedFreeBusyIntervalInMinutes
api_type:
- schema
ms.assetid: 481cdbc6-d5aa-49fa-a3fa-9d119d3dca99
description: El elemento MergedFreeBusyIntervalInMinutes representa la diferencia de tiempo entre dos ranuras sucesivos en la vista FreeBusyMerged.
ms.openlocfilehash: 99c8c69424a0a9d9594005fdf6b2ceba53e6288a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836451"
---
# <a name="mergedfreebusyintervalinminutes"></a><span data-ttu-id="24d03-103">MergedFreeBusyIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="24d03-103">MergedFreeBusyIntervalInMinutes</span></span>

<span data-ttu-id="24d03-104">El elemento **MergedFreeBusyIntervalInMinutes** representa la diferencia de tiempo entre dos ranuras sucesivos en la vista **FreeBusyMerged** .</span><span class="sxs-lookup"><span data-stu-id="24d03-104">The **MergedFreeBusyIntervalInMinutes** element represents the time difference between two successive slots in the **FreeBusyMerged** view.</span></span> 
  
[<span data-ttu-id="24d03-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="24d03-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="24d03-106">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="24d03-106">FreeBusyViewOptions</span></span>](freebusyviewoptions.md)
  
[<span data-ttu-id="24d03-107">MergedFreeBusyIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="24d03-107">MergedFreeBusyIntervalInMinutes</span></span>](mergedfreebusyintervalinminutes.md)
  
```xml
<MergedFreeBusyIntervalInMinutes>...</MergedFreeBusyIntervalInMinutes>
```

 <span data-ttu-id="24d03-108">**int**</span><span class="sxs-lookup"><span data-stu-id="24d03-108">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="24d03-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="24d03-109">Attributes and elements</span></span>

<span data-ttu-id="24d03-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="24d03-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="24d03-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="24d03-111">Attributes</span></span>

<span data-ttu-id="24d03-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="24d03-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="24d03-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="24d03-113">Child elements</span></span>

<span data-ttu-id="24d03-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="24d03-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="24d03-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="24d03-115">Parent elements</span></span>

|<span data-ttu-id="24d03-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="24d03-116">**Element**</span></span>|<span data-ttu-id="24d03-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="24d03-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="24d03-118">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="24d03-118">FreeBusyViewOptions</span></span>](freebusyviewoptions.md) <br/> |<span data-ttu-id="24d03-119">Especifica el tipo de información de libre/ocupado devuelto en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="24d03-119">Specifies the type of free/busy information returned in the response.</span></span>  <br/> <span data-ttu-id="24d03-120">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="24d03-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="24d03-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="24d03-121">Text value</span></span>

<span data-ttu-id="24d03-122">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="24d03-122">A text value is required.</span></span> <span data-ttu-id="24d03-123">El valor de texto representa el tiempo en minutos.</span><span class="sxs-lookup"><span data-stu-id="24d03-123">The text value represents time in minutes.</span></span> <span data-ttu-id="24d03-124">El valor predeterminado es 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="24d03-124">The default value is 30 minutes.</span></span> <span data-ttu-id="24d03-125">Seis minutos es el intervalo mínimo y un día (1440 minutos) es el intervalo máximo para este elemento.</span><span class="sxs-lookup"><span data-stu-id="24d03-125">Six minutes is the minimum interval and one day (1440 minutes) is the maximum interval for this element.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="24d03-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="24d03-126">Remarks</span></span>

<span data-ttu-id="24d03-127">Este valor sólo se utiliza si el elemento [RequestedView](requestedview.md) es igual a **MergedOnly**, **FreeBusyMerged**o **DetailedMerge**.</span><span class="sxs-lookup"><span data-stu-id="24d03-127">This value is used only if the [RequestedView](requestedview.md) element is equal to **MergedOnly**, **FreeBusyMerged**, or **DetailedMerge**.</span></span> <span data-ttu-id="24d03-128">Esto es un tipo de datos integer.</span><span class="sxs-lookup"><span data-stu-id="24d03-128">This is an integer data type.</span></span> <span data-ttu-id="24d03-129">Se devuelve la secuencia que contiene los intervalos definidos por este elemento en el elemento [MergedFreeBusy](mergedfreebusy.md) .</span><span class="sxs-lookup"><span data-stu-id="24d03-129">The stream that contains the intervals defined by this element is returned in the [MergedFreeBusy](mergedfreebusy.md) element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="24d03-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="24d03-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="24d03-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="24d03-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="24d03-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="24d03-132">Schema Name</span></span>  <br/> |<span data-ttu-id="24d03-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="24d03-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="24d03-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="24d03-134">Validation File</span></span>  <br/> |<span data-ttu-id="24d03-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="24d03-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="24d03-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="24d03-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="24d03-137">False</span><span class="sxs-lookup"><span data-stu-id="24d03-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24d03-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="24d03-138">See also</span></span>



[<span data-ttu-id="24d03-139">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="24d03-139">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="24d03-140">Operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="24d03-140">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)


[<span data-ttu-id="24d03-141">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="24d03-141">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

