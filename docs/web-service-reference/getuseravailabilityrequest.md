---
title: GetUserAvailabilityRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserAvailabilityRequest
api_type:
- schema
ms.assetid: 7906711b-80a1-42ae-8b33-26eeac036a5a
description: El elemento GetUserAvailabilityRequest contiene los argumentos utilizados para obtener información de disponibilidad del usuario. Esto es un elemento raíz.
ms.openlocfilehash: 5440f739b09bfbe27ad97cba99c08756686594f7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835683"
---
# <a name="getuseravailabilityrequest"></a><span data-ttu-id="3674b-104">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="3674b-104">GetUserAvailabilityRequest</span></span>

<span data-ttu-id="3674b-105">El elemento **GetUserAvailabilityRequest** contiene los argumentos utilizados para obtener información de disponibilidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="3674b-105">The **GetUserAvailabilityRequest** element contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="3674b-106">Esto es un elemento raíz.</span><span class="sxs-lookup"><span data-stu-id="3674b-106">This is a root element.</span></span> 
  
```xml
<GetUserAvailabilityRequest>
   <TimeZone>...</TimeZone>
   <MailboxDataArray>...</MailboxDataArray>
   <FreeBusyViewOptions>...</FreeBusyViewOptions>
   <SuggestionsViewOptions>...</SuggestionsViewOptions>
</GetUserAvailabilityRequest>
```

 <span data-ttu-id="3674b-107">**GetUserAvailabilityRequestType**</span><span class="sxs-lookup"><span data-stu-id="3674b-107">**GetUserAvailabilityRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3674b-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3674b-108">Attributes and elements</span></span>

<span data-ttu-id="3674b-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3674b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3674b-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="3674b-110">Attributes</span></span>

<span data-ttu-id="3674b-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3674b-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3674b-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3674b-112">Child elements</span></span>

|<span data-ttu-id="3674b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3674b-113">**Element**</span></span>|<span data-ttu-id="3674b-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3674b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3674b-115">TimeZone (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="3674b-115">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> |<span data-ttu-id="3674b-116">Contiene elementos que identifican la información de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="3674b-116">Contains elements that identify time zone information.</span></span> <span data-ttu-id="3674b-117">Este elemento también contiene información sobre la transición entre la hora estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="3674b-117">This element also contains information about the transition between standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="3674b-118">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="3674b-118">MailboxDataArray</span></span>](mailboxdataarray.md) <br/> |<span data-ttu-id="3674b-119">Contiene una lista de buzones de correo para consultar la información de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="3674b-119">Contains a list of mailboxes to query for availability information.</span></span>  <br/> |
|[<span data-ttu-id="3674b-120">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="3674b-120">FreeBusyViewOptions</span></span>](freebusyviewoptions.md) <br/> |<span data-ttu-id="3674b-121">Especifica el tipo de información de libre/ocupado devuelto en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3674b-121">Specifies the type of free/busy information returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="3674b-122">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="3674b-122">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="3674b-123">Contiene las opciones para obtener información de la sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="3674b-123">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3674b-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3674b-124">Parent elements</span></span>

<span data-ttu-id="3674b-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3674b-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3674b-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3674b-126">Remarks</span></span>

<span data-ttu-id="3674b-127">El esquema que describe este elemento se encuentra en el directorio /EWS/ del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="3674b-127">The schema that describes this element is located in the /EWS/ directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="3674b-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3674b-128">Example</span></span>

<span data-ttu-id="3674b-129">En el ejemplo siguiente se muestra una solicitud para obtener información de libre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="3674b-129">The following example shows a request for free/busy information.</span></span>
  
```
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUserAvailabilityRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <TimeZone xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <Bias>480</Bias>
        <StandardTime>
          <Bias>0</Bias>
          <Time>02:00:00</Time>
          <DayOrder>5</DayOrder>
          <Month>10</Month>
          <DayOfWeek>Sunday</DayOfWeek>
        </StandardTime>
        <DaylightTime>
          <Bias>-60</Bias>
          <Time>02:00:00</Time>
          <DayOrder>1</DayOrder>
          <Month>4</Month>
          <DayOfWeek>Sunday</DayOfWeek>
        </DaylightTime>
      </TimeZone>
      <MailboxDataArray>
        <MailboxData xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Email>
            <Name></Name>
            <Address>someone@exchangeserver.example.com</Address>
            <RoutingType>SMTP</RoutingType>
          </Email>
          <AttendeeType>Organizer</AttendeeType>
          <ExcludeConflicts>false</ExcludeConflicts>
          <ExcludeNonWorkingHours>false</ExcludeNonWorkingHours>
        </MailboxData>
      </MailboxDataArray>
      <FreeBusyViewOptions xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <TimeWindow>
          <StartTime>2006-02-06T00:00:00</StartTime>
          <EndTime>2006-02-30T23:59:59</EndTime>
        </TimeWindow>
        <MergedFreeBusyIntervalInMinutes>60</MergedFreeBusyIntervalInMinutes>
        <RequestedView>FreeBusyMerged</RequestedView>
      </FreeBusyViewOptions>
    </GetUserAvailabilityRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="3674b-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3674b-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3674b-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3674b-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3674b-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3674b-132">Schema Name</span></span>  <br/> |<span data-ttu-id="3674b-133">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3674b-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3674b-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3674b-134">Validation File</span></span>  <br/> |<span data-ttu-id="3674b-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3674b-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3674b-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3674b-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="3674b-137">False</span><span class="sxs-lookup"><span data-stu-id="3674b-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3674b-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="3674b-138">See also</span></span>



[<span data-ttu-id="3674b-139">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="3674b-139">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="3674b-140">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="3674b-140">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="3674b-141">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="3674b-141">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

