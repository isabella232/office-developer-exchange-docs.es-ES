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
# <a name="export-items-by-using-ews-in-exchange"></a>Exportar elementos mediante el uso de EWS en Exchange

Obtenga información sobre cómo exportar las citas, mensajes de correo electrónico, contactos, tareas y otros elementos mediante la API administrada de EWS o EWS en Exchange.
  
Puede exportar elementos de Exchange mediante la API administrada de EWS o EWS de varias maneras diferentes. La opción que usar depende de:
  
- El tipo de elemento que se ha exportado.
    
- El grado de fidelidad que desea mantener entre el estado del elemento de Exchange y el elemento exportado.
    
- El formato del elemento exportado.
    
- Todos los requisitos de procesamiento posterior.
    
- Si desea volver a importar el elemento a Exchange.
    
En este artículo se muestra cómo usar cada una de las diferentes opciones para exportar elementos. Puede usar cualquier opción para exportar elementos fuera de Exchange de lote.
  
## <a name="export-an-item-into-a-custom-format"></a>Exportar un elemento en un formato personalizado
<a name="bk_exportcustom"> </a>

Puede usar los resultados de una llamada al método [Item.Bind](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) API administrada de EWS o analizar los resultados de una operación de EWS [GetItem](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) en un formato que funciona con los requisitos de la aplicación. Use esta opción cuando se va a exportar los elementos con el fin de importarlos en una base de datos, el archivo .csv, u otro formato o del sistema. Incluso puede guardar el elemento en el formulario del elemento XML EWS, que puede ser útil debido a que muchos sistemas tienen capacidad de análisis de XML. Se recomienda que use el método **Item.Bind** o la operación **GetItem** (sin la propiedad [Item.MimeContent](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) ) debido a que esta opción le permite controlar a través de las propiedades que se exporta. 
  
## <a name="export-items-with-full-fidelity"></a>Exportar elementos con plena fidelidad
<a name="bk_exportfullfidelity"> </a>

Si desea exportar elementos con plena fidelidad, puede usar la operación de EWS [ExportItems](http://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) . La operación **ExportItems** exporta cada elemento como una secuencia de datos. Esta secuencia de datos no es para análisis, pero se puede usar como una copia de seguridad de nivel de elemento que puede volver a importarse en un buzón de Exchange. Puede incluir muchos elementos en cada solicitud de **ExportItems** , aunque se recomienda que incluya no más de 100 elementos en cada llamada. Debido a que la API administrada de EWS no implementa la operación **ExportItems** , si usa la API administrada de EWS, debe escribir una rutina para enviar las solicitudes web. Opcionalmente, puede usar el método [Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) para obtener los metadatos sobre el elemento para que pueda indizar y almacenar información acerca de la secuencia de datos. 
  
Se recomienda que use la operación de **ExportItems** para exportar elementos que se va a importar a un buzón de Exchange. 
  
En el ejemplo siguiente se muestra cómo usar la operación **ExportItems** . En este ejemplo, el identificador de elemento es más cortos para mejorar la legibilidad. 
  
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

El servidor responde a la solicitud de **ExportItems** con un elemento [ExportItemsResponse](http://msdn.microsoft.com/library/ef44354b-fbdb-4f7c-b6bd-b27f56a1d018%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que el elemento se ha exportado correctamente. La respuesta incluye también el identificador de elemento del elemento exportado y la secuencia de datos que contiene el contenido exportado. En el ejemplo siguiente se muestra el cuerpo SOAP que contiene el elemento exportado.
  
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

## <a name="use-the-mime-stream-to-export-into-common-file-formats"></a>Utilice la secuencia MIME para exportar a formatos de archivo comunes
<a name="bk_exportfullfidelity"> </a>

Puede usar el método de la API administrada de EWS [Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) o la operación de EWS [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) para obtener una representación de MIME de un elemento. Debido a que Exchange no almacena el contenido MIME de cada elemento, debe convertir la representación de la base de datos de cada elemento en la secuencia MIME. Dado que esta conversión es costosa, que no se recomienda que solicite la secuencia MIME para los elementos a gran escala. Tenga en cuenta también que la secuencia MIME contiene un conjunto limitado de propiedades; debe tener en cuenta otras opciones si el conjunto de propiedades no contiene las propiedades que necesita. 
  
### <a name="use-the-ews-managed-api-to-export-an-email-into-an-eml-and-mht-file-by-using-the-mime-stream"></a>Utilice la API administrada de EWS para exportar un correo electrónico a un archivo EML y .mht mediante el uso de la secuencia MIME
<a name="bk_exportemailmime"> </a>

Outlook y otras aplicaciones de correo electrónico comunes pueden abrir el formato de archivo EML (EML). En el ejemplo siguiente se muestra cómo se puede exportar un correo electrónico mediante el uso de la secuencia MIME y usar la secuencia MIME para crear un EML y un archivo MIME HTML (.mht). Muchos exploradores web admiten el formato de archivo MIME HTML. En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se puede autenticar en un servidor de Exchange. 
  
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

### <a name="use-the-ews-managed-api-to-export-an-appointment-into-an-ical-file-by-using-the-mime-stream"></a>Usar la API administrada de EWS para exportar una cita en un archivo de iCalendar mediante el uso de la secuencia MIME
<a name="bk_exporticalmime"> </a>

Outlook y otras aplicaciones de calendario comunes pueden abrir el formato de archivo iCalendar (.ics). En el ejemplo siguiente se muestra cómo exportar una cita mediante la secuencia MIME y usar la secuencia MIME para crear un archivo de iCalendar. Tenga en cuenta que muchas propiedades no se exportan con la secuencia MIME, incluidos los asistentes y las propiedades relacionadas con datos adjuntos. Puede capturar otras propiedades de EWS solicitando ellos y guardarlos en el archivo de iCalendar como extensiones privadas. Estas extensiones privadas llevan el prefijo "x-". 
  
En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se puede autenticar en un servidor de Exchange. En este ejemplo también se supone que tiene una cita con el asunto "proyecciones financieras 2015" en la carpeta Calendario. 
  
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

### <a name="use-the-ews-managed-api-to-export-a-contact-into-a-vcard-file-by-using-the-mime-stream"></a>Usar la API administrada de EWS para exportar un contacto en un archivo vCard mediante el uso de la secuencia MIME
<a name="bk_exportvcardmime"> </a>

Outlook y otras aplicaciones de administración de contactos comunes pueden abrir el formato de archivo vCard (.vcf). En el ejemplo siguiente se muestra cómo exportar un contacto mediante el uso de la secuencia MIME y utilizar la secuencia MIME para crear una vCard. Puede capturar otras propiedades de EWS solicitando ellos y guardarlos en el. vCard como extensiones privadas. Estas extensiones llevan el prefijo "x-". 
  
En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se puede autenticar en un servidor de Exchange. 
  
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
> No se puede importar archivos vCard mediante el uso de la propiedad **MimeContent** . Puede importar contactos mediante el método de la API administrada de EWS [Contact.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.save%28v=exchg.80%29.aspx) o la operación de EWS [CreateItem](http://msdn.microsoft.com/library/417e994b-0a17-4c24-9527-04796b80b029%28Office.15%29.aspx) . 
  
### <a name="use-ews-to-export-any-item-by-using-the-mime-stream"></a>Uso de EWS para exportar cualquier elemento mediante la secuencia MIME
<a name="bk_exportewsmime"> </a>

Use la operación **GetItem** para obtener la secuencia MIME de un elemento. La solicitud **GetItem** siguiente muestra cómo solicitar el contenido MIME de un elemento. 
  
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

En el ejemplo siguiente se muestra la respuesta a una solicitud para obtener la secuencia MIME. La secuencia MIME se ha acortado para mejorar la legibilidad.
  
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
<a name="bk_exportfullfidelity"> </a>

Después de exportar elementos, es posible que desee [Importar elementos en Exchange](how-to-import-items-by-using-ews-in-exchange.md).
  
## <a name="see-also"></a>Ver también


- [Exportación e importación de elementos mediante el uso de EWS en Exchange](exporting-and-importing-items-by-using-ews-in-exchange.md)
    
- [Importar elementos mediante el uso de EWS en Exchange](how-to-import-items-by-using-ews-in-exchange.md)
    
- [Las carpetas y elementos de EWS en Exchange](folders-and-items-in-ews-in-exchange.md)
    
- [Sincronización de buzón de correo y EWS en Exchange](mailbox-synchronization-and-ews-in-exchange.md)
    

