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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763126"
---
# <a name="import-items-by-using-ews-in-exchange"></a>Importar elementos mediante el uso de EWS en Exchange

Obtenga información sobre cómo importar las citas, mensajes de correo electrónico, contactos, tareas y otros elementos mediante la API administrada de EWS o EWS en Exchange.
  
Muchos sistemas contienen citas, mensajes de correo electrónico, contactos y tareas, y puede importar esos elementos en Exchange en un número de formas diferentes. Importar elementos en Exchange es simple cuando no se mantienen las relaciones de buzón de correo en esos elementos. Puede usar el método de la API administrada de EWS [Item.Save](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) o la operación de EWS [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) para crear los elementos en un buzón de Exchange. El enfoque simple no admite todos los escenarios, sin embargo; Por ejemplo: 
  
- No se puede mantener la relación entre los organizadores y los asistentes al importar citas con los asistentes (reuniones). Esto significa que el organizador de la reunión tendrá que volver a enviar invitaciones de reunión a los asistentes con el fin de volver a establecer la relación entre el organizador y los asistentes. Si la cita se importó en el calendario de un asistente, la cita no estarán relacionada a cita del organizador de la reunión. Los asistentes se necesitan Aceptar la invitación de reunión reciente desde el organizador con el fin de volver a establecer la relación de organizador asistente.
    
- Obtener información acerca de los encargados no se conserva cuando se importan las tareas asignadas.
    
Todas las opciones de importación pueden utilizarse para importar elementos de lote en Exchange.
  
## <a name="use-ews-managed-api-or-ews-item-types-to-import-an-item"></a>API administrada de EWS de uso o EWS tipos para importar un elemento de elemento
<a name="bk_importproperties"> </a>

Puede usar la API administrada de EWS o EWS para importar los mensajes de correo electrónico, contactos, citas o tareas de otros sistemas. Acaba de definir las [Propiedades](properties-and-extended-properties-in-ews-in-exchange.md) de su formato de origen en cualquiera de los objetos siguientes, dependiendo de lo que va a importar. 
  
**La tabla 1. Objetos de la API administrada de EWS y elementos EWS**

|**Objeto de la API administrada de EWS**|**Elemento EWS**|
|:-----|:-----|
|[EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) <br/> |[Message](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) <br/> |
|[Contact](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) <br/> |[Contact](http://msdn.microsoft.com/library/66bfff50-7a91-4d81-b6a0-610b9962f677%28Office.15%29.aspx) <br/> |
|[Appointment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) <br/> |[CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) <br/> |
|[Tarea](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.task%28v=exchg.80%29.aspx) <br/> |[Tarea](http://msdn.microsoft.com/library/7c84927e-db28-4c5d-b0b5-cbcc2b88d869%28Office.15%29.aspx) <br/> |
   
Use el método de la API administrada de EWS [Item.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) o la operación de EWS [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) para llevar a cabo la importación de elementos. Se recomienda este enfoque al importar elementos de otros sistemas porque tiene control sobre el que se importarán propiedades. Para obtener más información acerca de cómo establecer las propiedades de los elementos y, a continuación, guarde el elemento, vea [crear un elemento mediante el uso de la API administrada de EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createewsma) o [crear un elemento mediante el uso de EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createews).
  
## <a name="import-items-with-full-fidelity"></a>Importar elementos con plena fidelidad
<a name="bk_importproperties"> </a>

Puede usar la operación de EWS [UploadItems](http://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) para cargar un elemento como una secuencia de datos. Esta representación de secuencia de datos de un elemento tiene que proceden de los resultados de una llamada a una operación [ExportItems](http://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) . Debido a que la API administrada de EWS no implementa la operación **UploadItems** , si usa la API administrada de EWS, debe escribir una rutina para enviar las solicitudes web. 
  
Esta es la manera más fácil para importar los elementos que se han exportado desde otro servidor de Exchange.
  
En el siguiente ejemplo, se acortan los identificadores y el contenido del elemento de **datos** para mejorar la legibilidad. 
  
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

El servidor responde a la solicitud de **UploadItems** con un elemento [UploadItemsResponse](http://msdn.microsoft.com/library/93044d39-4489-456a-8cce-b6d69873348f%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que el elemento se ha cargado correctamente. La respuesta incluye también el identificador de elemento del elemento que se cargan. 
  
## <a name="use-the-mime-stream-to-import-from-common-file-formats"></a>Usar la secuencia MIME para importar desde formatos de archivos comunes
<a name="bk_importproperties"> </a>

Puede importar EWS EML (EML) y archivos de iCalendar (.ics). Desea probar el contenido MIME para ver cómo el analizador de MIME de Exchange administra el contenido de la secuencia MIME. Aunque el uso de la secuencia MIME es conveniente, es suele ser mejor a la [API administrada de EWS de uso o EWS tipos para importar un elemento de elemento](#bk_importproperties). Este es un ejemplo de cómo importar [una vCard](http://code.msdn.microsoft.com/How-to-Import-vCard-Files-ffa0ff50).
  
### <a name="use-the-ews-managed-api-to-import-an-email-from-an-eml-file-by-using-the-mime-stream"></a>Usar la API administrada de EWS para importar un correo electrónico desde un archivo EML mediante el uso de la secuencia MIME

En el ejemplo siguiente se muestra cómo establecer la propiedad [MimeContent](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) con el contenido de un archivo EML y, a continuación, importar el correo electrónico a un buzón de correo. En este ejemplo también muestra cómo establecer el [PidTagMessageFlags (0x0E07)](http://msdn.microsoft.com/en-us/library/office/cc839733%28v=office.15%29.aspx) extendido (propiedad) en un correo electrónico importado para que no aparezca en el buzón de correo como un elemento de borrador. En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se puede autenticar en un servidor de Exchange. 
  
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

### <a name="use-the-ews-managed-api-to-import-an-appointment-from-an-ical-file-by-using-the-mime-stream"></a>Usar la API administrada de EWS para importar una cita desde un archivo de iCalendar mediante el uso de la secuencia MIME

Puede importar citas simples en forma de archivos de iCalendar mediante el uso de la secuencia MIME. No se puede importar las reuniones, que son las citas con los asistentes, ya que la relación entre los organizadores de reuniones y los asistentes debe establecerse como parte del flujo de trabajo de [calendario de Exchange](calendars-and-ews-in-exchange.md) . Los asistentes no se puede capturar en la secuencia MIME. 
  
En el ejemplo de código siguiente se muestra cómo importar un archivo .ics simple en el buzón de un usuario.
  
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

### <a name="use-ews-to-import-an-item-by-using-the-mime-stream"></a>Uso de EWS para importar un elemento mediante el uso de la secuencia MIME

Puede usar la operación de EWS [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) para importar elementos iCal y EML mediante su secuencia MIME. 
  
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

## <a name="next-steps"></a>Siguientes pasos
<a name="bk_importproperties"> </a>

Después de importar elementos en un buzón de correo, es posible que desee [crear una carpeta personalizada para almacenar los elementos importados](how-to-work-with-folders-by-using-ews-in-exchange.md)o [sincronizar los elementos del cliente y buzón de correo](mailbox-synchronization-and-ews-in-exchange.md).
  
## <a name="see-also"></a>Ver también


- [Exportación e importación de elementos mediante el uso de EWS en Exchange](exporting-and-importing-items-by-using-ews-in-exchange.md)
    
- [Exportar elementos mediante el uso de EWS en Exchange](how-to-export-items-by-using-ews-in-exchange.md)
    
- [Las carpetas y elementos de EWS en Exchange](folders-and-items-in-ews-in-exchange.md)
    
- [Sincronización de buzón de correo y EWS en Exchange](mailbox-synchronization-and-ews-in-exchange.md)
    

