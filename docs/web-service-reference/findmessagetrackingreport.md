---
title: FindMessageTrackingReport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindMessageTrackingReport
api_type:
- schema
ms.assetid: 7ca6e2f7-aae1-4920-b839-73513ba8d4d8
description: El elemento FindMessageTrackingReport especifica los criterios para los tipos de mensajes para buscar.
ms.openlocfilehash: 77545121aa056992248c045af3f3d36566678b94
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764642"
---
# <a name="findmessagetrackingreport"></a><span data-ttu-id="1126e-103">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="1126e-103">FindMessageTrackingReport</span></span>

<span data-ttu-id="1126e-104">El elemento **FindMessageTrackingReport** especifica los criterios para los tipos de mensajes para buscar.</span><span class="sxs-lookup"><span data-stu-id="1126e-104">The **FindMessageTrackingReport** element specifies criteria for the types of messages to find.</span></span> 
  
```xml
<FindMessageTrackingReport>
   <Scope/>
   <Domain/>
   <Sender/>
   <PurportedSender/>
   <Recipient/>
   <Subject/>
   <StartDateTime/>
   <EndDateTime/>
   <MessageId/>
   <FederatedDeliveryMailbox/>
   <DiagnosticsLevel/>
   <ServerHint/>
   <Properties/>
</FindMessageTrackingReport>
```

 <span data-ttu-id="1126e-105">**FindMessageTrackingReportRequestType**</span><span class="sxs-lookup"><span data-stu-id="1126e-105">**FindMessageTrackingReportRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1126e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1126e-106">Attributes and elements</span></span>

<span data-ttu-id="1126e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1126e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1126e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1126e-108">Attributes</span></span>

<span data-ttu-id="1126e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1126e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1126e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1126e-110">Child elements</span></span>

|<span data-ttu-id="1126e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1126e-111">**Element**</span></span>|<span data-ttu-id="1126e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1126e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1126e-113">Ámbito (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="1126e-113">Scope (NonEmptyStringType)</span></span>](scope-nonemptystringtype.md) <br/> |<span data-ttu-id="1126e-114">Representa la extensión deben ser el informe de seguimiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1126e-114">Represents how extensive the message tracking report should be.</span></span>  <br/> |
|[<span data-ttu-id="1126e-115">Dominio (el seguimiento de mensajes)</span><span class="sxs-lookup"><span data-stu-id="1126e-115">Domain (Message Tracking)</span></span>](domain-message-tracking.md) <br/> |<span data-ttu-id="1126e-116">Contiene el nombre del dominio donde se ejecutan el seguimiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1126e-116">Contains the name of the domain where the message tracking is executed.</span></span>  <br/> |
|[<span data-ttu-id="1126e-117">Remitente (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="1126e-117">Sender (EmailAddressType)</span></span>](sender-emailaddresstype.md) <br/> |<span data-ttu-id="1126e-118">Contiene información de contacto para el remitente del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1126e-118">Contains contact information for the sender of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="1126e-119">PurportedSender</span><span class="sxs-lookup"><span data-stu-id="1126e-119">PurportedSender</span></span>](purportedsender.md) <br/> |<span data-ttu-id="1126e-120">Contiene información de contacto para el remitente presunta de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1126e-120">Contains contact information for the alleged sender of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="1126e-121">Recipient</span><span class="sxs-lookup"><span data-stu-id="1126e-121">Recipient</span></span>](recipient.md) <br/> |<span data-ttu-id="1126e-122">Contiene la dirección de correo electrónico para el destinatario del mensaje.</span><span class="sxs-lookup"><span data-stu-id="1126e-122">Contains the e-mail address for the recipient of the message.</span></span>  <br/> |
|[<span data-ttu-id="1126e-123">Subject</span><span class="sxs-lookup"><span data-stu-id="1126e-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="1126e-124">Contiene al asunto del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1126e-124">Contains the subject of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="1126e-125">StartDateTime</span><span class="sxs-lookup"><span data-stu-id="1126e-125">StartDateTime</span></span>](startdatetime.md) <br/> |<span data-ttu-id="1126e-126">Contiene la fecha y la hora para la búsqueda inicial.</span><span class="sxs-lookup"><span data-stu-id="1126e-126">Contains the starting date and time for the search.</span></span>  <br/> |
|[<span data-ttu-id="1126e-127">EndDateTime</span><span class="sxs-lookup"><span data-stu-id="1126e-127">EndDateTime</span></span>](enddatetime.md) <br/> |<span data-ttu-id="1126e-128">Contiene la fecha final y la hora para la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1126e-128">Contains the ending date and time for the search.</span></span>  <br/> |
|[<span data-ttu-id="1126e-129">MessageId</span><span class="sxs-lookup"><span data-stu-id="1126e-129">MessageId</span></span>](messageid.md) <br/> |<span data-ttu-id="1126e-130">Contiene el identificador de mensaje para la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1126e-130">Contains the message identifier for the search.</span></span>  <br/> |
|[<span data-ttu-id="1126e-131">FederatedDeliveryMailbox</span><span class="sxs-lookup"><span data-stu-id="1126e-131">FederatedDeliveryMailbox</span></span>](federateddeliverymailbox.md) <br/> |<span data-ttu-id="1126e-132">Contiene el nombre del buzón donde se envió el mensaje entre locales.</span><span class="sxs-lookup"><span data-stu-id="1126e-132">Contains the name of the mailbox where the cross-premise message was sent.</span></span>  <br/> |
|[<span data-ttu-id="1126e-133">DiagnosticsLevel</span><span class="sxs-lookup"><span data-stu-id="1126e-133">DiagnosticsLevel</span></span>](diagnosticslevel.md) <br/> |<span data-ttu-id="1126e-134">Representa el nivel de detalle de los informes de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="1126e-134">Represents the level of detail for diagnostic reports.</span></span>  <br/> |
|[<span data-ttu-id="1126e-135">ServerHint</span><span class="sxs-lookup"><span data-stu-id="1126e-135">ServerHint</span></span>](serverhint.md) <br/> |<span data-ttu-id="1126e-136">Representa el punto de partida para el seguimiento de un mensaje en un sitio remoto o un bosque.</span><span class="sxs-lookup"><span data-stu-id="1126e-136">Represents the starting point for tracking a message in a remote site or forest.</span></span>  <br/> |
|[<span data-ttu-id="1126e-137">Propiedades (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="1126e-137">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="1126e-138">Contiene una lista de una o varias propiedades de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="1126e-138">Contains a list of one or more tracking properties.</span></span> <span data-ttu-id="1126e-139">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="1126e-139">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1126e-140">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1126e-140">Parent elements</span></span>

<span data-ttu-id="1126e-141">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1126e-141">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="1126e-142">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1126e-142">Text value</span></span>

<span data-ttu-id="1126e-143">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1126e-143">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1126e-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1126e-144">Remarks</span></span>

<span data-ttu-id="1126e-145">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="1126e-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1126e-146">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1126e-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1126e-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1126e-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1126e-148">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1126e-148">Schema Name</span></span>  <br/> |<span data-ttu-id="1126e-149">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="1126e-149">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1126e-150">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1126e-150">Validation File</span></span>  <br/> |<span data-ttu-id="1126e-151">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1126e-151">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1126e-152">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1126e-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="1126e-153">False</span><span class="sxs-lookup"><span data-stu-id="1126e-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1126e-154">Ver también</span><span class="sxs-lookup"><span data-stu-id="1126e-154">See also</span></span>



[<span data-ttu-id="1126e-155">Operación FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="1126e-155">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)


- [<span data-ttu-id="1126e-156">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="1126e-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

