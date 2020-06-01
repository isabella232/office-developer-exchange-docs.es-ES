---
title: DeletedOccurrenceStateDefinition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a9c01c64-e76c-4adc-8b04-88af97bd0cc8
description: DeletedOccurrenceStateDefinition especifica el estado de una ocurrencia eliminada de un elemento de calendario.
ms.openlocfilehash: ff8ad1d9c35d7bab3f6fe2cd1896bb16384c18e6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458799"
---
# <a name="deletedoccurrencestatedefinition"></a><span data-ttu-id="1d1bf-103">DeletedOccurrenceStateDefinition</span><span class="sxs-lookup"><span data-stu-id="1d1bf-103">DeletedOccurrenceStateDefinition</span></span>

<span data-ttu-id="1d1bf-104">**DeletedOccurrenceStateDefinition** especifica el estado de una ocurrencia eliminada de un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="1d1bf-104">The **DeletedOccurrenceStateDefinition** specifies the state for a deleted occurrence of a calendar item.</span></span> 
  
```XML
<DeletedOccurrenceStateDefinition>
    <OccurrenceDate></OccurrenceDate>
    <IsOccurrencePresent></IsOccurrencePresent>
</DeletedOccurrenceStateDefinition>
```

 <span data-ttu-id="1d1bf-105">**DeletedOccurrenceStateDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="1d1bf-105">**DeletedOccurrenceStateDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1d1bf-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1d1bf-106">Attributes and elements</span></span>

<span data-ttu-id="1d1bf-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1d1bf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1d1bf-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1d1bf-108">Attributes</span></span>

<span data-ttu-id="1d1bf-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1d1bf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1d1bf-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1d1bf-110">Child elements</span></span>

|<span data-ttu-id="1d1bf-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1d1bf-111">**Element**</span></span>|<span data-ttu-id="1d1bf-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d1bf-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d1bf-113">Aparición (transición de zona horaria)</span><span class="sxs-lookup"><span data-stu-id="1d1bf-113">Occurrence (Time Zone Transition)</span></span>](occurrence-time-zone-transition.md) <br/> |<span data-ttu-id="1d1bf-114">Especifica la fecha de la ocurrencia de un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="1d1bf-114">Specifies the date of the occurrence of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="1d1bf-115">IsOccurrencePresent</span><span class="sxs-lookup"><span data-stu-id="1d1bf-115">IsOccurrencePresent</span></span>](isoccurrencepresent.md) <br/> |<span data-ttu-id="1d1bf-116">Especifica un valor booleano que indica si existe una ocurrencia del elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="1d1bf-116">Specifies a Boolean value that indicates whether an occurrence of the calendar item is present.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1d1bf-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1d1bf-117">Parent elements</span></span>

|<span data-ttu-id="1d1bf-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1d1bf-118">**Element**</span></span>|<span data-ttu-id="1d1bf-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d1bf-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d1bf-120">StateDefinition</span><span class="sxs-lookup"><span data-stu-id="1d1bf-120">StateDefinition</span></span>](statedefinition.md) <br/> |<span data-ttu-id="1d1bf-121">Especifica una definición de estado.</span><span class="sxs-lookup"><span data-stu-id="1d1bf-121">Specifies a state definition.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d1bf-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1d1bf-122">Remarks</span></span>

<span data-ttu-id="1d1bf-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1d1bf-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1d1bf-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="1d1bf-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1d1bf-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1d1bf-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d1bf-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="1d1bf-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1d1bf-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1d1bf-127">Schema Name</span></span>  <br/> |<span data-ttu-id="1d1bf-128">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="1d1bf-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="1d1bf-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1d1bf-129">Validation File</span></span>  <br/> |<span data-ttu-id="1d1bf-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1d1bf-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="1d1bf-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1d1bf-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="1d1bf-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d1bf-132">See also</span></span>

- [<span data-ttu-id="1d1bf-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1d1bf-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

