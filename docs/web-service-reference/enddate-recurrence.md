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
description: El elemento EndDate representa la fecha de finalización de una tarea recurrente o un elemento de calendario que tiene el tipo de patrón EndDateRecurrence.
ms.openlocfilehash: 53d9b04faf1d8f740c858080b5fcbeadf577df0d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460165"
---
# <a name="enddate-recurrence"></a><span data-ttu-id="e58f1-103">EndDate (periodicidad)</span><span class="sxs-lookup"><span data-stu-id="e58f1-103">EndDate (Recurrence)</span></span>

<span data-ttu-id="e58f1-104">El elemento **EndDate** representa la fecha de finalización de una tarea recurrente o un elemento de calendario que tiene el tipo de patrón EndDateRecurrence.</span><span class="sxs-lookup"><span data-stu-id="e58f1-104">The **EndDate** element represents the end date of a recurring task or a calendar item that has the EndDateRecurrence pattern type.</span></span> 
  
```xml
<EndDate/>
```

 <span data-ttu-id="e58f1-105">**date**</span><span class="sxs-lookup"><span data-stu-id="e58f1-105">**date**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e58f1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e58f1-106">Attributes and elements</span></span>

<span data-ttu-id="e58f1-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e58f1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e58f1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e58f1-108">Attributes</span></span>

<span data-ttu-id="e58f1-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e58f1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e58f1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e58f1-110">Child elements</span></span>

<span data-ttu-id="e58f1-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e58f1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e58f1-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e58f1-112">Parent elements</span></span>

|<span data-ttu-id="e58f1-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e58f1-113">**Element**</span></span>|<span data-ttu-id="e58f1-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e58f1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e58f1-115">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="e58f1-115">EndDateRecurrence</span></span>](enddaterecurrence.md) <br/> |<span data-ttu-id="e58f1-116">Describe la fecha de inicio y la fecha de finalización de un patrón de periodicidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="e58f1-116">Describes the start date and the end date of an item recurrence pattern.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e58f1-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e58f1-117">Text value</span></span>

<span data-ttu-id="e58f1-118">Si se usa este elemento, es necesario un valor de texto que represente una fecha.</span><span class="sxs-lookup"><span data-stu-id="e58f1-118">A text value that represents a date is required if this element is used.</span></span> <span data-ttu-id="e58f1-119">El valor no puede ser superior a 1 de septiembre de 4500 00:00:00.</span><span class="sxs-lookup"><span data-stu-id="e58f1-119">The value cannot be larger than September 1, 4500 00:00:00.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e58f1-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e58f1-120">Remarks</span></span>

<span data-ttu-id="e58f1-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="e58f1-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e58f1-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e58f1-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e58f1-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="e58f1-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e58f1-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e58f1-124">Schema name</span></span>  <br/> |<span data-ttu-id="e58f1-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e58f1-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="e58f1-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e58f1-126">Validation file</span></span>  <br/> |<span data-ttu-id="e58f1-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e58f1-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e58f1-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e58f1-128">Can be empty</span></span>  <br/> |<span data-ttu-id="e58f1-129">Falso</span><span class="sxs-lookup"><span data-stu-id="e58f1-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e58f1-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="e58f1-130">See also</span></span>



- [<span data-ttu-id="e58f1-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e58f1-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

