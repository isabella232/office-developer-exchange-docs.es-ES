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
description: El elemento Properties contiene una lista de una o varias propiedades de seguimiento.
ms.openlocfilehash: 007a4dc14c84c47ea7af8ccacc554c134d563e44
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/01/2020
ms.locfileid: "44465635"
---
# <a name="properties-arrayoftrackingpropertiestype"></a><span data-ttu-id="31393-103">Propiedades (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="31393-103">Properties (ArrayOfTrackingPropertiesType)</span></span>

<span data-ttu-id="31393-104">El elemento **Properties** contiene una lista de una o varias propiedades de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="31393-104">The **Properties** element contains a list of one or more tracking properties.</span></span> 
  
- [<span data-ttu-id="31393-105">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="31393-105">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md)
  
- [<span data-ttu-id="31393-106">Propiedades (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="31393-106">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md)
  
```xml
<Properties>
   <TrackingPropertyType/>
</Properties>
```

<span data-ttu-id="31393-107">**ArrayOfTrackingPropertiesType**</span><span class="sxs-lookup"><span data-stu-id="31393-107">**ArrayOfTrackingPropertiesType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="31393-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="31393-108">Attributes and elements</span></span>

<span data-ttu-id="31393-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="31393-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="31393-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="31393-110">Attributes</span></span>

<span data-ttu-id="31393-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="31393-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="31393-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="31393-112">Child elements</span></span>

|<span data-ttu-id="31393-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="31393-113">**Element**</span></span>|<span data-ttu-id="31393-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="31393-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31393-115">TrackingPropertyType</span><span class="sxs-lookup"><span data-stu-id="31393-115">TrackingPropertyType</span></span>](trackingpropertytype.md) <br/> |<span data-ttu-id="31393-116">Representa un par de nombre y valor de cadenas que se usa para crear propiedades para los informes de seguimiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="31393-116">Represents a name and value pair of strings that is used to create properties for message tracking reports.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="31393-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="31393-117">Parent elements</span></span>

|<span data-ttu-id="31393-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="31393-118">**Element**</span></span>|<span data-ttu-id="31393-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="31393-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31393-120">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="31393-120">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="31393-121">Especifica los criterios para los tipos de mensajes que se van a buscar.</span><span class="sxs-lookup"><span data-stu-id="31393-121">Specifies criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="31393-122">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="31393-122">FindMessageTrackingReportResponse</span></span>](findmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="31393-123">Contiene el estado y el resultado de una sola solicitud de [operación FindMessageTrackingReport](findmessagetrackingreport-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="31393-123">Contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="31393-124">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="31393-124">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="31393-125">Contiene la solicitud de la [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md) para recuperar el informe completo de seguimiento de mensajes del identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="31393-125">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
|[<span data-ttu-id="31393-126">GetMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="31393-126">GetMessageTrackingReportResponse</span></span>](getmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="31393-127">Contiene el resultado de una única solicitud de [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="31393-127">Contains the result of a single [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="31393-128">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="31393-128">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="31393-129">Contiene información de un evento único para un destinatario.</span><span class="sxs-lookup"><span data-stu-id="31393-129">Contains information for a single event for a recipient.</span></span>  <br/> |
|[<span data-ttu-id="31393-130">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="31393-130">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="31393-131">Contiene un solo mensaje que se devuelve en una [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md).</span><span class="sxs-lookup"><span data-stu-id="31393-131">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="31393-132">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="31393-132">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="31393-133">Contiene un único resultado de mensaje para un elemento [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="31393-133">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="31393-134">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="31393-134">Text value</span></span>

<span data-ttu-id="31393-135">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="31393-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="31393-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="31393-136">Remarks</span></span>

<span data-ttu-id="31393-137">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="31393-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="31393-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="31393-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31393-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="31393-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="31393-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="31393-140">Schema Name</span></span>  <br/> |<span data-ttu-id="31393-141">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="31393-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="31393-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="31393-142">Validation File</span></span>  <br/> |<span data-ttu-id="31393-143">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="31393-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="31393-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="31393-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="31393-145">Falso</span><span class="sxs-lookup"><span data-stu-id="31393-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="31393-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="31393-146">See also</span></span>

- [<span data-ttu-id="31393-147">Operación FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="31393-147">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)
- [<span data-ttu-id="31393-148">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="31393-148">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)
- [<span data-ttu-id="31393-149">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="31393-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

