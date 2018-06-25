---
title: EndDate (periodicidad)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EndDate
api_type:
- schema
ms.assetid: 16026595-26f8-4770-8a6d-0d3e4157effd
description: El elemento EndDate representa la fecha de finalización de una tarea periódica o de un elemento de calendario que tiene el tipo de trama de EndDateRecurrence.
ms.openlocfilehash: b8570a069fc0a2d05044a9c85ab2d5c39d70ccdf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764395"
---
# <a name="enddate-recurrence"></a><span data-ttu-id="d6334-103">EndDate (periodicidad)</span><span class="sxs-lookup"><span data-stu-id="d6334-103">EndDate (Recurrence)</span></span>

<span data-ttu-id="d6334-104">El elemento **EndDate** representa la fecha de finalización de una tarea periódica o de un elemento de calendario que tiene el tipo de trama de EndDateRecurrence.</span><span class="sxs-lookup"><span data-stu-id="d6334-104">The **EndDate** element represents the end date of a recurring task or a calendar item that has the EndDateRecurrence pattern type.</span></span> 
  
```xml
<EndDate/>
```

 <span data-ttu-id="d6334-105">**fecha**</span><span class="sxs-lookup"><span data-stu-id="d6334-105">**date**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d6334-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d6334-106">Attributes and elements</span></span>

<span data-ttu-id="d6334-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d6334-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d6334-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d6334-108">Attributes</span></span>

<span data-ttu-id="d6334-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d6334-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d6334-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d6334-110">Child elements</span></span>

<span data-ttu-id="d6334-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d6334-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d6334-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d6334-112">Parent elements</span></span>

|<span data-ttu-id="d6334-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6334-113">**Element**</span></span>|<span data-ttu-id="d6334-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d6334-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d6334-115">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="d6334-115">EndDateRecurrence</span></span>](enddaterecurrence.md) <br/> |<span data-ttu-id="d6334-116">Describe la fecha de inicio y la fecha de finalización de un patrón de periodicidad de elemento.</span><span class="sxs-lookup"><span data-stu-id="d6334-116">Describes the start date and the end date of an item recurrence pattern.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d6334-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d6334-117">Text value</span></span>

<span data-ttu-id="d6334-118">Si se usa este elemento, es necesario un valor de texto que representa una fecha.</span><span class="sxs-lookup"><span data-stu-id="d6334-118">A text value that represents a date is required if this element is used.</span></span> <span data-ttu-id="d6334-119">El valor no puede ser mayor que 1 de septiembre, 4500 00:00:00.</span><span class="sxs-lookup"><span data-stu-id="d6334-119">The value cannot be larger than September 1, 4500 00:00:00.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d6334-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d6334-120">Remarks</span></span>

<span data-ttu-id="d6334-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="d6334-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d6334-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d6334-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d6334-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d6334-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d6334-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d6334-124">Schema name</span></span>  <br/> |<span data-ttu-id="d6334-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d6334-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="d6334-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d6334-126">Validation file</span></span>  <br/> |<span data-ttu-id="d6334-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d6334-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d6334-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d6334-128">Can be empty</span></span>  <br/> |<span data-ttu-id="d6334-129">False</span><span class="sxs-lookup"><span data-stu-id="d6334-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d6334-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6334-130">See also</span></span>



- [<span data-ttu-id="d6334-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d6334-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

