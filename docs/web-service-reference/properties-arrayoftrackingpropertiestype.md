---
title: Propiedades (ArrayOfTrackingPropertiesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Properties
api_type:
- schema
ms.assetid: 175566d2-fd62-45a2-8518-2827912cec88
description: El elemento de propiedades contiene una lista de una o varias propiedades de seguimiento.
ms.openlocfilehash: 079d2d2c101fdeb7f26d65798048c3c6c59f3e94
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836897"
---
# <a name="properties-arrayoftrackingpropertiestype"></a><span data-ttu-id="c8bed-103">Propiedades (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="c8bed-103">Properties (ArrayOfTrackingPropertiesType)</span></span>

<span data-ttu-id="c8bed-104">El elemento de **Propiedades** contiene una lista de una o varias propiedades de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="c8bed-104">The **Properties** element contains a list of one or more tracking properties.</span></span> 
  
- [<span data-ttu-id="c8bed-105">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="c8bed-105">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md)
  
- [<span data-ttu-id="c8bed-106">Propiedades (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="c8bed-106">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md)
  
```xml
<Properties>
   <TrackingPropertyType/>
</Properties>
```

<span data-ttu-id="c8bed-107">**ArrayOfTrackingPropertiesType**</span><span class="sxs-lookup"><span data-stu-id="c8bed-107">**ArrayOfTrackingPropertiesType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c8bed-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c8bed-108">Attributes and elements</span></span>

<span data-ttu-id="c8bed-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c8bed-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c8bed-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="c8bed-110">Attributes</span></span>

<span data-ttu-id="c8bed-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c8bed-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c8bed-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c8bed-112">Child elements</span></span>

|<span data-ttu-id="c8bed-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c8bed-113">**Element**</span></span>|<span data-ttu-id="c8bed-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c8bed-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8bed-115">TrackingPropertyType</span><span class="sxs-lookup"><span data-stu-id="c8bed-115">TrackingPropertyType</span></span>](trackingpropertytype.md) <br/> |<span data-ttu-id="c8bed-116">Representa un par de cadenas nombre y valor que se usa para crear las propiedades de los informes de seguimiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c8bed-116">Represents a name and value pair of strings that is used to create properties for message tracking reports.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c8bed-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c8bed-117">Parent elements</span></span>

|<span data-ttu-id="c8bed-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="c8bed-118">**Element**</span></span>|<span data-ttu-id="c8bed-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c8bed-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8bed-120">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="c8bed-120">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="c8bed-121">Especifica los criterios para los tipos de mensajes para buscar.</span><span class="sxs-lookup"><span data-stu-id="c8bed-121">Specifies criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="c8bed-122">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="c8bed-122">FindMessageTrackingReportResponse</span></span>](findmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="c8bed-123">Contiene el estado y el resultado de una única solicitud de [operación FindMessageTrackingReport](findmessagetrackingreport-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="c8bed-123">Contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="c8bed-124">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="c8bed-124">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="c8bed-125">Contiene la solicitud para la [operación de GetMessageTrackingReport](getmessagetrackingreport-operation.md) recuperar el mensaje completo informe de seguimiento para el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="c8bed-125">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
|[<span data-ttu-id="c8bed-126">GetMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="c8bed-126">GetMessageTrackingReportResponse</span></span>](getmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="c8bed-127">Contiene el resultado de una única solicitud de [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="c8bed-127">Contains the result of a single [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="c8bed-128">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="c8bed-128">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="c8bed-129">Contiene información de un solo evento de un destinatario.</span><span class="sxs-lookup"><span data-stu-id="c8bed-129">Contains information for a single event for a recipient.</span></span>  <br/> |
|[<span data-ttu-id="c8bed-130">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="c8bed-130">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="c8bed-131">Contiene un solo mensaje que se devuelve en una [operación de GetMessageTrackingReport](getmessagetrackingreport-operation.md).</span><span class="sxs-lookup"><span data-stu-id="c8bed-131">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="c8bed-132">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="c8bed-132">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="c8bed-133">Contiene un resultado de mensaje único para un elemento [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="c8bed-133">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c8bed-134">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c8bed-134">Text value</span></span>

<span data-ttu-id="c8bed-135">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c8bed-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c8bed-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c8bed-136">Remarks</span></span>

<span data-ttu-id="c8bed-137">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c8bed-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c8bed-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c8bed-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8bed-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c8bed-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c8bed-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c8bed-140">Schema Name</span></span>  <br/> |<span data-ttu-id="c8bed-141">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c8bed-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c8bed-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c8bed-142">Validation File</span></span>  <br/> |<span data-ttu-id="c8bed-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c8bed-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c8bed-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c8bed-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="c8bed-145">False</span><span class="sxs-lookup"><span data-stu-id="c8bed-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c8bed-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8bed-146">See also</span></span>

- [<span data-ttu-id="c8bed-147">Operación FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="c8bed-147">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)
- [<span data-ttu-id="c8bed-148">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="c8bed-148">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)
- [<span data-ttu-id="c8bed-149">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c8bed-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

