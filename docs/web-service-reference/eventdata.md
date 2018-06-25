---
title: EventData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EventData
api_type:
- schema
ms.assetid: 74acdbad-d6ee-47e6-82fb-e45ecaaa0500
description: El elemento EventData representa los datos que está asociadas con el paso de procesamiento para el evento.
ms.openlocfilehash: 2bf38cd4fd956580b31b6e455b947066f07f5593
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764453"
---
# <a name="eventdata"></a><span data-ttu-id="d543e-103">EventData</span><span class="sxs-lookup"><span data-stu-id="d543e-103">EventData</span></span>

<span data-ttu-id="d543e-104">El elemento **EventData** representa los datos que está asociadas con el paso de procesamiento para el evento.</span><span class="sxs-lookup"><span data-stu-id="d543e-104">The **EventData** element represents data that is associated with the processing step for the event.</span></span> 
  
```XML
<EventData>
   <String/>
</EventData>
```

 <span data-ttu-id="d543e-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="d543e-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d543e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d543e-106">Attributes and elements</span></span>

<span data-ttu-id="d543e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d543e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d543e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d543e-108">Attributes</span></span>

<span data-ttu-id="d543e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d543e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d543e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d543e-110">Child elements</span></span>

|<span data-ttu-id="d543e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d543e-111">**Element**</span></span>|<span data-ttu-id="d543e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d543e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d543e-113">String</span><span class="sxs-lookup"><span data-stu-id="d543e-113">String</span></span>](string.md) <br/> |<span data-ttu-id="d543e-114">Contiene una cadena que identifica un evento.</span><span class="sxs-lookup"><span data-stu-id="d543e-114">Contains a string that identifies an event.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d543e-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d543e-115">Parent elements</span></span>

|<span data-ttu-id="d543e-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="d543e-116">**Element**</span></span>|<span data-ttu-id="d543e-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d543e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d543e-118">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="d543e-118">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="d543e-119">Contiene información de un solo evento de un destinatario.</span><span class="sxs-lookup"><span data-stu-id="d543e-119">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d543e-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d543e-120">Text value</span></span>

<span data-ttu-id="d543e-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d543e-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d543e-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d543e-122">Remarks</span></span>

<span data-ttu-id="d543e-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d543e-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d543e-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d543e-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d543e-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d543e-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d543e-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d543e-126">Schema Name</span></span>  <br/> |<span data-ttu-id="d543e-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d543e-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="d543e-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d543e-128">Validation File</span></span>  <br/> |<span data-ttu-id="d543e-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d543e-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d543e-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d543e-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="d543e-131">False</span><span class="sxs-lookup"><span data-stu-id="d543e-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d543e-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="d543e-132">See also</span></span>



- [<span data-ttu-id="d543e-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d543e-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

