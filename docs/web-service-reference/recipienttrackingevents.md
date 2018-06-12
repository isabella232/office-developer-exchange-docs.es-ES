---
title: RecipientTrackingEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecipientTrackingEvents
api_type:
- schema
ms.assetid: c4f729aa-674e-43b2-97f2-bf49740b0a34
description: El elemento RecipientTrackingEvents representa una colección de uno o más eventos para un mensaje.
ms.openlocfilehash: 5fa5df422eff533891d021b77d5443b314d36244
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836993"
---
# <a name="recipienttrackingevents"></a><span data-ttu-id="b660d-103">RecipientTrackingEvents</span><span class="sxs-lookup"><span data-stu-id="b660d-103">RecipientTrackingEvents</span></span>

<span data-ttu-id="b660d-104">El elemento **RecipientTrackingEvents** representa una colección de uno o más eventos para un mensaje.</span><span class="sxs-lookup"><span data-stu-id="b660d-104">The **RecipientTrackingEvents** element represents a collection of one or more events for a message.</span></span> 
  
```XML
<RecipientTrackingEvents>
   <RecipientTrackingEvent/>
</RecipientTrackingEvents>
```

 <span data-ttu-id="b660d-105">**ArrayOfRecipientTrackingEventType**</span><span class="sxs-lookup"><span data-stu-id="b660d-105">**ArrayOfRecipientTrackingEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b660d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b660d-106">Attributes and elements</span></span>

<span data-ttu-id="b660d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b660d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b660d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b660d-108">Attributes</span></span>

<span data-ttu-id="b660d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b660d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b660d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b660d-110">Child elements</span></span>

|<span data-ttu-id="b660d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b660d-111">**Element**</span></span>|<span data-ttu-id="b660d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b660d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b660d-113">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="b660d-113">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="b660d-114">Contiene los detalles de un evento específico en el informe de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="b660d-114">Contains details for a specific event in the tracking report.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b660d-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b660d-115">Parent elements</span></span>

|<span data-ttu-id="b660d-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="b660d-116">**Element**</span></span>|<span data-ttu-id="b660d-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b660d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b660d-118">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="b660d-118">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="b660d-119">Contiene un solo mensaje que se devuelve en una [operación de GetMessageTrackingReport](getmessagetrackingreport-operation.md).</span><span class="sxs-lookup"><span data-stu-id="b660d-119">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b660d-120">Notas</span><span class="sxs-lookup"><span data-stu-id="b660d-120">Remarks</span></span>

<span data-ttu-id="b660d-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b660d-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b660d-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b660d-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b660d-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b660d-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b660d-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b660d-124">Schema Name</span></span>  <br/> |<span data-ttu-id="b660d-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b660d-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="b660d-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b660d-126">Validation File</span></span>  <br/> |<span data-ttu-id="b660d-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b660d-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b660d-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b660d-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="b660d-129">False</span><span class="sxs-lookup"><span data-stu-id="b660d-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b660d-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="b660d-130">See also</span></span>



[<span data-ttu-id="b660d-131">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="b660d-131">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="b660d-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b660d-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

