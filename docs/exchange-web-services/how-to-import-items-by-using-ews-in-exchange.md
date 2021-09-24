---
title: Importar elementos mediante EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: dd3d3221-c98e-4fa0-81f0-77f733d2f432
description: Obtenga información sobre cómo importar citas, correos electrónicos, contactos, tareas y otros elementos mediante la API administrada ews o EWS en Exchange.
ms.openlocfilehash: 1e111a03f43c7c6ea30ab0dedf5cc0bb5c6a41f8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513167"
---
# <a name="import-items-by-using-ews-in-exchange"></a>Importar elementos mediante EWS en Exchange

Obtenga información sobre cómo importar citas, correos electrónicos, contactos, tareas y otros elementos mediante la API administrada ews o EWS en Exchange.
  
Muchos sistemas contienen citas, correos electrónicos, contactos y tareas, y puede importar esos elementos Exchange de varias maneras diferentes. Importar elementos a Exchange es sencillo cuando las relaciones de buzones no se mantienen en esos elementos. Puede usar el método de API administrada de EWS [Item.Save](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) o la operación [EWS CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) para crear los elementos en un buzón Exchange correo. Sin embargo, el enfoque simple no admite todos los escenarios; por ejemplo: 
  
- No puede mantener la relación entre organizadores y asistentes al importar citas con asistentes (reuniones). Esto significa que el organizador de la reunión tendrá que volver a enviar invitaciones a reuniones a los asistentes para restablecer la relación entre el organizador y los asistentes. Si la cita se importó en el calendario de un asistente, la cita no estará relacionada con la cita del organizador de la reunión. Los asistentes tendrán que aceptar la invitación de reunión resentida del organizador para restablecer la relación organizador-asistente.
    
- La información sobre los usuarios asignados no se conserva cuando se importan las tareas asignadas.
    
Todas las opciones de importación se pueden usar para importar elementos por lotes en Exchange.
  
## <a name="use-ews-managed-api-or-ews-item-types-to-import-an-item"></a>Usar tipos de elementos EWS o API administrada ews para importar un elemento
<a name="bk_importproperties"> </a>

Puede usar la API administrada ews o EWS para importar correos electrónicos, contactos, citas o tareas de otros sistemas. Solo tienes que [establecer las ](properties-and-extended-properties-in-ews-in-exchange.md) propiedades del formato de origen en cualquiera de los siguientes objetos, en función de lo que importes. 
  
**Tabla 1. Objetos de API administrada EWS y elementos EWS**

|**Objeto de API administrada ews**|**Elemento EWS**|
|:-----|:-----|
|[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) <br/> |[Mensaje](https://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) <br/> |
|[Contact](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) <br/> |[Contact](https://msdn.microsoft.com/library/66bfff50-7a91-4d81-b6a0-610b9962f677%28Office.15%29.aspx) <br/> |
|[Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) <br/> |[CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) <br/> |
|[Tarea](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.task%28v=exchg.80%29.aspx) <br/> |[Tarea](https://msdn.microsoft.com/library/7c84927e-db28-4c5d-b0b5-cbcc2b88d869%28Office.15%29.aspx) <br/> |
   
Use el método de LA API administrada de EWS [Item.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) o [la operación EWS CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) para realizar la importación de elementos. Se recomienda este enfoque al importar elementos de otros sistemas porque tiene control sobre las propiedades que se importan. Para obtener más información acerca de cómo establecer propiedades en los elementos y, a continuación, guardar el elemento, vea Create [an item by using the EWS Managed API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createewsma) or Create an item by using [EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createews).
  
## <a name="import-items-with-full-fidelity"></a>Importar elementos con total fidelidad
<a name="bk_importproperties"> </a>

Puede usar la operación [EWS UploadItems](https://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) para cargar un elemento como secuencia de datos. Esta representación de secuencia de datos de un elemento tiene que venir de los resultados de una llamada de [operación ExportItems.](https://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) Dado que la API administrada ews no implementa la operación **UploadItems,** si usa la API administrada de EWS, deberá escribir una rutina para enviar las solicitudes web. 
  
Esta es la forma más sencilla de importar elementos que se han exportado desde otro Exchange servidor.
  
En el siguiente ejemplo, los identificadores y el contenido del elemento **Data** se acortan para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xmlns:xsd="http://www.w3.org/2001/XMLSchema"
      xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
      xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

El servidor responde a la solicitud **UploadItems** con un elemento [UploadItemsResponse](https://msdn.microsoft.com/library/93044d39-4489-456a-8cce-b6d69873348f%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que el elemento se ha cargado correctamente. La respuesta también incluye el identificador de elemento del elemento cargado. 
  
## <a name="use-the-mime-stream-to-import-from-common-file-formats"></a>Usar la secuencia MIME para importar desde formatos de archivo comunes
<a name="bk_importproperties"> </a>

EWS puede importar archivos EML (.eml) e iCal (.ics). You'll want to test your MIME content to see how the Exchange MIME parser handles the content of your MIME stream. Aunque el uso de la secuencia MIME es conveniente, normalmente es mejor usar tipos de elementos EWS o API administrada EWS para [importar un elemento.](#bk_importproperties) Este es un ejemplo de cómo [importar un vCard](https://code.msdn.microsoft.com/How-to-Import-vCard-Files-ffa0ff50).
  
### <a name="use-the-ews-managed-api-to-import-an-email-from-an-eml-file-by-using-the-mime-stream"></a>Usar la API administrada ews para importar un correo electrónico desde un archivo EML mediante la secuencia MIME

En el ejemplo siguiente se muestra cómo establecer la [propiedad MimeContent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) con el contenido de un archivo EML y, a continuación, importar el correo electrónico a un buzón. En este ejemplo también se muestra cómo establecer la propiedad extendida [PidTagMessageFlags (0x0E07)](https://msdn.microsoft.com/library/office/cc839733%28v=office.15%29.aspx) en un correo electrónico importado para que no aparezca en el buzón como un elemento borrador. En este ejemplo se supone que **el servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario puede autenticarse en un Exchange servidor. 
  
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

### <a name="use-the-ews-managed-api-to-import-an-appointment-from-an-ical-file-by-using-the-mime-stream"></a>Usar la API administrada ews para importar una cita de un archivo iCal mediante la secuencia MIME

Puede importar citas sencillas en forma de archivos iCalendar mediante la secuencia MIME. No se pueden importar reuniones, que son citas con asistentes, ya que la relación entre los organizadores de la reunión y los asistentes debe establecerse como parte del flujo de trabajo de calendario Exchange [de](calendars-and-ews-in-exchange.md) calendario. Los asistentes no se pueden capturar en la secuencia MIME. 
  
En el siguiente ejemplo de código se muestra cómo importar un archivo .ics simple en el buzón de un usuario.
  
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

### <a name="use-ews-to-import-an-item-by-using-the-mime-stream"></a>Usar EWS para importar un elemento mediante la secuencia MIME

Puede usar la operación [EWS CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) para importar elementos EML e iCal mediante su secuencia MIME. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="next-steps"></a>Pasos siguientes
<a name="bk_importproperties"> </a>

Después de importar elementos en un buzón, es posible que desee crear una carpeta personalizada para almacenar los elementos importados [o](how-to-work-with-folders-by-using-ews-in-exchange.md)sincronizar los elementos de cliente y buzón de [correo.](mailbox-synchronization-and-ews-in-exchange.md)
  
## <a name="see-also"></a>Ver también


- [Exportar e importar elementos mediante EWS en Exchange](exporting-and-importing-items-by-using-ews-in-exchange.md)
    
- [Exportar elementos mediante EWS en Exchange](how-to-export-items-by-using-ews-in-exchange.md)
    
- [Carpetas y elementos de EWS en Exchange](folders-and-items-in-ews-in-exchange.md)
    
- [Sincronización del buzón y EWS en Exchange](mailbox-synchronization-and-ews-in-exchange.md)
    

