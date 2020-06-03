---
title: Exportar elementos mediante EWS en Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.assetid: e93ee68c-e134-4469-9070-fba404d46cb4
description: Obtenga información sobre cómo exportar citas, mensajes de correo electrónico, contactos, tareas y otros elementos mediante la API administrada de EWS o EWS en Exchange.
localization_priority: Priority
ms.openlocfilehash: a01c9487821958b06ec162f2aee27e2d2804eaaf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455887"
---
# <a name="export-items-by-using-ews-in-exchange"></a><span data-ttu-id="c1546-103">Exportar elementos mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c1546-103">Export items by using EWS in Exchange</span></span>

<span data-ttu-id="c1546-104">Obtenga información sobre cómo exportar citas, mensajes de correo electrónico, contactos, tareas y otros elementos mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="c1546-104">Learn how to export appointments, emails, contacts, tasks, and other items by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="c1546-105">Puede exportar elementos de Exchange mediante la API administrada de EWS o EWS de varias formas.</span><span class="sxs-lookup"><span data-stu-id="c1546-105">You can export items from Exchange by using the EWS Managed API or EWS in a number of different ways.</span></span> <span data-ttu-id="c1546-106">La opción que use dependerá de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c1546-106">The option you use depends on:</span></span>
  
- <span data-ttu-id="c1546-107">El tipo de elemento que se exporta.</span><span class="sxs-lookup"><span data-stu-id="c1546-107">The item type that is exported.</span></span>
    
- <span data-ttu-id="c1546-108">El grado de fidelidad que desea mantener entre el estado del elemento en Exchange y el elemento exportado.</span><span class="sxs-lookup"><span data-stu-id="c1546-108">The degree of fidelity that you want maintained between the item state in Exchange and the exported item.</span></span>
    
- <span data-ttu-id="c1546-109">Formato del elemento exportado.</span><span class="sxs-lookup"><span data-stu-id="c1546-109">The format of the exported item.</span></span>
    
- <span data-ttu-id="c1546-110">Requisitos posteriores al procesamiento.</span><span class="sxs-lookup"><span data-stu-id="c1546-110">Any post-processing requirements.</span></span>
    
- <span data-ttu-id="c1546-111">Si desea volver a importar el elemento en Exchange.</span><span class="sxs-lookup"><span data-stu-id="c1546-111">Whether you want to import the item back into Exchange.</span></span>
    
<span data-ttu-id="c1546-112">En este artículo se muestra cómo usar cada una de las distintas opciones para exportar elementos.</span><span class="sxs-lookup"><span data-stu-id="c1546-112">This article shows you how to use each of the different options to export items.</span></span> <span data-ttu-id="c1546-113">Puede usar cualquier opción para exportar por lotes elementos de la información de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c1546-113">You can use any option to batch export items out of Exchange.</span></span>
  
## <a name="export-an-item-into-a-custom-format"></a><span data-ttu-id="c1546-114">Exportar un elemento a un formato personalizado</span><span class="sxs-lookup"><span data-stu-id="c1546-114">Export an item into a custom format</span></span>
<span data-ttu-id="c1546-115"><a name="bk_exportcustom"> </a></span><span class="sxs-lookup"><span data-stu-id="c1546-115"><a name="bk_exportcustom"> </a></span></span>

<span data-ttu-id="c1546-116">Puede usar los resultados de un método [Item. bind](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) de la API administrada de EWS llame o analice los resultados de una operación de EWS de [GetItem](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) en un formato que funcione con los requisitos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c1546-116">You can use the results of an [Item.Bind](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) EWS Managed API method call or parse the results of a [GetItem](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) EWS operation into a format that works with your application requirements.</span></span> <span data-ttu-id="c1546-117">Use esta opción cuando exporte elementos para importarlos a una base de datos, archivo. csv u otro formato o sistema.</span><span class="sxs-lookup"><span data-stu-id="c1546-117">Use this option when you are exporting items in order to import them into a database, .csv file, or another format or system.</span></span> <span data-ttu-id="c1546-118">Incluso puede guardar el elemento en forma de XML EWS del elemento, lo que puede resultar útil porque muchos sistemas tienen una capacidad de análisis XML.</span><span class="sxs-lookup"><span data-stu-id="c1546-118">You can even save the item in the form of the item EWS XML, which can be useful because many systems have XML parsing capability.</span></span> <span data-ttu-id="c1546-119">Se recomienda usar el método **Item. bind** o la operación **GetItem** (sin la propiedad [Item. MimeContent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) ) porque esta opción permite controlar qué propiedades se exportan.</span><span class="sxs-lookup"><span data-stu-id="c1546-119">We recommend that you use the **Item.Bind** method or the **GetItem** operation (without the [Item.MimeContent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) property) because this option gives you control over which properties are exported.</span></span> 
  
## <a name="export-items-with-full-fidelity"></a><span data-ttu-id="c1546-120">Exportar elementos con total fidelidad</span><span class="sxs-lookup"><span data-stu-id="c1546-120">Export items with full fidelity</span></span>
<span data-ttu-id="c1546-121"><a name="bk_exportfullfidelity"> </a></span><span class="sxs-lookup"><span data-stu-id="c1546-121"><a name="bk_exportfullfidelity"> </a></span></span>

<span data-ttu-id="c1546-122">Si desea exportar elementos con total fidelidad, puede usar la operación de EWS de [ExportItems](https://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c1546-122">If you want to export items with full fidelity, you can use the [ExportItems](https://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="c1546-123">La operación **ExportItems** exporta cada elemento como una secuencia de datos.</span><span class="sxs-lookup"><span data-stu-id="c1546-123">The **ExportItems** operation exports each item as a data stream.</span></span> <span data-ttu-id="c1546-124">Esta secuencia de datos no se puede analizar, pero se puede usar como una copia de seguridad de nivel de elemento que se puede importar de nuevo a un buzón de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c1546-124">This data stream is not for parsing, but can be used as an item-level backup that can be imported back into an Exchange mailbox.</span></span> <span data-ttu-id="c1546-125">Puede incluir muchos elementos en cada solicitud **ExportItems** , aunque se recomienda incluir un máximo de 100 elementos en cada llamada.</span><span class="sxs-lookup"><span data-stu-id="c1546-125">You can include many items in each **ExportItems** request, although we recommend that you include no more than 100 items in each call.</span></span> <span data-ttu-id="c1546-126">Debido a que la API administrada de EWS no implementa la operación **ExportItems** , si usa la API administrada de EWS, tendrá que escribir una rutina para enviar las solicitudes Web.</span><span class="sxs-lookup"><span data-stu-id="c1546-126">Because the EWS Managed API does not implement the **ExportItems** operation, if you use the EWS Managed API, you'll need to write a routine to send the web requests.</span></span> <span data-ttu-id="c1546-127">Opcionalmente, puede usar el método [Item. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) para obtener los metadatos sobre el elemento para que pueda indizar y almacenar información sobre la secuencia de datos.</span><span class="sxs-lookup"><span data-stu-id="c1546-127">You can optionally use the [Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) method to get metadata about the item so that you can index and store information about the data stream.</span></span> 
  
<span data-ttu-id="c1546-128">Le recomendamos que use la operación **ExportItems** para exportar los elementos que planea importar a un buzón de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c1546-128">We recommend that you use the **ExportItems** operation to export items that you plan to import into an Exchange mailbox.</span></span> 
  
<span data-ttu-id="c1546-129">En el ejemplo siguiente se muestra cómo usar la operación **ExportItems** .</span><span class="sxs-lookup"><span data-stu-id="c1546-129">The following example shows how to use the **ExportItems** operation.</span></span> <span data-ttu-id="c1546-130">En este ejemplo, el identificador del elemento se acorta para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="c1546-130">In this example, the item identifier is shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xmlns:xsd="http://www.w3.org/2001/XMLSchema"
      xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
      xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

El servidor responde a la solicitud **ExportItems** con un elemento [ExportItemsResponse](https://msdn.microsoft.com/library/ef44354b-fbdb-4f7c-b6bd-b27f56a1d018%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que el elemento se ha exportado correctamente. La respuesta también incluye el identificador de elemento del elemento exportado y la secuencia de datos que contiene el contenido exportado. <span data-ttu-id="c1546-133">En el ejemplo siguiente se muestra el cuerpo SOAP que contiene el elemento exportado.</span><span class="sxs-lookup"><span data-stu-id="c1546-133">The following example shows the SOAP body that contains the exported item.</span></span>
  
```XML
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <m:ExportItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="use-the-mime-stream-to-export-into-common-file-formats"></a><span data-ttu-id="c1546-134">Usar la secuencia MIME para exportar a formatos de archivo comunes</span><span class="sxs-lookup"><span data-stu-id="c1546-134">Use the MIME stream to export into common file formats</span></span>
<span data-ttu-id="c1546-135"><a name="bk_exportfullfidelity"> </a></span><span class="sxs-lookup"><span data-stu-id="c1546-135"><a name="bk_exportfullfidelity"> </a></span></span>

<span data-ttu-id="c1546-136">Puede usar el método de la API administrada de EWS [Item. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) o la operación de EWS de [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) para obtener una representación MIME de un elemento.</span><span class="sxs-lookup"><span data-stu-id="c1546-136">You can use the [Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) EWS Managed API method or the [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) EWS operation to get a MIME representation of an item.</span></span> <span data-ttu-id="c1546-137">Como Exchange no almacena el contenido MIME de cada elemento, tiene que convertir la representación de la base de datos de cada elemento en la secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="c1546-137">Because Exchange doesn't store the MIME content of each item, it has to convert the database representation of each item into the MIME stream.</span></span> <span data-ttu-id="c1546-138">Como esta conversión es costosa, no se recomienda solicitar la secuencia MIME para los elementos a gran escala.</span><span class="sxs-lookup"><span data-stu-id="c1546-138">Because this conversion is costly, we do not recommend that you request the MIME stream for items on a large scale.</span></span> <span data-ttu-id="c1546-139">Tenga en cuenta también que la secuencia MIME contiene un conjunto limitado de propiedades; es posible que tenga que tener en cuenta otras opciones si el conjunto de propiedades no contiene las propiedades que necesita.</span><span class="sxs-lookup"><span data-stu-id="c1546-139">Also note that the MIME stream contains a limited set of properties; you might have to consider other options if the property set doesn't contain the properties you need.</span></span> 
  
### <a name="use-the-ews-managed-api-to-export-an-email-into-an-eml-and-mht-file-by-using-the-mime-stream"></a><span data-ttu-id="c1546-140">Usar la API administrada de EWS para exportar un correo electrónico a un archivo. eml y. mht mediante el flujo MIME</span><span class="sxs-lookup"><span data-stu-id="c1546-140">Use the EWS Managed API to export an email into an .eml and .mht file by using the MIME stream</span></span>
<span data-ttu-id="c1546-141"><a name="bk_exportemailmime"> </a></span><span class="sxs-lookup"><span data-stu-id="c1546-141"><a name="bk_exportemailmime"> </a></span></span>

<span data-ttu-id="c1546-142">Outlook y otras aplicaciones de correo electrónico comunes pueden abrir el formato de archivo EML (. eml).</span><span class="sxs-lookup"><span data-stu-id="c1546-142">Outlook and other common email applications can open the EML (.eml) file format.</span></span> <span data-ttu-id="c1546-143">En el ejemplo siguiente se muestra cómo exportar un correo electrónico mediante la secuencia MIME y usar la secuencia MIME para crear un archivo EML HTML (. MHT) y MIME.</span><span class="sxs-lookup"><span data-stu-id="c1546-143">The following example shows you how you can export an email by using the MIME stream, and use the MIME stream to create an EML and a MIME HTML (.mht) file.</span></span> <span data-ttu-id="c1546-144">Muchos exploradores Web admiten el formato de archivo HTML MIME.</span><span class="sxs-lookup"><span data-stu-id="c1546-144">Many web browsers support the MIME HTML file format.</span></span> <span data-ttu-id="c1546-145">En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario puede autenticarse en un servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="c1546-145">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that the user can authenticate to an Exchange server.</span></span> 
  
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

### <a name="use-the-ews-managed-api-to-export-an-appointment-into-an-ical-file-by-using-the-mime-stream"></a><span data-ttu-id="c1546-146">Usar la API administrada de EWS para exportar una cita a un archivo iCal mediante el flujo MIME</span><span class="sxs-lookup"><span data-stu-id="c1546-146">Use the EWS Managed API to export an appointment into an iCal file by using the MIME stream</span></span>
<span data-ttu-id="c1546-147"><a name="bk_exporticalmime"> </a></span><span class="sxs-lookup"><span data-stu-id="c1546-147"><a name="bk_exporticalmime"> </a></span></span>

<span data-ttu-id="c1546-148">Outlook y otras aplicaciones de calendario comunes pueden abrir el formato de archivo de iCal (. ICS).</span><span class="sxs-lookup"><span data-stu-id="c1546-148">Outlook and other common calendar applications can open the iCal (.ics) file format.</span></span> <span data-ttu-id="c1546-149">En el ejemplo siguiente se muestra cómo exportar una cita mediante la secuencia MIME y usar la secuencia MIME para crear un archivo iCal.</span><span class="sxs-lookup"><span data-stu-id="c1546-149">The following example shows you how to export an appointment by using the MIME stream, and use the MIME stream to create an iCal file.</span></span> <span data-ttu-id="c1546-150">Tenga en cuenta que muchas propiedades no se exportan con la secuencia MIME, incluidos los asistentes y las propiedades relacionadas con datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="c1546-150">Note that many properties are not exported with the MIME stream, including attendees and attachment-related properties.</span></span> <span data-ttu-id="c1546-151">Puede capturar otras propiedades de EWS si las solicita y las guarda en el archivo de iCal como extensiones privadas.</span><span class="sxs-lookup"><span data-stu-id="c1546-151">You can capture other properties from EWS by requesting them and saving them in the iCal file as private extensions.</span></span> <span data-ttu-id="c1546-152">Estas extensiones privadas llevan el prefijo "x-".</span><span class="sxs-lookup"><span data-stu-id="c1546-152">These private extensions are prefixed with "x-".</span></span> 
  
<span data-ttu-id="c1546-153">En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario puede autenticarse en un servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="c1546-153">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that the user can authenticate to an Exchange server.</span></span> <span data-ttu-id="c1546-154">En este ejemplo también se presupone que tiene una cita con el asunto "2015 Financial proyecciones" en la carpeta calendario.</span><span class="sxs-lookup"><span data-stu-id="c1546-154">This example also assumes that you have an appointment with the subject "2015 Financial Projections" in the calendar folder.</span></span> 
  
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

### <a name="use-the-ews-managed-api-to-export-a-contact-into-a-vcard-file-by-using-the-mime-stream"></a><span data-ttu-id="c1546-155">Usar la API administrada de EWS para exportar un contacto a un archivo vCard mediante el flujo MIME</span><span class="sxs-lookup"><span data-stu-id="c1546-155">Use the EWS Managed API to export a contact into a vCard file by using the MIME stream</span></span>
<span data-ttu-id="c1546-156"><a name="bk_exportvcardmime"> </a></span><span class="sxs-lookup"><span data-stu-id="c1546-156"><a name="bk_exportvcardmime"> </a></span></span>

<span data-ttu-id="c1546-157">Outlook y otras aplicaciones de administración de contactos comunes pueden abrir el formato de archivo vCard (. vcf).</span><span class="sxs-lookup"><span data-stu-id="c1546-157">Outlook and other common contact management applications can open the vCard (.vcf) file format.</span></span> <span data-ttu-id="c1546-158">En el ejemplo siguiente se muestra cómo exportar un contacto mediante la secuencia MIME y usar la secuencia MIME para crear una vCard.</span><span class="sxs-lookup"><span data-stu-id="c1546-158">The following example shows you how to export a contact by using the MIME stream, and use the MIME stream to create a vCard.</span></span> <span data-ttu-id="c1546-159">Puede capturar otras propiedades de EWS si las solicita y las guarda en el.</span><span class="sxs-lookup"><span data-stu-id="c1546-159">You can capture other properties from EWS by requesting them and saving them in the .</span></span> <span data-ttu-id="c1546-160">vCard como extensiones privadas.</span><span class="sxs-lookup"><span data-stu-id="c1546-160">vCard as private extensions.</span></span> <span data-ttu-id="c1546-161">Estas extensiones llevan el prefijo "x-".</span><span class="sxs-lookup"><span data-stu-id="c1546-161">These extensions are prefixed with "x-".</span></span> 
  
<span data-ttu-id="c1546-162">En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario puede autenticarse en un servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="c1546-162">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that the user can authenticate to an Exchange server.</span></span> 
  
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
> <span data-ttu-id="c1546-163">No se pueden importar archivos vCard mediante la propiedad **MimeContent** .</span><span class="sxs-lookup"><span data-stu-id="c1546-163">You cannot import vCard files by using the **MimeContent** property.</span></span> <span data-ttu-id="c1546-164">Puede importar contactos con el método [Contact. Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.save%28v=exchg.80%29.aspx) la API administrada de EWS o la operación de EWS de [CreateItem](https://msdn.microsoft.com/library/417e994b-0a17-4c24-9527-04796b80b029%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c1546-164">You can import contacts by using the [Contact.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.save%28v=exchg.80%29.aspx) EWS Managed API method or the [CreateItem](https://msdn.microsoft.com/library/417e994b-0a17-4c24-9527-04796b80b029%28Office.15%29.aspx) EWS operation.</span></span> 
  
### <a name="use-ews-to-export-any-item-by-using-the-mime-stream"></a><span data-ttu-id="c1546-165">Usar EWS para exportar cualquier elemento mediante la secuencia MIME</span><span class="sxs-lookup"><span data-stu-id="c1546-165">Use EWS to export any item by using the MIME stream</span></span>
<span data-ttu-id="c1546-166"><a name="bk_exportewsmime"> </a></span><span class="sxs-lookup"><span data-stu-id="c1546-166"><a name="bk_exportewsmime"> </a></span></span>

<span data-ttu-id="c1546-167">Use la operación **GetItem** para obtener la secuencia MIME de un elemento.</span><span class="sxs-lookup"><span data-stu-id="c1546-167">Use the **GetItem** operation to get the MIME stream of an item.</span></span> <span data-ttu-id="c1546-168">La siguiente solicitud **GetItem** muestra cómo solicitar el contenido MIME de un elemento.</span><span class="sxs-lookup"><span data-stu-id="c1546-168">The following **GetItem** request shows how to request the MIME content of an item.</span></span> 
  
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
        <t:IncludeMimeContent>true</t:IncludeMimeContent>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="AAMkADEzYjJkLTYxMwB8GqYicWAAA=" ChangeKey="CQAAABzXv"/>
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="c1546-169">En el ejemplo siguiente se muestra la respuesta a una solicitud para obtener la secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="c1546-169">The following example shows the response to a request to get the MIME stream.</span></span> <span data-ttu-id="c1546-170">La secuencia MIME se ha abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="c1546-170">The MIME stream has been shortened for readability.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="893" 
                         MinorBuildNumber="17" 
                         Version="V2_10" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
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
<span data-ttu-id="c1546-171"><a name="bk_exportfullfidelity"> </a></span><span class="sxs-lookup"><span data-stu-id="c1546-171"><a name="bk_exportfullfidelity"> </a></span></span>

<span data-ttu-id="c1546-172">Después de exportar los elementos, es posible que desee [importar elementos a Exchange](how-to-import-items-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="c1546-172">After exporting items, you might want to [import items into Exchange](how-to-import-items-by-using-ews-in-exchange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c1546-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1546-173">See also</span></span>


- [<span data-ttu-id="c1546-174">Exportación e importación de elementos mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c1546-174">Exporting and importing items by using EWS in Exchange</span></span>](exporting-and-importing-items-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="c1546-175">Importar elementos mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c1546-175">Import items by using EWS in Exchange</span></span>](how-to-import-items-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="c1546-176">Carpetas y elementos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c1546-176">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)
    
- [<span data-ttu-id="c1546-177">Sincronización de buzones de correo y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c1546-177">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)
    

