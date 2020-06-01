---
title: TimeZoneDefinition
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
description: El elemento TimeZoneDefinition especifica los períodos y las transiciones que definen una zona horaria.
ms.openlocfilehash: 58d34556686bfc77244b5829798eada51a1df843
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466069"
---
# <a name="timezonedefinition"></a><span data-ttu-id="9080e-103">TimeZoneDefinition</span><span class="sxs-lookup"><span data-stu-id="9080e-103">TimeZoneDefinition</span></span>

<span data-ttu-id="9080e-104">El elemento **TimeZoneDefinition** especifica los períodos y las transiciones que definen una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="9080e-104">The **TimeZoneDefinition** element specifies the periods and transitions that define a time zone.</span></span> 
  
```XML
<TimeZoneDefinition Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</TimeZoneDefinition>

```

 <span data-ttu-id="9080e-105">**TimeZoneDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="9080e-105">**TimeZoneDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9080e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9080e-106">Attributes and elements</span></span>

<span data-ttu-id="9080e-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9080e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9080e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9080e-108">Attributes</span></span>

|<span data-ttu-id="9080e-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="9080e-109">**Attribute**</span></span>|<span data-ttu-id="9080e-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9080e-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9080e-111">Id</span><span class="sxs-lookup"><span data-stu-id="9080e-111">Id</span></span>  <br/> |<span data-ttu-id="9080e-112">Representa el identificador único de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="9080e-112">Represents the unique identifier of the time zone.</span></span>  <br/> |
|<span data-ttu-id="9080e-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="9080e-113">Name</span></span>  <br/> |<span data-ttu-id="9080e-114">Representa el nombre descriptivo de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="9080e-114">Represents the descriptive name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9080e-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9080e-115">Child elements</span></span>

|<span data-ttu-id="9080e-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9080e-116">**Element**</span></span>|<span data-ttu-id="9080e-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9080e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9080e-118">Períodos</span><span class="sxs-lookup"><span data-stu-id="9080e-118">Periods</span></span>](periods.md) <br/> |<span data-ttu-id="9080e-119">Representa una matriz de elementos [period](period.md) que define el desplazamiento de tiempo en diferentes etapas de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="9080e-119">Represents an array of [Period](period.md) elements that define the time offset at different stages of the time zone.</span></span>  <br/> |
|[<span data-ttu-id="9080e-120">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="9080e-120">TransitionsGroups</span></span>](transitionsgroups.md) <br/> |<span data-ttu-id="9080e-121">Representa una matriz de elementos [TransitionsGroup](transitionsgroup.md) que especifican las transiciones de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="9080e-121">Represents an array of [TransitionsGroup](transitionsgroup.md) elements that specify time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="9080e-122">Transiciones</span><span class="sxs-lookup"><span data-stu-id="9080e-122">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="9080e-123">Representa una matriz de transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="9080e-123">Represents an array of time zone transitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9080e-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9080e-124">Parent elements</span></span>

|<span data-ttu-id="9080e-125">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9080e-125">**Element**</span></span>|<span data-ttu-id="9080e-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9080e-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9080e-127">TimeZoneDefinitions</span><span class="sxs-lookup"><span data-stu-id="9080e-127">TimeZoneDefinitions</span></span>](timezonedefinitions.md) <br/> |<span data-ttu-id="9080e-128">Representa una matriz de definiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="9080e-128">Represents an array of time zone definitions.</span></span>  <br/> |
|[<span data-ttu-id="9080e-129">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="9080e-129">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="9080e-130">Representa la definición de zona horaria predeterminada que se va a usar para establecer el ámbito de las propiedades DateTime de los objetos que se crean, actualizan y recuperan mediante los servicios web Exchange (EWS).</span><span class="sxs-lookup"><span data-stu-id="9080e-130">Represents the default time zone definition that is to be used for scoping the DateTime properties of objects that are created, updated, and retrieved by using Exchange Web Services (EWS).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9080e-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9080e-131">Remarks</span></span>

<span data-ttu-id="9080e-132">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="9080e-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9080e-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9080e-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9080e-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="9080e-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9080e-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9080e-135">Schema Name</span></span>  <br/> |<span data-ttu-id="9080e-136">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="9080e-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="9080e-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9080e-137">Validation File</span></span>  <br/> |<span data-ttu-id="9080e-138">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="9080e-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9080e-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9080e-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="9080e-140">Falso</span><span class="sxs-lookup"><span data-stu-id="9080e-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9080e-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="9080e-141">See also</span></span>



- [<span data-ttu-id="9080e-142">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="9080e-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

