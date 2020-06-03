---
title: ModifiedOccurrences
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ModifiedOccurrences
api_type:
- schema
ms.assetid: 552932fc-b3b4-486e-8d73-32c0bb10bd68
description: El elemento ModifiedOccurrences contiene una matriz de repeticiones de elementos de calendario periódicas que se han modificado para que sean diferentes del elemento principal de periodicidad.
ms.openlocfilehash: d599e3d232bfffc5bedd37f3dae4d8b10a82ffde
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530425"
---
# <a name="modifiedoccurrences"></a><span data-ttu-id="b3c5e-103">ModifiedOccurrences</span><span class="sxs-lookup"><span data-stu-id="b3c5e-103">ModifiedOccurrences</span></span>

<span data-ttu-id="b3c5e-104">El elemento **ModifiedOccurrences** contiene una matriz de repeticiones de elementos de calendario periódicas que se han modificado para que sean diferentes del elemento principal de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-104">The **ModifiedOccurrences** element contains an array of recurring calendar item occurrences that have been modified so that they are different than the recurrence master item.</span></span> 
  
```xml
<ModifiedOccurrences>
   <Occurrence/>
</ModifiedOccurrences>
```

 <span data-ttu-id="b3c5e-105">**NonEmptyArrayOfOccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="b3c5e-105">**NonEmptyArrayOfOccurrenceInfoType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b3c5e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b3c5e-106">Attributes and elements</span></span>

<span data-ttu-id="b3c5e-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b3c5e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b3c5e-108">Attributes</span></span>

<span data-ttu-id="b3c5e-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b3c5e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b3c5e-110">Child elements</span></span>

|<span data-ttu-id="b3c5e-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b3c5e-111">**Element**</span></span>|<span data-ttu-id="b3c5e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b3c5e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3c5e-113">Suceda</span><span class="sxs-lookup"><span data-stu-id="b3c5e-113">Occurrence</span></span>](occurrence.md) <br/> |<span data-ttu-id="b3c5e-114">Representa una ocurrencia única modificada de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-114">Represents a single modified occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b3c5e-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b3c5e-115">Parent elements</span></span>

|<span data-ttu-id="b3c5e-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b3c5e-116">**Element**</span></span>|<span data-ttu-id="b3c5e-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b3c5e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3c5e-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="b3c5e-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="b3c5e-119">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="b3c5e-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="b3c5e-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="b3c5e-121">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3c5e-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b3c5e-122">Remarks</span></span>

<span data-ttu-id="b3c5e-123">Este elemento es válido si [CalendarItemType](calendaritemtype.md) tiene el valor RecurringMaster.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-123">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span> 
  
<span data-ttu-id="b3c5e-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b3c5e-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b3c5e-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b3c5e-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="b3c5e-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b3c5e-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b3c5e-127">Schema name</span></span>  <br/> |<span data-ttu-id="b3c5e-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b3c5e-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="b3c5e-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b3c5e-129">Validation file</span></span>  <br/> |<span data-ttu-id="b3c5e-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="b3c5e-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b3c5e-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b3c5e-131">Can be empty</span></span>  <br/> |<span data-ttu-id="b3c5e-132">Falso</span><span class="sxs-lookup"><span data-stu-id="b3c5e-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b3c5e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3c5e-133">See also</span></span>



- [<span data-ttu-id="b3c5e-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b3c5e-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

