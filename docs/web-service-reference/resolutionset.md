---
title: ResolutionSet
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResolutionSet
api_type:
- schema
ms.assetid: 43d5b876-0e87-4414-9b1d-bff1c1ec825c
description: El elemento ResolutionSet contiene una matriz de soluciones para un nombre ambiguo.
ms.openlocfilehash: ad7bd31c85051e8c80aea25aa9e6f2914cf0ad01
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837160"
---
# <a name="resolutionset"></a><span data-ttu-id="20344-103">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="20344-103">ResolutionSet</span></span>

<span data-ttu-id="20344-104">El elemento **ResolutionSet** contiene una matriz de soluciones para un nombre ambiguo.</span><span class="sxs-lookup"><span data-stu-id="20344-104">The **ResolutionSet** element contains an array of resolutions for an ambiguous name.</span></span> 
  
[<span data-ttu-id="20344-105">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="20344-105">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
  
[<span data-ttu-id="20344-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="20344-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="20344-107">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="20344-107">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
  
[<span data-ttu-id="20344-108">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="20344-108">ResolutionSet</span></span>](resolutionset.md)
  
```xml
<ResolutionSet IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Resolution/>
</ResolutionSet>
```

 <span data-ttu-id="20344-109">**ArrayOfResolutionType**</span><span class="sxs-lookup"><span data-stu-id="20344-109">**ArrayOfResolutionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="20344-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="20344-110">Attributes and elements</span></span>

<span data-ttu-id="20344-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="20344-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="20344-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="20344-112">Attributes</span></span>

|<span data-ttu-id="20344-113">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="20344-113">**Attribute**</span></span>|<span data-ttu-id="20344-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="20344-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="20344-115">**IndexedPagingOffset**</span><span class="sxs-lookup"><span data-stu-id="20344-115">**IndexedPagingOffset**</span></span> <br/> |<span data-ttu-id="20344-116">Representa el siguiente índice que se debe usar para la solicitud siguiente cuando se usa una vista de página indizados.</span><span class="sxs-lookup"><span data-stu-id="20344-116">Represents the next index that should be used for the next request when you are using an indexed page view.</span></span>  <br/> |
|<span data-ttu-id="20344-117">**NumeratorOffset**</span><span class="sxs-lookup"><span data-stu-id="20344-117">**NumeratorOffset**</span></span> <br/> |<span data-ttu-id="20344-118">Representa el nuevo valor: número que se usará para la solicitud siguiente cuando se utilizan vistas de página de fracción.</span><span class="sxs-lookup"><span data-stu-id="20344-118">Represents the new numerator value to use for the next request when you are using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="20344-119">**AbsoluteDenominator**</span><span class="sxs-lookup"><span data-stu-id="20344-119">**AbsoluteDenominator**</span></span> <br/> |<span data-ttu-id="20344-120">Representa el denominador siguiente para usar para la solicitud siguiente cuando se utilizan vistas de página de fracción.</span><span class="sxs-lookup"><span data-stu-id="20344-120">Represents the next denominator to use for the next request when you are using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="20344-121">**IncludesLastItemInRange**</span><span class="sxs-lookup"><span data-stu-id="20344-121">**IncludesLastItemInRange**</span></span> <br/> |<span data-ttu-id="20344-122">Este atributo será true si los resultados actuales contienen el último elemento de la consulta, por lo que no es necesaria la paginación adicional.</span><span class="sxs-lookup"><span data-stu-id="20344-122">This attribute will be true if the current results contain the last item in the query, so that additional paging is not needed.</span></span>  <br/> |
|<span data-ttu-id="20344-123">**TotalItemsInView**</span><span class="sxs-lookup"><span data-stu-id="20344-123">**TotalItemsInView**</span></span> <br/> |<span data-ttu-id="20344-124">Representa el número total de elementos en la vista.</span><span class="sxs-lookup"><span data-stu-id="20344-124">Represents the total number of items in the view.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="20344-125">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="20344-125">Child elements</span></span>

|<span data-ttu-id="20344-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="20344-126">**Element**</span></span>|<span data-ttu-id="20344-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="20344-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="20344-128">Resoluci?n</span><span class="sxs-lookup"><span data-stu-id="20344-128">Resolution</span></span>](resolution.md) <br/> |<span data-ttu-id="20344-129">Contiene una única entidad resuelta.</span><span class="sxs-lookup"><span data-stu-id="20344-129">Contains a single resolved entity.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="20344-130">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="20344-130">Parent elements</span></span>

|<span data-ttu-id="20344-131">**Element**</span><span class="sxs-lookup"><span data-stu-id="20344-131">**Element**</span></span>|<span data-ttu-id="20344-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="20344-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="20344-133">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="20344-133">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md) <br/> |<span data-ttu-id="20344-134">Contiene el estado y el resultado de una solicitud de ResolveNames.</span><span class="sxs-lookup"><span data-stu-id="20344-134">Contains the status and result of a ResolveNames request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20344-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="20344-135">Remarks</span></span>

<span data-ttu-id="20344-136">Un elemento **ResolutionSet** puede contener un máximo de 100 entidades resueltos.</span><span class="sxs-lookup"><span data-stu-id="20344-136">A **ResolutionSet** element can contain a maximum of 100 resolved entities.</span></span> 
  
<span data-ttu-id="20344-137">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="20344-137">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="20344-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="20344-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="20344-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="20344-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="20344-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="20344-140">Schema Name</span></span>  <br/> |<span data-ttu-id="20344-141">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="20344-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="20344-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="20344-142">Validation File</span></span>  <br/> |<span data-ttu-id="20344-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="20344-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="20344-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="20344-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="20344-145">False</span><span class="sxs-lookup"><span data-stu-id="20344-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="20344-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="20344-146">See also</span></span>



[<span data-ttu-id="20344-147">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="20344-147">ResolveNames</span></span>](resolvenames.md)
  
[<span data-ttu-id="20344-148">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="20344-148">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
  
[<span data-ttu-id="20344-149">Operación ResolveNames</span><span class="sxs-lookup"><span data-stu-id="20344-149">ResolveNames operation</span></span>](resolvenames-operation.md)


- [<span data-ttu-id="20344-150">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="20344-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

