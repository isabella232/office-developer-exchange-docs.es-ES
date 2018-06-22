---
title: Exportar elementos mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e93ee68c-e134-4469-9070-fba404d46cb4
description: Obtenga información sobre cómo exportar las citas, mensajes de correo electrónico, contactos, tareas y otros elementos mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 65b5b2ef1eba66877d5b6f6c3d4237a26a254196
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763068"
---
# <a name="export-items-by-using-ews-in-exchange"></a><span data-ttu-id="f0b57-103">Exportar elementos mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f0b57-103">Export items by using EWS in Exchange</span></span>

<span data-ttu-id="f0b57-104">Obtenga información sobre cómo exportar las citas, mensajes de correo electrónico, contactos, tareas y otros elementos mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="f0b57-104">Learn how to export appointments, emails, contacts, tasks, and other items by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="f0b57-105">Puede exportar elementos de Exchange mediante la API administrada de EWS o EWS de varias maneras diferentes.</span><span class="sxs-lookup"><span data-stu-id="f0b57-105">You can export items from Exchange by using the EWS Managed API or EWS in a number of different ways.</span></span> <span data-ttu-id="f0b57-106">La opción que usar depende de:</span><span class="sxs-lookup"><span data-stu-id="f0b57-106">The option you use depends on:</span></span>
  
- <span data-ttu-id="f0b57-107">El tipo de elemento que se ha exportado.</span><span class="sxs-lookup"><span data-stu-id="f0b57-107">The item type that is exported.</span></span>
    
- <span data-ttu-id="f0b57-108">El grado de fidelidad que desea mantener entre el estado del elemento de Exchange y el elemento exportado.</span><span class="sxs-lookup"><span data-stu-id="f0b57-108">The degree of fidelity that you want maintained between the item state in Exchange and the exported item.</span></span>
    
- <span data-ttu-id="f0b57-109">El formato del elemento exportado.</span><span class="sxs-lookup"><span data-stu-id="f0b57-109">The format of the exported item.</span></span>
    
- <span data-ttu-id="f0b57-110">Todos los requisitos de procesamiento posterior.</span><span class="sxs-lookup"><span data-stu-id="f0b57-110">Any post-processing requirements.</span></span>
    
- <span data-ttu-id="f0b57-111">Si desea volver a importar el elemento a Exchange.</span><span class="sxs-lookup"><span data-stu-id="f0b57-111">Whether you want to import the item back into Exchange.</span></span>
    
<span data-ttu-id="f0b57-112">En este artículo se muestra cómo usar cada una de las diferentes opciones para exportar elementos.</span><span class="sxs-lookup"><span data-stu-id="f0b57-112">This article shows you how to use each of the different options to export items.</span></span> <span data-ttu-id="f0b57-113">Puede usar cualquier opción para exportar elementos fuera de Exchange de lote.</span><span class="sxs-lookup"><span data-stu-id="f0b57-113">You can use any option to batch export items out of Exchange.</span></span>
  
## <a name="export-an-item-into-a-custom-format"></a><span data-ttu-id="f0b57-114">Exportar un elemento en un formato personalizado</span><span class="sxs-lookup"><span data-stu-id="f0b57-114">Export an item into a custom format</span></span>
<span data-ttu-id="f0b57-115"><a name="bk_exportcustom"> </a></span><span class="sxs-lookup"><span data-stu-id="f0b57-115"></span></span>

<span data-ttu-id="f0b57-116">Puede usar los resultados de una llamada al método [Item.Bind](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) API administrada de EWS o analizar los resultados de una operación de EWS [GetItem](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) en un formato que funciona con los requisitos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f0b57-116">You can use the results of an [Item.Bind](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) EWS Managed API method call or parse the results of a [GetItem](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) EWS operation into a format that works with your application requirements.</span></span> <span data-ttu-id="f0b57-117">Use esta opción cuando se va a exportar los elementos con el fin de importarlos en una base de datos, el archivo .csv, u otro formato o del sistema.</span><span class="sxs-lookup"><span data-stu-id="f0b57-117">Use this option when you are exporting items in order to import them into a database, .csv file, or another format or system.</span></span> <span data-ttu-id="f0b57-118">Incluso puede guardar el elemento en el formulario del elemento XML EWS, que puede ser útil debido a que muchos sistemas tienen capacidad de análisis de XML.</span><span class="sxs-lookup"><span data-stu-id="f0b57-118">You can even save the item in the form of the item EWS XML, which can be useful because many systems have XML parsing capability.</span></span> <span data-ttu-id="f0b57-119">Se recomienda que use el método **Item.Bind** o la operación **GetItem** (sin la propiedad [Item.MimeContent](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) ) debido a que esta opción le permite controlar a través de las propiedades que se exporta.</span><span class="sxs-lookup"><span data-stu-id="f0b57-119">We recommend that you use the **Item.Bind** method or the **GetItem** operation (without the [Item.MimeContent](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) property) because this option gives you control over which properties are exported.</span></span> 
  
## <a name="export-items-with-full-fidelity"></a><span data-ttu-id="f0b57-120">Exportar elementos con plena fidelidad</span><span class="sxs-lookup"><span data-stu-id="f0b57-120">Export items with full fidelity</span></span>
<span data-ttu-id="f0b57-121"><a name="bk_exportfullfidelity"> </a></span><span class="sxs-lookup"><span data-stu-id="f0b57-121"></span></span>

<span data-ttu-id="f0b57-122">Si desea exportar elementos con plena fidelidad, puede usar la operación de EWS [ExportItems](http://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f0b57-122">If you want to export items with full fidelity, you can use the [ExportItems](http://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="f0b57-123">La operación **ExportItems** exporta cada elemento como una secuencia de datos.</span><span class="sxs-lookup"><span data-stu-id="f0b57-123">The **ExportItems** operation exports each item as a data stream.</span></span> <span data-ttu-id="f0b57-124">Esta secuencia de datos no es para análisis, pero se puede usar como una copia de seguridad de nivel de elemento que puede volver a importarse en un buzón de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f0b57-124">This data stream is not for parsing, but can be used as an item-level backup that can be imported back into an Exchange mailbox.</span></span> <span data-ttu-id="f0b57-125">Puede incluir muchos elementos en cada solicitud de **ExportItems** , aunque se recomienda que incluya no más de 100 elementos en cada llamada.</span><span class="sxs-lookup"><span data-stu-id="f0b57-125">You can include many items in each **ExportItems** request, although we recommend that you include no more than 100 items in each call.</span></span> <span data-ttu-id="f0b57-126">Debido a que la API administrada de EWS no implementa la operación **ExportItems** , si usa la API administrada de EWS, debe escribir una rutina para enviar las solicitudes web.</span><span class="sxs-lookup"><span data-stu-id="f0b57-126">Because the EWS Managed API does not implement the **ExportItems** operation, if you use the EWS Managed API, you'll need to write a routine to send the web requests.</span></span> <span data-ttu-id="f0b57-127">Opcionalmente, puede usar el método [Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) para obtener los metadatos sobre el elemento para que pueda indizar y almacenar información acerca de la secuencia de datos.</span><span class="sxs-lookup"><span data-stu-id="f0b57-127">You can optionally use the [Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) method to get metadata about the item so that you can index and store information about the data stream.</span></span> 
  
<span data-ttu-id="f0b57-128">Se recomienda que use la operación de **ExportItems** para exportar elementos que se va a importar a un buzón de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f0b57-128">We recommend that you use the **ExportItems** operation to export items that you plan to import into an Exchange mailbox.</span></span> 
  
<span data-ttu-id="f0b57-129">En el ejemplo siguiente se muestra cómo usar la operación **ExportItems** .</span><span class="sxs-lookup"><span data-stu-id="f0b57-129">The following example shows how to use the **ExportItems** operation.</span></span> <span data-ttu-id="f0b57-130">En este ejemplo, el identificador de elemento es más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="f0b57-130">In this example, the item identifier is shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xmlns:xsd="http://www.w3.org/2001/XMLSchema"
      xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
      xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013"/>
  </soap:Header>
  <soap:Body>
    <m:ExportItems>
      <m:ItemIds>
        <t:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY89GAAA="/>
      </m:ItemIds>
    </m:ExportItems>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud de **ExportItems** con un elemento [ExportItemsResponse](http://msdn.microsoft.com/library/ef44354b-fbdb-4f7c-b6bd-b27f56a1d018%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que el elemento se ha exportado correctamente. La respuesta incluye también el identificador de elemento del elemento exportado y la secuencia de datos que contiene el contenido exportado. <span data-ttu-id="f0b57-133">En el ejemplo siguiente se muestra el cuerpo SOAP que contiene el elemento exportado.</span><span class="sxs-lookup"><span data-stu-id="f0b57-133">The following example shows the SOAP body that contains the exported item.</span></span>
  
```XML
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <m:ExportItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
    <m:ResponseMessages>
      <m:ExportItemsResponseMessage ResponseClass="Success">
        <m:ResponseCode>NoError</m:ResponseCode>
        <m:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY89GAAA=" ChangeKey="FwAAAA=="/>
        <m:Data>
          AQAAAAgAAAAAAAAALgBlAHgAdABlAHMAdAAuAG0AaQBjAHIAbwBzAG8AZgB0AC4A
          cgAyAEAAYQB1AGoAaQBuAGcALQBkAG8AbQAuAGUAeAB0AGUAcwB0AC4AbQBpAGMAcgBvAHMA
          bwBmAHQALgBjAG8AbQAAAAMAADkAAAAAAwD+DwYAAAADAARAAwACQAMADkA=
        </m:Data>
      </m:ExportItemsResponseMessage>
     </m:ResponseMessages>
  </m:ExportItemsResponse>
</s:Body>
```

## <a name="use-the-mime-stream-to-export-into-common-file-formats"></a><span data-ttu-id="f0b57-134">Utilice la secuencia MIME para exportar a formatos de archivo comunes</span><span class="sxs-lookup"><span data-stu-id="f0b57-134">Use the MIME stream to export into common file formats</span></span>
<span data-ttu-id="f0b57-135"><a name="bk_exportfullfidelity"> </a></span><span class="sxs-lookup"><span data-stu-id="f0b57-135"></span></span>

<span data-ttu-id="f0b57-136">Puede usar el método de la API administrada de EWS [Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) o la operación de EWS [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) para obtener una representación de MIME de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f0b57-136">You can use the [Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) EWS Managed API method or the [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) EWS operation to get a MIME representation of an item.</span></span> <span data-ttu-id="f0b57-137">Debido a que Exchange no almacena el contenido MIME de cada elemento, debe convertir la representación de la base de datos de cada elemento en la secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="f0b57-137">Because Exchange doesn't store the MIME content of each item, it has to convert the database representation of each item into the MIME stream.</span></span> <span data-ttu-id="f0b57-138">Dado que esta conversión es costosa, que no se recomienda que solicite la secuencia MIME para los elementos a gran escala.</span><span class="sxs-lookup"><span data-stu-id="f0b57-138">Because this conversion is costly, we do not recommend that you request the MIME stream for items on a large scale.</span></span> <span data-ttu-id="f0b57-139">Tenga en cuenta también que la secuencia MIME contiene un conjunto limitado de propiedades; debe tener en cuenta otras opciones si el conjunto de propiedades no contiene las propiedades que necesita.</span><span class="sxs-lookup"><span data-stu-id="f0b57-139">Also note that the MIME stream contains a limited set of properties; you might have to consider other options if the property set doesn't contain the properties you need.</span></span> 
  
### <a name="use-the-ews-managed-api-to-export-an-email-into-an-eml-and-mht-file-by-using-the-mime-stream"></a><span data-ttu-id="f0b57-140">Utilice la API administrada de EWS para exportar un correo electrónico a un archivo EML y .mht mediante el uso de la secuencia MIME</span><span class="sxs-lookup"><span data-stu-id="f0b57-140">Use the EWS Managed API to export an email into an .eml and .mht file by using the MIME stream</span></span>
<span data-ttu-id="f0b57-141"><a name="bk_exportemailmime"> </a></span><span class="sxs-lookup"><span data-stu-id="f0b57-141"></span></span>

<span data-ttu-id="f0b57-142">Outlook y otras aplicaciones de correo electrónico comunes pueden abrir el formato de archivo EML (EML).</span><span class="sxs-lookup"><span data-stu-id="f0b57-142">Outlook and other common email applications can open the EML (.eml) file format.</span></span> <span data-ttu-id="f0b57-143">En el ejemplo siguiente se muestra cómo se puede exportar un correo electrónico mediante el uso de la secuencia MIME y usar la secuencia MIME para crear un EML y un archivo MIME HTML (.mht).</span><span class="sxs-lookup"><span data-stu-id="f0b57-143">The following example shows you how you can export an email by using the MIME stream, and use the MIME stream to create an EML and a MIME HTML (.mht) file.</span></span> <span data-ttu-id="f0b57-144">Muchos exploradores web admiten el formato de archivo MIME HTML.</span><span class="sxs-lookup"><span data-stu-id="f0b57-144">Many web browsers support the MIME HTML file format.</span></span> <span data-ttu-id="f0b57-145">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se puede autenticar en un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f0b57-145">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that the user can authenticate to an Exchange server.</span></span> 
  
```cs
private static void ExportMIMEEmail(ExchangeService service)
{
    Folder inbox = Folder.Bind(service, WellKnownFolderName.Inbox);
    ItemView view = new ItemView(1);
    view.PropertySet = new PropertySet(BasePropertySet.IdOnly);
    // This results in a FindItem call to EWS.
    FindItemsResults<Item> results = inbox.FindItems(view);
    foreach (var item in results)
    { 
        PropertySet props = new PropertySet(EmailMessageSchema.MimeContent);
        // This results in a GetItem call to EWS.
        var email = EmailMessage.Bind(service, item.Id, props);
                
        string emlFileName = @"C:\export\email.eml";
        string mhtFileName = @"C:\export\email.mht";
        // Save as .eml.
        using (FileStream fs = new FileStream(emlFileName, FileMode.Create, FileAccess.Write))
        {
            fs.Write(email.MimeContent.Content, 0, email.MimeContent.Content.Length);
        }
        // Save as .mht.
        using (FileStream fs = new FileStream(mhtFileName, FileMode.Create, FileAccess.Write))
        {
            fs.Write(email.MimeContent.Content, 0, email.MimeContent.Content.Length);
        }
    }
}
```

### <a name="use-the-ews-managed-api-to-export-an-appointment-into-an-ical-file-by-using-the-mime-stream"></a><span data-ttu-id="f0b57-146">Usar la API administrada de EWS para exportar una cita en un archivo de iCalendar mediante el uso de la secuencia MIME</span><span class="sxs-lookup"><span data-stu-id="f0b57-146">Use the EWS Managed API to export an appointment into an iCal file by using the MIME stream</span></span>
<span data-ttu-id="f0b57-147"><a name="bk_exporticalmime"> </a></span><span class="sxs-lookup"><span data-stu-id="f0b57-147"></span></span>

<span data-ttu-id="f0b57-148">Outlook y otras aplicaciones de calendario comunes pueden abrir el formato de archivo iCalendar (.ics).</span><span class="sxs-lookup"><span data-stu-id="f0b57-148">Outlook and other common calendar applications can open the iCal (.ics) file format.</span></span> <span data-ttu-id="f0b57-149">En el ejemplo siguiente se muestra cómo exportar una cita mediante la secuencia MIME y usar la secuencia MIME para crear un archivo de iCalendar.</span><span class="sxs-lookup"><span data-stu-id="f0b57-149">The following example shows you how to export an appointment by using the MIME stream, and use the MIME stream to create an iCal file.</span></span> <span data-ttu-id="f0b57-150">Tenga en cuenta que muchas propiedades no se exportan con la secuencia MIME, incluidos los asistentes y las propiedades relacionadas con datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="f0b57-150">Note that many properties are not exported with the MIME stream, including attendees and attachment-related properties.</span></span> <span data-ttu-id="f0b57-151">Puede capturar otras propiedades de EWS solicitando ellos y guardarlos en el archivo de iCalendar como extensiones privadas.</span><span class="sxs-lookup"><span data-stu-id="f0b57-151">You can capture other properties from EWS by requesting them and saving them in the iCal file as private extensions.</span></span> <span data-ttu-id="f0b57-152">Estas extensiones privadas llevan el prefijo "x-".</span><span class="sxs-lookup"><span data-stu-id="f0b57-152">These private extensions are prefixed with "x-".</span></span> 
  
<span data-ttu-id="f0b57-153">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se puede autenticar en un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f0b57-153">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that the user can authenticate to an Exchange server.</span></span> <span data-ttu-id="f0b57-154">En este ejemplo también se supone que tiene una cita con el asunto "proyecciones financieras 2015" en la carpeta Calendario.</span><span class="sxs-lookup"><span data-stu-id="f0b57-154">This example also assumes that you have an appointment with the subject "2015 Financial Projections" in the calendar folder.</span></span> 
  
```cs
private static void ExportMIMEAppointment(ExchangeService service)
{
    Folder inbox = Folder.Bind(service, WellKnownFolderName.Calendar);
    ItemView view = new ItemView(1);
    view.PropertySet = new PropertySet(BasePropertySet.IdOnly); 
    // This results in a FindItem call to EWS.
    FindItemsResults<Item> results = inbox.FindItems("subject:'2015 Financial Projections'", view);
    foreach (var item in results)
    {
        PropertySet props = new PropertySet(AppointmentSchema.MimeContent);
        // This results in a GetItem call to EWS.
        var email = Appointment.Bind(service, item.Id, props);
        string iCalFileName = @"C:\export\appointment.ics";
        // Save as .ics.
        using (FileStream fs = new FileStream(iCalFileName, FileMode.Create, FileAccess.Write))
        {
            fs.Write(email.MimeContent.Content, 0, email.MimeContent.Content.Length);
        }
    }
}
```

### <a name="use-the-ews-managed-api-to-export-a-contact-into-a-vcard-file-by-using-the-mime-stream"></a><span data-ttu-id="f0b57-155">Usar la API administrada de EWS para exportar un contacto en un archivo vCard mediante el uso de la secuencia MIME</span><span class="sxs-lookup"><span data-stu-id="f0b57-155">Use the EWS Managed API to export a contact into a vCard file by using the MIME stream</span></span>
<span data-ttu-id="f0b57-156"><a name="bk_exportvcardmime"> </a></span><span class="sxs-lookup"><span data-stu-id="f0b57-156"></span></span>

<span data-ttu-id="f0b57-157">Outlook y otras aplicaciones de administración de contactos comunes pueden abrir el formato de archivo vCard (.vcf).</span><span class="sxs-lookup"><span data-stu-id="f0b57-157">Outlook and other common contact management applications can open the vCard (.vcf) file format.</span></span> <span data-ttu-id="f0b57-158">En el ejemplo siguiente se muestra cómo exportar un contacto mediante el uso de la secuencia MIME y utilizar la secuencia MIME para crear una vCard.</span><span class="sxs-lookup"><span data-stu-id="f0b57-158">The following example shows you how to export a contact by using the MIME stream, and use the MIME stream to create a vCard.</span></span> <span data-ttu-id="f0b57-159">Puede capturar otras propiedades de EWS solicitando ellos y guardarlos en el.</span><span class="sxs-lookup"><span data-stu-id="f0b57-159">You can capture other properties from EWS by requesting them and saving them in the .</span></span> <span data-ttu-id="f0b57-160">vCard como extensiones privadas.</span><span class="sxs-lookup"><span data-stu-id="f0b57-160">vCard as private extensions.</span></span> <span data-ttu-id="f0b57-161">Estas extensiones llevan el prefijo "x-".</span><span class="sxs-lookup"><span data-stu-id="f0b57-161">These extensions are prefixed with "x-".</span></span> 
  
<span data-ttu-id="f0b57-162">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se puede autenticar en un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f0b57-162">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that the user can authenticate to an Exchange server.</span></span> 
  
```cs
private static void ExportMIMEContact(ExchangeService service)
{
    Folder inbox = Folder.Bind(service, WellKnownFolderName.Contacts);
    ItemView view = new ItemView(1);
    view.PropertySet = new PropertySet(BasePropertySet.IdOnly);
    // This results in a FindItem call to EWS.
    FindItemsResults<Item> results = inbox.FindItems(view);
    foreach (var item in results)
    {
        PropertySet props = new PropertySet(ContactSchema.MimeContent);
        // This results in a GetItem call to EWS.
        var email = Contact.Bind(service, item.Id, props);
        string vcfFileName = @"C:\export\contact.vcf";
        // Save as .vcf.
        using (FileStream fs = new FileStream(vcfFileName, FileMode.Create, FileAccess.Write))
        {
            fs.Write(email.MimeContent.Content, 0, email.MimeContent.Content.Length);
        }
    }
}
```

> [!NOTE]
> <span data-ttu-id="f0b57-163">No se puede importar archivos vCard mediante el uso de la propiedad **MimeContent** .</span><span class="sxs-lookup"><span data-stu-id="f0b57-163">You cannot import vCard files by using the **MimeContent** property.</span></span> <span data-ttu-id="f0b57-164">Puede importar contactos mediante el método de la API administrada de EWS [Contact.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.save%28v=exchg.80%29.aspx) o la operación de EWS [CreateItem](http://msdn.microsoft.com/library/417e994b-0a17-4c24-9527-04796b80b029%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f0b57-164">You can import contacts by using the [Contact.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.save%28v=exchg.80%29.aspx) EWS Managed API method or the [CreateItem](http://msdn.microsoft.com/library/417e994b-0a17-4c24-9527-04796b80b029%28Office.15%29.aspx) EWS operation.</span></span> 
  
### <a name="use-ews-to-export-any-item-by-using-the-mime-stream"></a><span data-ttu-id="f0b57-165">Uso de EWS para exportar cualquier elemento mediante la secuencia MIME</span><span class="sxs-lookup"><span data-stu-id="f0b57-165">Use EWS to export any item by using the MIME stream</span></span>
<span data-ttu-id="f0b57-166"><a name="bk_exportewsmime"> </a></span><span class="sxs-lookup"><span data-stu-id="f0b57-166"></span></span>

<span data-ttu-id="f0b57-167">Use la operación **GetItem** para obtener la secuencia MIME de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f0b57-167">Use the **GetItem** operation to get the MIME stream of an item.</span></span> <span data-ttu-id="f0b57-168">La solicitud **GetItem** siguiente muestra cómo solicitar el contenido MIME de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f0b57-168">The following **GetItem** request shows how to request the MIME content of an item.</span></span> 
  
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
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:IncludeMimeContent>true</t:IncludeMimeContent>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="AAMkADEzYjJkLTYxMwB8GqYicWAAA=" ChangeKey="CQAAABzXv"/>
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="f0b57-169">En el ejemplo siguiente se muestra la respuesta a una solicitud para obtener la secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="f0b57-169">The following example shows the response to a request to get the MIME stream.</span></span> <span data-ttu-id="f0b57-170">La secuencia MIME se ha acortado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="f0b57-170">The MIME stream has been shortened for readability.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="893" 
                         MinorBuildNumber="17" 
                         Version="V2_10" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:MimeContent CharacterSet="UTF-8">UmVjZ6IGZyb2b2suY29y5hMzgwZTA1YtDQo=</t:MimeContent>
              <t:ItemId Id="AAMkADEzYjJkLTYxMwB8GqYicWAAA=" ChangeKey="CQAAABzXv"/>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

## 
<span data-ttu-id="f0b57-171"><a name="bk_exportfullfidelity"> </a></span><span class="sxs-lookup"><span data-stu-id="f0b57-171"></span></span>

<span data-ttu-id="f0b57-172">Después de exportar elementos, es posible que desee [Importar elementos en Exchange](how-to-import-items-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="f0b57-172">After exporting items, you might want to [import items into Exchange](how-to-import-items-by-using-ews-in-exchange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f0b57-173">Ver también</span><span class="sxs-lookup"><span data-stu-id="f0b57-173">See also</span></span>


- [<span data-ttu-id="f0b57-174">Exportación e importación de elementos mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f0b57-174">Exporting and importing items by using EWS in Exchange</span></span>](exporting-and-importing-items-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="f0b57-175">Importar elementos mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f0b57-175">Import items by using EWS in Exchange</span></span>](how-to-import-items-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="f0b57-176">Las carpetas y elementos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f0b57-176">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)
    
- [<span data-ttu-id="f0b57-177">Sincronización de buzón de correo y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f0b57-177">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)
    

