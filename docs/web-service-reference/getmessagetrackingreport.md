---
title: GetMessageTrackingReport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetMessageTrackingReport
api_type:
- schema
ms.assetid: b6ffa8ef-90f6-402d-afac-c3f5ee55cf49
description: El elemento GetMessageTrackingReport contiene la solicitud de la operación GetMessageTrackingReport para recuperar el informe completo de seguimiento de mensajes del identificador especificado.
ms.openlocfilehash: 30596acd209580147e0f03e12a7868502159b29c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466580"
---
# <a name="getmessagetrackingreport"></a><span data-ttu-id="0fdbf-103">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="0fdbf-103">GetMessageTrackingReport</span></span>

<span data-ttu-id="0fdbf-104">El elemento **GetMessageTrackingReport** contiene la solicitud de la [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md) para recuperar el informe completo de seguimiento de mensajes del identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="0fdbf-104">The **GetMessageTrackingReport** element contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span> 
  
```XML
<GetMessageTrackingReport>
   <Scope/>
   <ReportTemplate/>
   <RecipientFilter/>
   <MessageTrackingReportId/>
   <ReturnQueueEvents/>
   <DiagnosticsLevel/>
   <Properties/>
</GetMessageTrackingReport>
```

 <span data-ttu-id="0fdbf-105">**GetMessageTrackingReportRequestType**</span><span class="sxs-lookup"><span data-stu-id="0fdbf-105">**GetMessageTrackingReportRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0fdbf-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0fdbf-106">Attributes and elements</span></span>

<span data-ttu-id="0fdbf-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0fdbf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0fdbf-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0fdbf-108">Attributes</span></span>

<span data-ttu-id="0fdbf-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0fdbf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0fdbf-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0fdbf-110">Child elements</span></span>

|<span data-ttu-id="0fdbf-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0fdbf-111">**Element**</span></span>|<span data-ttu-id="0fdbf-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0fdbf-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0fdbf-113">Ámbito (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="0fdbf-113">Scope (NonEmptyStringType)</span></span>](scope-nonemptystringtype.md) <br/> |<span data-ttu-id="0fdbf-114">Especifica dónde se va a realizar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="0fdbf-114">Specifies where to perform the search.</span></span> <span data-ttu-id="0fdbf-115">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="0fdbf-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="0fdbf-116">ReportTemplate</span><span class="sxs-lookup"><span data-stu-id="0fdbf-116">ReportTemplate</span></span>](reporttemplate.md) <br/> |<span data-ttu-id="0fdbf-117">Especifica el tipo de informe de seguimiento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="0fdbf-117">Specifies the type of tracking report to retrieve.</span></span> <span data-ttu-id="0fdbf-118">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="0fdbf-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="0fdbf-119">RecipientFilter</span><span class="sxs-lookup"><span data-stu-id="0fdbf-119">RecipientFilter</span></span>](recipientfilter.md) <br/> |<span data-ttu-id="0fdbf-120">Especifica la dirección del destinatario que se va a usar con el informe de seguimiento especificado.</span><span class="sxs-lookup"><span data-stu-id="0fdbf-120">Specifies a recipient address to use with the specified tracking report.</span></span> <span data-ttu-id="0fdbf-121">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="0fdbf-121">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="0fdbf-122">MessageTrackingReportId</span><span class="sxs-lookup"><span data-stu-id="0fdbf-122">MessageTrackingReportId</span></span>](messagetrackingreportid.md) <br/> |<span data-ttu-id="0fdbf-123">Especifica una cadena de identidad obtenida de la operación **FindMessageTrackingReport** .</span><span class="sxs-lookup"><span data-stu-id="0fdbf-123">Specifies an identity string that was obtained from the **FindMessageTrackingReport** operation.</span></span> <span data-ttu-id="0fdbf-124">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="0fdbf-124">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="0fdbf-125">ReturnQueueEvents</span><span class="sxs-lookup"><span data-stu-id="0fdbf-125">ReturnQueueEvents</span></span>](returnqueueevents.md) <br/> |<span data-ttu-id="0fdbf-126">Especifica que la persona que ejecuta la tarea tiene un rol privilegiado.</span><span class="sxs-lookup"><span data-stu-id="0fdbf-126">Specifies that the person who is running the task has a privileged role.</span></span> <span data-ttu-id="0fdbf-127">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="0fdbf-127">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="0fdbf-128">DiagnosticsLevel</span><span class="sxs-lookup"><span data-stu-id="0fdbf-128">DiagnosticsLevel</span></span>](diagnosticslevel.md) <br/> |<span data-ttu-id="0fdbf-129">Especifica la información de tiempo y rendimiento que se usará para derivar el informe de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="0fdbf-129">Specifies timing and performance information that will be used to derive the tracking report.</span></span> <span data-ttu-id="0fdbf-130">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="0fdbf-130">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="0fdbf-131">Propiedades (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="0fdbf-131">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="0fdbf-132">Especifica una lista de una o varias propiedades de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="0fdbf-132">Specifies a list of one or more tracking properties.</span></span> <span data-ttu-id="0fdbf-133">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="0fdbf-133">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0fdbf-134">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0fdbf-134">Parent elements</span></span>

<span data-ttu-id="0fdbf-135">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0fdbf-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0fdbf-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0fdbf-136">Remarks</span></span>

<span data-ttu-id="0fdbf-137">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0fdbf-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0fdbf-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0fdbf-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0fdbf-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0fdbf-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0fdbf-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0fdbf-140">Schema Name</span></span>  <br/> |<span data-ttu-id="0fdbf-141">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="0fdbf-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0fdbf-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0fdbf-142">Validation File</span></span>  <br/> |<span data-ttu-id="0fdbf-143">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="0fdbf-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0fdbf-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0fdbf-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="0fdbf-145">Falso</span><span class="sxs-lookup"><span data-stu-id="0fdbf-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0fdbf-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="0fdbf-146">See also</span></span>



[<span data-ttu-id="0fdbf-147">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="0fdbf-147">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="0fdbf-148">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0fdbf-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

