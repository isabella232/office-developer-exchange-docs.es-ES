---
title: DeleteFromFolderStateDefinition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3aba59a0-f12a-48b5-842b-11cf4530dd51
description: El elemento DeleteFromFolderStateDefinition especifica el estado cuando se elimina un elemento de una carpeta.
ms.openlocfilehash: 7b6374b9fa55d3b08569e8ac9e247dd6e5bebc24
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764097"
---
# <a name="deletefromfolderstatedefinition"></a><span data-ttu-id="ff436-103">DeleteFromFolderStateDefinition</span><span class="sxs-lookup"><span data-stu-id="ff436-103">DeleteFromFolderStateDefinition</span></span>

<span data-ttu-id="ff436-104">El elemento **DeleteFromFolderStateDefinition** especifica el estado cuando se elimina un elemento de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="ff436-104">The **DeleteFromFolderStateDefinition** element specifies the state when an item is deleted from a folder.</span></span> 
  
```XML
<DeleteFromFolderStateDefinition>
    <OccurrenceDate></OccurrenceDate>
    <IsOccurrencePresent></IsOccurrencePresent>
</DeleteFromFolderStateDefinition>
```

 <span data-ttu-id="ff436-105">**DeleteFromFolderStateDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="ff436-105">**DeleteFromFolderStateDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ff436-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ff436-106">Attributes and elements</span></span>

<span data-ttu-id="ff436-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ff436-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ff436-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ff436-108">Attributes</span></span>

<span data-ttu-id="ff436-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ff436-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ff436-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ff436-110">Child elements</span></span>

|<span data-ttu-id="ff436-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ff436-111">**Element**</span></span>|<span data-ttu-id="ff436-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ff436-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff436-113">Aparición (transición de la zona horaria)</span><span class="sxs-lookup"><span data-stu-id="ff436-113">Occurrence (Time Zone Transition)</span></span>](occurrence-time-zone-transition.md) <br/> |<span data-ttu-id="ff436-114">Especifica la fecha de la aparición de un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="ff436-114">Specifies the date of the occurrence of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="ff436-115">IsOccurrencePresent</span><span class="sxs-lookup"><span data-stu-id="ff436-115">IsOccurrencePresent</span></span>](isoccurrencepresent.md) <br/> |<span data-ttu-id="ff436-116">Especifica un valor booleano que indica si está presente una ocurrencia en el elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="ff436-116">Specifies a Boolean value that indicates whether an occurrence of the calendar item is present.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ff436-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ff436-117">Parent elements</span></span>

|<span data-ttu-id="ff436-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="ff436-118">**Element**</span></span>|<span data-ttu-id="ff436-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ff436-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff436-120">StateDefinition</span><span class="sxs-lookup"><span data-stu-id="ff436-120">StateDefinition</span></span>](statedefinition.md) <br/> |<span data-ttu-id="ff436-121">Especifica una definición de estado.</span><span class="sxs-lookup"><span data-stu-id="ff436-121">Specifies a state definition.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff436-122">Notas</span><span class="sxs-lookup"><span data-stu-id="ff436-122">Remarks</span></span>

<span data-ttu-id="ff436-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ff436-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ff436-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff436-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ff436-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ff436-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff436-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ff436-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ff436-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ff436-127">Schema Name</span></span>  <br/> |<span data-ttu-id="ff436-128">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="ff436-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="ff436-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ff436-129">Validation File</span></span>  <br/> |<span data-ttu-id="ff436-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ff436-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="ff436-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ff436-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="ff436-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="ff436-132">See also</span></span>

- [<span data-ttu-id="ff436-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="ff436-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

