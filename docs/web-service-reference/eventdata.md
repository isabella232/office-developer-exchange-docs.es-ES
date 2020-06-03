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
description: El elemento EventData representa los datos asociados con el paso de procesamiento del evento.
ms.openlocfilehash: ef5da21a3300a6939c60d62584b46ca48b071853
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526182"
---
# <a name="eventdata"></a><span data-ttu-id="4716a-103">EventData</span><span class="sxs-lookup"><span data-stu-id="4716a-103">EventData</span></span>

<span data-ttu-id="4716a-104">El elemento **EventData** representa los datos asociados con el paso de procesamiento del evento.</span><span class="sxs-lookup"><span data-stu-id="4716a-104">The **EventData** element represents data that is associated with the processing step for the event.</span></span> 
  
```XML
<EventData>
   <String/>
</EventData>
```

 <span data-ttu-id="4716a-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="4716a-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4716a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4716a-106">Attributes and elements</span></span>

<span data-ttu-id="4716a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4716a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4716a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4716a-108">Attributes</span></span>

<span data-ttu-id="4716a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4716a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4716a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4716a-110">Child elements</span></span>

|<span data-ttu-id="4716a-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4716a-111">**Element**</span></span>|<span data-ttu-id="4716a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4716a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4716a-113">String</span><span class="sxs-lookup"><span data-stu-id="4716a-113">String</span></span>](string.md) <br/> |<span data-ttu-id="4716a-114">Contiene una cadena que identifica un evento.</span><span class="sxs-lookup"><span data-stu-id="4716a-114">Contains a string that identifies an event.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4716a-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4716a-115">Parent elements</span></span>

|<span data-ttu-id="4716a-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4716a-116">**Element**</span></span>|<span data-ttu-id="4716a-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4716a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4716a-118">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="4716a-118">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="4716a-119">Contiene información de un evento único para un destinatario.</span><span class="sxs-lookup"><span data-stu-id="4716a-119">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4716a-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4716a-120">Text value</span></span>

<span data-ttu-id="4716a-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4716a-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4716a-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4716a-122">Remarks</span></span>

<span data-ttu-id="4716a-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="4716a-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4716a-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4716a-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4716a-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="4716a-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4716a-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4716a-126">Schema Name</span></span>  <br/> |<span data-ttu-id="4716a-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4716a-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="4716a-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4716a-128">Validation File</span></span>  <br/> |<span data-ttu-id="4716a-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="4716a-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4716a-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4716a-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="4716a-131">Falso</span><span class="sxs-lookup"><span data-stu-id="4716a-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4716a-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="4716a-132">See also</span></span>



- [<span data-ttu-id="4716a-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4716a-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

