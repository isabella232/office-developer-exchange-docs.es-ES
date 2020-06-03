---
title: CalendarView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarView
api_type:
- schema
ms.assetid: a4a953b8-0710-416c-95ef-59e51eba9982
description: El elemento CalendarView define una operación FindItem como elementos de calendario devueltos en un conjunto como aparecen en un calendario.
ms.openlocfilehash: e547a4b2db5c09ebefd9a072da6cc4733818002e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462265"
---
# <a name="calendarview"></a><span data-ttu-id="ee34f-103">CalendarView</span><span class="sxs-lookup"><span data-stu-id="ee34f-103">CalendarView</span></span>

<span data-ttu-id="ee34f-104">El elemento **CalendarView** define una [operación FindItem](finditem-operation.md) como elementos de calendario devueltos en un conjunto como aparecen en un calendario.</span><span class="sxs-lookup"><span data-stu-id="ee34f-104">The **CalendarView** element defines a [FindItem operation](finditem-operation.md) as returning calendar items in a set as they appear in a calendar.</span></span> 
  
[<span data-ttu-id="ee34f-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="ee34f-105">FindItem</span></span>](finditem.md)
  
[<span data-ttu-id="ee34f-106">CalendarView</span><span class="sxs-lookup"><span data-stu-id="ee34f-106">CalendarView</span></span>](calendarview.md)
  
```XML
<CalendarView MaxEntriesReturned="" StartDate="" EndDate="" />
```

<span data-ttu-id="ee34f-107">**CalendarView**</span><span class="sxs-lookup"><span data-stu-id="ee34f-107">**CalendarView**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ee34f-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ee34f-108">Attributes and elements</span></span>

<span data-ttu-id="ee34f-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ee34f-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ee34f-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="ee34f-110">Attributes</span></span>

|<span data-ttu-id="ee34f-111">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ee34f-111">**Attribute**</span></span>|<span data-ttu-id="ee34f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ee34f-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ee34f-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="ee34f-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="ee34f-114">Describe el número máximo de resultados que se devolverá en la respuesta FindItem.</span><span class="sxs-lookup"><span data-stu-id="ee34f-114">Describes the maximum number of results to return in the FindItem response.</span></span>  <br/> |
|<span data-ttu-id="ee34f-115">**StartDate**</span><span class="sxs-lookup"><span data-stu-id="ee34f-115">**StartDate**</span></span> <br/> |<span data-ttu-id="ee34f-116">Identifica el inicio de un intervalo de tiempo consultado para los elementos de calendario.</span><span class="sxs-lookup"><span data-stu-id="ee34f-116">Identifies the start of a time span queried for calendar items.</span></span> <span data-ttu-id="ee34f-117">No se devolverán todos los elementos de calendario que tengan una hora de finalización antes de **startDate** .</span><span class="sxs-lookup"><span data-stu-id="ee34f-117">All calendar items that have an end time that is before **StartDate** will not be returned.</span></span> <span data-ttu-id="ee34f-118">El valor de **startDate** se puede especificar en formato de hora universal coordinada (UTC), como en 2006-01-02T12:00:00Z, o en un formato donde se especifica la hora local y la zona horaria, como en 2006-01-02T04:00:00-08:00.</span><span class="sxs-lookup"><span data-stu-id="ee34f-118">The value of **StartDate** can be specified in coordinated universal time (UTC) format, as in 2006-01-02T12:00:00Z, or in a format where local time and time zone offset is specified, as in 2006-01-02T04:00:00-08:00.</span></span>  <br/><br/><span data-ttu-id="ee34f-119">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ee34f-119">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="ee34f-120">**EndDate**</span><span class="sxs-lookup"><span data-stu-id="ee34f-120">**EndDate**</span></span> <br/> |<span data-ttu-id="ee34f-121">Identifica el final de un intervalo de tiempo consultado para los elementos de calendario.</span><span class="sxs-lookup"><span data-stu-id="ee34f-121">Identifies the end of a time span queried for calendar items.</span></span> <span data-ttu-id="ee34f-122">No se devolverán todos los elementos de calendario que tengan una hora de inicio que sea posterior o posterior a **EndDate** .</span><span class="sxs-lookup"><span data-stu-id="ee34f-122">All calendar items that have a start time that is on or after **EndDate** will not be returned.</span></span> <span data-ttu-id="ee34f-123">El valor de **EndDate** puede especificarse en formato UTC, como en 2006-02-02T12:00:00Z, o en un formato en el que se especifica la hora local y el desplazamiento de zona horaria, como en 2006-02-02T04:00:00-08:00.</span><span class="sxs-lookup"><span data-stu-id="ee34f-123">The value of **EndDate** can be specified in UTC format, as in 2006-02-02T12:00:00Z, or in a format where local time and time zone offset is specified, as in 2006-02-02T04:00:00-08:00.</span></span>  <br/><br/><span data-ttu-id="ee34f-124">**EndDate** debe ser mayor o igual que **startDate**; de lo contrario, se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="ee34f-124">**EndDate** must be greater than or equal to **StartDate**; otherwise an error is returned.</span></span> <span data-ttu-id="ee34f-125">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ee34f-125">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ee34f-126">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ee34f-126">Child elements</span></span>

<span data-ttu-id="ee34f-127">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ee34f-127">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ee34f-128">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ee34f-128">Parent elements</span></span>

|<span data-ttu-id="ee34f-129">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ee34f-129">**Element**</span></span>|<span data-ttu-id="ee34f-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ee34f-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ee34f-131">FindItem</span><span class="sxs-lookup"><span data-stu-id="ee34f-131">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="ee34f-132">Define una solicitud para buscar elementos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="ee34f-132">Defines a request to find items in a mailbox.</span></span><br/><br/> <span data-ttu-id="ee34f-133">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="ee34f-133">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee34f-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ee34f-134">Remarks</span></span>

<span data-ttu-id="ee34f-135">Si el elemento **CalendarView** se especifica en una solicitud FindItem, el servicio Web devuelve una lista de elementos de calendario únicos y repeticiones de elementos de calendario periódicos dentro del intervalo especificado por **startDate** y **EndDate**.</span><span class="sxs-lookup"><span data-stu-id="ee34f-135">If the **CalendarView** element is specified in a FindItem request, the Web service returns a list of single calendar items and occurrences of recurring calendar items within the range specified by **StartDate** and **EndDate**.</span></span>
  
<span data-ttu-id="ee34f-136">Si el elemento **CalendarView** no se especifica en una solicitud FindItem, el servicio Web devuelve una lista de elementos de calendario únicos y elementos de calendario maestro periódicos.</span><span class="sxs-lookup"><span data-stu-id="ee34f-136">If the **CalendarView** element is not specified in a FindItem request, the Web service returns a list of single calendar items and recurring master calendar items.</span></span> <span data-ttu-id="ee34f-137">Las ocurrencias de calendario de un elemento de calendario periódico no se expanden.</span><span class="sxs-lookup"><span data-stu-id="ee34f-137">Calendar occurrences of a recurring calendar item are not expanded.</span></span> 
  
<span data-ttu-id="ee34f-138">Las consultas CalendarView solo deben usar las siguientes propiedades, ya que admiten consultas de calendario más rápidas.</span><span class="sxs-lookup"><span data-stu-id="ee34f-138">CalendarView queries should only make use of the following properties since they support faster calendar queries.</span></span>
  
### <a name="recurrence-blob-properties"></a><span data-ttu-id="ee34f-139">Propiedades del objeto binario de periodicidad</span><span class="sxs-lookup"><span data-stu-id="ee34f-139">Recurrence blob properties</span></span>
  
- <span data-ttu-id="ee34f-140">MapiStartTime</span><span class="sxs-lookup"><span data-stu-id="ee34f-140">MapiStartTime</span></span>
    
- <span data-ttu-id="ee34f-141">MapiEndTime</span><span class="sxs-lookup"><span data-stu-id="ee34f-141">MapiEndTime</span></span>
    
- <span data-ttu-id="ee34f-142">SubjectPrefixInternal</span><span class="sxs-lookup"><span data-stu-id="ee34f-142">SubjectPrefixInternal</span></span>
    
- <span data-ttu-id="ee34f-143">NormalizedSubjectInternal</span><span class="sxs-lookup"><span data-stu-id="ee34f-143">NormalizedSubjectInternal</span></span>
    
- <span data-ttu-id="ee34f-144">MapiSubject</span><span class="sxs-lookup"><span data-stu-id="ee34f-144">MapiSubject</span></span>
    
- <span data-ttu-id="ee34f-145">Ubicación</span><span class="sxs-lookup"><span data-stu-id="ee34f-145">Location</span></span>
    
- <span data-ttu-id="ee34f-146">AppointmentColor</span><span class="sxs-lookup"><span data-stu-id="ee34f-146">AppointmentColor</span></span>
    
- <span data-ttu-id="ee34f-147">MapiIsAllDayEvent</span><span class="sxs-lookup"><span data-stu-id="ee34f-147">MapiIsAllDayEvent</span></span>
    
- <span data-ttu-id="ee34f-148">MapiHasAttachment</span><span class="sxs-lookup"><span data-stu-id="ee34f-148">MapiHasAttachment</span></span>
    
- <span data-ttu-id="ee34f-149">FreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="ee34f-149">FreeBusyStatus</span></span>
    
- <span data-ttu-id="ee34f-150">ReminderIsSetInternal</span><span class="sxs-lookup"><span data-stu-id="ee34f-150">ReminderIsSetInternal</span></span>
    
- <span data-ttu-id="ee34f-151">ReminderMinutesBeforeStartInternal</span><span class="sxs-lookup"><span data-stu-id="ee34f-151">ReminderMinutesBeforeStartInternal</span></span>
    
- <span data-ttu-id="ee34f-152">AppointmentState</span><span class="sxs-lookup"><span data-stu-id="ee34f-152">AppointmentState</span></span>
    
- <span data-ttu-id="ee34f-153">AllAttachmentsHidden</span><span class="sxs-lookup"><span data-stu-id="ee34f-153">AllAttachmentsHidden</span></span>
    
- <span data-ttu-id="ee34f-154">ChangeHighlight</span><span class="sxs-lookup"><span data-stu-id="ee34f-154">ChangeHighlight</span></span>
    
### <a name="calculated-from-the-primary-recurrence-blob-or-master"></a><span data-ttu-id="ee34f-155">Calculado a partir del BLOB de periodicidad o el patrón principal</span><span class="sxs-lookup"><span data-stu-id="ee34f-155">Calculated from the primary recurrence blob or master</span></span>
  
- <span data-ttu-id="ee34f-156">ItemId</span><span class="sxs-lookup"><span data-stu-id="ee34f-156">ItemId</span></span>
    
- <span data-ttu-id="ee34f-157">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="ee34f-157">IsRecurring</span></span>
    
- <span data-ttu-id="ee34f-158">IsException</span><span class="sxs-lookup"><span data-stu-id="ee34f-158">IsException</span></span>
    
- <span data-ttu-id="ee34f-159">AppointmentRecurring</span><span class="sxs-lookup"><span data-stu-id="ee34f-159">AppointmentRecurring</span></span>
    
- <span data-ttu-id="ee34f-160">MapiStartTime</span><span class="sxs-lookup"><span data-stu-id="ee34f-160">MapiStartTime</span></span>
    
- <span data-ttu-id="ee34f-161">MapiPRStartDate</span><span class="sxs-lookup"><span data-stu-id="ee34f-161">MapiPRStartDate</span></span>
    
- <span data-ttu-id="ee34f-162">MapiEndTime</span><span class="sxs-lookup"><span data-stu-id="ee34f-162">MapiEndTime</span></span>
    
- <span data-ttu-id="ee34f-163">MapiPREndDate</span><span class="sxs-lookup"><span data-stu-id="ee34f-163">MapiPREndDate</span></span>
    
- <span data-ttu-id="ee34f-164">CalendarItemType</span><span class="sxs-lookup"><span data-stu-id="ee34f-164">CalendarItemType</span></span>
    
- <span data-ttu-id="ee34f-165">GlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="ee34f-165">GlobalObjectId</span></span>
    
- <span data-ttu-id="ee34f-166">TimeZoneDefinitionStart</span><span class="sxs-lookup"><span data-stu-id="ee34f-166">TimeZoneDefinitionStart</span></span>
    
- <span data-ttu-id="ee34f-167">TimeZoneDefinitionEnd</span><span class="sxs-lookup"><span data-stu-id="ee34f-167">TimeZoneDefinitionEnd</span></span>
    
### <a name="master-calendar-item-properties"></a><span data-ttu-id="ee34f-168">Propiedades de elemento de calendario principal</span><span class="sxs-lookup"><span data-stu-id="ee34f-168">Master calendar item properties</span></span>
  
- <span data-ttu-id="ee34f-169">EntryId</span><span class="sxs-lookup"><span data-stu-id="ee34f-169">EntryId</span></span>
    
- <span data-ttu-id="ee34f-170">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="ee34f-170">ChangeKey</span></span>
    
- <span data-ttu-id="ee34f-171">ItemClass</span><span class="sxs-lookup"><span data-stu-id="ee34f-171">ItemClass</span></span>
    
- <span data-ttu-id="ee34f-172">SentRepresentingEmailAddress</span><span class="sxs-lookup"><span data-stu-id="ee34f-172">SentRepresentingEmailAddress</span></span>
    
- <span data-ttu-id="ee34f-173">SentRepresentingDisplayName</span><span class="sxs-lookup"><span data-stu-id="ee34f-173">SentRepresentingDisplayName</span></span>
    
- <span data-ttu-id="ee34f-174">SentRepresentingEntryId</span><span class="sxs-lookup"><span data-stu-id="ee34f-174">SentRepresentingEntryId</span></span>
    
- <span data-ttu-id="ee34f-175">AppointmentRecurrenceBlob</span><span class="sxs-lookup"><span data-stu-id="ee34f-175">AppointmentRecurrenceBlob</span></span>
    
- <span data-ttu-id="ee34f-176">TimeZone</span><span class="sxs-lookup"><span data-stu-id="ee34f-176">TimeZone</span></span>
    
- <span data-ttu-id="ee34f-177">TimeZoneBlob</span><span class="sxs-lookup"><span data-stu-id="ee34f-177">TimeZoneBlob</span></span>
    
- <span data-ttu-id="ee34f-178">TimeZoneDefinitionRecurring</span><span class="sxs-lookup"><span data-stu-id="ee34f-178">TimeZoneDefinitionRecurring</span></span>
    
- <span data-ttu-id="ee34f-179">CleanGlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="ee34f-179">CleanGlobalObjectId</span></span>
    
- <span data-ttu-id="ee34f-180">AppointmentRecurring</span><span class="sxs-lookup"><span data-stu-id="ee34f-180">AppointmentRecurring</span></span>
    
- <span data-ttu-id="ee34f-181">IsException</span><span class="sxs-lookup"><span data-stu-id="ee34f-181">IsException</span></span>
    
- <span data-ttu-id="ee34f-182">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="ee34f-182">IsRecurring</span></span>
    
- <span data-ttu-id="ee34f-183">MapiSensitivity</span><span class="sxs-lookup"><span data-stu-id="ee34f-183">MapiSensitivity</span></span>
    
- <span data-ttu-id="ee34f-184">ContainerClass</span><span class="sxs-lookup"><span data-stu-id="ee34f-184">ContainerClass</span></span>
    
- <span data-ttu-id="ee34f-185">MapiPRStartDate</span><span class="sxs-lookup"><span data-stu-id="ee34f-185">MapiPRStartDate</span></span>
    
- <span data-ttu-id="ee34f-186">MapiPREndDate</span><span class="sxs-lookup"><span data-stu-id="ee34f-186">MapiPREndDate</span></span>
    
- <span data-ttu-id="ee34f-187">Categorías</span><span class="sxs-lookup"><span data-stu-id="ee34f-187">Categories</span></span>
    
<span data-ttu-id="ee34f-188">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ee34f-188">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="ee34f-189">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ee34f-189">Example</span></span>

<span data-ttu-id="ee34f-190">En el ejemplo siguiente se muestra una solicitud FindItem.</span><span class="sxs-lookup"><span data-stu-id="ee34f-190">The following example shows a FindItem request.</span></span> <span data-ttu-id="ee34f-191">Una solicitud correcta devuelve una respuesta que incluye los elementos del calendario que se iniciaron en 2006-05-18T00:00:00-08:00 o After y finalizan antes del 2006-05-19T00:00:00-08:00.</span><span class="sxs-lookup"><span data-stu-id="ee34f-191">A successful request returns a response that includes calendar items that started at 2006-05-18T00:00:00-08:00 or after and ended before 2006-05-19T00:00:00-08:00.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="calendar:Start"/>
          <t:FieldURI FieldURI="calendar:End"/>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <CalendarView MaxEntriesReturned="2" StartDate="2006-05-18T00:00:00-08:00" EndDate="2006-05-19T00:00:00-08:00"/>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="ee34f-192">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ee34f-192">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ee34f-193">Namespace</span><span class="sxs-lookup"><span data-stu-id="ee34f-193">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ee34f-194">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ee34f-194">Schema Name</span></span>  <br/> |<span data-ttu-id="ee34f-195">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ee34f-195">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ee34f-196">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ee34f-196">Validation File</span></span>  <br/> |<span data-ttu-id="ee34f-197">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ee34f-197">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ee34f-198">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ee34f-198">Can be Empty</span></span>  <br/> |<span data-ttu-id="ee34f-199">Falso</span><span class="sxs-lookup"><span data-stu-id="ee34f-199">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ee34f-200">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee34f-200">See also</span></span>

- [<span data-ttu-id="ee34f-201">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="ee34f-201">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="ee34f-202">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="ee34f-202">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

