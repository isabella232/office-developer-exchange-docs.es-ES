---
title: Importar elementos mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd3d3221-c98e-4fa0-81f0-77f733d2f432
description: Obtenga información sobre cómo importar las citas, mensajes de correo electrónico, contactos, tareas y otros elementos mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: c09c96eff455b7584b084e71b937853abfde731d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763126"
---
# <a name="import-items-by-using-ews-in-exchange"></a><span data-ttu-id="2d9c1-103">Importar elementos mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2d9c1-103">Import items by using EWS in Exchange</span></span>

<span data-ttu-id="2d9c1-104">Obtenga información sobre cómo importar las citas, mensajes de correo electrónico, contactos, tareas y otros elementos mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-104">Learn how to import appointments, emails, contacts, tasks, and other items by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="2d9c1-105">Muchos sistemas contienen citas, mensajes de correo electrónico, contactos y tareas, y puede importar esos elementos en Exchange en un número de formas diferentes.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-105">Many systems contain appointments, emails, contacts, and tasks, and you can import those items into Exchange in a number of different ways.</span></span> <span data-ttu-id="2d9c1-106">Importar elementos en Exchange es simple cuando no se mantienen las relaciones de buzón de correo en esos elementos.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-106">Importing items into Exchange is simple when mailbox relationships aren't maintained on those items.</span></span> <span data-ttu-id="2d9c1-107">Puede usar el método de la API administrada de EWS [Item.Save](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) o la operación de EWS [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) para crear los elementos en un buzón de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-107">You can use the [Item.Save](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) EWS Managed API method or the [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS operation to create the items in an Exchange mailbox.</span></span> <span data-ttu-id="2d9c1-108">El enfoque simple no admite todos los escenarios, sin embargo; Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2d9c1-108">The simple approach does not support all scenarios, however; for example:</span></span> 
  
- <span data-ttu-id="2d9c1-109">No se puede mantener la relación entre los organizadores y los asistentes al importar citas con los asistentes (reuniones).</span><span class="sxs-lookup"><span data-stu-id="2d9c1-109">You cannot maintain the relationship between organizers and attendees when importing appointments with attendees (meetings).</span></span> <span data-ttu-id="2d9c1-110">Esto significa que el organizador de la reunión tendrá que volver a enviar invitaciones de reunión a los asistentes con el fin de volver a establecer la relación entre el organizador y los asistentes.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-110">This means that the meeting organizer will need to resend meeting invites to attendees in order to reestablish the relationship between the organizer and attendees.</span></span> <span data-ttu-id="2d9c1-111">Si la cita se importó en el calendario de un asistente, la cita no estarán relacionada a cita del organizador de la reunión.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-111">If the appointment was imported into an attendee's calendar, the appointment will not be related to the meeting organizer's appointment.</span></span> <span data-ttu-id="2d9c1-112">Los asistentes se necesitan Aceptar la invitación de reunión reciente desde el organizador con el fin de volver a establecer la relación de organizador asistente.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-112">The attendees will need to accept the resent meeting invite from the organizer in order to reestablish the organizer-attendee relationship.</span></span>
    
- <span data-ttu-id="2d9c1-113">Obtener información acerca de los encargados no se conserva cuando se importan las tareas asignadas.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-113">Information about the assignees is not preserved when assigned tasks are imported.</span></span>
    
<span data-ttu-id="2d9c1-114">Todas las opciones de importación pueden utilizarse para importar elementos de lote en Exchange.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-114">All the import options can be used to batch import items into Exchange.</span></span>
  
## <a name="use-ews-managed-api-or-ews-item-types-to-import-an-item"></a><span data-ttu-id="2d9c1-115">API administrada de EWS de uso o EWS tipos para importar un elemento de elemento</span><span class="sxs-lookup"><span data-stu-id="2d9c1-115">Use EWS Managed API or EWS item types to import an item</span></span>
<span data-ttu-id="2d9c1-116"><a name="bk_importproperties"> </a></span><span class="sxs-lookup"><span data-stu-id="2d9c1-116"></span></span>

<span data-ttu-id="2d9c1-117">Puede usar la API administrada de EWS o EWS para importar los mensajes de correo electrónico, contactos, citas o tareas de otros sistemas.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-117">You can use the EWS Managed API or EWS to import emails, contacts, appointments, or tasks from other systems.</span></span> <span data-ttu-id="2d9c1-118">Acaba de definir las [Propiedades](properties-and-extended-properties-in-ews-in-exchange.md) de su formato de origen en cualquiera de los objetos siguientes, dependiendo de lo que va a importar.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-118">Just set the [properties ](properties-and-extended-properties-in-ews-in-exchange.md) from your source format on any of the following objects, depending on what you're importing.</span></span> 
  
<span data-ttu-id="2d9c1-119">**La tabla 1. Objetos de la API administrada de EWS y elementos EWS**</span><span class="sxs-lookup"><span data-stu-id="2d9c1-119">**Table 1. EWS Managed API objects and EWS elements**</span></span>

|<span data-ttu-id="2d9c1-120">**Objeto de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="2d9c1-120">**EWS Managed API object**</span></span>|<span data-ttu-id="2d9c1-121">**Elemento EWS**</span><span class="sxs-lookup"><span data-stu-id="2d9c1-121">**EWS element**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d9c1-122">EmailMessage</span><span class="sxs-lookup"><span data-stu-id="2d9c1-122">EmailMessage</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="2d9c1-123">Message</span><span class="sxs-lookup"><span data-stu-id="2d9c1-123">Message</span></span>](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="2d9c1-124">Contact</span><span class="sxs-lookup"><span data-stu-id="2d9c1-124">Contact</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="2d9c1-125">Contact</span><span class="sxs-lookup"><span data-stu-id="2d9c1-125">Contact</span></span>](http://msdn.microsoft.com/library/66bfff50-7a91-4d81-b6a0-610b9962f677%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="2d9c1-126">Appointment</span><span class="sxs-lookup"><span data-stu-id="2d9c1-126">Appointment</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="2d9c1-127">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="2d9c1-127">CalendarItem</span></span>](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="2d9c1-128">Tarea</span><span class="sxs-lookup"><span data-stu-id="2d9c1-128">Task</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.task%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="2d9c1-129">Tarea</span><span class="sxs-lookup"><span data-stu-id="2d9c1-129">Task</span></span>](http://msdn.microsoft.com/library/7c84927e-db28-4c5d-b0b5-cbcc2b88d869%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="2d9c1-130">Use el método de la API administrada de EWS [Item.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) o la operación de EWS [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) para llevar a cabo la importación de elementos.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-130">Use the [Item.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) EWS Managed API method or the [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS operation to perform the import of items.</span></span> <span data-ttu-id="2d9c1-131">Se recomienda este enfoque al importar elementos de otros sistemas porque tiene control sobre el que se importarán propiedades.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-131">We recommend this approach when you're importing items from other systems because you have control over which properties get imported.</span></span> <span data-ttu-id="2d9c1-132">Para obtener más información acerca de cómo establecer las propiedades de los elementos y, a continuación, guarde el elemento, vea [crear un elemento mediante el uso de la API administrada de EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createewsma) o [crear un elemento mediante el uso de EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createews).</span><span class="sxs-lookup"><span data-stu-id="2d9c1-132">For more information about how to set properties on items and then save the item, see [Create an item by using the EWS Managed API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createewsma) or [Create an item by using EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createews).</span></span>
  
## <a name="import-items-with-full-fidelity"></a><span data-ttu-id="2d9c1-133">Importar elementos con plena fidelidad</span><span class="sxs-lookup"><span data-stu-id="2d9c1-133">Import items with full fidelity</span></span>
<span data-ttu-id="2d9c1-134"><a name="bk_importproperties"> </a></span><span class="sxs-lookup"><span data-stu-id="2d9c1-134"></span></span>

<span data-ttu-id="2d9c1-135">Puede usar la operación de EWS [UploadItems](http://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) para cargar un elemento como una secuencia de datos.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-135">You can use the [UploadItems](http://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) EWS operation to upload an item as a data stream.</span></span> <span data-ttu-id="2d9c1-136">Esta representación de secuencia de datos de un elemento tiene que proceden de los resultados de una llamada a una operación [ExportItems](http://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2d9c1-136">This data stream representation of an item has to come from the results of an [ExportItems](http://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) operation call.</span></span> <span data-ttu-id="2d9c1-137">Debido a que la API administrada de EWS no implementa la operación **UploadItems** , si usa la API administrada de EWS, debe escribir una rutina para enviar las solicitudes web.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-137">Because the EWS Managed API does not implement the **UploadItems** operation, if you use the EWS Managed API, you'll need to write a routine to send the web requests.</span></span> 
  
<span data-ttu-id="2d9c1-138">Esta es la manera más fácil para importar los elementos que se han exportado desde otro servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-138">This is the easiest way to import items that have been exported from another Exchange server.</span></span>
  
<span data-ttu-id="2d9c1-139">En el siguiente ejemplo, se acortan los identificadores y el contenido del elemento de **datos** para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-139">In the following example, the identifiers and the **Data** element content are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xmlns:xsd="http://www.w3.org/2001/XMLSchema"
      xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
      xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1"/>
  </soap:Header>
  <soap:Body>
    <m:UploadItems>
      <m:Items>
        <t:Item CreateAction="CreateNew">
          <t:ParentFolderId  Id="AAMkADEzOTE7kV0AAA=" ChangeKey="AQAAAA=="/>
          <t:Data>AQAAAAgAAAAAAQAAAAADABZADQASDkANABMO</t:Data>
        </t:Item>
      </m:Items>
    </m:UploadItems>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud de **UploadItems** con un elemento [UploadItemsResponse](http://msdn.microsoft.com/library/93044d39-4489-456a-8cce-b6d69873348f%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que el elemento se ha cargado correctamente. <span data-ttu-id="2d9c1-141">La respuesta incluye también el identificador de elemento del elemento que se cargan.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-141">The response also includes the item ID of the uploaded item.</span></span> 
  
## <a name="use-the-mime-stream-to-import-from-common-file-formats"></a><span data-ttu-id="2d9c1-142">Usar la secuencia MIME para importar desde formatos de archivos comunes</span><span class="sxs-lookup"><span data-stu-id="2d9c1-142">Use the MIME stream to import from common file formats</span></span>
<span data-ttu-id="2d9c1-143"><a name="bk_importproperties"> </a></span><span class="sxs-lookup"><span data-stu-id="2d9c1-143"></span></span>

<span data-ttu-id="2d9c1-144">Puede importar EWS EML (EML) y archivos de iCalendar (.ics).</span><span class="sxs-lookup"><span data-stu-id="2d9c1-144">EWS can import EML (.eml) and iCal (.ics) files.</span></span> <span data-ttu-id="2d9c1-145">Desea probar el contenido MIME para ver cómo el analizador de MIME de Exchange administra el contenido de la secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-145">You'll want to test your MIME content to see how the Exchange MIME parser handles the content of your MIME stream.</span></span> <span data-ttu-id="2d9c1-146">Aunque el uso de la secuencia MIME es conveniente, es suele ser mejor a la [API administrada de EWS de uso o EWS tipos para importar un elemento de elemento](#bk_importproperties).</span><span class="sxs-lookup"><span data-stu-id="2d9c1-146">Although using the MIME stream is convenient, it is typically better to [Use EWS Managed API or EWS item types to import an item](#bk_importproperties).</span></span> <span data-ttu-id="2d9c1-147">Este es un ejemplo de cómo importar [una vCard](http://code.msdn.microsoft.com/How-to-Import-vCard-Files-ffa0ff50).</span><span class="sxs-lookup"><span data-stu-id="2d9c1-147">Here's an example of how to [import a vCard](http://code.msdn.microsoft.com/How-to-Import-vCard-Files-ffa0ff50).</span></span>
  
### <a name="use-the-ews-managed-api-to-import-an-email-from-an-eml-file-by-using-the-mime-stream"></a><span data-ttu-id="2d9c1-148">Usar la API administrada de EWS para importar un correo electrónico desde un archivo EML mediante el uso de la secuencia MIME</span><span class="sxs-lookup"><span data-stu-id="2d9c1-148">Use the EWS Managed API to import an email from an EML file by using the MIME stream</span></span>

<span data-ttu-id="2d9c1-149">En el ejemplo siguiente se muestra cómo establecer la propiedad [MimeContent](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) con el contenido de un archivo EML y, a continuación, importar el correo electrónico a un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-149">The following example shows how to set the [MimeContent](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) property with the contents of an EML file and then import the email into a mailbox.</span></span> <span data-ttu-id="2d9c1-150">En este ejemplo también muestra cómo establecer el [PidTagMessageFlags (0x0E07)](http://msdn.microsoft.com/en-us/library/office/cc839733%28v=office.15%29.aspx) extendido (propiedad) en un correo electrónico importado para que no aparezca en el buzón de correo como un elemento de borrador.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-150">This example also shows how to set the [PidTagMessageFlags (0x0E07)](http://msdn.microsoft.com/en-us/library/office/cc839733%28v=office.15%29.aspx) extended property on an imported email so that it doesn't appear in the mailbox as a draft item.</span></span> <span data-ttu-id="2d9c1-151">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se puede autenticar en un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-151">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that the user can authenticate to an Exchange server.</span></span> 
  
```cs
private static void UploadMIMEEmail(ExchangeService service)
{
    EmailMessage email = new EmailMessage(service);
    
    string emlFileName = @"C:\import\email.eml";
    using (FileStream fs = new FileStream(emlFileName, FileMode.Open, FileAccess.Read))
    {
        byte[] bytes = new byte[fs.Length];
        int numBytesToRead = (int)fs.Length;
        int numBytesRead = 0;
        while (numBytesToRead > 0)
        {
            int n = fs.Read(bytes, numBytesRead, numBytesToRead);
            if (n == 0)
                break;
            numBytesRead += n;
            numBytesToRead -= n;
        }
        // Set the contents of the .eml file to the MimeContent property.
        email.MimeContent = new MimeContent("UTF-8", bytes);
    }
    
    // Indicate that this email is not a draft. Otherwise, the email will appear as a 
    // draft to clients.
    ExtendedPropertyDefinition PR_MESSAGE_FLAGS_msgflag_read = new ExtendedPropertyDefinition(3591, MapiPropertyType.Integer);
    email.SetExtendedProperty(PR_MESSAGE_FLAGS_msgflag_read, 1);
    // This results in a CreateItem call to EWS. The email will be saved in the Inbox folder.
    email.Save(WellKnownFolderName.Inbox);
}
```

### <a name="use-the-ews-managed-api-to-import-an-appointment-from-an-ical-file-by-using-the-mime-stream"></a><span data-ttu-id="2d9c1-152">Usar la API administrada de EWS para importar una cita desde un archivo de iCalendar mediante el uso de la secuencia MIME</span><span class="sxs-lookup"><span data-stu-id="2d9c1-152">Use the EWS Managed API to import an appointment from an iCal file by using the MIME stream</span></span>

<span data-ttu-id="2d9c1-153">Puede importar citas simples en forma de archivos de iCalendar mediante el uso de la secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-153">You can import simple appointments in the form of iCalendar files by using the MIME stream.</span></span> <span data-ttu-id="2d9c1-154">No se puede importar las reuniones, que son las citas con los asistentes, ya que la relación entre los organizadores de reuniones y los asistentes debe establecerse como parte del flujo de trabajo de [calendario de Exchange](calendars-and-ews-in-exchange.md) .</span><span class="sxs-lookup"><span data-stu-id="2d9c1-154">You can't import meetings, which are appointments with attendees, because the relationship between meeting organizers and attendees has to be set as part of the [Exchange calendaring](calendars-and-ews-in-exchange.md) workflow.</span></span> <span data-ttu-id="2d9c1-155">Los asistentes no se puede capturar en la secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-155">Attendees cannot be captured in the MIME stream.</span></span> 
  
<span data-ttu-id="2d9c1-156">En el ejemplo de código siguiente se muestra cómo importar un archivo .ics simple en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-156">The following code example shows you how to import a simple .ics file into a user's mailbox.</span></span>
  
```cs
private static void UploadMIMEAppointment(ExchangeService service)
{
    Appointment appointment = new Appointment(service);
    string iCalFileName = @"C:\import\appointment.ics";
    using (FileStream fs = new FileStream(iCalFileName, FileMode.Open, FileAccess.Read))
    {
        byte[] bytes = new byte[fs.Length];
        int numBytesToRead = (int)fs.Length;
        int numBytesRead = 0;
        while (numBytesToRead > 0)
        {
            int n = fs.Read(bytes, numBytesRead, numBytesToRead);
            if (n == 0)
                break;
            numBytesRead += n;
            numBytesToRead -= n;
        }
        // Set the contents of the .ics file to the MimeContent property.
        appointment.MimeContent = new MimeContent("UTF-8", bytes);
    }
    // This results in a CreateItem call to EWS. 
    appointment.Save(WellKnownFolderName.Calendar);
}
```

### <a name="use-ews-to-import-an-item-by-using-the-mime-stream"></a><span data-ttu-id="2d9c1-157">Uso de EWS para importar un elemento mediante el uso de la secuencia MIME</span><span class="sxs-lookup"><span data-stu-id="2d9c1-157">Use EWS to import an item by using the MIME stream</span></span>

<span data-ttu-id="2d9c1-158">Puede usar la operación de EWS [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) para importar elementos iCal y EML mediante su secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-158">You can use the [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS operation to import EML and iCal items by using their MIME stream.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
    <t:MailboxCulture>en-US</t:MailboxCulture>
  </soap:Header>
  <soap:Body >
    <m:CreateItem>
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="inbox"/>
      </m:SavedItemFolderId> 
        <m:Items>
        <t:Message>
          <t:MimeContent CharacterSet="UTF-8">
            <!-- Insert MIME content here-->
          </t:MimeContent>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="next-steps"></a><span data-ttu-id="2d9c1-159">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="2d9c1-159">Next steps</span></span>
<span data-ttu-id="2d9c1-160"><a name="bk_importproperties"> </a></span><span class="sxs-lookup"><span data-stu-id="2d9c1-160"></span></span>

<span data-ttu-id="2d9c1-161">Después de importar elementos en un buzón de correo, es posible que desee [crear una carpeta personalizada para almacenar los elementos importados](how-to-work-with-folders-by-using-ews-in-exchange.md)o [sincronizar los elementos del cliente y buzón de correo](mailbox-synchronization-and-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="2d9c1-161">After you import items into a mailbox, you might want to [create a custom folder to store your imported items](how-to-work-with-folders-by-using-ews-in-exchange.md), or [synchronize your client and mailbox items](mailbox-synchronization-and-ews-in-exchange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2d9c1-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d9c1-162">See also</span></span>


- [<span data-ttu-id="2d9c1-163">Exportación e importación de elementos mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2d9c1-163">Exporting and importing items by using EWS in Exchange</span></span>](exporting-and-importing-items-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="2d9c1-164">Exportar elementos mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2d9c1-164">Export items by using EWS in Exchange</span></span>](how-to-export-items-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="2d9c1-165">Las carpetas y elementos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2d9c1-165">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)
    
- [<span data-ttu-id="2d9c1-166">Sincronización de buzón de correo y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2d9c1-166">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)
    

