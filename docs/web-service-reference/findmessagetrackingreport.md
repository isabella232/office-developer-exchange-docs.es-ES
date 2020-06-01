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
description: El elemento FindMessageTrackingReport especifica criterios para los tipos de mensajes que se van a buscar.
ms.openlocfilehash: d30e5391bb4305cae0004a9788df971a57297cae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462939"
---
# <a name="findmessagetrackingreport"></a><span data-ttu-id="a819a-103">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="a819a-103">FindMessageTrackingReport</span></span>

<span data-ttu-id="a819a-104">El elemento **FindMessageTrackingReport** especifica criterios para los tipos de mensajes que se van a buscar.</span><span class="sxs-lookup"><span data-stu-id="a819a-104">The **FindMessageTrackingReport** element specifies criteria for the types of messages to find.</span></span> 
  
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

 <span data-ttu-id="a819a-105">**FindMessageTrackingReportRequestType**</span><span class="sxs-lookup"><span data-stu-id="a819a-105">**FindMessageTrackingReportRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a819a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a819a-106">Attributes and elements</span></span>

<span data-ttu-id="a819a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a819a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a819a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a819a-108">Attributes</span></span>

<span data-ttu-id="a819a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a819a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a819a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a819a-110">Child elements</span></span>

|<span data-ttu-id="a819a-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a819a-111">**Element**</span></span>|<span data-ttu-id="a819a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a819a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a819a-113">Ámbito (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="a819a-113">Scope (NonEmptyStringType)</span></span>](scope-nonemptystringtype.md) <br/> |<span data-ttu-id="a819a-114">Representa la extensión que debe tener el informe de seguimiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a819a-114">Represents how extensive the message tracking report should be.</span></span>  <br/> |
|[<span data-ttu-id="a819a-115">Dominio (seguimiento de mensajes)</span><span class="sxs-lookup"><span data-stu-id="a819a-115">Domain (Message Tracking)</span></span>](domain-message-tracking.md) <br/> |<span data-ttu-id="a819a-116">Contiene el nombre del dominio donde se ejecuta el seguimiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a819a-116">Contains the name of the domain where the message tracking is executed.</span></span>  <br/> |
|[<span data-ttu-id="a819a-117">Remitente (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="a819a-117">Sender (EmailAddressType)</span></span>](sender-emailaddresstype.md) <br/> |<span data-ttu-id="a819a-118">Contiene la información de contacto del remitente del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a819a-118">Contains contact information for the sender of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="a819a-119">PurportedSender</span><span class="sxs-lookup"><span data-stu-id="a819a-119">PurportedSender</span></span>](purportedsender.md) <br/> |<span data-ttu-id="a819a-120">Contiene la información de contacto del remitente de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a819a-120">Contains contact information for the alleged sender of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="a819a-121">Destinatario</span><span class="sxs-lookup"><span data-stu-id="a819a-121">Recipient</span></span>](recipient.md) <br/> |<span data-ttu-id="a819a-122">Contiene la dirección de correo electrónico del destinatario del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a819a-122">Contains the e-mail address for the recipient of the message.</span></span>  <br/> |
|[<span data-ttu-id="a819a-123">Asunto</span><span class="sxs-lookup"><span data-stu-id="a819a-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="a819a-124">Contiene el asunto del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a819a-124">Contains the subject of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="a819a-125">StartDateTime</span><span class="sxs-lookup"><span data-stu-id="a819a-125">StartDateTime</span></span>](startdatetime.md) <br/> |<span data-ttu-id="a819a-126">Contiene la fecha y hora de inicio de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a819a-126">Contains the starting date and time for the search.</span></span>  <br/> |
|[<span data-ttu-id="a819a-127">EndDateTime</span><span class="sxs-lookup"><span data-stu-id="a819a-127">EndDateTime</span></span>](enddatetime.md) <br/> |<span data-ttu-id="a819a-128">Contiene la fecha y hora de finalización de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a819a-128">Contains the ending date and time for the search.</span></span>  <br/> |
|[<span data-ttu-id="a819a-129">MessageId</span><span class="sxs-lookup"><span data-stu-id="a819a-129">MessageId</span></span>](messageid.md) <br/> |<span data-ttu-id="a819a-130">Contiene el identificador de mensaje para la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a819a-130">Contains the message identifier for the search.</span></span>  <br/> |
|[<span data-ttu-id="a819a-131">FederatedDeliveryMailbox</span><span class="sxs-lookup"><span data-stu-id="a819a-131">FederatedDeliveryMailbox</span></span>](federateddeliverymailbox.md) <br/> |<span data-ttu-id="a819a-132">Contiene el nombre del buzón en el que se envió el mensaje entre locales.</span><span class="sxs-lookup"><span data-stu-id="a819a-132">Contains the name of the mailbox where the cross-premise message was sent.</span></span>  <br/> |
|[<span data-ttu-id="a819a-133">DiagnosticsLevel</span><span class="sxs-lookup"><span data-stu-id="a819a-133">DiagnosticsLevel</span></span>](diagnosticslevel.md) <br/> |<span data-ttu-id="a819a-134">Representa el nivel de detalle de los informes de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="a819a-134">Represents the level of detail for diagnostic reports.</span></span>  <br/> |
|[<span data-ttu-id="a819a-135">ServerHint</span><span class="sxs-lookup"><span data-stu-id="a819a-135">ServerHint</span></span>](serverhint.md) <br/> |<span data-ttu-id="a819a-136">Representa el punto de inicio para el seguimiento de un mensaje en un sitio o bosque remoto.</span><span class="sxs-lookup"><span data-stu-id="a819a-136">Represents the starting point for tracking a message in a remote site or forest.</span></span>  <br/> |
|[<span data-ttu-id="a819a-137">Propiedades (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="a819a-137">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="a819a-138">Contiene una lista de una o varias propiedades de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="a819a-138">Contains a list of one or more tracking properties.</span></span> <span data-ttu-id="a819a-139">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="a819a-139">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a819a-140">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a819a-140">Parent elements</span></span>

<span data-ttu-id="a819a-141">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a819a-141">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="a819a-142">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a819a-142">Text value</span></span>

<span data-ttu-id="a819a-143">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a819a-143">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a819a-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a819a-144">Remarks</span></span>

<span data-ttu-id="a819a-145">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a819a-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a819a-146">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a819a-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a819a-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="a819a-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a819a-148">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a819a-148">Schema Name</span></span>  <br/> |<span data-ttu-id="a819a-149">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="a819a-149">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a819a-150">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a819a-150">Validation File</span></span>  <br/> |<span data-ttu-id="a819a-151">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a819a-151">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a819a-152">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a819a-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="a819a-153">Falso</span><span class="sxs-lookup"><span data-stu-id="a819a-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a819a-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="a819a-154">See also</span></span>



[<span data-ttu-id="a819a-155">Operación FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="a819a-155">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)


- [<span data-ttu-id="a819a-156">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a819a-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

