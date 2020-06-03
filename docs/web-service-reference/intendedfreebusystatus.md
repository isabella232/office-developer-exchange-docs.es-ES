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
description: El elemento IntendedFreeBusyStatus representa el estado previsto para el elemento de calendario que está asociado a la convocatoria de reunión.
ms.openlocfilehash: c5502bcfb308aa2f02a9575ab43f80261b5fa4ed
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465621"
---
# <a name="intendedfreebusystatus"></a><span data-ttu-id="3ac21-103">IntendedFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="3ac21-103">IntendedFreeBusyStatus</span></span>

<span data-ttu-id="3ac21-104">El elemento **IntendedFreeBusyStatus** representa el estado previsto para el elemento de calendario que está asociado a la convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="3ac21-104">The **IntendedFreeBusyStatus** element represents the intended status for the calendar item that is associated with the meeting request.</span></span> 
  
```xml
<IntendedFreeBusyStatus/>
```

 <span data-ttu-id="3ac21-105">**LegacyFreeBusyType**</span><span class="sxs-lookup"><span data-stu-id="3ac21-105">**LegacyFreeBusyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3ac21-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3ac21-106">Attributes and elements</span></span>

<span data-ttu-id="3ac21-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3ac21-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3ac21-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3ac21-108">Attributes</span></span>

<span data-ttu-id="3ac21-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3ac21-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3ac21-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3ac21-110">Child elements</span></span>

<span data-ttu-id="3ac21-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3ac21-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3ac21-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3ac21-112">Parent elements</span></span>

|<span data-ttu-id="3ac21-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3ac21-113">**Element**</span></span>|<span data-ttu-id="3ac21-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3ac21-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3ac21-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="3ac21-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="3ac21-116">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3ac21-116">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3ac21-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3ac21-117">Text value</span></span>

<span data-ttu-id="3ac21-118">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="3ac21-118">A text value is required.</span></span> <span data-ttu-id="3ac21-119">A continuación se muestran los valores posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="3ac21-119">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="3ac21-120">Libre</span><span class="sxs-lookup"><span data-stu-id="3ac21-120">Free</span></span>
    
- <span data-ttu-id="3ac21-121">Provisional</span><span class="sxs-lookup"><span data-stu-id="3ac21-121">Tentative</span></span>
    
- <span data-ttu-id="3ac21-122">Ocupado</span><span class="sxs-lookup"><span data-stu-id="3ac21-122">Busy</span></span>
    
- <span data-ttu-id="3ac21-123">Oficina</span><span class="sxs-lookup"><span data-stu-id="3ac21-123">OOF</span></span>
    
- <span data-ttu-id="3ac21-124">NoData</span><span class="sxs-lookup"><span data-stu-id="3ac21-124">NoData</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3ac21-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3ac21-125">Remarks</span></span>

<span data-ttu-id="3ac21-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="3ac21-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3ac21-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3ac21-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ac21-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="3ac21-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3ac21-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3ac21-129">Schema Name</span></span>  <br/> |<span data-ttu-id="3ac21-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="3ac21-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="3ac21-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3ac21-131">Validation File</span></span>  <br/> |<span data-ttu-id="3ac21-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="3ac21-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3ac21-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3ac21-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="3ac21-134">Falso</span><span class="sxs-lookup"><span data-stu-id="3ac21-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3ac21-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ac21-135">See also</span></span>



- [<span data-ttu-id="3ac21-136">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="3ac21-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

