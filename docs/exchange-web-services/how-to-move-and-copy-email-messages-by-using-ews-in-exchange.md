---
title: Mover y copiar los mensajes de correo electrónico mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4771668f-5623-4397-a5c0-b75a7ba01698
description: Obtenga información sobre cómo mover y copiar los mensajes de correo electrónico mediante el uso de la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 16f0604a16785c34dd04bdabedeedd331668a479
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763140"
---
# <a name="move-and-copy-email-messages-by-using-ews-in-exchange"></a>Mover y copiar los mensajes de correo electrónico mediante el uso de EWS en Exchange

Obtenga información sobre cómo mover y copiar los mensajes de correo electrónico mediante el uso de la API administrada de EWS o EWS en Exchange.
  
Puede usar la API administrada de EWS o EWS para mover y copiar los mensajes en un buzón de correo electrónico.
  
**La tabla 1. Métodos de la API administrada de EWS y las operaciones de EWS para mover y copiar mensajes de correo electrónico**

|**Tarea**|**Método de la API administrada de EWS**|**Operación de EWS**|
|:-----|:-----|:-----|
|Mover un mensaje de correo electrónico  <br/> |[EmailMessage.Move](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) <br/> |[MoveItem](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> |
|Copiar un mensaje de correo electrónico  <br/> |[EmailMessage.Copy](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) <br/> |[CopyItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |
   
Es importante tener en cuenta que al mover o copiar un mensaje de correo electrónico en una carpeta diferente, se crea un nuevo elemento en la nueva carpeta con un identificador de elemento único, y se elimina el mensaje original. Si está mover o copiar un mensaje de correo electrónico entre dos carpetas en el mismo buzón, se devuelve el nuevo elemento en la respuesta, que le proporciona acceso para el nuevo identificador de elemento. Sin embargo, si va a mover o copiar un mensaje de correo electrónico entre dos buzones o entre un buzón de correo y una carpeta pública, el nuevo elemento no se devuelve en la respuesta. Para obtener acceso a los mensajes que se ha movido en esa situación, utilice el método de la API administrada de EWS [FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) u operación de EWS [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) , [crear una definición de propiedad extendida](properties-and-extended-properties-in-ews-in-exchange.md) para la propiedad [PidTagSearchKey](http://msdn.microsoft.com/en-us/library/cc839918.aspx) (0x300B0102), o crear y establecer un ampliado personalizado (propiedad) y, a continuación, busque la propiedad extendida personalizada en la nueva carpeta. 
  
Eliminación de un mensaje de correo electrónico es diferente de mover un elemento a la carpeta Elementos eliminados. Si usa el método de la API administrada de EWS [Item.Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx) o la operación de EWS [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) , se quita el elemento especificado en la solicitud de la carpeta original y se coloca una copia en la carpeta Elementos eliminados con un nuevo identificador de elemento. A diferencia de al mover o copiar cualquier elemento, el nuevo elemento no se devuelve en la respuesta de la operación **DeleteItem** o en el método **Delete** . Los pasos implicados en la [eliminación de un correo electrónico mediante el uso de la API administrada de EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) o [EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) son los mismos que los para eliminar cualquier elemento genérico desde el almacén de Exchange. 
  
## <a name="move-an-email-message-by-using-the-ews-managed-api"></a>Mover un mensaje de correo electrónico mediante el uso de la API administrada de EWS
<a name="bk_moveewsma"> </a>

En el ejemplo de código siguiente se muestra cómo utilizar el método [EmailMessage.Move](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) para mover un mensaje de correo electrónico existente de una carpeta a otra. 
  
En este ejemplo se supone que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido, y ese **ItemId** es el [identificador](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) de mensaje de correo electrónico para mover o copiar. 
  
```cs
// As a best practice, limit the properties returned by the Bind method to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, EmailMessageSchema.ParentFolderId);
// Bind to the existing item by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage beforeMessage = EmailMessage.Bind(service, ItemId, propSet);
// Move the specified mail to the JunkEmail folder and store the returned item.
Item item = beforeMessage.Move(WellKnownFolderName.JunkEmail);
// Check that the item was moved by binding to the moved email message 
// and retrieving the new ParentFolderId.
// This method call results in a GetItem call to EWS.
EmailMessage movedMessage = EmailMessage.Bind(service, item.Id, propSet);
Console.WriteLine("An email message with the subject '" + beforeMessage.Subject + "' has been moved from the '" + beforeMessage.ParentFolderId + "' folder to the '" + movedMessage.ParentFolderId + "' folder.");
```

## <a name="move-an-email-message-by-using-ews"></a>Mover un mensaje de correo electrónico mediante el uso de EWS
<a name="bk_moveews"> </a>

En el ejemplo de código siguiente se muestra cómo usar la operación [MoveItem](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) para mover un mensaje de correo electrónico a la carpeta correo electrónico no deseado. 
  
También es la solicitud XML que se envía por la API administrada de EWS al llamar al método [mover](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) . Los valores de algunos elementos y atributos se han abreviado para mejorar la legibilidad. 
  
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
    <m:MoveItem>
      <m:ToFolderId>
        <t:DistinguishedFolderId Id="junkemail" />
      </m:ToFolderId>
      <m:ItemIds>
        <t:ItemId Id="AfwDoAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF25sM1" />
      </m:ItemIds>
    </m:MoveItem>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud de **MoveItem** con un mensaje de [MoveItemResponse](http://msdn.microsoft.com/library/77be5104-1e09-4d50-abec-4fadb3a230e5%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que el mensaje de correo electrónico se ha movido correctamente. La respuesta incluye también la **ItemId** para el mensaje de correo electrónico en la nueva carpeta, lo que es importante para almacenar porque la **ItemId** es distinto en la nueva carpeta. 
  
## <a name="copy-an-email-message-by-using-the-ews-managed-api"></a>Copiar un mensaje de correo electrónico mediante el uso de la API administrada de EWS
<a name="bk_copyewsma"> </a>

En el ejemplo de código siguiente se muestra cómo utilizar el método [EmailMessage.Copy](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) para copiar un mensaje de correo electrónico existente de una carpeta a otra. 
  
En este ejemplo se supone que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido, y ese **ItemId** es el [identificador](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) de mensaje de correo electrónico para copiar. Los valores de algunos parámetros se han abreviado para mejorar la legibilidad. 
  
```cs
// As a best practice, limit the properties returned by the Bind method to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, EmailMessageSchema.ParentFolderId);
// Bind to the existing item by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage originalMessage = EmailMessage.Bind(service, ItemId, propSet);
// Copy the orignal message into another folder in the mailbox and store the returned item.
Item item = originalMessage.Copy("epQ/3AAA=");
// Check that the item was copied by binding to the copied email message 
// and retrieving the new ParentFolderId.
// This method call results in a GetItem call to EWS.
EmailMessage copiedMessage = EmailMessage.Bind(service, item.Id, propSet);
Console.WriteLine("An email message with the subject '" + originalMessage.Subject + "' has been copied from the '" + originalMessage.ParentFolderId + "' folder to the '" + copiedMessage.ParentFolderId + "' folder.");
```

## <a name="copy-an-email-message-by-using-ews"></a>Copiar un mensaje de correo electrónico mediante el uso de EWS
<a name="bk_copyews"> </a>

En el ejemplo de código siguiente se muestra cómo utilizar la operación [CopyItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) para copiar un mensaje de correo electrónico a una carpeta diferente en el mismo buzón mediante el envío del [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) del mensaje de correo electrónico para mover y especificar la carpeta de destino en la [ToFolderId ](http://msdn.microsoft.com/library/bd6a4265-ad40-43f6-bcc4-0bf5df4e984c%28Office.15%29.aspx)elemento. 
  
También es la solicitud XML que se envía por la API administrada de EWS al llamar al método de [copia](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) . Los valores de algunos elementos y atributos se han abreviado para mejorar la legibilidad. 
  
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
    <m:CopyItem>
      <m:ToFolderId>
        <t:FolderId Id="pQ/3AAA=" />
      </m:ToFolderId>
      <m:ItemIds>
        <t:ItemId Id="2TSeSAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF2d+3+" />
      </m:ItemIds>
    </m:CopyItem>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud de **CopyItem** con un mensaje de [CopyItemResponse](http://msdn.microsoft.com/library/ae402bc1-4589-45e0-a929-f368c916a7e4%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que el mensaje de correo electrónico se ha copiado correctamente. La respuesta incluye también la **ItemId** para el mensaje de correo electrónico en la nueva carpeta, lo que es importante para almacenar porque la **ItemId** es distinto en la nueva carpeta. 
  
## <a name="see-also"></a>Vea también


- [Correo electrónico y EWS en Exchange](email-and-ews-in-exchange.md)
    
- [Enviar mensajes de correo electrónico mediante el uso de EWS en Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md)
    

