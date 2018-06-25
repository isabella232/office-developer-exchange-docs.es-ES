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
description: El elemento CalendarView define una operación FindItem como devolver elementos de calendario en un conjunto, tal como aparecen en un calendario.
ms.openlocfilehash: 79b5ad268a8013092c1122c99bdcd10d876abf2c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763717"
---
# <a name="calendarview"></a><span data-ttu-id="6df9e-103">CalendarView</span><span class="sxs-lookup"><span data-stu-id="6df9e-103">CalendarView</span></span>

<span data-ttu-id="6df9e-104">El elemento **CalendarView** define una [operación FindItem](finditem-operation.md) como devolver elementos de calendario en un conjunto, tal como aparecen en un calendario.</span><span class="sxs-lookup"><span data-stu-id="6df9e-104">The **CalendarView** element defines a [FindItem operation](finditem-operation.md) as returning calendar items in a set as they appear in a calendar.</span></span> 
  
[<span data-ttu-id="6df9e-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="6df9e-105">FindItem</span></span>](finditem.md)
  
[<span data-ttu-id="6df9e-106">CalendarView</span><span class="sxs-lookup"><span data-stu-id="6df9e-106">CalendarView</span></span>](calendarview.md)
  
```XML
<CalendarView MaxEntriesReturned="" StartDate="" EndDate="" />
```

<span data-ttu-id="6df9e-107">**CalendarView**</span><span class="sxs-lookup"><span data-stu-id="6df9e-107">**CalendarView**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6df9e-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6df9e-108">Attributes and elements</span></span>

<span data-ttu-id="6df9e-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6df9e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6df9e-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="6df9e-110">Attributes</span></span>

|<span data-ttu-id="6df9e-111">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="6df9e-111">**Attribute**</span></span>|<span data-ttu-id="6df9e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6df9e-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6df9e-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="6df9e-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="6df9e-114">Describe el número máximo de resultados a devolver en la respuesta FindItem.</span><span class="sxs-lookup"><span data-stu-id="6df9e-114">Describes the maximum number of results to return in the FindItem response.</span></span>  <br/> |
|<span data-ttu-id="6df9e-115">**StartDate**</span><span class="sxs-lookup"><span data-stu-id="6df9e-115">**StartDate**</span></span> <br/> |<span data-ttu-id="6df9e-116">Identifica el inicio de un intervalo de tiempo de consulta para los elementos del calendario.</span><span class="sxs-lookup"><span data-stu-id="6df9e-116">Identifies the start of a time span queried for calendar items.</span></span> <span data-ttu-id="6df9e-117">Todos los elementos de calendario que tienen una hora de finalización que no antes se devolverán **StartDate** .</span><span class="sxs-lookup"><span data-stu-id="6df9e-117">All calendar items that have an end time that is before **StartDate** will not be returned.</span></span> <span data-ttu-id="6df9e-118">Se puede especificar el valor de **StartDate** en formato de hora universal coordinada (UTC), al igual que en 2006-01-02T12:00:00Z, o en un formato donde se especifica el desplazamiento de hora local y la zona horaria, al igual que en 2006-01-02T04:00:00-08:00.</span><span class="sxs-lookup"><span data-stu-id="6df9e-118">The value of **StartDate** can be specified in coordinated universal time (UTC) format, as in 2006-01-02T12:00:00Z, or in a format where local time and time zone offset is specified, as in 2006-01-02T04:00:00-08:00.</span></span>  <br/><br/><span data-ttu-id="6df9e-119">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="6df9e-119">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="6df9e-120">**EndDate**</span><span class="sxs-lookup"><span data-stu-id="6df9e-120">**EndDate**</span></span> <br/> |<span data-ttu-id="6df9e-121">Identifica el final de un intervalo de tiempo de consulta para los elementos del calendario.</span><span class="sxs-lookup"><span data-stu-id="6df9e-121">Identifies the end of a time span queried for calendar items.</span></span> <span data-ttu-id="6df9e-122">No se devolverán todos los elementos de calendario que tienen una hora de inicio que se encuentra en o después de la **fecha de finalización** .</span><span class="sxs-lookup"><span data-stu-id="6df9e-122">All calendar items that have a start time that is on or after **EndDate** will not be returned.</span></span> <span data-ttu-id="6df9e-123">Se puede especificar el valor de **fecha de finalización** en formato UTC, como se muestra en 2006-02-02T12:00:00Z, o en un formato donde se especifica el desplazamiento de hora local y la zona horaria, al igual que en 2006-02-02T04:00:00-08:00.</span><span class="sxs-lookup"><span data-stu-id="6df9e-123">The value of **EndDate** can be specified in UTC format, as in 2006-02-02T12:00:00Z, or in a format where local time and time zone offset is specified, as in 2006-02-02T04:00:00-08:00.</span></span>  <br/><br/><span data-ttu-id="6df9e-124">**Fecha de finalización** debe ser mayor o igual a **StartDate**; en caso contrario, se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="6df9e-124">**EndDate** must be greater than or equal to **StartDate**; otherwise an error is returned.</span></span> <span data-ttu-id="6df9e-125">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="6df9e-125">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6df9e-126">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6df9e-126">Child elements</span></span>

<span data-ttu-id="6df9e-127">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6df9e-127">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6df9e-128">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6df9e-128">Parent elements</span></span>

|<span data-ttu-id="6df9e-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="6df9e-129">**Element**</span></span>|<span data-ttu-id="6df9e-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6df9e-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6df9e-131">FindItem</span><span class="sxs-lookup"><span data-stu-id="6df9e-131">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="6df9e-132">Define una solicitud para buscar elementos en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="6df9e-132">Defines a request to find items in a mailbox.</span></span><br/><br/> <span data-ttu-id="6df9e-133">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="6df9e-133">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6df9e-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6df9e-134">Remarks</span></span>

<span data-ttu-id="6df9e-135">Si el elemento **CalendarView** está especificado en una solicitud FindItem, el servicio Web devuelve una lista de elementos de calendario único y las apariciones de los elementos de calendario periódicos dentro del intervalo especificado por **StartDate** y **EndDate**.</span><span class="sxs-lookup"><span data-stu-id="6df9e-135">If the **CalendarView** element is specified in a FindItem request, the Web service returns a list of single calendar items and occurrences of recurring calendar items within the range specified by **StartDate** and **EndDate**.</span></span>
  
<span data-ttu-id="6df9e-136">Si no se especifica el elemento **CalendarView** en una solicitud FindItem, el servicio Web devuelve una lista de elementos de calendario único y elementos periódicos del calendario principal.</span><span class="sxs-lookup"><span data-stu-id="6df9e-136">If the **CalendarView** element is not specified in a FindItem request, the Web service returns a list of single calendar items and recurring master calendar items.</span></span> <span data-ttu-id="6df9e-137">Repeticiones de calendario de un elemento periódico de calendario no se expanden.</span><span class="sxs-lookup"><span data-stu-id="6df9e-137">Calendar occurrences of a recurring calendar item are not expanded.</span></span> 
  
<span data-ttu-id="6df9e-138">Solo deben realizar consultas CalendarView utilizar de las siguientes propiedades, ya que estos admiten las consultas de calendario más rápidas.</span><span class="sxs-lookup"><span data-stu-id="6df9e-138">CalendarView queries should only make use of the following properties since they support faster calendar queries.</span></span>
  
### <a name="recurrence-blob-properties"></a><span data-ttu-id="6df9e-139">Propiedades de blob de periodicidad</span><span class="sxs-lookup"><span data-stu-id="6df9e-139">Recurrence blob properties</span></span>
  
- <span data-ttu-id="6df9e-140">MapiStartTime</span><span class="sxs-lookup"><span data-stu-id="6df9e-140">MapiStartTime</span></span>
    
- <span data-ttu-id="6df9e-141">MapiEndTime</span><span class="sxs-lookup"><span data-stu-id="6df9e-141">MapiEndTime</span></span>
    
- <span data-ttu-id="6df9e-142">SubjectPrefixInternal</span><span class="sxs-lookup"><span data-stu-id="6df9e-142">SubjectPrefixInternal</span></span>
    
- <span data-ttu-id="6df9e-143">NormalizedSubjectInternal</span><span class="sxs-lookup"><span data-stu-id="6df9e-143">NormalizedSubjectInternal</span></span>
    
- <span data-ttu-id="6df9e-144">MapiSubject</span><span class="sxs-lookup"><span data-stu-id="6df9e-144">MapiSubject</span></span>
    
- <span data-ttu-id="6df9e-145">Ubicación</span><span class="sxs-lookup"><span data-stu-id="6df9e-145">Location</span></span>
    
- <span data-ttu-id="6df9e-146">AppointmentColor</span><span class="sxs-lookup"><span data-stu-id="6df9e-146">AppointmentColor</span></span>
    
- <span data-ttu-id="6df9e-147">MapiIsAllDayEvent</span><span class="sxs-lookup"><span data-stu-id="6df9e-147">MapiIsAllDayEvent</span></span>
    
- <span data-ttu-id="6df9e-148">MapiHasAttachment</span><span class="sxs-lookup"><span data-stu-id="6df9e-148">MapiHasAttachment</span></span>
    
- <span data-ttu-id="6df9e-149">FreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="6df9e-149">FreeBusyStatus</span></span>
    
- <span data-ttu-id="6df9e-150">ReminderIsSetInternal</span><span class="sxs-lookup"><span data-stu-id="6df9e-150">ReminderIsSetInternal</span></span>
    
- <span data-ttu-id="6df9e-151">ReminderMinutesBeforeStartInternal</span><span class="sxs-lookup"><span data-stu-id="6df9e-151">ReminderMinutesBeforeStartInternal</span></span>
    
- <span data-ttu-id="6df9e-152">AppointmentState</span><span class="sxs-lookup"><span data-stu-id="6df9e-152">AppointmentState</span></span>
    
- <span data-ttu-id="6df9e-153">AllAttachmentsHidden</span><span class="sxs-lookup"><span data-stu-id="6df9e-153">AllAttachmentsHidden</span></span>
    
- <span data-ttu-id="6df9e-154">ChangeHighlight</span><span class="sxs-lookup"><span data-stu-id="6df9e-154">ChangeHighlight</span></span>
    
### <a name="calculated-from-the-primary-recurrence-blob-or-master"></a><span data-ttu-id="6df9e-155">Calcular a partir la blob de periodicidad principal o del patrón</span><span class="sxs-lookup"><span data-stu-id="6df9e-155">Calculated from the primary recurrence blob or master</span></span>
  
- <span data-ttu-id="6df9e-156">ItemId</span><span class="sxs-lookup"><span data-stu-id="6df9e-156">ItemId</span></span>
    
- <span data-ttu-id="6df9e-157">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="6df9e-157">IsRecurring</span></span>
    
- <span data-ttu-id="6df9e-158">IsException</span><span class="sxs-lookup"><span data-stu-id="6df9e-158">IsException</span></span>
    
- <span data-ttu-id="6df9e-159">AppointmentRecurring</span><span class="sxs-lookup"><span data-stu-id="6df9e-159">AppointmentRecurring</span></span>
    
- <span data-ttu-id="6df9e-160">MapiStartTime</span><span class="sxs-lookup"><span data-stu-id="6df9e-160">MapiStartTime</span></span>
    
- <span data-ttu-id="6df9e-161">MapiPRStartDate</span><span class="sxs-lookup"><span data-stu-id="6df9e-161">MapiPRStartDate</span></span>
    
- <span data-ttu-id="6df9e-162">MapiEndTime</span><span class="sxs-lookup"><span data-stu-id="6df9e-162">MapiEndTime</span></span>
    
- <span data-ttu-id="6df9e-163">MapiPREndDate</span><span class="sxs-lookup"><span data-stu-id="6df9e-163">MapiPREndDate</span></span>
    
- <span data-ttu-id="6df9e-164">CalendarItemType</span><span class="sxs-lookup"><span data-stu-id="6df9e-164">CalendarItemType</span></span>
    
- <span data-ttu-id="6df9e-165">GlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="6df9e-165">GlobalObjectId</span></span>
    
- <span data-ttu-id="6df9e-166">TimeZoneDefinitionStart</span><span class="sxs-lookup"><span data-stu-id="6df9e-166">TimeZoneDefinitionStart</span></span>
    
- <span data-ttu-id="6df9e-167">TimeZoneDefinitionEnd</span><span class="sxs-lookup"><span data-stu-id="6df9e-167">TimeZoneDefinitionEnd</span></span>
    
### <a name="master-calendar-item-properties"></a><span data-ttu-id="6df9e-168">Propiedades de elementos de calendario principal</span><span class="sxs-lookup"><span data-stu-id="6df9e-168">Master calendar item properties</span></span>
  
- <span data-ttu-id="6df9e-169">Propiedad EntryId</span><span class="sxs-lookup"><span data-stu-id="6df9e-169">EntryId</span></span>
    
- <span data-ttu-id="6df9e-170">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="6df9e-170">ChangeKey</span></span>
    
- <span data-ttu-id="6df9e-171">ItemClass</span><span class="sxs-lookup"><span data-stu-id="6df9e-171">ItemClass</span></span>
    
- <span data-ttu-id="6df9e-172">SentRepresentingEmailAddress</span><span class="sxs-lookup"><span data-stu-id="6df9e-172">SentRepresentingEmailAddress</span></span>
    
- <span data-ttu-id="6df9e-173">SentRepresentingDisplayName</span><span class="sxs-lookup"><span data-stu-id="6df9e-173">SentRepresentingDisplayName</span></span>
    
- <span data-ttu-id="6df9e-174">SentRepresentingEntryId</span><span class="sxs-lookup"><span data-stu-id="6df9e-174">SentRepresentingEntryId</span></span>
    
- <span data-ttu-id="6df9e-175">AppointmentRecurrenceBlob</span><span class="sxs-lookup"><span data-stu-id="6df9e-175">AppointmentRecurrenceBlob</span></span>
    
- <span data-ttu-id="6df9e-176">TimeZone</span><span class="sxs-lookup"><span data-stu-id="6df9e-176">TimeZone</span></span>
    
- <span data-ttu-id="6df9e-177">TimeZoneBlob</span><span class="sxs-lookup"><span data-stu-id="6df9e-177">TimeZoneBlob</span></span>
    
- <span data-ttu-id="6df9e-178">TimeZoneDefinitionRecurring</span><span class="sxs-lookup"><span data-stu-id="6df9e-178">TimeZoneDefinitionRecurring</span></span>
    
- <span data-ttu-id="6df9e-179">CleanGlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="6df9e-179">CleanGlobalObjectId</span></span>
    
- <span data-ttu-id="6df9e-180">AppointmentRecurring</span><span class="sxs-lookup"><span data-stu-id="6df9e-180">AppointmentRecurring</span></span>
    
- <span data-ttu-id="6df9e-181">IsException</span><span class="sxs-lookup"><span data-stu-id="6df9e-181">IsException</span></span>
    
- <span data-ttu-id="6df9e-182">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="6df9e-182">IsRecurring</span></span>
    
- <span data-ttu-id="6df9e-183">MapiSensitivity</span><span class="sxs-lookup"><span data-stu-id="6df9e-183">MapiSensitivity</span></span>
    
- <span data-ttu-id="6df9e-184">ContainerClass</span><span class="sxs-lookup"><span data-stu-id="6df9e-184">ContainerClass</span></span>
    
- <span data-ttu-id="6df9e-185">MapiPRStartDate</span><span class="sxs-lookup"><span data-stu-id="6df9e-185">MapiPRStartDate</span></span>
    
- <span data-ttu-id="6df9e-186">MapiPREndDate</span><span class="sxs-lookup"><span data-stu-id="6df9e-186">MapiPREndDate</span></span>
    
- <span data-ttu-id="6df9e-187">Categorías</span><span class="sxs-lookup"><span data-stu-id="6df9e-187">Categories</span></span>
    
<span data-ttu-id="6df9e-188">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6df9e-188">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="6df9e-189">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6df9e-189">Example</span></span>

<span data-ttu-id="6df9e-190">En el ejemplo siguiente se muestra una solicitud FindItem.</span><span class="sxs-lookup"><span data-stu-id="6df9e-190">The following example shows a FindItem request.</span></span> <span data-ttu-id="6df9e-191">Una solicitud correcta devuelve una respuesta que incluye los elementos de calendario que se iniciaron a 2006-05-18T00:00:00-08:00 o posterior y terminado antes de 2006-05-19T00:00:00-08:00.</span><span class="sxs-lookup"><span data-stu-id="6df9e-191">A successful request returns a response that includes calendar items that started at 2006-05-18T00:00:00-08:00 or after and ended before 2006-05-19T00:00:00-08:00.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="element-information"></a><span data-ttu-id="6df9e-192">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6df9e-192">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6df9e-193">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6df9e-193">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6df9e-194">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6df9e-194">Schema Name</span></span>  <br/> |<span data-ttu-id="6df9e-195">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="6df9e-195">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6df9e-196">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6df9e-196">Validation File</span></span>  <br/> |<span data-ttu-id="6df9e-197">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6df9e-197">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6df9e-198">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6df9e-198">Can be Empty</span></span>  <br/> |<span data-ttu-id="6df9e-199">False</span><span class="sxs-lookup"><span data-stu-id="6df9e-199">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6df9e-200">Vea también</span><span class="sxs-lookup"><span data-stu-id="6df9e-200">See also</span></span>

- [<span data-ttu-id="6df9e-201">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="6df9e-201">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="6df9e-202">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="6df9e-202">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

