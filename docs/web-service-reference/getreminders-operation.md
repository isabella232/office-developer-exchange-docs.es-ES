---
title: Operación GetReminders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1b56f83f-3b87-4b55-8259-fde6692da681
description: Busque información sobre la EWS GetReminders operación.
ms.openlocfilehash: 803dabf51b94dbd8fb01f2709a42ff59a597bfd1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764959"
---
# <a name="getreminders-operation"></a><span data-ttu-id="f39c2-103">Operación GetReminders</span><span class="sxs-lookup"><span data-stu-id="f39c2-103">GetReminders operation</span></span>

<span data-ttu-id="f39c2-104">Obtenga información acerca de la operación de EWS **GetReminders** .</span><span class="sxs-lookup"><span data-stu-id="f39c2-104">Find information about the **GetReminders** EWS operation.</span></span> 
  
<span data-ttu-id="f39c2-105">La operación de Exchange Web Services (EWS) **GetReminders** recupera avisos para los elementos de calendario y tareas.</span><span class="sxs-lookup"><span data-stu-id="f39c2-105">The **GetReminders** Exchange Web Services (EWS) operation retrieves reminders for calendar and task items.</span></span> 
  
<span data-ttu-id="f39c2-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f39c2-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getreminders-operation"></a><span data-ttu-id="f39c2-107">Mediante la operación GetReminders</span><span class="sxs-lookup"><span data-stu-id="f39c2-107">Using the GetReminders operation</span></span>

<span data-ttu-id="f39c2-108">La operación **GetReminders** obtiene avisos de calendario actual y futuro y elementos de tarea en el buzón del usuario, según los valores de elemento que se pasan en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f39c2-108">The **GetReminders** operation gets reminders for current and future calendar and task items in the user's mailbox, depending on the element values passed in the request.</span></span> <span data-ttu-id="f39c2-109">La operación puede recuperar todos los elementos de calendario actuales y futuros así como las tareas que tienen un aviso a establecer.</span><span class="sxs-lookup"><span data-stu-id="f39c2-109">The operation can retrieve all current and future calendar items as well as tasks that have a reminder set.</span></span> <span data-ttu-id="f39c2-110">Elementos de calendario privados se incluyen en las respuestas.</span><span class="sxs-lookup"><span data-stu-id="f39c2-110">Private calendar items are included in responses.</span></span> <span data-ttu-id="f39c2-111">Tareas sin avisos no se incluyen en las respuestas, ni son mensajes de correo electrónico con avisos o marcas de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="f39c2-111">Tasks without reminders are not included in responses, nor are emails with reminders or follow up flags.</span></span> 
  
<span data-ttu-id="f39c2-112">Para recuperar todos los avisos actuales, se recomienda establecer el [ReminderType](remindertype.md) a **todos** y la [hora de finalización](endtime-remindermessagedatatype.md) a la hora actual.</span><span class="sxs-lookup"><span data-stu-id="f39c2-112">To retrieve all current reminders, we recommend setting the [ReminderType](remindertype.md) to **All** and the [EndTime](endtime-remindermessagedatatype.md) to the current time.</span></span> 
  
<span data-ttu-id="f39c2-113">Si los elementos [BeginTime](begintime.md) y **EndTime** se incluyen en la solicitud, la respuesta incluye avisos para cualquier calendario y elementos de tarea que se producen entre tengan un aviso que se produce entre el **BeginTime** y **EndTime**.</span><span class="sxs-lookup"><span data-stu-id="f39c2-113">If the [BeginTime](begintime.md) and **EndTime** elements are included in the request, the response includes reminders for any calendar and task items that occur between have a reminder that occurs between the **BeginTime** and **EndTime**.</span></span>
  
<span data-ttu-id="f39c2-114">En la siguiente tabla se describe el comportamiento del elemento **ReminderType** cuando se incluyen los elementos **BeginTime** y **EndTime** .</span><span class="sxs-lookup"><span data-stu-id="f39c2-114">The following table describes the behavior of the **ReminderType** element when the **BeginTime** and **EndTime** elements are included.</span></span> 
  
|<span data-ttu-id="f39c2-115">ReminderType ** elemento valor **</span><span class="sxs-lookup"><span data-stu-id="f39c2-115">****ReminderType** element value**</span></span>|<span data-ttu-id="f39c2-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f39c2-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f39c2-117">Todos</span><span class="sxs-lookup"><span data-stu-id="f39c2-117">All</span></span>  <br/> |<span data-ttu-id="f39c2-118">Avisos que se producen entre el **BeginTime** y **EndTime**.</span><span class="sxs-lookup"><span data-stu-id="f39c2-118">Reminders that occur between the **BeginTime** and **EndTime**.</span></span>  <br/> |
|<span data-ttu-id="f39c2-119">Actual</span><span class="sxs-lookup"><span data-stu-id="f39c2-119">Current</span></span>  <br/> |<span data-ttu-id="f39c2-120">Avisos devueltos por **todos los**, además de avisos que sean anteriores a la ventana de tiempo solicitado si el evento todavía está en curso, además de todas las citas independientemente de su antigüedad.</span><span class="sxs-lookup"><span data-stu-id="f39c2-120">Reminders returned by **All**, plus reminders that are earlier than the requested time window if the event is still ongoing, plus all appointments regardless of age.</span></span>  <br/> |
|<span data-ttu-id="f39c2-121">Antiguo</span><span class="sxs-lookup"><span data-stu-id="f39c2-121">Old</span></span>  <br/> |<span data-ttu-id="f39c2-122">Avisos devueltos por **todos los**, menos eventos que no se han completado todavía, menos todas las citas.</span><span class="sxs-lookup"><span data-stu-id="f39c2-122">Reminders returned by **All**, minus events that haven't completed yet, minus all appointments.</span></span> <span data-ttu-id="f39c2-123">Los elementos **BeginTime** y **EndTime** deben establecerse para usar el valor **anterior** .</span><span class="sxs-lookup"><span data-stu-id="f39c2-123">The **BeginTime** and **EndTime** elements must be set to use the **Old** value.</span></span>  <br/> |
   
### <a name="getreminders-operation-soap-headers"></a><span data-ttu-id="f39c2-124">Encabezados SOAP de operación de GetReminders</span><span class="sxs-lookup"><span data-stu-id="f39c2-124">GetReminders operation SOAP headers</span></span>

<span data-ttu-id="f39c2-125">La operación de **GetReminders** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="f39c2-125">The **GetReminders** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="f39c2-126">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="f39c2-126">**Header name**</span></span>|<span data-ttu-id="f39c2-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="f39c2-127">**Element**</span></span>|<span data-ttu-id="f39c2-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f39c2-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f39c2-129">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="f39c2-129">**Impersonation**</span></span> <br/> |[<span data-ttu-id="f39c2-130">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="f39c2-130">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="f39c2-131">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="f39c2-131">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="f39c2-132">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="f39c2-132">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f39c2-133">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="f39c2-133">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="f39c2-134">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="f39c2-134">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="f39c2-135">Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón.</span><span class="sxs-lookup"><span data-stu-id="f39c2-135">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="f39c2-136">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="f39c2-136">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f39c2-137">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="f39c2-137">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="f39c2-138">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="f39c2-138">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="f39c2-139">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="f39c2-139">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="f39c2-140">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="f39c2-140">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f39c2-141">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="f39c2-141">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="f39c2-142">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="f39c2-142">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="f39c2-143">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f39c2-143">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="f39c2-144">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="f39c2-144">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getreminders-operation-request-example"></a><span data-ttu-id="f39c2-145">Ejemplo de solicitud de operación de GetReminders</span><span class="sxs-lookup"><span data-stu-id="f39c2-145">GetReminders operation request example</span></span>

<span data-ttu-id="f39c2-146">El siguiente ejemplo de una solicitud de operación **GetReminders** muestra cómo recuperar los primeros elementos de cinco calendario que se producen entre el **BeginTime** y **EndTime**.</span><span class="sxs-lookup"><span data-stu-id="f39c2-146">The following example of a **GetReminders** operation request shows how to retrieve the first five calendar items that occur between the **BeginTime** and **EndTime**.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:GetReminders>
      <m:EndTime>2014-04-16T21:00:00Z</m:EndTime>
      <m:ReminderType>All</m:ReminderType>
    </m:GetReminders>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="f39c2-147">El ejemplo de solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="f39c2-147">The example request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f39c2-148">GetReminders</span><span class="sxs-lookup"><span data-stu-id="f39c2-148">GetReminders</span></span>](getreminders.md)
    
- [<span data-ttu-id="f39c2-149">Hora de finalización</span><span class="sxs-lookup"><span data-stu-id="f39c2-149">EndTime</span></span>](endtime-remindermessagedatatype.md)
    
- [<span data-ttu-id="f39c2-150">ReminderType</span><span class="sxs-lookup"><span data-stu-id="f39c2-150">ReminderType</span></span>](remindertype.md)
    
<span data-ttu-id="f39c2-151">El cuerpo SOAP también puede contener los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="f39c2-151">The SOAP body can also contain the following elements:</span></span>
  
- [<span data-ttu-id="f39c2-152">BeginTime</span><span class="sxs-lookup"><span data-stu-id="f39c2-152">BeginTime</span></span>](begintime.md)
    
- [<span data-ttu-id="f39c2-153">MaxItems</span><span class="sxs-lookup"><span data-stu-id="f39c2-153">MaxItems</span></span>](maxitems.md)
    
## <a name="successful-getreminders-operation-response"></a><span data-ttu-id="f39c2-154">Respuesta es correcta de operación GetReminders</span><span class="sxs-lookup"><span data-stu-id="f39c2-154">Successful GetReminders operation response</span></span>

<span data-ttu-id="f39c2-155">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **GetReminders** .</span><span class="sxs-lookup"><span data-stu-id="f39c2-155">The following example shows a successful response to a **GetReminders** operation request.</span></span> <span data-ttu-id="f39c2-156">La respuesta contiene un aviso para el elemento de calendario "Reunión de equipo" y un aviso para la tarea "De tareas para enviar notas de la reunión".</span><span class="sxs-lookup"><span data-stu-id="f39c2-156">The response contains a reminder for the "Team meeting" calendar item and a reminder for the "Task to send meeting notes" task.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f39c2-157">Se han abreviado identificadores para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="f39c2-157">Identifiers have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="7"
                       Version="V2_10"
                       xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRemindersResponse ResponseClass="Success"
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <Reminders>
        <Reminder xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Subject>Team meeting</Subject>
          <Location />
          <ReminderTime>2014-04-15T21:00:00Z</ReminderTime>
          <StartDate>2014-04-15T21:00:00Z</StartDate>
          <EndDate>2014-04-15T21:30:00Z</EndDate>
          <ItemId Id="vQAAAA=="
                  ChangeKey="DwAAABYAAAB4to43JyybTYwHLBM1k8MxAAACRoV4" />
          <RecurringMasterItemId Id="K7u5AAA=" ChangeKey="DwAAABYAAAB4to43JyybTYwHLBM1k8MxAAACRoV0" />
          <ReminderGroup>Calendar</ReminderGroup>
          <UID>6CF2FA62</UID>
        </Reminder>
        <Reminder xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Subject>Task to send meeting notes</Subject>
          <Location />
          <ReminderTime>2014-04-16T14:00:00Z</ReminderTime>
          <StartDate>0001-01-02T00:00:00Z</StartDate>
          <EndDate>0001-01-02T00:00:00Z</EndDate>
          <ItemId Id="vAAAAA=="
                  ChangeKey="EwAAABQAAACOs0HEMq1WTKpI7sNu5qXNAAAIDg==" />
          <ReminderGroup>Task</ReminderGroup>
          <UID>vAAAAA==</UID>
        </Reminder>
      </Reminders>
    </GetRemindersResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="f39c2-158">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="f39c2-158">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f39c2-159">GetRemindersResponse</span><span class="sxs-lookup"><span data-stu-id="f39c2-159">GetRemindersResponse</span></span>](getremindersresponse.md)
    
- [<span data-ttu-id="f39c2-160">Reminders</span><span class="sxs-lookup"><span data-stu-id="f39c2-160">Reminders</span></span>](reminders.md)
    
- [<span data-ttu-id="f39c2-161">Aviso</span><span class="sxs-lookup"><span data-stu-id="f39c2-161">Reminder</span></span>](reminder.md)
    
- [<span data-ttu-id="f39c2-162">Subject</span><span class="sxs-lookup"><span data-stu-id="f39c2-162">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="f39c2-163">Location</span><span class="sxs-lookup"><span data-stu-id="f39c2-163">Location</span></span>](location-remindermessagedatatype.md)
    
- [<span data-ttu-id="f39c2-164">ReminderTime</span><span class="sxs-lookup"><span data-stu-id="f39c2-164">ReminderTime</span></span>](remindertime.md)
    
- [<span data-ttu-id="f39c2-165">StartDate</span><span class="sxs-lookup"><span data-stu-id="f39c2-165">StartDate</span></span>](startdate.md)
    
- [<span data-ttu-id="f39c2-166">EndDate</span><span class="sxs-lookup"><span data-stu-id="f39c2-166">EndDate</span></span>](enddate-remindertype.md)
    
- [<span data-ttu-id="f39c2-167">ItemId</span><span class="sxs-lookup"><span data-stu-id="f39c2-167">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="f39c2-168">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="f39c2-168">RecurringMasterItemId</span></span>](recurringmasteritemid.md)
    
- [<span data-ttu-id="f39c2-169">ReminderGroup</span><span class="sxs-lookup"><span data-stu-id="f39c2-169">ReminderGroup</span></span>](remindergroup.md)
    
- [<span data-ttu-id="f39c2-170">UID</span><span class="sxs-lookup"><span data-stu-id="f39c2-170">UID</span></span>](uid-remindertype.md)
    
## <a name="getreminders-operation-error-response-example"></a><span data-ttu-id="f39c2-171">Ejemplo de respuesta de error de operación de GetReminders</span><span class="sxs-lookup"><span data-stu-id="f39c2-171">GetReminders operation error response example</span></span>

<span data-ttu-id="f39c2-172">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **GetReminders** .</span><span class="sxs-lookup"><span data-stu-id="f39c2-172">The following example shows an error response to a **GetReminders** operation request.</span></span> <span data-ttu-id="f39c2-173">Esta es una respuesta a una solicitud en el que la fecha de finalización era anterior a la fecha de inicio.</span><span class="sxs-lookup"><span data-stu-id="f39c2-173">This is a response to a request in which the end date was earlier than the start date.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="7"
                       Version="V2_10"
                       xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRemindersResponse ResponseClass="Error"
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>EndDate is earlier than StartDate</MessageText>
      <ResponseCode>ErrorInvalidOperation</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetRemindersResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="f39c2-174">La respuesta de error SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="f39c2-174">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f39c2-175">GetRemindersResponse</span><span class="sxs-lookup"><span data-stu-id="f39c2-175">GetRemindersResponse</span></span>](getremindersresponse.md)
    
- [<span data-ttu-id="f39c2-176">MessageText</span><span class="sxs-lookup"><span data-stu-id="f39c2-176">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="f39c2-177">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f39c2-177">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f39c2-178">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f39c2-178">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="f39c2-179">Para códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="f39c2-179">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f39c2-180">Ver también</span><span class="sxs-lookup"><span data-stu-id="f39c2-180">See also</span></span>


- [<span data-ttu-id="f39c2-181">PerformReminderAction</span><span class="sxs-lookup"><span data-stu-id="f39c2-181">PerformReminderAction</span></span>](performreminderaction.md)
    

