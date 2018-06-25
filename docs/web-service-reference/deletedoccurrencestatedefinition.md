---
title: DeletedOccurrenceStateDefinition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a9c01c64-e76c-4adc-8b04-88af97bd0cc8
description: El DeletedOccurrenceStateDefinition especifica el estado de una repetición eliminado de un elemento de calendario.
ms.openlocfilehash: ad0434d604ee78ebf1905b60857929e1af4d45f6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764086"
---
# <a name="deletedoccurrencestatedefinition"></a><span data-ttu-id="0329a-103">DeletedOccurrenceStateDefinition</span><span class="sxs-lookup"><span data-stu-id="0329a-103">DeletedOccurrenceStateDefinition</span></span>

<span data-ttu-id="0329a-104">El **DeletedOccurrenceStateDefinition** especifica el estado de una repetición eliminado de un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="0329a-104">The **DeletedOccurrenceStateDefinition** specifies the state for a deleted occurrence of a calendar item.</span></span> 
  
```XML
<DeletedOccurrenceStateDefinition>
    <OccurrenceDate></OccurrenceDate>
    <IsOccurrencePresent></IsOccurrencePresent>
</DeletedOccurrenceStateDefinition>
```

 <span data-ttu-id="0329a-105">**DeletedOccurrenceStateDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="0329a-105">**DeletedOccurrenceStateDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0329a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0329a-106">Attributes and elements</span></span>

<span data-ttu-id="0329a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0329a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0329a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0329a-108">Attributes</span></span>

<span data-ttu-id="0329a-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0329a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0329a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0329a-110">Child elements</span></span>

|<span data-ttu-id="0329a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="0329a-111">**Element**</span></span>|<span data-ttu-id="0329a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0329a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0329a-113">Aparición (transición de la zona horaria)</span><span class="sxs-lookup"><span data-stu-id="0329a-113">Occurrence (Time Zone Transition)</span></span>](occurrence-time-zone-transition.md) <br/> |<span data-ttu-id="0329a-114">Especifica la fecha de la aparición de un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="0329a-114">Specifies the date of the occurrence of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="0329a-115">IsOccurrencePresent</span><span class="sxs-lookup"><span data-stu-id="0329a-115">IsOccurrencePresent</span></span>](isoccurrencepresent.md) <br/> |<span data-ttu-id="0329a-116">Especifica un valor booleano que indica si está presente una ocurrencia en el elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="0329a-116">Specifies a Boolean value that indicates whether an occurrence of the calendar item is present.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0329a-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0329a-117">Parent elements</span></span>

|<span data-ttu-id="0329a-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="0329a-118">**Element**</span></span>|<span data-ttu-id="0329a-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0329a-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0329a-120">StateDefinition</span><span class="sxs-lookup"><span data-stu-id="0329a-120">StateDefinition</span></span>](statedefinition.md) <br/> |<span data-ttu-id="0329a-121">Especifica una definición de estado.</span><span class="sxs-lookup"><span data-stu-id="0329a-121">Specifies a state definition.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0329a-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0329a-122">Remarks</span></span>

<span data-ttu-id="0329a-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0329a-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0329a-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0329a-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0329a-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0329a-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0329a-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0329a-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0329a-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0329a-127">Schema Name</span></span>  <br/> |<span data-ttu-id="0329a-128">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="0329a-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="0329a-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0329a-129">Validation File</span></span>  <br/> |<span data-ttu-id="0329a-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0329a-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="0329a-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0329a-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="0329a-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="0329a-132">See also</span></span>

- [<span data-ttu-id="0329a-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0329a-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

