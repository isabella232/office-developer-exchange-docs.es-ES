---
title: Extraer una entidad de un mensaje de correo electrónico mediante EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: 6396b009-5f6e-41eb-a75a-224d43e864ae
description: Obtenga información sobre cómo extraer información del cuerpo de un mensaje de correo electrónico mediante la API administrada de EWS o EWS en Exchange.
localization_priority: Priority
ms.openlocfilehash: fb90eb05441667e6b327b09d568117f5040e6fd8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528114"
---
# <a name="extract-an-entity-from-an-email-message-by-using-ews-in-exchange"></a><span data-ttu-id="b8c84-103">Extraer una entidad de un mensaje de correo electrónico mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b8c84-103">Extract an entity from an email message by using EWS in Exchange</span></span>

<span data-ttu-id="b8c84-104">Obtenga información sobre cómo extraer información del cuerpo de un mensaje de correo electrónico mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="b8c84-104">Learn how to extract information from the body of an email message by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="b8c84-105">Puede usar la API administrada de EWS o EWS para tener acceso a las direcciones, los contactos, las direcciones de correo electrónico, las sugerencias de reunión, los números de teléfono, las tareas y las direcciones URL que un servidor de Exchange extrae de los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="b8c84-105">You can use the EWS Managed API or EWS to access the addresses, contacts, email addresses, meeting suggestions, phone numbers, tasks, and URLs that an Exchange server extracts from email messages.</span></span> <span data-ttu-id="b8c84-106">A continuación, puede usar esta información para nuevas aplicaciones o para sugerir acciones de seguimiento en las aplicaciones existentes.</span><span class="sxs-lookup"><span data-stu-id="b8c84-106">You can then use this information for new applications or to suggest follow up actions in existing applications.</span></span> <span data-ttu-id="b8c84-107">Por ejemplo, si se identifica una entidad de contacto, una sugerencia de reunión o una sugerencia de tarea en un correo electrónico, la aplicación puede sugerir que se cree un nuevo elemento con información rellenada previamente.</span><span class="sxs-lookup"><span data-stu-id="b8c84-107">For example, if a contact entity, meeting suggestion, or task suggestion is identified in an email, your application can suggest that a new item with prepopulated information be created.</span></span> <span data-ttu-id="b8c84-108">Mediante el uso de entidades extraídas, puede aprovecharse de la intención de los datos y ayudar a los usuarios a integrar sin problemas su contenido de mensajes de correo electrónico en resultados accionables.</span><span class="sxs-lookup"><span data-stu-id="b8c84-108">By using extracted entities, you can capitalize on the intent behind the data — and help users seamlessly integrate their email message content into actionable results.</span></span>
  
<span data-ttu-id="b8c84-109">La extracción de entidades para direcciones, contactos, direcciones de correo electrónico, sugerencias de reunión, números de teléfono, tareas y direcciones URL ya está integrada en todos los elementos del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b8c84-109">Entity extraction for addresses, contacts, email addresses, meeting suggestions, phone numbers, tasks, and URLs is already built in to every item in the Exchange store.</span></span> <span data-ttu-id="b8c84-110">Si está usando la API administrada de EWS, la propiedad [Item. EntityExtractionResult](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.entityextractionresult%28v=exchg.80%29.aspx) recupera las entidades en una llamada al método [Item. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b8c84-110">If you're using the EWS Managed API, the [Item.EntityExtractionResult](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.entityextractionresult%28v=exchg.80%29.aspx) property retrieves the entities for you in an [Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) method call.</span></span> <span data-ttu-id="b8c84-111">Si está usando EWS, el elemento [EntityExtractionResult](https://msdn.microsoft.com/library/643b99ab-ff90-4411-864c-1077623028d6%28Office.15%29.aspx) obtiene todas las entidades extraídas en una llamada de la operación [GetItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b8c84-111">If you're using EWS, the [EntityExtractionResult](https://msdn.microsoft.com/library/643b99ab-ff90-4411-864c-1077623028d6%28Office.15%29.aspx) element gets all the extracted entities for you in a [GetItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) operation call.</span></span> <span data-ttu-id="b8c84-112">Después de recuperar los resultados de las entidades extraídas, puede recorrer cada colección de entidades para recopilar la información relevante.</span><span class="sxs-lookup"><span data-stu-id="b8c84-112">After you retrieve the results of the extracted entities, you can walk through each entity collection to gather pertinent information.</span></span> <span data-ttu-id="b8c84-113">Por ejemplo, si se ha extraído una sugerencia de reunión, puede recuperar el asunto de la reunión, la lista de asistentes, la hora de inicio y la hora de finalización sugeridos.</span><span class="sxs-lookup"><span data-stu-id="b8c84-113">For example, if a meeting suggestion was extracted, you can retrieve the suggested meeting subject, attendee list, start time, and end time.</span></span> 
  
<span data-ttu-id="b8c84-114">**Tabla 1. Propiedades de la API administrada de EWS y elementos EWS que contienen entidades extraídas**</span><span class="sxs-lookup"><span data-stu-id="b8c84-114">**Table 1. EWS Managed API properties and EWS elements that contain extracted entities**</span></span>

|<span data-ttu-id="b8c84-115">**Entidad extraída**</span><span class="sxs-lookup"><span data-stu-id="b8c84-115">**Extracted entity**</span></span>|<span data-ttu-id="b8c84-116">**Propiedad de la API administrada EWS**</span><span class="sxs-lookup"><span data-stu-id="b8c84-116">**EWS Managed API property**</span></span>|<span data-ttu-id="b8c84-117">**Elemento EWS**</span><span class="sxs-lookup"><span data-stu-id="b8c84-117">**EWS element**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b8c84-118">Direcciones</span><span class="sxs-lookup"><span data-stu-id="b8c84-118">Addresses</span></span>  <br/> |[<span data-ttu-id="b8c84-119">EntityExtractionResult. Addresses</span><span class="sxs-lookup"><span data-stu-id="b8c84-119">EntityExtractionResult.Addresses</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.entityextractionresult.addresses%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="b8c84-120">Direcciones</span><span class="sxs-lookup"><span data-stu-id="b8c84-120">Addresses</span></span>](https://msdn.microsoft.com/library/0c1f3fd3-1b78-46ee-8dd4-b2aff51e767e%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="b8c84-121">Contactos</span><span class="sxs-lookup"><span data-stu-id="b8c84-121">Contacts</span></span>  <br/> |[<span data-ttu-id="b8c84-122">EntityExtractionResult. contacts</span><span class="sxs-lookup"><span data-stu-id="b8c84-122">EntityExtractionResult.Contacts</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.entityextractionresult.contacts%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="b8c84-123">Contactos</span><span class="sxs-lookup"><span data-stu-id="b8c84-123">Contacts</span></span>](https://msdn.microsoft.com/library/a2c1e833-5f8c-438d-bad7-bb5dcc29ca9e%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="b8c84-124">Direcciones de correo</span><span class="sxs-lookup"><span data-stu-id="b8c84-124">Email addresses</span></span>  <br/> |[<span data-ttu-id="b8c84-125">EntityExtractionResult. EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="b8c84-125">EntityExtractionResult.EmailAddresses</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.entityextractionresult.emailaddresses%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="b8c84-126">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="b8c84-126">EmailAddresses</span></span>](https://msdn.microsoft.com/library/2fc4a8e8-5377-4059-8fb4-3fdabfd30fe3%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="b8c84-127">Sugerencias de reunión</span><span class="sxs-lookup"><span data-stu-id="b8c84-127">Meeting suggestions</span></span>  <br/> |[<span data-ttu-id="b8c84-128">EntityExtractionResult. MeetingSuggestions</span><span class="sxs-lookup"><span data-stu-id="b8c84-128">EntityExtractionResult.MeetingSuggestions</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.entityextractionresult.meetingsuggestions%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="b8c84-129">MeetingSuggestions</span><span class="sxs-lookup"><span data-stu-id="b8c84-129">MeetingSuggestions</span></span>](https://msdn.microsoft.com/library/c99e9a60-9e38-425d-ad03-47c8917f41da%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="b8c84-130">Números de teléfono</span><span class="sxs-lookup"><span data-stu-id="b8c84-130">Phone numbers</span></span>  <br/> |[<span data-ttu-id="b8c84-131">EntityExtractionResult. PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="b8c84-131">EntityExtractionResult.PhoneNumbers</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.entityextractionresult.phonenumbers%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="b8c84-132">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="b8c84-132">PhoneNumbers</span></span>](https://msdn.microsoft.com/library/9ff6ae98-34a1-47f7-bde5-608251a789f7%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="b8c84-133">Sugerencias de tareas</span><span class="sxs-lookup"><span data-stu-id="b8c84-133">Task suggestions</span></span>  <br/> |[<span data-ttu-id="b8c84-134">EntityExtractionResult. TaskSuggestions</span><span class="sxs-lookup"><span data-stu-id="b8c84-134">EntityExtractionResult.TaskSuggestions</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.entityextractionresult.addresses%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="b8c84-135">TaskSuggestions</span><span class="sxs-lookup"><span data-stu-id="b8c84-135">TaskSuggestions</span></span>](https://msdn.microsoft.com/library/7d3c6314-2a5c-4fc3-b5f9-ae6d4946aac3%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="b8c84-136">Direcciones URL</span><span class="sxs-lookup"><span data-stu-id="b8c84-136">URLs</span></span>  <br/> |[<span data-ttu-id="b8c84-137">EntityExtractionResult. URL</span><span class="sxs-lookup"><span data-stu-id="b8c84-137">EntityExtractionResult.Urls</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.entityextractionresult.addresses%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="b8c84-138">Urls</span><span class="sxs-lookup"><span data-stu-id="b8c84-138">Urls</span></span>](https://msdn.microsoft.com/library/c39744ea-0cee-4954-8653-8279d6b10161%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="b8c84-139">Debido a que la extracción de entidades depende del reconocimiento de lenguaje natural, el reconocimiento de las entidades puede no ser determinista y el éxito a veces se basa en el contexto.</span><span class="sxs-lookup"><span data-stu-id="b8c84-139">Because entity extraction relies on natural language recognition, the recognition of entities can be non-deterministic and success sometimes relies on the context.</span></span> <span data-ttu-id="b8c84-140">Para demostrar cómo funciona el reconocimiento de idioma natural, los ejemplos de este artículo usan el siguiente correo electrónico como entrada.</span><span class="sxs-lookup"><span data-stu-id="b8c84-140">To demonstrate how natural language recognition works, the examples in this article use the following email as input.</span></span>
  
 `From: Ronnie Sturgis`
  
 `To: Sadie Daniels`
  
 `Subject: Dinner party`
  
 `Hi Sadie`
  
 `Are you free this Friday at 7 to join us for a dinner party at our house?`
  
 `We're at 789 International Blvd, St Paul MN 55104.`
  
 `Our number is 612-555-0158 if you have trouble finding it.`
  
 `Please RSVP to either myself or Mara (mara@contoso.com) before Friday morning. Best for you organics (http://www.bestforyouorganics.com) will be catering so we can fully enjoy ourselves!`
  
 `Also, can you forward this to Magdalena? I don't have her contact information.`
  
 `See you then!`
  
 `Ronnie`
  
## <a name="extract-all-entities-from-an-email-by-using-the-ews-managed-api"></a><span data-ttu-id="b8c84-141">Extraer todas las entidades de un correo electrónico mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="b8c84-141">Extract all entities from an email by using the EWS Managed API</span></span>
<span data-ttu-id="b8c84-142"><a name="bk_extractewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="b8c84-142"><a name="bk_extractewsma"> </a></span></span>

<span data-ttu-id="b8c84-143">En el siguiente ejemplo de código se muestra cómo mostrar todas las entidades extraídas por el servidor mediante el método [Item. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) y, a continuación, cómo enumerar cada una de las entidades extraídas y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="b8c84-143">The following code example shows how to display all the entities extracted by the server, by using the [Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) method, and then enumerating through each of the extracted entities and their properties.</span></span> 
  
<span data-ttu-id="b8c84-144">En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que **Itemid** es el [identificador](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del mensaje de correo electrónico que se va a mover o copiar.</span><span class="sxs-lookup"><span data-stu-id="b8c84-144">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that **ItemId** is the [Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the email message to move or copy.</span></span> 
  
```cs
public static void ExtractEntities(ExchangeService service, ItemId ItemId)
{
    // Create a property set that limits the properties returned 
    // by the Bind method to only those that are required.
    PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, ItemSchema.EntityExtractionResult);
    // Get the item from the server.
    // This method call results in an GetItem call to EWS.
    Item item = Item.Bind(service, ItemId, propSet);
    Console.WriteLine("The following entities have been extracted from the message:");
    Console.WriteLine(" ");
    // If address entities are extracted from the message, print the results.
    if (item.EntityExtractionResult != null)
    {
        if (item.EntityExtractionResult.Addresses != null)
        {
            Console.WriteLine("--------------------Addresses---------------------------");
            foreach (AddressEntity address in item.EntityExtractionResult.Addresses)
            {
                Console.WriteLine("Address: {0}", address.Address);
            }
            Console.WriteLine(" ");
        }
        // If contact entities are extracted from the message, print the results.
        if (item.EntityExtractionResult.Contacts != null)
        {
            Console.WriteLine("--------------------Contacts----------------------------");
            foreach (ContactEntity contact in item.EntityExtractionResult.Contacts)
            {
                Console.WriteLine("Addresses:       {0}", contact.Addresses);
                Console.WriteLine("Business name:   {0}", contact.BusinessName);
                Console.WriteLine("Contact string:  {0}", contact.ContactString);
                Console.WriteLine("Email addresses: {0}", contact.EmailAddresses);
                Console.WriteLine("Person name:     {0}", contact.PersonName);
                Console.WriteLine("Phone numbers:   {0}", contact.PhoneNumbers);
                Console.WriteLine("URLs:            {0}", contact.Urls);
            }
            Console.WriteLine(" ");
        }
        // If email address entities are extracted from the message, print the results.
        if (item.EntityExtractionResult.EmailAddresses != null)
        {
            Console.WriteLine("--------------------Email addresses---------------------");
            foreach (EmailAddressEntity email in item.EntityExtractionResult.EmailAddresses)
            {
                Console.WriteLine("Email addresses: {0}", email.EmailAddress);
            }
            Console.WriteLine(" ");
        }
        // If meeting suggestion entities are extracted from the message, print the results.
        if (item.EntityExtractionResult.MeetingSuggestions != null)
        {
            Console.WriteLine("--------------------Meeting suggestions-----------------");
            foreach (MeetingSuggestion meetingSuggestion in item.EntityExtractionResult.MeetingSuggestions)
            {
                Console.WriteLine("Meeting subject:  {0}", meetingSuggestion.Subject);
                Console.WriteLine("Meeting string:   {0}", meetingSuggestion.MeetingString);
                foreach (EmailUserEntity attendee in meetingSuggestion.Attendees)
                {
                    Console.WriteLine("Attendee name:    {0}", attendee.Name);
                    Console.WriteLine("Attendee user ID: {0}", attendee.UserId);
                }
                Console.WriteLine("Start time:       {0}", meetingSuggestion.StartTime);
                Console.WriteLine("End time:         {0}", meetingSuggestion.EndTime);
                Console.WriteLine("Location:         {0}", meetingSuggestion.Location);
            }
            Console.WriteLine(" ");
        }
        // If phone number entities are extracted from the message, print the results.
        if (item.EntityExtractionResult.PhoneNumbers != null)
        {
            Console.WriteLine("--------------------Phone numbers-----------------------");
            foreach (PhoneEntity phone in item.EntityExtractionResult.PhoneNumbers)
            {
                Console.WriteLine("Original phone string:  {0}", phone.OriginalPhoneString);
                Console.WriteLine("Phone string:           {0}", phone.PhoneString);
                Console.WriteLine("Type:                   {0}", phone.Type);
            }
            Console.WriteLine(" ");
        }
        // If task suggestion entities are extracted from the message, print the results.
        if (item.EntityExtractionResult.TaskSuggestions != null)
        {
            Console.WriteLine("--------------------Task suggestions--------------------");
            foreach (TaskSuggestion task in item.EntityExtractionResult.TaskSuggestions)
            {
                foreach (EmailUserEntity assignee in task.Assignees)
                {
                    Console.WriteLine("Assignee name:    {0}", assignee.Name);
                    Console.WriteLine("Assignee user ID: {0}", assignee.UserId);
                }
                Console.WriteLine("Task string:      {0}", task.TaskString);
            }
            Console.WriteLine(" ");
        }
        // If URL entities are extracted from the message, print the results.
        if (item.EntityExtractionResult.Urls != null)
        {
            Console.WriteLine("--------------------URLs--------------------------------");
            foreach (UrlEntity url in item.EntityExtractionResult.Urls)
            {
                Console.WriteLine("URL: {0}", url.Url);
            }
            Console.WriteLine(" ");
        }
    }
    // If no entities are extracted from the message, print the result.
    else if (item.EntityExtractionResult == null)
    {
        Console.WriteLine("No entities extracted");
    }
}
```

<span data-ttu-id="b8c84-145">Se muestra el siguiente resultado en la consola.</span><span class="sxs-lookup"><span data-stu-id="b8c84-145">The following output is displayed on the console.</span></span>
  
```text
The following entities have been extracted from the message:
 
--------------------Addresses---------------------------
Address: 789 International Blvd, St Paul MN 55104
 
--------------------Contacts----------------------------
Addresses:       
Business name:   
Contact string:  Mara (mara@contoso.com)
Email addresses: mara@contoso.com
Person name:     Mara
Phone numbers:   
URLs:            
 
--------------------Email addresses---------------------
Email addresses: mara@contoso.com
 
--------------------Meeting suggestions-----------------
Meeting subject:  dinner party
Meeting string:   Are you free this Friday at 7 to join us for a dinner party at our house?
Attendee name:    Ronnie Sturgis
Attendee user ID: ronnie@contoso.com
Attendee name:    Sadie Daniels
Attendee user ID: sadie@cntoso.com
Start time:       10/1/0104 2:00:00 PM
End time:         10/1/0104 2:30:00 PM
Location:         
 
--------------------Phone numbers-----------------------
Original phone string:  612-555-0158
Phone string:           6125550158
Type:                   Unspecified
 
--------------------Task suggestions--------------------
Assignee name:    Sadie Daniels
Assignee user ID: sadie@contoso.com
Task string:      Also, can you forward this to Magdalena?
 
--------------------URLs--------------------------------
URL: http://www.bestforyouorganics.com
```

<span data-ttu-id="b8c84-146">Observe que todas las direcciones, los contactos, las direcciones de correo electrónico, los números de teléfono, las tareas y las direcciones URL se han extraído como se esperaba.</span><span class="sxs-lookup"><span data-stu-id="b8c84-146">Notice that all addresses, contacts, email addresses, phone numbers, tasks, and URLs were extracted as expected.</span></span> <span data-ttu-id="b8c84-147">Sin embargo, la sugerencia de reunión es un poco más compleja.</span><span class="sxs-lookup"><span data-stu-id="b8c84-147">The meeting suggestion, however, is a bit more complex.</span></span> <span data-ttu-id="b8c84-148">Observe que la hora de inicio y la hora de finalización de la sugerencia de reunión no son lo que esperaba.</span><span class="sxs-lookup"><span data-stu-id="b8c84-148">Notice the start time and end time of the meeting suggestion are not what you might expect.</span></span> <span data-ttu-id="b8c84-149">La hora de inicio del correo electrónico es "este viernes al 7", pero el valor extraído para la hora de inicio es 10/1/0104 2:00:00 PM.</span><span class="sxs-lookup"><span data-stu-id="b8c84-149">The start time in the email is "this Friday at 7", but the extracted value for the start time is 10/1/0104 2:00:00 PM.</span></span> <span data-ttu-id="b8c84-150">Esto se debe a que la hora de inicio y la hora de finalización extraídas por el servidor son fechas codificadas.</span><span class="sxs-lookup"><span data-stu-id="b8c84-150">This is because the start time and end time extracted by the server are encoded dates.</span></span> <span data-ttu-id="b8c84-151">Para obtener más información sobre cómo interpretar los valores de **fecha y hora** en las sugerencias de reunión, vea [[ms-OXCEXT]: Protocolo de objetos de mensajes de extensión de cliente](https://msdn.microsoft.com/library/hh968601%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b8c84-151">For more information about how to interpret **dateTime** values in meeting suggestions, see [[MS-OXCEXT]: Client Extension Message Object Protocol](https://msdn.microsoft.com/library/hh968601%28v=exchg.80%29.aspx).</span></span>
  
## <a name="extract-all-entities-from-an-email-by-using-ews"></a><span data-ttu-id="b8c84-152">Extraer todas las entidades de un correo electrónico mediante EWS</span><span class="sxs-lookup"><span data-stu-id="b8c84-152">Extract all entities from an email by using EWS</span></span>
<span data-ttu-id="b8c84-153"><a name="bk_extractews"> </a></span><span class="sxs-lookup"><span data-stu-id="b8c84-153"><a name="bk_extractews"> </a></span></span>

<span data-ttu-id="b8c84-154">En el ejemplo de código siguiente se muestra cómo usar la operación [GetItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) y el elemento [EntityExtractionResult](https://msdn.microsoft.com/library/643b99ab-ff90-4411-864c-1077623028d6%28Office.15%29.aspx) para recuperar las entidades extraídas de un elemento.</span><span class="sxs-lookup"><span data-stu-id="b8c84-154">The following code example shows how to use the [GetItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) operation and the [EntityExtractionResult](https://msdn.microsoft.com/library/643b99ab-ff90-4411-864c-1077623028d6%28Office.15%29.aspx) element to retrieve the extracted entities from an item.</span></span> 
  
<span data-ttu-id="b8c84-155">Esta es también la solicitud XML que la API administrada de EWS envía cuando se usa el método **BIND** para [extraer todas las entidades de un correo electrónico mediante la API administrada de EWS](#bk_extractewsma).</span><span class="sxs-lookup"><span data-stu-id="b8c84-155">This is also the XML request that is sent by the EWS Managed API when you use the **Bind** method to [Extract all entities from an email by using the EWS Managed API](#bk_extractewsma).</span></span>
  
<span data-ttu-id="b8c84-156">El valor del elemento [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) se acorta para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="b8c84-156">The value of the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element is shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:EntityExtractionResult" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="sVC5AAA=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud **GetItem** con un mensaje [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que el mensaje de correo electrónico se ha recuperado correctamente. <span data-ttu-id="b8c84-158">La respuesta también incluye el **EntityExtractionResult** para cada entidad extraída.</span><span class="sxs-lookup"><span data-stu-id="b8c84-158">The response also includes the **EntityExtractionResult** for each extracted entity.</span></span> 
  
<span data-ttu-id="b8c84-159">El valor del elemento **Itemid** se acorta para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="b8c84-159">The value of the **ItemId** element is shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="883"
                         MinorBuildNumber="10"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="sVC5AAA="
                        ChangeKey="CQAAABYAAAD32nSTjepyT63rYH17n9THAAAOOqJN" />
              <t:EntityExtractionResult>
                <t:Addresses>
                  <t:AddressEntity>
                    <t:Position>LatestReply</t:Position>
                    <t:Address>789 International Blvd, St Paul MN 55104</t:Address>
                  </t:AddressEntity>
                </t:Addresses>
                <t:MeetingSuggestions>
                  <t:MeetingSuggestion>
                    <t:Position>LatestReply</t:Position>
                    <t:Attendees>
                      <t:EmailUser>
                        <t:Name>Ronnie Sturgis</t:Name>
                        <t:UserId>ronnie@contoso.com</t:UserId>
                      </t:EmailUser>
                      <t:EmailUser>
                        <t:Name>Sadie Daniels</t:Name>
                        <t:UserId>sadie@contoso.com</t:UserId>
                      </t:EmailUser>
                    </t:Attendees>
                    <t:Subject>dinner party</t:Subject>
                    <t:MeetingString>Are you free this Friday at 7 to join us for a dinner party at our house?</t:MeetingString>
                    <t:StartTime>0104-10-01T19:00:00Z</t:StartTime>
                    <t:EndTime>0104-10-01T19:30:00Z</t:EndTime>
                  </t:MeetingSuggestion>
                </t:MeetingSuggestions>
                <t:TaskSuggestions>
                  <t:TaskSuggestion>
                    <t:Position>LatestReply</t:Position>
                    <t:TaskString>Also, can you forward this to Magdalena?</t:TaskString>
                    <t:Assignees>
                      <t:EmailUser>
                        <t:Name>Sadie Daniels</t:Name>
                        <t:UserId>sadie@contoso.com</t:UserId>
                      </t:EmailUser>
                    </t:Assignees>
                  </t:TaskSuggestion>
                </t:TaskSuggestions>
                <t:EmailAddresses>
                  <t:EmailAddressEntity>
                    <t:Position>LatestReply</t:Position>
                    <t:EmailAddress>mara@contoso.com</t:EmailAddress>
                  </t:EmailAddressEntity>
                </t:EmailAddresses>
                <t:Contacts>
                  <t:Contact>
                    <t:Position>LatestReply</t:Position>
                    <t:PersonName>Mara</t:PersonName>
                    <t:EmailAddresses>
                      <t:EmailAddress>mara@contoso.com</t:EmailAddress>
                    </t:EmailAddresses>
                    <t:ContactString>Mara (mara@contoso.com</t:ContactString>
                  </t:Contact>
                </t:Contacts>
                <t:Urls>
                  <t:UrlEntity>
                    <t:Position>LatestReply</t:Position>
                    <t:Url>http://www.bestforyouorganics.com</t:Url>
                  </t:UrlEntity>
                </t:Urls>
                <t:PhoneNumbers>
                  <t:Phone>
                    <t:Position>LatestReply</t:Position>
                    <t:OriginalPhoneString>612-555-0158</t:OriginalPhoneString>
                    <t:PhoneString>6125550158</t:PhoneString>
                    <t:Type>Unspecified</t:Type>
                  </t:Phone>
                </t:PhoneNumbers>
              </t:EntityExtractionResult>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="b8c84-160">Observe que todas las direcciones, los contactos, las direcciones de correo electrónico, los números de teléfono, las tareas y las direcciones URL se han extraído como se esperaba.</span><span class="sxs-lookup"><span data-stu-id="b8c84-160">Notice that all addresses, contacts, email addresses, phone numbers, tasks, and URLs were extracted as expected.</span></span> <span data-ttu-id="b8c84-161">Sin embargo, la sugerencia de reunión es un poco más compleja.</span><span class="sxs-lookup"><span data-stu-id="b8c84-161">The meeting suggestion, however, is a bit more complex.</span></span> <span data-ttu-id="b8c84-162">Observe que la hora de inicio y la hora de finalización de la sugerencia de reunión no son lo que esperaba.</span><span class="sxs-lookup"><span data-stu-id="b8c84-162">Notice the start time and end time of the meeting suggestion are not what you might expect.</span></span> <span data-ttu-id="b8c84-163">La hora de inicio del correo electrónico fue de "este viernes al 7", pero el valor extraído de la hora de inicio es de 10/1/0104 2:00:00 PM.</span><span class="sxs-lookup"><span data-stu-id="b8c84-163">The start time in the email was "this Friday at 7", but the extracted value for the start time is 10/1/0104 2:00:00 PM.</span></span> <span data-ttu-id="b8c84-164">Esto se debe a que la hora de inicio y la hora de finalización extraídas por el servidor son fechas codificadas.</span><span class="sxs-lookup"><span data-stu-id="b8c84-164">This is because the start time and end time extracted by the server are encoded dates.</span></span> <span data-ttu-id="b8c84-165">Para obtener más información acerca de la interpretación de valores **DateTime** en sugerencias de reuniones, consulte [[ms-OXCEXT]: Protocolo de objetos de mensajes de extensión de cliente](https://msdn.microsoft.com/library/hh968601%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b8c84-165">For more information about interpreting **dateTime** values in meeting suggestions, see [[MS-OXCEXT]: Client Extension Message Object Protocol](https://msdn.microsoft.com/library/hh968601%28v=exchg.80%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b8c84-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8c84-166">See also</span></span>

- [<span data-ttu-id="b8c84-167">Correo electrónico y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b8c84-167">Email and EWS in Exchange</span></span>](email-and-ews-in-exchange.md)
- [<span data-ttu-id="b8c84-168">Item. EntityExtractionResult</span><span class="sxs-lookup"><span data-stu-id="b8c84-168">Item.EntityExtractionResult</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.entityextractionresult%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="b8c84-169">EntityExtractionResult</span><span class="sxs-lookup"><span data-stu-id="b8c84-169">EntityExtractionResult</span></span>](https://msdn.microsoft.com/library/643b99ab-ff90-4411-864c-1077623028d6%28Office.15%29.aspx)
    

