---
title: IntendedFreeBusyStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IntendedFreeBusyStatus
api_type:
- schema
ms.assetid: 0e0fa898-69a4-4c57-8bb2-52f716b5b478
description: El elemento IntendedFreeBusyStatus representa el estado deseado para el elemento de calendario que está asociado con la convocatoria de reunión.
ms.openlocfilehash: 3254becf8c6885f7d6dc401ecf31da149e7de2d4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835945"
---
# <a name="intendedfreebusystatus"></a><span data-ttu-id="b648b-103">IntendedFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="b648b-103">IntendedFreeBusyStatus</span></span>

<span data-ttu-id="b648b-104">El elemento **IntendedFreeBusyStatus** representa el estado deseado para el elemento de calendario que está asociado con la convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="b648b-104">The **IntendedFreeBusyStatus** element represents the intended status for the calendar item that is associated with the meeting request.</span></span> 
  
```xml
<IntendedFreeBusyStatus/>
```

 <span data-ttu-id="b648b-105">**LegacyFreeBusyType**</span><span class="sxs-lookup"><span data-stu-id="b648b-105">**LegacyFreeBusyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b648b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b648b-106">Attributes and elements</span></span>

<span data-ttu-id="b648b-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b648b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b648b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b648b-108">Attributes</span></span>

<span data-ttu-id="b648b-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b648b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b648b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b648b-110">Child elements</span></span>

<span data-ttu-id="b648b-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b648b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b648b-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b648b-112">Parent elements</span></span>

|<span data-ttu-id="b648b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b648b-113">**Element**</span></span>|<span data-ttu-id="b648b-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b648b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b648b-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="b648b-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="b648b-116">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b648b-116">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b648b-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b648b-117">Text value</span></span>

<span data-ttu-id="b648b-118">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="b648b-118">A text value is required.</span></span> <span data-ttu-id="b648b-119">Los siguientes son los valores posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="b648b-119">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="b648b-120">Gratuito</span><span class="sxs-lookup"><span data-stu-id="b648b-120">Free</span></span>
    
- <span data-ttu-id="b648b-121">Provisional</span><span class="sxs-lookup"><span data-stu-id="b648b-121">Tentative</span></span>
    
- <span data-ttu-id="b648b-122">Ocupado</span><span class="sxs-lookup"><span data-stu-id="b648b-122">Busy</span></span>
    
- <span data-ttu-id="b648b-123">FUERA DE LA OFICINA</span><span class="sxs-lookup"><span data-stu-id="b648b-123">OOF</span></span>
    
- <span data-ttu-id="b648b-124">NoData</span><span class="sxs-lookup"><span data-stu-id="b648b-124">NoData</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b648b-125">Notas</span><span class="sxs-lookup"><span data-stu-id="b648b-125">Remarks</span></span>

<span data-ttu-id="b648b-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="b648b-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b648b-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b648b-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b648b-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b648b-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b648b-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b648b-129">Schema Name</span></span>  <br/> |<span data-ttu-id="b648b-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b648b-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="b648b-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b648b-131">Validation File</span></span>  <br/> |<span data-ttu-id="b648b-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b648b-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b648b-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b648b-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="b648b-134">False</span><span class="sxs-lookup"><span data-stu-id="b648b-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b648b-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="b648b-135">See also</span></span>



- [<span data-ttu-id="b648b-136">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b648b-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

