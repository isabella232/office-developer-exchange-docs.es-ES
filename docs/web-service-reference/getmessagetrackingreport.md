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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764912"
---
# <a name="getmessagetrackingreport"></a><span data-ttu-id="1dd56-103">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="1dd56-103">GetMessageTrackingReport</span></span>

<span data-ttu-id="1dd56-104">El elemento **GetMessageTrackingReport** contiene la solicitud para la [operación de GetMessageTrackingReport](getmessagetrackingreport-operation.md) recuperar el mensaje completo informe de seguimiento para el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="1dd56-104">The **GetMessageTrackingReport** element contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span> 
  
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

 <span data-ttu-id="1dd56-105">**GetMessageTrackingReportRequestType**</span><span class="sxs-lookup"><span data-stu-id="1dd56-105">**GetMessageTrackingReportRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1dd56-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1dd56-106">Attributes and elements</span></span>

<span data-ttu-id="1dd56-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1dd56-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1dd56-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1dd56-108">Attributes</span></span>

<span data-ttu-id="1dd56-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1dd56-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1dd56-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1dd56-110">Child elements</span></span>

|<span data-ttu-id="1dd56-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1dd56-111">**Element**</span></span>|<span data-ttu-id="1dd56-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1dd56-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1dd56-113">Ámbito (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="1dd56-113">Scope (NonEmptyStringType)</span></span>](scope-nonemptystringtype.md) <br/> |<span data-ttu-id="1dd56-114">Especifica dónde se debe realizar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1dd56-114">Specifies where to perform the search.</span></span> <span data-ttu-id="1dd56-115">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="1dd56-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="1dd56-116">ReportTemplate</span><span class="sxs-lookup"><span data-stu-id="1dd56-116">ReportTemplate</span></span>](reporttemplate.md) <br/> |<span data-ttu-id="1dd56-117">Especifica el tipo de informe para recuperar de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="1dd56-117">Specifies the type of tracking report to retrieve.</span></span> <span data-ttu-id="1dd56-118">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="1dd56-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="1dd56-119">RecipientFilter</span><span class="sxs-lookup"><span data-stu-id="1dd56-119">RecipientFilter</span></span>](recipientfilter.md) <br/> |<span data-ttu-id="1dd56-120">Especifica una dirección de destinatario para usar con el informe de seguimiento especificado.</span><span class="sxs-lookup"><span data-stu-id="1dd56-120">Specifies a recipient address to use with the specified tracking report.</span></span> <span data-ttu-id="1dd56-121">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="1dd56-121">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="1dd56-122">MessageTrackingReportId</span><span class="sxs-lookup"><span data-stu-id="1dd56-122">MessageTrackingReportId</span></span>](messagetrackingreportid.md) <br/> |<span data-ttu-id="1dd56-123">Especifica una cadena de identidad que se ha obtenido de la operación de **FindMessageTrackingReport** .</span><span class="sxs-lookup"><span data-stu-id="1dd56-123">Specifies an identity string that was obtained from the **FindMessageTrackingReport** operation.</span></span> <span data-ttu-id="1dd56-124">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="1dd56-124">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="1dd56-125">ReturnQueueEvents</span><span class="sxs-lookup"><span data-stu-id="1dd56-125">ReturnQueueEvents</span></span>](returnqueueevents.md) <br/> |<span data-ttu-id="1dd56-126">Especifica que la persona que está ejecutando la tarea tiene una función que tiene privilegios.</span><span class="sxs-lookup"><span data-stu-id="1dd56-126">Specifies that the person who is running the task has a privileged role.</span></span> <span data-ttu-id="1dd56-127">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="1dd56-127">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="1dd56-128">DiagnosticsLevel</span><span class="sxs-lookup"><span data-stu-id="1dd56-128">DiagnosticsLevel</span></span>](diagnosticslevel.md) <br/> |<span data-ttu-id="1dd56-129">Especifica información de rendimiento y control de tiempo que se utilizará para derivar el informe de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="1dd56-129">Specifies timing and performance information that will be used to derive the tracking report.</span></span> <span data-ttu-id="1dd56-130">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="1dd56-130">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="1dd56-131">Propiedades (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="1dd56-131">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="1dd56-132">Especifica una lista de una o varias propiedades de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="1dd56-132">Specifies a list of one or more tracking properties.</span></span> <span data-ttu-id="1dd56-133">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="1dd56-133">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1dd56-134">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1dd56-134">Parent elements</span></span>

<span data-ttu-id="1dd56-135">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1dd56-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1dd56-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1dd56-136">Remarks</span></span>

<span data-ttu-id="1dd56-137">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="1dd56-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1dd56-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1dd56-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1dd56-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1dd56-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1dd56-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1dd56-140">Schema Name</span></span>  <br/> |<span data-ttu-id="1dd56-141">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="1dd56-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1dd56-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1dd56-142">Validation File</span></span>  <br/> |<span data-ttu-id="1dd56-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1dd56-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1dd56-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1dd56-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="1dd56-145">False</span><span class="sxs-lookup"><span data-stu-id="1dd56-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1dd56-146">Ver también</span><span class="sxs-lookup"><span data-stu-id="1dd56-146">See also</span></span>



[<span data-ttu-id="1dd56-147">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="1dd56-147">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="1dd56-148">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="1dd56-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

