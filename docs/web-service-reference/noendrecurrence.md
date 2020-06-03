---
title: NoEndRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NoEndRecurrence
api_type:
- schema
ms.assetid: ab2ebd9c-388e-45f1-abf9-56e293ef123b
description: El elemento NoEndRecurrence describe la fecha de inicio de un patrón de periodicidad de un elemento que no tiene una fecha de finalización definida.
ms.openlocfilehash: 31a3bd6ae2d7ce94debbeebc4fd4f536447433a7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466797"
---
# <a name="noendrecurrence"></a><span data-ttu-id="0a583-103">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="0a583-103">NoEndRecurrence</span></span>

<span data-ttu-id="0a583-104">El elemento **NoEndRecurrence** describe la fecha de inicio de un patrón de periodicidad de un elemento que no tiene una fecha de finalización definida.</span><span class="sxs-lookup"><span data-stu-id="0a583-104">The **NoEndRecurrence** element describes the start date of an item recurrence pattern that does not have a defined end date.</span></span> 
  
```xml
<NoEndRecurrence>
   <StartDate/>
</NoEndRecurrence>
```

 <span data-ttu-id="0a583-105">**NoEndRecurrenceRangeType**</span><span class="sxs-lookup"><span data-stu-id="0a583-105">**NoEndRecurrenceRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0a583-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0a583-106">Attributes and elements</span></span>

<span data-ttu-id="0a583-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0a583-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0a583-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0a583-108">Attributes</span></span>

<span data-ttu-id="0a583-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0a583-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0a583-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0a583-110">Child elements</span></span>

|<span data-ttu-id="0a583-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0a583-111">**Element**</span></span>|<span data-ttu-id="0a583-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0a583-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0a583-113">StartDate (periodicidad)</span><span class="sxs-lookup"><span data-stu-id="0a583-113">StartDate (Recurrence)</span></span>](startdate-recurrence.md) <br/> |<span data-ttu-id="0a583-114">Representa la fecha de inicio de una tarea periódica o un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="0a583-114">Represents the start date of a recurring task or calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0a583-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0a583-115">Parent elements</span></span>

|<span data-ttu-id="0a583-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0a583-116">**Element**</span></span>|<span data-ttu-id="0a583-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0a583-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0a583-118">Recurrence (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="0a583-118">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="0a583-119">Contiene el patrón de periodicidad para los elementos de calendario y las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="0a583-119">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="0a583-120">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="0a583-120">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="0a583-121">Contiene información de periodicidad para tareas periódicas.</span><span class="sxs-lookup"><span data-stu-id="0a583-121">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a583-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0a583-122">Remarks</span></span>

<span data-ttu-id="0a583-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="0a583-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0a583-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0a583-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0a583-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="0a583-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0a583-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0a583-126">Schema name</span></span>  <br/> |<span data-ttu-id="0a583-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0a583-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="0a583-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0a583-128">Validation file</span></span>  <br/> |<span data-ttu-id="0a583-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="0a583-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0a583-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0a583-130">Can be empty</span></span>  <br/> |<span data-ttu-id="0a583-131">Falso</span><span class="sxs-lookup"><span data-stu-id="0a583-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0a583-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a583-132">See also</span></span>



- [<span data-ttu-id="0a583-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0a583-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

