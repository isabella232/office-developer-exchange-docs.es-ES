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
description: El elemento GetMessageTrackingReport contiene la solicitud para la operación GetMessageTrackingReport recuperar el mensaje completo informe de seguimiento para el identificador especificado.
ms.openlocfilehash: cb16f6e9d322cefb0d59c962af8e2f60ebae0e90
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764912"
---
# <a name="getmessagetrackingreport"></a><span data-ttu-id="450db-103">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="450db-103">GetMessageTrackingReport</span></span>

<span data-ttu-id="450db-104">El elemento **GetMessageTrackingReport** contiene la solicitud para la [operación de GetMessageTrackingReport](getmessagetrackingreport-operation.md) recuperar el mensaje completo informe de seguimiento para el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="450db-104">The **GetMessageTrackingReport** element contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span> 
  
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

 <span data-ttu-id="450db-105">**GetMessageTrackingReportRequestType**</span><span class="sxs-lookup"><span data-stu-id="450db-105">**GetMessageTrackingReportRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="450db-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="450db-106">Attributes and elements</span></span>

<span data-ttu-id="450db-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="450db-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="450db-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="450db-108">Attributes</span></span>

<span data-ttu-id="450db-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="450db-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="450db-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="450db-110">Child elements</span></span>

|<span data-ttu-id="450db-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="450db-111">**Element**</span></span>|<span data-ttu-id="450db-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="450db-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="450db-113">Ámbito (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="450db-113">Scope (NonEmptyStringType)</span></span>](scope-nonemptystringtype.md) <br/> |<span data-ttu-id="450db-114">Especifica dónde se debe realizar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="450db-114">Specifies where to perform the search.</span></span> <span data-ttu-id="450db-115">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="450db-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="450db-116">ReportTemplate</span><span class="sxs-lookup"><span data-stu-id="450db-116">ReportTemplate</span></span>](reporttemplate.md) <br/> |<span data-ttu-id="450db-117">Especifica el tipo de informe para recuperar de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="450db-117">Specifies the type of tracking report to retrieve.</span></span> <span data-ttu-id="450db-118">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="450db-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="450db-119">RecipientFilter</span><span class="sxs-lookup"><span data-stu-id="450db-119">RecipientFilter</span></span>](recipientfilter.md) <br/> |<span data-ttu-id="450db-120">Especifica una dirección de destinatario para usar con el informe de seguimiento especificado.</span><span class="sxs-lookup"><span data-stu-id="450db-120">Specifies a recipient address to use with the specified tracking report.</span></span> <span data-ttu-id="450db-121">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="450db-121">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="450db-122">MessageTrackingReportId</span><span class="sxs-lookup"><span data-stu-id="450db-122">MessageTrackingReportId</span></span>](messagetrackingreportid.md) <br/> |<span data-ttu-id="450db-123">Especifica una cadena de identidad que se ha obtenido de la operación de **FindMessageTrackingReport** .</span><span class="sxs-lookup"><span data-stu-id="450db-123">Specifies an identity string that was obtained from the **FindMessageTrackingReport** operation.</span></span> <span data-ttu-id="450db-124">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="450db-124">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="450db-125">ReturnQueueEvents</span><span class="sxs-lookup"><span data-stu-id="450db-125">ReturnQueueEvents</span></span>](returnqueueevents.md) <br/> |<span data-ttu-id="450db-126">Especifica que la persona que está ejecutando la tarea tiene una función que tiene privilegios.</span><span class="sxs-lookup"><span data-stu-id="450db-126">Specifies that the person who is running the task has a privileged role.</span></span> <span data-ttu-id="450db-127">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="450db-127">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="450db-128">DiagnosticsLevel</span><span class="sxs-lookup"><span data-stu-id="450db-128">DiagnosticsLevel</span></span>](diagnosticslevel.md) <br/> |<span data-ttu-id="450db-129">Especifica información de rendimiento y control de tiempo que se utilizará para derivar el informe de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="450db-129">Specifies timing and performance information that will be used to derive the tracking report.</span></span> <span data-ttu-id="450db-130">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="450db-130">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="450db-131">Propiedades (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="450db-131">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="450db-132">Especifica una lista de una o varias propiedades de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="450db-132">Specifies a list of one or more tracking properties.</span></span> <span data-ttu-id="450db-133">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="450db-133">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="450db-134">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="450db-134">Parent elements</span></span>

<span data-ttu-id="450db-135">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="450db-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="450db-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="450db-136">Remarks</span></span>

<span data-ttu-id="450db-137">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="450db-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="450db-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="450db-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="450db-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="450db-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="450db-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="450db-140">Schema Name</span></span>  <br/> |<span data-ttu-id="450db-141">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="450db-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="450db-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="450db-142">Validation File</span></span>  <br/> |<span data-ttu-id="450db-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="450db-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="450db-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="450db-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="450db-145">False</span><span class="sxs-lookup"><span data-stu-id="450db-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="450db-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="450db-146">See also</span></span>



[<span data-ttu-id="450db-147">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="450db-147">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="450db-148">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="450db-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

