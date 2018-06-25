---
title: MyResponseType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MyResponseType
api_type:
- schema
ms.assetid: 9741b71d-a310-4520-81d5-3787a1ee630f
description: El elemento MyResponseType contiene el estado de o la respuesta a un elemento de calendario.
ms.openlocfilehash: 3be900ed6d2932699e3e83a0bca2918c016eb689
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836497"
---
# <a name="myresponsetype"></a><span data-ttu-id="a12a9-103">MyResponseType</span><span class="sxs-lookup"><span data-stu-id="a12a9-103">MyResponseType</span></span>

<span data-ttu-id="a12a9-104">El elemento **MyResponseType** contiene el estado de o la respuesta a un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="a12a9-104">The **MyResponseType** element contains the status of or response to a calendar item.</span></span> 
  
```xml
<MyResponseType/>
```

 <span data-ttu-id="a12a9-105">**ResponseTypeType**</span><span class="sxs-lookup"><span data-stu-id="a12a9-105">**ResponseTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a12a9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a12a9-106">Attributes and elements</span></span>

<span data-ttu-id="a12a9-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a12a9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a12a9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a12a9-108">Attributes</span></span>

<span data-ttu-id="a12a9-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a12a9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a12a9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a12a9-110">Child elements</span></span>

<span data-ttu-id="a12a9-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a12a9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a12a9-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a12a9-112">Parent elements</span></span>

|<span data-ttu-id="a12a9-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a12a9-113">**Element**</span></span>|<span data-ttu-id="a12a9-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a12a9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a12a9-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="a12a9-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="a12a9-116">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a12a9-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="a12a9-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="a12a9-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="a12a9-118">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a12a9-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a12a9-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a12a9-119">Text value</span></span>

<span data-ttu-id="a12a9-120">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="a12a9-120">A text value is required.</span></span> <span data-ttu-id="a12a9-121">Los siguientes son los posibles valores de texto para este elemento:</span><span class="sxs-lookup"><span data-stu-id="a12a9-121">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="a12a9-122">Desconocido</span><span class="sxs-lookup"><span data-stu-id="a12a9-122">Unknown</span></span>
    
- <span data-ttu-id="a12a9-123">Organizador</span><span class="sxs-lookup"><span data-stu-id="a12a9-123">Organizer</span></span>
    
- <span data-ttu-id="a12a9-124">Provisional</span><span class="sxs-lookup"><span data-stu-id="a12a9-124">Tentative</span></span>
    
- <span data-ttu-id="a12a9-125">Accept</span><span class="sxs-lookup"><span data-stu-id="a12a9-125">Accept</span></span>
    
- <span data-ttu-id="a12a9-126">Rechazar</span><span class="sxs-lookup"><span data-stu-id="a12a9-126">Decline</span></span>
    
- <span data-ttu-id="a12a9-127">NoResponseReceived</span><span class="sxs-lookup"><span data-stu-id="a12a9-127">NoResponseReceived</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a12a9-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a12a9-128">Remarks</span></span>

<span data-ttu-id="a12a9-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="a12a9-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a12a9-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a12a9-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a12a9-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a12a9-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a12a9-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a12a9-132">Schema name</span></span>  <br/> |<span data-ttu-id="a12a9-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a12a9-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="a12a9-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a12a9-134">Validation file</span></span>  <br/> |<span data-ttu-id="a12a9-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a12a9-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a12a9-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a12a9-136">Can be empty</span></span>  <br/> |<span data-ttu-id="a12a9-137">False</span><span class="sxs-lookup"><span data-stu-id="a12a9-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a12a9-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="a12a9-138">See also</span></span>



- [<span data-ttu-id="a12a9-139">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a12a9-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

