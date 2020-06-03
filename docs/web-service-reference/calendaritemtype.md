---
title: CalendarItemType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarItemType
api_type:
- schema
ms.assetid: 1feb0788-adf7-4a7c-830c-005214ad930f
description: El elemento CalendarItemType representa el tipo de un elemento de calendario.
ms.openlocfilehash: 05e93b6db3ae574c03f6e43c5ebec2288edec3e5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527197"
---
# <a name="calendaritemtype"></a><span data-ttu-id="cb7dd-103">CalendarItemType</span><span class="sxs-lookup"><span data-stu-id="cb7dd-103">CalendarItemType</span></span>

<span data-ttu-id="cb7dd-104">El elemento **CalendarItemType** representa el tipo de un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="cb7dd-104">The **CalendarItemType** element represents the type of a calendar item.</span></span> 
  
```xml
<CalendarItemType/>
```

 <span data-ttu-id="cb7dd-105">**CalendarItemTypeType**</span><span class="sxs-lookup"><span data-stu-id="cb7dd-105">**CalendarItemTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cb7dd-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cb7dd-106">Attributes and elements</span></span>

<span data-ttu-id="cb7dd-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cb7dd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb7dd-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="cb7dd-108">Attributes</span></span>

<span data-ttu-id="cb7dd-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cb7dd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cb7dd-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cb7dd-110">Child elements</span></span>

<span data-ttu-id="cb7dd-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cb7dd-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cb7dd-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cb7dd-112">Parent elements</span></span>

|<span data-ttu-id="cb7dd-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cb7dd-113">**Element**</span></span>|<span data-ttu-id="cb7dd-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cb7dd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb7dd-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="cb7dd-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="cb7dd-116">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cb7dd-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="cb7dd-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="cb7dd-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="cb7dd-118">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cb7dd-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cb7dd-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="cb7dd-119">Text value</span></span>

<span data-ttu-id="cb7dd-120">Es necesario un valor de texto si se usa este elemento.</span><span class="sxs-lookup"><span data-stu-id="cb7dd-120">A text value is required if this element is used.</span></span> <span data-ttu-id="cb7dd-121">A continuación se muestran los valores posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="cb7dd-121">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="cb7dd-122">**Un solo** El elemento no está asociado a un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="cb7dd-122">**Single** The item is not associated with a recurring calendar item.</span></span> 
    
- <span data-ttu-id="cb7dd-123">**Ocurrencia** El elemento es una ocurrencia de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="cb7dd-123">**Occurrence** The item is an occurrence of a recurring calendar item.</span></span> 
    
- <span data-ttu-id="cb7dd-124">**Excepción** El elemento es una excepción a un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="cb7dd-124">**Exception** The item is an exception to a recurring calendar item.</span></span> 
    
- <span data-ttu-id="cb7dd-125">**RecurringMaster** El elemento es principal para un conjunto de elementos de calendario periódicos.</span><span class="sxs-lookup"><span data-stu-id="cb7dd-125">**RecurringMaster** The item is master for a set of recurring calendar items.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cb7dd-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cb7dd-126">Remarks</span></span>

<span data-ttu-id="cb7dd-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="cb7dd-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cb7dd-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cb7dd-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb7dd-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="cb7dd-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cb7dd-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cb7dd-130">Schema name</span></span>  <br/> |<span data-ttu-id="cb7dd-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="cb7dd-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="cb7dd-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cb7dd-132">Validation file</span></span>  <br/> |<span data-ttu-id="cb7dd-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="cb7dd-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cb7dd-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cb7dd-134">Can be empty</span></span>  <br/> |<span data-ttu-id="cb7dd-135">Falso</span><span class="sxs-lookup"><span data-stu-id="cb7dd-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb7dd-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb7dd-136">See also</span></span>



- [<span data-ttu-id="cb7dd-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="cb7dd-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

