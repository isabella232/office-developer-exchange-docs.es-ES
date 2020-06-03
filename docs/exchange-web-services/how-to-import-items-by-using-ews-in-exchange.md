---
title: Importar elementos mediante EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd3d3221-c98e-4fa0-81f0-77f733d2f432
description: Obtenga información sobre cómo importar citas, mensajes de correo electrónico, contactos, tareas y otros elementos mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: bc874c667c31beb4e59a305626247488cb1a1781
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527988"
---
# <a name="import-items-by-using-ews-in-exchange"></a>Importar elementos mediante EWS en Exchange

Obtenga información sobre cómo importar citas, mensajes de correo electrónico, contactos, tareas y otros elementos mediante la API administrada de EWS o EWS en Exchange.
  
Muchos sistemas contienen citas, mensajes de correo electrónico, contactos y tareas, y puede importar dichos elementos a Exchange de varias formas. La importación de elementos en Exchange es sencilla cuando no se mantienen relaciones con los buzones en estos elementos. Puede usar el método [Item. Save](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) de la API administrada de EWS o la operación de EWS de [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) para crear los elementos en un buzón de Exchange. Sin embargo, el enfoque sencillo no es compatible con todos los escenarios; por ejemplo: 
  
- No se puede mantener la relación entre los organizadores y los asistentes al importar citas con asistentes (reuniones). Esto significa que el organizador de la reunión tendrá que volver a enviar las invitaciones de reunión a los asistentes para restablecer la relación entre el organizador y los asistentes. Si la cita se importó en el calendario de un asistente, la cita no estará relacionada con la cita del organizador de la reunión. Los asistentes deberán aceptar la invitación a la reunión que se ha reenviado desde el organizador para restablecer la relación de organizador-asistente.
    
- La información sobre los usuarios a los que se asignan no se conserva cuando se importan las tareas asignadas.
    
Todas las opciones de importación se pueden usar para importar elementos por lotes a Exchange.
  
## <a name="use-ews-managed-api-or-ews-item-types-to-import-an-item"></a>Usar la API administrada de EWS o los tipos de elemento EWS para importar un elemento
<a name="bk_importproperties"> </a>

Puede usar la API administrada de EWS o EWS para importar correos electrónicos, contactos, citas o tareas desde otros sistemas. Solo tiene que establecer las [propiedades](properties-and-extended-properties-in-ews-in-exchange.md) del formato de origen en cualquiera de los objetos siguientes, en función de lo que esté importando. 
  
**Tabla 1. Objetos de la API administrada de EWS y elementos EWS**

|**Objeto de API administrada de EWS**|**Elemento EWS**|
|:-----|:-----|
|[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) <br/> |[Message](https://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) <br/> |
|[Contacto](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) <br/> |[Contacto](https://msdn.microsoft.com/library/66bfff50-7a91-4d81-b6a0-610b9962f677%28Office.15%29.aspx) <br/> |
|[Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) <br/> |[CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) <br/> |
|[Tarea](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.task%28v=exchg.80%29.aspx) <br/> |[Tarea](https://msdn.microsoft.com/library/7c84927e-db28-4c5d-b0b5-cbcc2b88d869%28Office.15%29.aspx) <br/> |
   
Use el método de la API administrada de EWS [Item. Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) o la operación de EWS de [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) para realizar la importación de elementos. Se recomienda este método cuando se importan elementos de otros sistemas, ya que se tiene control sobre las propiedades que se van a importar. Para obtener más información sobre cómo establecer propiedades en elementos y, a continuación, guardar el elemento, vea [crear un elemento mediante la API administrada de EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createewsma) o [crear un elemento mediante EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createews).
  
## <a name="import-items-with-full-fidelity"></a>Importación de elementos con total fidelidad
<a name="bk_importproperties"> </a>

Puede usar la operación de EWS de [UploadItems](https://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) para cargar un elemento como una secuencia de datos. Esta representación de secuencia de datos de un elemento tiene que provenir de los resultados de una llamada a la operación [ExportItems](https://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) . Debido a que la API administrada de EWS no implementa la operación **UploadItems** , si usa la API administrada de EWS, tendrá que escribir una rutina para enviar las solicitudes Web. 
  
Esta es la forma más sencilla de importar elementos que se han exportado desde otro servidor de Exchange.
  
En el siguiente ejemplo, los identificadores y el contenido del elemento de **datos** se acortan para facilitar su lectura. 
  
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

El servidor responde a la solicitud **UploadItems** con un elemento [UploadItemsResponse](https://msdn.microsoft.com/library/93044d39-4489-456a-8cce-b6d69873348f%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que el elemento se cargó correctamente. La respuesta también incluye el identificador de elemento del elemento cargado. 
  
## <a name="use-the-mime-stream-to-import-from-common-file-formats"></a>Usar el flujo MIME para importar desde formatos de archivo comunes
<a name="bk_importproperties"> </a>

EWS puede importar archivos EML (. eml) e iCal (. ICS). Querrá probar el contenido MIME para ver cómo el analizador MIME de Exchange controla el contenido de la secuencia MIME. Aunque el uso de la secuencia MIME es conveniente, suele ser mejor [usar la API administrada de EWS o los tipos de elemento EWS para importar un elemento](#bk_importproperties). A continuación, se muestra un ejemplo de cómo [importar una vCard](https://code.msdn.microsoft.com/How-to-Import-vCard-Files-ffa0ff50).
  
### <a name="use-the-ews-managed-api-to-import-an-email-from-an-eml-file-by-using-the-mime-stream"></a>Usar la API administrada de EWS para importar un correo electrónico de un archivo EML mediante el flujo MIME

En el ejemplo siguiente se muestra cómo establecer la propiedad [MimeContent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) con el contenido de un archivo eml y, a continuación, importar el correo electrónico a un buzón. En este ejemplo también se muestra cómo establecer la propiedad extendida [PidTagMessageFlags (0x0E07)](https://msdn.microsoft.com/library/office/cc839733%28v=office.15%29.aspx) en un correo electrónico importado para que no aparezca en el buzón como elemento de borrador. En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario puede autenticarse en un servidor Exchange. 
  
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

### <a name="use-the-ews-managed-api-to-import-an-appointment-from-an-ical-file-by-using-the-mime-stream"></a>Usar la API administrada de EWS para importar una cita de un archivo iCal mediante el flujo MIME

Puede importar citas simples en forma de archivos de iCalendar mediante la secuencia MIME. No puede importar reuniones, que son citas con asistentes, porque la relación entre los organizadores de reuniones y los asistentes tiene que establecerse como parte del flujo de trabajo de [calendario de Exchange](calendars-and-ews-in-exchange.md) . No se pueden capturar los asistentes en la secuencia MIME. 
  
El siguiente ejemplo de código muestra cómo importar un archivo. ICS sencillo en el buzón de un usuario.
  
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

Puede usar la operación EWS de [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) para importar los elementos eml y iCal mediante su secuencia MIME. 
  
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

## <a name="next-steps"></a>Siguientes pasos
<a name="bk_importproperties"> </a>

Después de importar elementos en un buzón de correo, es posible que desee [crear una carpeta personalizada para almacenar los elementos importados](how-to-work-with-folders-by-using-ews-in-exchange.md)o [sincronizar los elementos de cliente y de buzón](mailbox-synchronization-and-ews-in-exchange.md).
  
## <a name="see-also"></a>Vea también


- [Exportación e importación de elementos mediante EWS en Exchange](exporting-and-importing-items-by-using-ews-in-exchange.md)
    
- [Exportar elementos mediante EWS en Exchange](how-to-export-items-by-using-ews-in-exchange.md)
    
- [Carpetas y elementos de EWS en Exchange](folders-and-items-in-ews-in-exchange.md)
    
- [Sincronización de buzones de correo y EWS en Exchange](mailbox-synchronization-and-ews-in-exchange.md)
    

