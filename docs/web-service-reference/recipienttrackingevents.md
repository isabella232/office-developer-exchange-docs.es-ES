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
ms.openlocfilehash: c0b25a0e22d13bc1f26768b9b7089d96eb2e8cfc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468484"
---
# <a name="recipienttrackingevents"></a><span data-ttu-id="ea827-103">RecipientTrackingEvents</span><span class="sxs-lookup"><span data-stu-id="ea827-103">RecipientTrackingEvents</span></span>

<span data-ttu-id="ea827-104">El elemento **RecipientTrackingEvents** representa una colección de uno o más eventos para un mensaje.</span><span class="sxs-lookup"><span data-stu-id="ea827-104">The **RecipientTrackingEvents** element represents a collection of one or more events for a message.</span></span> 
  
```XML
<RecipientTrackingEvents>
   <RecipientTrackingEvent/>
</RecipientTrackingEvents>
```

 <span data-ttu-id="ea827-105">**ArrayOfRecipientTrackingEventType**</span><span class="sxs-lookup"><span data-stu-id="ea827-105">**ArrayOfRecipientTrackingEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ea827-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ea827-106">Attributes and elements</span></span>

<span data-ttu-id="ea827-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ea827-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ea827-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ea827-108">Attributes</span></span>

<span data-ttu-id="ea827-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ea827-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ea827-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ea827-110">Child elements</span></span>

|<span data-ttu-id="ea827-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ea827-111">**Element**</span></span>|<span data-ttu-id="ea827-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ea827-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ea827-113">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="ea827-113">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="ea827-114">Contiene los detalles de un evento específico en el informe de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="ea827-114">Contains details for a specific event in the tracking report.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ea827-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ea827-115">Parent elements</span></span>

|<span data-ttu-id="ea827-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ea827-116">**Element**</span></span>|<span data-ttu-id="ea827-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ea827-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ea827-118">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="ea827-118">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="ea827-119">Contiene un solo mensaje que se devuelve en una [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md).</span><span class="sxs-lookup"><span data-stu-id="ea827-119">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea827-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ea827-120">Remarks</span></span>

<span data-ttu-id="ea827-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ea827-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ea827-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ea827-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ea827-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="ea827-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ea827-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ea827-124">Schema Name</span></span>  <br/> |<span data-ttu-id="ea827-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ea827-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="ea827-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ea827-126">Validation File</span></span>  <br/> |<span data-ttu-id="ea827-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ea827-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ea827-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ea827-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="ea827-129">Falso</span><span class="sxs-lookup"><span data-stu-id="ea827-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ea827-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea827-130">See also</span></span>



[<span data-ttu-id="ea827-131">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="ea827-131">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="ea827-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ea827-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

