---
title: Definición de zona horaria
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeZoneDefinition
api_type:
- schema
ms.assetid: b005a80c-addb-4409-beff-e5162076752c
description: El elemento de la definición de zona horaria especifica los períodos y las transiciones que definen una zona horaria.
ms.openlocfilehash: ffd5ed0c862af794e4aff2387f508849b1d5fd5d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840688"
---
# <a name="timezonedefinition"></a><span data-ttu-id="425ad-103">Definición de zona horaria</span><span class="sxs-lookup"><span data-stu-id="425ad-103">TimeZoneDefinition</span></span>

<span data-ttu-id="425ad-104">El elemento de la **definición de zona horaria** especifica los períodos y las transiciones que definen una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="425ad-104">The **TimeZoneDefinition** element specifies the periods and transitions that define a time zone.</span></span> 
  
```XML
<TimeZoneDefinition Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</TimeZoneDefinition>

```

 <span data-ttu-id="425ad-105">**TimeZoneDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="425ad-105">**TimeZoneDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="425ad-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="425ad-106">Attributes and elements</span></span>

<span data-ttu-id="425ad-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="425ad-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="425ad-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="425ad-108">Attributes</span></span>

|<span data-ttu-id="425ad-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="425ad-109">**Attribute**</span></span>|<span data-ttu-id="425ad-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="425ad-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="425ad-111">Id</span><span class="sxs-lookup"><span data-stu-id="425ad-111">Id</span></span>  <br/> |<span data-ttu-id="425ad-112">Representa el identificador único de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="425ad-112">Represents the unique identifier of the time zone.</span></span>  <br/> |
|<span data-ttu-id="425ad-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="425ad-113">Name</span></span>  <br/> |<span data-ttu-id="425ad-114">Representa el nombre descriptivo de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="425ad-114">Represents the descriptive name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="425ad-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="425ad-115">Child elements</span></span>

|<span data-ttu-id="425ad-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="425ad-116">**Element**</span></span>|<span data-ttu-id="425ad-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="425ad-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="425ad-118">Períodos</span><span class="sxs-lookup"><span data-stu-id="425ad-118">Periods</span></span>](periods.md) <br/> |<span data-ttu-id="425ad-119">Representa una matriz de elementos de [período](period.md) que definen el desplazamiento de tiempo en diferentes fases de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="425ad-119">Represents an array of [Period](period.md) elements that define the time offset at different stages of the time zone.</span></span>  <br/> |
|[<span data-ttu-id="425ad-120">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="425ad-120">TransitionsGroups</span></span>](transitionsgroups.md) <br/> |<span data-ttu-id="425ad-121">Representa una matriz de elementos de [TransitionsGroup](transitionsgroup.md) que especifican las transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="425ad-121">Represents an array of [TransitionsGroup](transitionsgroup.md) elements that specify time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="425ad-122">Transiciones</span><span class="sxs-lookup"><span data-stu-id="425ad-122">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="425ad-123">Representa una matriz de las transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="425ad-123">Represents an array of time zone transitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="425ad-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="425ad-124">Parent elements</span></span>

|<span data-ttu-id="425ad-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="425ad-125">**Element**</span></span>|<span data-ttu-id="425ad-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="425ad-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="425ad-127">TimeZoneDefinitions</span><span class="sxs-lookup"><span data-stu-id="425ad-127">TimeZoneDefinitions</span></span>](timezonedefinitions.md) <br/> |<span data-ttu-id="425ad-128">Representa una matriz de definiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="425ad-128">Represents an array of time zone definitions.</span></span>  <br/> |
|[<span data-ttu-id="425ad-129">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="425ad-129">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="425ad-130">Representa la definición de zona horaria predeterminada que se utiliza para definir el ámbito de las propiedades de fecha y hora de objetos que se crean, actualizan y recuperados mediante servicios Web de Exchange (EWS).</span><span class="sxs-lookup"><span data-stu-id="425ad-130">Represents the default time zone definition that is to be used for scoping the DateTime properties of objects that are created, updated, and retrieved by using Exchange Web Services (EWS).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="425ad-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="425ad-131">Remarks</span></span>

<span data-ttu-id="425ad-132">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="425ad-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="425ad-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="425ad-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="425ad-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="425ad-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="425ad-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="425ad-135">Schema Name</span></span>  <br/> |<span data-ttu-id="425ad-136">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="425ad-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="425ad-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="425ad-137">Validation File</span></span>  <br/> |<span data-ttu-id="425ad-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="425ad-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="425ad-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="425ad-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="425ad-140">False</span><span class="sxs-lookup"><span data-stu-id="425ad-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="425ad-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="425ad-141">See also</span></span>



- [<span data-ttu-id="425ad-142">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="425ad-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

