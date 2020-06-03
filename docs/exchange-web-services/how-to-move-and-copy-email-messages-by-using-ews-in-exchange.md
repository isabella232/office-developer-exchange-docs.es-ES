---
title: Mover y copiar mensajes de correo electrónico mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 4771668f-5623-4397-a5c0-b75a7ba01698
description: Obtenga información sobre cómo mover y copiar mensajes de correo electrónico mediante la API administrada de EWS o EWS en Exchange.
localization_priority: Priority
ms.openlocfilehash: d13e84648f194dd4f431cf128396daf016addb22
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527939"
---
# <a name="move-and-copy-email-messages-by-using-ews-in-exchange"></a>Mover y copiar mensajes de correo electrónico mediante EWS en Exchange

Obtenga información sobre cómo mover y copiar mensajes de correo electrónico mediante la API administrada de EWS o EWS en Exchange.
  
Puede usar la API administrada de EWS o EWS para mover y copiar mensajes de correo electrónico en un buzón.
  
**Tabla 1. Métodos de API administrada de EWS y operaciones EWS para mover y copiar mensajes de correo electrónico**

|**Tarea**|**Método de la API administrada de EWS**|**Operación de EWS**|
|:-----|:-----|:-----|
|Mover un mensaje de correo electrónico  <br/> |[EmailMessage. Move](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) <br/> |[MoveItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> |
|Copiar un mensaje de correo electrónico  <br/> |[EmailMessage. Copy](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) <br/> |[CopyItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |
   
Es importante tener en cuenta que cuando se mueve o se copia un mensaje de correo electrónico en una carpeta diferente, se crea un nuevo elemento en la nueva carpeta con un identificador de elemento único y se elimina el mensaje original. Si está moviendo o copiando un mensaje de correo electrónico entre dos carpetas en el mismo buzón, el nuevo elemento se devuelve en la respuesta, lo que proporciona acceso al nuevo identificador de elemento. Sin embargo, si está moviendo o copiando un mensaje de correo electrónico entre dos buzones o entre un buzón y una carpeta pública, el nuevo elemento no se devolverá en la respuesta. Para obtener acceso al mensaje movido en ese escenario, use el método [FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) de la API administrada EWS o la operación de [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) de EWS, [cree una definición de propiedad](properties-and-extended-properties-in-ews-in-exchange.md) extendida para la propiedad [PidTagSearchKey](https://msdn.microsoft.com/library/cc839918.aspx) (0x300B0102) o cree y establezca una propiedad extendida personalizada y, a continuación, busque la propiedad extendida personalizada en la nueva carpeta. 
  
La eliminación de un mensaje de correo electrónico es diferente de mover un elemento a la carpeta elementos eliminados. Si usa el método [Item. Delete](https://msdn.microsoft.com/library/office/dd635072%28v=exchg.80%29.aspx) de la API administrada EWS o la operación de la aplicación [DeleteItem](../web-service-reference/deleteitem-operation.md) de EWS, el elemento especificado en la solicitud se quita de la carpeta original y se coloca una copia en la carpeta elementos ELIMINAdos con un identificador de elemento nuevo. A diferencia de cuando se mueve o se copia un elemento, el nuevo elemento no se devuelve en el método **Delete** o la respuesta de la operación **DeleteItem** . Los pasos necesarios para [eliminar un correo electrónico mediante la API administrada de EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) o [EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) son los mismos que para eliminar cualquier elemento genérico del almacén de Exchange. 
  
## <a name="move-an-email-message-by-using-the-ews-managed-api"></a>Mover un mensaje de correo electrónico mediante la API administrada de EWS
<a name="bk_moveewsma"> </a>

En el ejemplo de código siguiente se muestra cómo usar el método [EmailMessage. Move](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) para mover un mensaje de correo electrónico existente de una carpeta a otra. 
  
En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que **Itemid** es el [identificador](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del mensaje de correo electrónico que se va a mover o copiar. 
  
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

## <a name="move-an-email-message-by-using-ews"></a>Mover un mensaje de correo electrónico mediante EWS
<a name="bk_moveews"> </a>

En el siguiente ejemplo de código se muestra cómo usar la operación [MoveItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) para mover un mensaje de correo electrónico a la carpeta de correo electrónico no deseado. 
  
Esta es también la solicitud XML que la API administrada de EWS envía al llamar al método [Move](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) . Los valores de algunos atributos y elementos se han abreviado para facilitar su lectura. 
  
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

El servidor responde a la solicitud **MoveItem** con un mensaje [MoveItemResponse](https://msdn.microsoft.com/library/77be5104-1e09-4d50-abec-4fadb3a230e5%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que el mensaje de correo electrónico se ha movido correctamente. La respuesta también incluye el **Itemid** del mensaje de correo electrónico en la nueva carpeta, que es importante almacenar porque **Itemid** es diferente en la nueva carpeta. 
  
## <a name="copy-an-email-message-by-using-the-ews-managed-api"></a>Copiar un mensaje de correo electrónico mediante la API administrada de EWS
<a name="bk_copyewsma"> </a>

En el siguiente ejemplo de código se muestra cómo usar el método [EmailMessage. Copy](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) para copiar un mensaje de correo electrónico existente de una carpeta a otra. 
  
En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que **Itemid** es el [identificador](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del mensaje de correo electrónico que se va a copiar. Los valores de algunos parámetros se han abreviado para facilitar su lectura. 
  
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

## <a name="copy-an-email-message-by-using-ews"></a>Copiar un mensaje de correo electrónico mediante EWS
<a name="bk_copyews"> </a>

En el siguiente ejemplo de código se muestra cómo usar la operación [CopyItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) para copiar un mensaje de correo electrónico en una carpeta diferente del mismo buzón enviando el elemento [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) del mensaje de correo electrónico que se va a mover y especificando la carpeta de destino en el elemento [ToFolderId](https://msdn.microsoft.com/library/bd6a4265-ad40-43f6-bcc4-0bf5df4e984c%28Office.15%29.aspx) . 
  
Esta es también la solicitud XML que la API administrada de EWS envía al llamar al método [Copy](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) . Los valores de algunos atributos y elementos se han abreviado para facilitar su lectura. 
  
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

El servidor responde a la solicitud **CopyItem** con un mensaje [CopyItemResponse](https://msdn.microsoft.com/library/ae402bc1-4589-45e0-a929-f368c916a7e4%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que el mensaje de correo electrónico se ha copiado correctamente. La respuesta también incluye el **Itemid** del mensaje de correo electrónico en la nueva carpeta, que es importante almacenar porque **Itemid** es diferente en la nueva carpeta. 
  
## <a name="see-also"></a>Vea también


- [Correo electrónico y EWS en Exchange](email-and-ews-in-exchange.md)
    
- [Enviar mensajes de correo electrónico mediante EWS en Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md)
    

