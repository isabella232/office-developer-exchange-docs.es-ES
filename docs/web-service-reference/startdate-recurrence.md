---
title: StartDate (periodicidad)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StartDate
api_type:
- schema
ms.assetid: bd65ac06-b3ac-4c9b-9568-3e4dc94378e7
description: El elemento StartDate representa la fecha de comienzo de una tarea periódica o un elemento de calendario.
ms.openlocfilehash: 4514f126b1de31c64a2650b9e7cb6b7412a726c7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457210"
---
# <a name="startdate-recurrence"></a><span data-ttu-id="63ac9-103">StartDate (periodicidad)</span><span class="sxs-lookup"><span data-stu-id="63ac9-103">StartDate (Recurrence)</span></span>

<span data-ttu-id="63ac9-104">El elemento **startDate** representa la fecha de comienzo de una tarea periódica o un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="63ac9-104">The **StartDate** element represents the start date of a recurring task or calendar item.</span></span> 
  
```xml
<StartDate/>
```

<span data-ttu-id="63ac9-105">**Fecha**</span><span class="sxs-lookup"><span data-stu-id="63ac9-105">**Date**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="63ac9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="63ac9-106">Attributes and elements</span></span>

<span data-ttu-id="63ac9-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="63ac9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="63ac9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="63ac9-108">Attributes</span></span>

<span data-ttu-id="63ac9-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="63ac9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="63ac9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="63ac9-110">Child elements</span></span>

<span data-ttu-id="63ac9-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="63ac9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="63ac9-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="63ac9-112">Parent elements</span></span>

|<span data-ttu-id="63ac9-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="63ac9-113">**Element**</span></span>|<span data-ttu-id="63ac9-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="63ac9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="63ac9-115">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="63ac9-115">EndDateRecurrence</span></span>](enddaterecurrence.md) <br/> |<span data-ttu-id="63ac9-116">Describe la fecha de inicio y la fecha de finalización de un patrón de periodicidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="63ac9-116">Describes the start date and the end date of an item recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="63ac9-117">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="63ac9-117">NoEndRecurrence</span></span>](noendrecurrence.md) <br/> |<span data-ttu-id="63ac9-118">Describe la fecha de inicio de un patrón de periodicidad de un elemento que no tiene una fecha de finalización definida.</span><span class="sxs-lookup"><span data-stu-id="63ac9-118">Describes the start date of an item recurrence pattern that does not have a defined end date.</span></span>  <br/> |
|[<span data-ttu-id="63ac9-119">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="63ac9-119">NumberedRecurrence</span></span>](numberedrecurrence.md) <br/> |<span data-ttu-id="63ac9-120">Describe la fecha de inicio y el número de repeticiones de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="63ac9-120">Describes the start date and the number of occurrences of a recurring item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="63ac9-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="63ac9-121">Text value</span></span>

<span data-ttu-id="63ac9-122">Si se usa este elemento, es necesario un valor de texto que represente una fecha.</span><span class="sxs-lookup"><span data-stu-id="63ac9-122">A text value that represents a date is required if this element is used.</span></span> <span data-ttu-id="63ac9-123">El valor no puede ser menor que Apr, 1, 1601 00:00:00.</span><span class="sxs-lookup"><span data-stu-id="63ac9-123">The value cannot be less than Apr, 1, 1601 00:00:00.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="63ac9-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="63ac9-124">Remarks</span></span>

<span data-ttu-id="63ac9-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="63ac9-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="63ac9-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="63ac9-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63ac9-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="63ac9-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="63ac9-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="63ac9-128">Schema name</span></span>  <br/> |<span data-ttu-id="63ac9-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="63ac9-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="63ac9-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="63ac9-130">Validation file</span></span>  <br/> |<span data-ttu-id="63ac9-131">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="63ac9-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="63ac9-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="63ac9-132">Can be empty</span></span>  <br/> |<span data-ttu-id="63ac9-133">Falso</span><span class="sxs-lookup"><span data-stu-id="63ac9-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="63ac9-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="63ac9-134">See also</span></span>

- [<span data-ttu-id="63ac9-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="63ac9-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

