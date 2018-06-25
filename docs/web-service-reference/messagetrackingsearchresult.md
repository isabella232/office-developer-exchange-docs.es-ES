---
title: MessageTrackingSearchResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MessageTrackingSearchResult
api_type:
- schema
ms.assetid: 8ea77aa8-b93f-4287-be36-0a9da06e0946
description: El elemento MessageTrackingSearchResult contiene un resultado de mensaje único para un elemento FindMessageTrackingReportResponse.
ms.openlocfilehash: ad4fb9d9e2266222303bd2015a7afba0bb46721b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836460"
---
# <a name="messagetrackingsearchresult"></a><span data-ttu-id="955c0-103">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="955c0-103">MessageTrackingSearchResult</span></span>

<span data-ttu-id="955c0-104">El elemento **MessageTrackingSearchResult** contiene un resultado de mensaje único para un elemento [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="955c0-104">The **MessageTrackingSearchResult** element contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span> 
  
```xml
<MessageTrackingSearchResult>
   <Subject/>
   <Sender/>
   <PurportedSender/>
   <Recipients/>
   <SubmittedTime/>
   <MessageTrackingReportId/>
   <PreviousHopServer/>
   <FirstHopServer/>
   <Properties/>
</MessageTrackingSearchResult>
```

 <span data-ttu-id="955c0-105">**FindMessageTrackingSearchResultType**</span><span class="sxs-lookup"><span data-stu-id="955c0-105">**FindMessageTrackingSearchResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="955c0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="955c0-106">Attributes and elements</span></span>

<span data-ttu-id="955c0-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="955c0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="955c0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="955c0-108">Attributes</span></span>

<span data-ttu-id="955c0-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="955c0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="955c0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="955c0-110">Child elements</span></span>

|<span data-ttu-id="955c0-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="955c0-111">**Element**</span></span>|<span data-ttu-id="955c0-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="955c0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="955c0-113">Subject</span><span class="sxs-lookup"><span data-stu-id="955c0-113">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="955c0-114">Contiene al asunto del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="955c0-114">Contains the e-mail message subject.</span></span>  <br/> |
|[<span data-ttu-id="955c0-115">Remitente (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="955c0-115">Sender (EmailAddressType)</span></span>](sender-emailaddresstype.md) <br/> |<span data-ttu-id="955c0-116">Contiene la dirección del remitente del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="955c0-116">Contains the e-mail message sender's address.</span></span>  <br/> |
|[<span data-ttu-id="955c0-117">PurportedSender</span><span class="sxs-lookup"><span data-stu-id="955c0-117">PurportedSender</span></span>](purportedsender.md) <br/> |<span data-ttu-id="955c0-118">Contiene información de contacto para el remitente presunta de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="955c0-118">Contains contact information for the alleged sender of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="955c0-119">Recipients (ArrayOfRecipientsType)</span><span class="sxs-lookup"><span data-stu-id="955c0-119">Recipients (ArrayOfRecipientsType)</span></span>](recipients-arrayofrecipientstype.md) <br/> |<span data-ttu-id="955c0-120">Contiene una lista de direcciones de correo electrónico que recibió este mensaje.</span><span class="sxs-lookup"><span data-stu-id="955c0-120">Contains a list of e-mail addresses that received this message.</span></span>  <br/> |
|[<span data-ttu-id="955c0-121">SubmittedTime</span><span class="sxs-lookup"><span data-stu-id="955c0-121">SubmittedTime</span></span>](submittedtime.md) <br/> |<span data-ttu-id="955c0-122">Contiene la hora en que se envió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="955c0-122">Contains the time that the message was submitted.</span></span>  <br/> |
|[<span data-ttu-id="955c0-123">MessageTrackingReportId</span><span class="sxs-lookup"><span data-stu-id="955c0-123">MessageTrackingReportId</span></span>](messagetrackingreportid.md) <br/> |<span data-ttu-id="955c0-124">Contiene un identificador interno que identifica el mensaje en la base de datos de transporte.</span><span class="sxs-lookup"><span data-stu-id="955c0-124">Contains an internal ID that identifies the message in the transport database.</span></span>  <br/> |
|[<span data-ttu-id="955c0-125">PreviousHopServer</span><span class="sxs-lookup"><span data-stu-id="955c0-125">PreviousHopServer</span></span>](previoushopserver.md) <br/> |<span data-ttu-id="955c0-126">Contiene el nombre del servidor del bosque que anteriormente se aceptó el mensaje.</span><span class="sxs-lookup"><span data-stu-id="955c0-126">Contains the name of the server in the forest that previously accepted the message.</span></span>  <br/> |
|[<span data-ttu-id="955c0-127">FirstHopServer</span><span class="sxs-lookup"><span data-stu-id="955c0-127">FirstHopServer</span></span>](firsthopserver.md) <br/> |<span data-ttu-id="955c0-128">Contiene el nombre del servidor en el bosque que se acepta en primer lugar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="955c0-128">Contains the name of the server in the forest that first accepted the message.</span></span>  <br/> |
|[<span data-ttu-id="955c0-129">Propiedades (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="955c0-129">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="955c0-130">Contiene una lista de una o varias propiedades de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="955c0-130">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="955c0-131">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="955c0-131">Parent elements</span></span>

|<span data-ttu-id="955c0-132">**Element**</span><span class="sxs-lookup"><span data-stu-id="955c0-132">**Element**</span></span>|<span data-ttu-id="955c0-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="955c0-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="955c0-134">MessageTrackingSearchResults</span><span class="sxs-lookup"><span data-stu-id="955c0-134">MessageTrackingSearchResults</span></span>](messagetrackingsearchresults.md) <br/> |<span data-ttu-id="955c0-135">Contiene una lista de los mensajes que coinciden con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="955c0-135">Contains a list of messages that match the search criteria.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="955c0-136">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="955c0-136">Text value</span></span>

<span data-ttu-id="955c0-137">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="955c0-137">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="955c0-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="955c0-138">Remarks</span></span>

<span data-ttu-id="955c0-139">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="955c0-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="955c0-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="955c0-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="955c0-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="955c0-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="955c0-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="955c0-142">Schema Name</span></span>  <br/> |<span data-ttu-id="955c0-143">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="955c0-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="955c0-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="955c0-144">Validation File</span></span>  <br/> |<span data-ttu-id="955c0-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="955c0-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="955c0-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="955c0-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="955c0-147">False</span><span class="sxs-lookup"><span data-stu-id="955c0-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="955c0-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="955c0-148">See also</span></span>



[<span data-ttu-id="955c0-149">Operación FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="955c0-149">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)


- [<span data-ttu-id="955c0-150">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="955c0-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

