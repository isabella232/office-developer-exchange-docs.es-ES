---
title: Operación GetReminders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1b56f83f-3b87-4b55-8259-fde6692da681
description: Buscar información sobre la operación de EWS de GetReminders.
ms.openlocfilehash: dcbe20c674d7524a7776d374fa6964899abf472f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458309"
---
# <a name="getreminders-operation"></a><span data-ttu-id="dec83-103">Operación GetReminders</span><span class="sxs-lookup"><span data-stu-id="dec83-103">GetReminders operation</span></span>

<span data-ttu-id="dec83-104">Buscar información sobre la operación de EWS de **GetReminders** .</span><span class="sxs-lookup"><span data-stu-id="dec83-104">Find information about the **GetReminders** EWS operation.</span></span> 
  
<span data-ttu-id="dec83-105">La operación **GetReminders** de servicios web Exchange (EWS) recupera avisos para los elementos de calendario y tarea.</span><span class="sxs-lookup"><span data-stu-id="dec83-105">The **GetReminders** Exchange Web Services (EWS) operation retrieves reminders for calendar and task items.</span></span> 
  
<span data-ttu-id="dec83-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dec83-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getreminders-operation"></a><span data-ttu-id="dec83-107">Uso de la operación GetReminders</span><span class="sxs-lookup"><span data-stu-id="dec83-107">Using the GetReminders operation</span></span>

<span data-ttu-id="dec83-108">La operación **GetReminders** obtiene avisos para los elementos de calendario y tarea actuales y futuros en el buzón de correo del usuario, en función de los valores de elemento que se pasan en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dec83-108">The **GetReminders** operation gets reminders for current and future calendar and task items in the user's mailbox, depending on the element values passed in the request.</span></span> <span data-ttu-id="dec83-109">La operación puede recuperar todos los elementos de calendario actuales y futuros, así como las tareas que tienen un conjunto de avisos.</span><span class="sxs-lookup"><span data-stu-id="dec83-109">The operation can retrieve all current and future calendar items as well as tasks that have a reminder set.</span></span> <span data-ttu-id="dec83-110">Los elementos de calendario privados se incluyen en las respuestas.</span><span class="sxs-lookup"><span data-stu-id="dec83-110">Private calendar items are included in responses.</span></span> <span data-ttu-id="dec83-111">Las tareas sin avisos no se incluyen en las respuestas ni son mensajes de correo electrónico con avisos o marcas de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="dec83-111">Tasks without reminders are not included in responses, nor are emails with reminders or follow up flags.</span></span> 
  
<span data-ttu-id="dec83-112">Para recuperar todos los avisos actuales, se recomienda establecer [ReminderType](remindertype.md) en **All** y el [EndTime](endtime-remindermessagedatatype.md) en la hora actual.</span><span class="sxs-lookup"><span data-stu-id="dec83-112">To retrieve all current reminders, we recommend setting the [ReminderType](remindertype.md) to **All** and the [EndTime](endtime-remindermessagedatatype.md) to the current time.</span></span> 
  
<span data-ttu-id="dec83-113">Si los elementos [BeginTime](begintime.md) y **EndTime** se incluyen en la solicitud, la respuesta incluye avisos para todos los elementos de calendario y tarea que se producen entre los que tienen un aviso entre la BeginTime **y la**hora de finalización. **BeginTime**</span><span class="sxs-lookup"><span data-stu-id="dec83-113">If the [BeginTime](begintime.md) and **EndTime** elements are included in the request, the response includes reminders for any calendar and task items that occur between have a reminder that occurs between the **BeginTime** and **EndTime**.</span></span>
  
<span data-ttu-id="dec83-114">En la tabla siguiente se describe el comportamiento del elemento **ReminderType** cuando se incluyen los elementos **BeginTime** y **EndTime** .</span><span class="sxs-lookup"><span data-stu-id="dec83-114">The following table describes the behavior of the **ReminderType** element when the **BeginTime** and **EndTime** elements are included.</span></span> 
  
|<span data-ttu-id="dec83-115">Valor del elemento ReminderType \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="dec83-115">\*\*\*\*ReminderType\*\* element value\*\*</span></span>|<span data-ttu-id="dec83-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dec83-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dec83-117">Todo</span><span class="sxs-lookup"><span data-stu-id="dec83-117">All</span></span>  <br/> |<span data-ttu-id="dec83-118">Avisos que se producen entre los **BeginTime** y **EndTime**.</span><span class="sxs-lookup"><span data-stu-id="dec83-118">Reminders that occur between the **BeginTime** and **EndTime**.</span></span>  <br/> |
|<span data-ttu-id="dec83-119">Current</span><span class="sxs-lookup"><span data-stu-id="dec83-119">Current</span></span>  <br/> |<span data-ttu-id="dec83-120">Avisos devueltos por **All**, además de los avisos anteriores a la ventana de tiempo solicitada si el evento sigue en curso, además de todas las citas independientemente de la antigüedad.</span><span class="sxs-lookup"><span data-stu-id="dec83-120">Reminders returned by **All**, plus reminders that are earlier than the requested time window if the event is still ongoing, plus all appointments regardless of age.</span></span>  <br/> |
|<span data-ttu-id="dec83-121">Obsolet</span><span class="sxs-lookup"><span data-stu-id="dec83-121">Old</span></span>  <br/> |<span data-ttu-id="dec83-122">Avisos devueltos por **All**, menos eventos que todavía no se han completado, pero menos todas las citas.</span><span class="sxs-lookup"><span data-stu-id="dec83-122">Reminders returned by **All**, minus events that haven't completed yet, minus all appointments.</span></span> <span data-ttu-id="dec83-123">Los elementos **BeginTime** y **EndTime** deben estar configurados para usar el valor **anterior** .</span><span class="sxs-lookup"><span data-stu-id="dec83-123">The **BeginTime** and **EndTime** elements must be set to use the **Old** value.</span></span>  <br/> |
   
### <a name="getreminders-operation-soap-headers"></a><span data-ttu-id="dec83-124">Encabezados SOAP de operación GetReminders</span><span class="sxs-lookup"><span data-stu-id="dec83-124">GetReminders operation SOAP headers</span></span>

<span data-ttu-id="dec83-125">La operación **GetReminders** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="dec83-125">The **GetReminders** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="dec83-126">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="dec83-126">**Header name**</span></span>|<span data-ttu-id="dec83-127">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="dec83-127">**Element**</span></span>|<span data-ttu-id="dec83-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dec83-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dec83-129">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="dec83-129">**Impersonation**</span></span> <br/> |[<span data-ttu-id="dec83-130">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="dec83-130">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="dec83-131">Identifica al usuario que está suplantando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="dec83-131">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="dec83-132">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="dec83-132">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="dec83-133">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="dec83-133">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="dec83-134">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="dec83-134">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="dec83-135">Identifica la referencia cultural, tal y como se define en RFC 3066, "etiquetas para la identificación de idiomas", que se va a usar para obtener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="dec83-135">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="dec83-136">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="dec83-136">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="dec83-137">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="dec83-137">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="dec83-138">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="dec83-138">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="dec83-139">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="dec83-139">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="dec83-140">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="dec83-140">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="dec83-141">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="dec83-141">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="dec83-142">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="dec83-142">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="dec83-143">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dec83-143">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="dec83-144">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="dec83-144">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getreminders-operation-request-example"></a><span data-ttu-id="dec83-145">Ejemplo de solicitud de operación GetReminders</span><span class="sxs-lookup"><span data-stu-id="dec83-145">GetReminders operation request example</span></span>

<span data-ttu-id="dec83-146">El siguiente ejemplo de una solicitud de operación de **GetReminders** muestra cómo recuperar los cinco primeros elementos de calendario que se producen entre la **BeginTime** y la **hora de finalización.**</span><span class="sxs-lookup"><span data-stu-id="dec83-146">The following example of a **GetReminders** operation request shows how to retrieve the first five calendar items that occur between the **BeginTime** and **EndTime**.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
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

<span data-ttu-id="dec83-147">El cuerpo SOAP de solicitud de ejemplo contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="dec83-147">The example request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="dec83-148">GetReminders</span><span class="sxs-lookup"><span data-stu-id="dec83-148">GetReminders</span></span>](getreminders.md)
    
- [<span data-ttu-id="dec83-149">EndTime</span><span class="sxs-lookup"><span data-stu-id="dec83-149">EndTime</span></span>](endtime-remindermessagedatatype.md)
    
- [<span data-ttu-id="dec83-150">ReminderType</span><span class="sxs-lookup"><span data-stu-id="dec83-150">ReminderType</span></span>](remindertype.md)
    
<span data-ttu-id="dec83-151">El cuerpo de SOAP también puede contener los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="dec83-151">The SOAP body can also contain the following elements:</span></span>
  
- [<span data-ttu-id="dec83-152">BeginTime</span><span class="sxs-lookup"><span data-stu-id="dec83-152">BeginTime</span></span>](begintime.md)
    
- [<span data-ttu-id="dec83-153">MaxItems</span><span class="sxs-lookup"><span data-stu-id="dec83-153">MaxItems</span></span>](maxitems.md)
    
## <a name="successful-getreminders-operation-response"></a><span data-ttu-id="dec83-154">Respuesta de operación GetReminders correcta</span><span class="sxs-lookup"><span data-stu-id="dec83-154">Successful GetReminders operation response</span></span>

<span data-ttu-id="dec83-155">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **GetReminders** .</span><span class="sxs-lookup"><span data-stu-id="dec83-155">The following example shows a successful response to a **GetReminders** operation request.</span></span> <span data-ttu-id="dec83-156">La respuesta contiene un aviso para el elemento de calendario "Team Meeting" y un aviso para la tarea "tarea para enviar notas de reunión".</span><span class="sxs-lookup"><span data-stu-id="dec83-156">The response contains a reminder for the "Team meeting" calendar item and a reminder for the "Task to send meeting notes" task.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="dec83-157">Los identificadores se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="dec83-157">Identifiers have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="7"
                       Version="V2_10"
                       xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRemindersResponse ResponseClass="Success"
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <Reminders>
        <Reminder xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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
        <Reminder xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="dec83-158">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="dec83-158">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="dec83-159">GetRemindersResponse</span><span class="sxs-lookup"><span data-stu-id="dec83-159">GetRemindersResponse</span></span>](getremindersresponse.md)
    
- [<span data-ttu-id="dec83-160">Avisos</span><span class="sxs-lookup"><span data-stu-id="dec83-160">Reminders</span></span>](reminders.md)
    
- [<span data-ttu-id="dec83-161">Aviso</span><span class="sxs-lookup"><span data-stu-id="dec83-161">Reminder</span></span>](reminder.md)
    
- [<span data-ttu-id="dec83-162">Asunto</span><span class="sxs-lookup"><span data-stu-id="dec83-162">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="dec83-163">Ubicación</span><span class="sxs-lookup"><span data-stu-id="dec83-163">Location</span></span>](location-remindermessagedatatype.md)
    
- [<span data-ttu-id="dec83-164">ReminderTime</span><span class="sxs-lookup"><span data-stu-id="dec83-164">ReminderTime</span></span>](remindertime.md)
    
- [<span data-ttu-id="dec83-165">StartDate</span><span class="sxs-lookup"><span data-stu-id="dec83-165">StartDate</span></span>](startdate.md)
    
- [<span data-ttu-id="dec83-166">EndDate</span><span class="sxs-lookup"><span data-stu-id="dec83-166">EndDate</span></span>](enddate-remindertype.md)
    
- [<span data-ttu-id="dec83-167">ItemId</span><span class="sxs-lookup"><span data-stu-id="dec83-167">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="dec83-168">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="dec83-168">RecurringMasterItemId</span></span>](recurringmasteritemid.md)
    
- [<span data-ttu-id="dec83-169">ReminderGroup</span><span class="sxs-lookup"><span data-stu-id="dec83-169">ReminderGroup</span></span>](remindergroup.md)
    
- [<span data-ttu-id="dec83-170">EXCLUSIVO</span><span class="sxs-lookup"><span data-stu-id="dec83-170">UID</span></span>](uid-remindertype.md)
    
## <a name="getreminders-operation-error-response-example"></a><span data-ttu-id="dec83-171">Ejemplo de respuesta de error de operación GetReminders</span><span class="sxs-lookup"><span data-stu-id="dec83-171">GetReminders operation error response example</span></span>

<span data-ttu-id="dec83-172">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **GetReminders** .</span><span class="sxs-lookup"><span data-stu-id="dec83-172">The following example shows an error response to a **GetReminders** operation request.</span></span> <span data-ttu-id="dec83-173">Se trata de una respuesta a una solicitud en la que la fecha de finalización era anterior a la fecha de inicio.</span><span class="sxs-lookup"><span data-stu-id="dec83-173">This is a response to a request in which the end date was earlier than the start date.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="7"
                       Version="V2_10"
                       xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRemindersResponse ResponseClass="Error"
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>EndDate is earlier than StartDate</MessageText>
      <ResponseCode>ErrorInvalidOperation</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetRemindersResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="dec83-174">El cuerpo SOAP de respuesta de error contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="dec83-174">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="dec83-175">GetRemindersResponse</span><span class="sxs-lookup"><span data-stu-id="dec83-175">GetRemindersResponse</span></span>](getremindersresponse.md)
    
- [<span data-ttu-id="dec83-176">MessageText</span><span class="sxs-lookup"><span data-stu-id="dec83-176">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="dec83-177">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="dec83-177">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="dec83-178">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="dec83-178">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="dec83-179">Para obtener los códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="dec83-179">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dec83-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="dec83-180">See also</span></span>


- [<span data-ttu-id="dec83-181">PerformReminderAction</span><span class="sxs-lookup"><span data-stu-id="dec83-181">PerformReminderAction</span></span>](performreminderaction.md)
    

