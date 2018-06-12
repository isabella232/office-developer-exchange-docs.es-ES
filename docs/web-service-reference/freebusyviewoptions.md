---
title: FreeBusyViewOptions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeBusyViewOptions
api_type:
- schema
ms.assetid: c07f3ddb-874b-4d30-a60e-7e5c7793bb6f
description: El elemento FreeBusyViewOptions especifica el tipo de información de libre/ocupado devuelto en la respuesta.
ms.openlocfilehash: 703fc6a3625d24cf874a785600e13ee4505b506f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764721"
---
# <a name="freebusyviewoptions"></a><span data-ttu-id="9ba56-103">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="9ba56-103">FreeBusyViewOptions</span></span>

<span data-ttu-id="9ba56-104">El elemento **FreeBusyViewOptions** especifica el tipo de información de libre/ocupado devuelto en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9ba56-104">The **FreeBusyViewOptions** element specifies the type of free/busy information returned in the response.</span></span> 
  
[<span data-ttu-id="9ba56-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="9ba56-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="9ba56-106">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="9ba56-106">FreeBusyViewOptions</span></span>](freebusyviewoptions.md)
  
```xml
<FreeBusyViewOptions>
   <TimeWindow>...</TimeWindow>
   <MergedFreeBusyIntervalInMinutes>...</MergedFreeBusyIntervalInMinutes>
<RequestedView>...</RequestedView>
</FreeBusyViewOptions>

```

 <span data-ttu-id="9ba56-107">**FreeBusyViewOptionsType**</span><span class="sxs-lookup"><span data-stu-id="9ba56-107">**FreeBusyViewOptionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9ba56-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9ba56-108">Attributes and elements</span></span>

<span data-ttu-id="9ba56-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9ba56-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9ba56-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="9ba56-110">Attributes</span></span>

<span data-ttu-id="9ba56-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9ba56-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9ba56-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9ba56-112">Child elements</span></span>

|<span data-ttu-id="9ba56-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9ba56-113">**Element**</span></span>|<span data-ttu-id="9ba56-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9ba56-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9ba56-115">Ventana de tiempo</span><span class="sxs-lookup"><span data-stu-id="9ba56-115">TimeWindow</span></span>](timewindow.md) <br/> |<span data-ttu-id="9ba56-116">Identifica el intervalo de tiempo de consulta para la información de disponibilidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="9ba56-116">Identifies the time span queried for the user availability information.</span></span>  <br/> |
|[<span data-ttu-id="9ba56-117">MergedFreeBusyIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="9ba56-117">MergedFreeBusyIntervalInMinutes</span></span>](mergedfreebusyintervalinminutes.md) <br/> |<span data-ttu-id="9ba56-118">Representa la diferencia de tiempo entre dos ranuras sucesivos en la vista **FreeBusyMerged** .</span><span class="sxs-lookup"><span data-stu-id="9ba56-118">Represents the time difference between two successive slots in the **FreeBusyMerged** view.</span></span>  <br/> |
|[<span data-ttu-id="9ba56-119">RequestedView</span><span class="sxs-lookup"><span data-stu-id="9ba56-119">RequestedView</span></span>](requestedview.md) <br/> |<span data-ttu-id="9ba56-120">Define el tipo de información del calendario que solicita un cliente.</span><span class="sxs-lookup"><span data-stu-id="9ba56-120">Defines the type of calendar information that a client requests.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9ba56-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9ba56-121">Parent elements</span></span>

|<span data-ttu-id="9ba56-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="9ba56-122">**Element**</span></span>|<span data-ttu-id="9ba56-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9ba56-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9ba56-124">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="9ba56-124">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) <br/> |<span data-ttu-id="9ba56-125">Contiene los argumentos utilizados para obtener información de disponibilidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="9ba56-125">Contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="9ba56-126">Esto es un elemento raíz.</span><span class="sxs-lookup"><span data-stu-id="9ba56-126">This is a root element.</span></span>  <br/> <span data-ttu-id="9ba56-127">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="9ba56-127">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ba56-128">Notas</span><span class="sxs-lookup"><span data-stu-id="9ba56-128">Remarks</span></span>

<span data-ttu-id="9ba56-129">Este elemento no es necesario y sólo puede aparecer una vez si se usa.</span><span class="sxs-lookup"><span data-stu-id="9ba56-129">This element is not required and can only occur once if used.</span></span> <span data-ttu-id="9ba56-130">Este valor puede ser null si el valor del elemento [SuggestionsViewOptions](suggestionsviewoptions.md) no es nulo.</span><span class="sxs-lookup"><span data-stu-id="9ba56-130">This value can be null if the value of the [SuggestionsViewOptions](suggestionsviewoptions.md) element is not null.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9ba56-131">El esquema que describe este elemento se encuentra en el directorio /epi/ del equipo que ejecuta Microsoft® Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="9ba56-131">The schema that describes this element is located in the /epi/ directory of the computer that is running Microsoft® Exchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="example"></a><span data-ttu-id="9ba56-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9ba56-132">Example</span></span>

<span data-ttu-id="9ba56-133">En el ejemplo siguiente se obtiene una lista de las reuniones y una secuencia de libre/ocupada en intervalos de 60 minutos.</span><span class="sxs-lookup"><span data-stu-id="9ba56-133">The following example obtains a list of meetings and a free/busy stream in 60-minute intervals.</span></span>
  
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
            <Address>someone@ExServer.example.com</Address>
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
          <EndTime>2006-02-25T23:59:59</EndTime>
        </TimeWindow>
        <MergedFreeBusyIntervalInMinutes>60</MergedFreeBusyIntervalInMinutes>
        <RequestedView>FreeBusyMerged</RequestedView>
      </FreeBusyViewOptions>
    </GetUserAvailabilityRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="9ba56-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9ba56-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9ba56-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9ba56-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9ba56-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9ba56-136">Schema Name</span></span>  <br/> |<span data-ttu-id="9ba56-137">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="9ba56-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="9ba56-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9ba56-138">Validation File</span></span>  <br/> |<span data-ttu-id="9ba56-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9ba56-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9ba56-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9ba56-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="9ba56-141">False</span><span class="sxs-lookup"><span data-stu-id="9ba56-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9ba56-142">Ver también</span><span class="sxs-lookup"><span data-stu-id="9ba56-142">See also</span></span>



[<span data-ttu-id="9ba56-143">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="9ba56-143">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="9ba56-144">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="9ba56-144">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

