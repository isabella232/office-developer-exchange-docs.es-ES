---
title: Eliminar datos adjuntos mediante EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 71871ac7-ee1a-4f93-9e81-77f312d432f4
description: Obtenga información sobre cómo eliminar datos adjuntos de elementos mediante la API administrada ews o EWS en Exchange.
ms.openlocfilehash: bc9b8bbf5833cfdb44f9ca4e8387681473fad3c3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521154"
---
# <a name="delete-attachments-by-using-ews-in-exchange"></a>Eliminar datos adjuntos mediante EWS en Exchange

Obtenga información sobre cómo eliminar datos adjuntos de elementos mediante la API administrada ews o EWS en Exchange.
  
Tiene varias opciones cuando se trata de eliminar datos adjuntos de archivos y elementos de los elementos mediante la API administrada ews. Puede eliminar todos los datos adjuntos del mensaje, eliminarlos por un nombre de archivo o eliminar por posición en la colección. Para cada una de estas opciones, hay un [método AttachmentCollection.](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection%28v=exchg.80%29.aspx) 
  
Por el contrario, con EWS, independientemente de si va a eliminar todos los datos adjuntos de un elemento o solo uno, la secuencia de operaciones es la misma. A diferencia de la API administrada ews, EWS no incluye operaciones independientes para eliminar en función del nombre o la posición de la matriz de datos adjuntos.
  
**Tabla 1. Métodos de API administrada ews y operaciones EWS para eliminar datos adjuntos**

|**Tarea**|**Método de la API administrada de EWS**|**Operación de EWS**|
|:-----|:-----|:-----|
|Elimine todos los datos adjuntos de un elemento.  <br/> |[Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), seguido de [AttachmentCollection.Clear](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.clear%28v=exchg.80%29.aspx), seguido de [EmailMessage.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[GetItem seguido](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) de [DeleteAttachment](https://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx) <br/> |
|Elimine los datos adjuntos de un elemento por su nombre.  <br/> |[Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), seguido de [AttachmentCollection.Remove](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx), seguido de [EmailMessage.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[GetItem seguido](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) de [DeleteAttachment](https://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx) <br/> |
|Elimine los datos adjuntos de un elemento por posición en la colección.  <br/> |[Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), seguido de [AttachmentCollection.RemoveAt](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.removeat%28v=exchg.80%29.aspx), seguido de [EmailMessage.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[GetItem seguido](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) de [DeleteAttachment](https://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx) <br/> |
   
## <a name="delete-all-attachments-from-an-email-by-using-the-ews-managed-api"></a>Eliminar todos los datos adjuntos de un correo electrónico mediante la API administrada de EWS
<a name="bk_deleteattachewsma"> </a>

En el siguiente ejemplo de código se muestra cómo eliminar todos los datos adjuntos de un correo electrónico:
  
1. Usar el [método EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) para enlazar a un mensaje de correo electrónico existente y recuperar la colección de [datos adjuntos](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx).
    
2. Uso del [método AttachmentCollection.Clear](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.clear%28v=exchg.80%29.aspx) para eliminar todos los datos adjuntos del correo electrónico. 
    
3. Usar el [método EmailMessage.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) para guardar los cambios. 
    
En este ejemplo se supone que **el** servicio es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido, **itemId** es [el ItemId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) del mensaje desde el que se eliminarán los datos adjuntos y que el usuario se ha autenticado en un servidor Exchange servidor. 
  
```cs
public static void DeleteAllAttachments(ExchangeService service, ItemId itemId)
{
    // Bind to an existing message by using its item ID and requesting its attachments collection.
    // This method results in a GetItem call to EWS.
    EmailMessage message = EmailMessage.Bind(service, itemId, new PropertySet(ItemSchema.Attachments));
    // Delete all attachments from the message.
    message.Attachments.Clear();
    // Save the updated message.
    // This method results in an DeleteAttachment call to EWS.
    message.Update(ConflictResolutionMode.AlwaysOverwrite);
}
```

## <a name="delete-an-attachment-by-name-from-an-email-by-using-the-ews-managed-api"></a>Eliminar datos adjuntos por su nombre de un correo electrónico mediante la API administrada de EWS
<a name="bk_deleteattachewsma"> </a>

En el siguiente ejemplo de código se muestra cómo eliminar datos adjuntos por su nombre:
  
1. Usar el [método EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) para enlazar a un mensaje de correo electrónico existente y recuperar la colección de [datos adjuntos](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx).
    
2. Usar el [método AttachmentCollection.Remove](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx) para eliminar un archivo adjunto denominado FileAttachment.txt. 
    
3. Usar el [método EmailMessage.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) para guardar los cambios. 
    
En este ejemplo se supone que **service** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido, **itemId** es [el ItemId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) del mensaje desde el que se eliminarán los datos adjuntos y que el usuario se ha autenticado en un servidor Exchange. 
  
```cs
public static void DeleteNamedAttachments(ExchangeService service, ItemId itemId)
{
    // Bind to an existing message by using its item ID and requesting its attachments collection.
    // This method results in a GetItem call to EWS.
    EmailMessage message = EmailMessage.Bind(service, itemId, new PropertySet(ItemSchema.Attachments));
    // Iterate through the attachments collection and delete the attachment named "FileAttachment.txt," if it exists.
    foreach (Attachment attachment in message.Attachments)
    {
        if (attachment.Name == "FileAttachment.txt")
        {
            message.Attachments.Remove(attachment);
            break;
        }
    }
    // Save the updated message.
    // This method results in an DeleteAttachment call to EWS.
    message.Update(ConflictResolutionMode.AlwaysOverwrite);
}
```

## <a name="delete-attachments-by-position-by-using-the-ews-managed-api"></a>Eliminar datos adjuntos por posición mediante la API administrada de EWS
<a name="bk_deleteattachewsma"> </a>

En el siguiente ejemplo de código se muestra cómo eliminar datos adjuntos por posición mediante:
  
1. Usar el [método EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) para enlazar a un mensaje de correo electrónico existente y recuperar la colección [de datos](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx) adjuntos y la [propiedad EmailMessage.HasAttachments.](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx) 
    
2. Uso del [método AttachmentCollection.Remove](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx) para eliminar los primeros datos adjuntos de la colección. 
    
3. Usar el [método EmailMessage.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) para guardar los cambios. 
    
En este ejemplo se supone que **service** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido, **itemId** es [el ItemId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) del mensaje desde el que se eliminarán los datos adjuntos y que el usuario se ha autenticado en un servidor Exchange. 
  
```cs
public static void DeleteAttachmentByPosition(ExchangeService service, ItemId itemId)
{
    // Bind to an existing message by using its item ID and requesting the HasAttachments property and the attachments collection.
    // This method results in a GetItem call to EWS.
    EmailMessage message = EmailMessage.Bind(service, itemId, new PropertySet(EmailMessageSchema.HasAttachments, ItemSchema.Attachments));
    // Remove attachments using the zero-based index position of the attachment in the attachments collection.
    if (message.HasAttachments)
    {
        message.Attachments.RemoveAt(0);
    }
    // Save the updated message.
    // This method results in an DeleteAttachment call to EWS.
    message.Update(ConflictResolutionMode.AlwaysOverwrite);
}
```

## <a name="delete-attachments-from-an-item-by-using-ews"></a>Eliminar datos adjuntos de un elemento mediante EWS
<a name="bk_deleteattachewsma"> </a>

Para eliminar datos adjuntos mediante EWS, primero debe recuperar el mensaje y la colección de datos adjuntos para determinar [el AttachmentId (GetAttachment y DeleteAttachment)](https://msdn.microsoft.com/library/4bea1cb5-0a0f-4e14-9b09-f91af8cf9899%28Office.15%29.aspx) de los datos adjuntos que se deben eliminar. Después de que tenga uno o varios valores **AttachmentId** que eliminar, llame a la [operación DeleteAttachment](https://msdn.microsoft.com/library/4d48e595-b98c-48e7-bbeb-cacf91d12a78%28Office.15%29.aspx) para quitar los datos adjuntos especificados del mensaje. 
  
En el siguiente ejemplo de código se muestra cómo usar la operación [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) para obtener un mensaje de correo electrónico y la colección de datos adjuntos en el mensaje. Esta es también la primera solicitud XML que envía la API administrada ews cuando se usa la API administrada ews para eliminar todos los datos [adjuntos de un correo electrónico.](#bk_deleteattachewsma) Los valores de algunos atributos se acortan para mejorar la legibilidad.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Central Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Attachments" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="uqE1AAA=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud **GetItem** con un mensaje [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) de **NoError**, que indica que el correo electrónico se recuperó correctamente y los valores [AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) de los datos adjuntos existentes. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="939"
                         MinorBuildNumber="12"
                         Version="V2_11"
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
              <t:ItemId Id="uqE1AAA="
                        ChangeKey="CQAAABYAAAAFI5DJmZv+TLtyLOLIF1S5AAAXulcd" />
              <t:Attachments>
                <t:FileAttachment>
                  <t:AttachmentId Id="IpHLObE=" />
                  <t:Name>FileAttachment.txt</t:Name>
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="QuHSSmY=" />
                  <t:Name>SecondAttachment.txt</t:Name>
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="qf2KoPo=" />
                  <t:Name>ThirdAttachment.jpg</t:Name>
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="NFQMnMc=" />
                  <t:Name>FourthAttachment.txt</t:Name>
                </t:FileAttachment>
                <t:ItemAttachment>
                  <t:AttachmentId Id="jJvbLXQ=" />
                  <t:Name>Attached Message Item</t:Name>
                </t:ItemAttachment>
              </t:Attachments>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

Después de determinar qué datos adjuntos eliminar, llame a [la operación DeleteAttachment](https://msdn.microsoft.com/library/4d48e595-b98c-48e7-bbeb-cacf91d12a78%28Office.15%29.aspx) e incluya los **valores AttachmentId** de los datos adjuntos que se eliminarán. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Central Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:DeleteAttachment>
      <m:AttachmentIds>
        <t:AttachmentId Id="IpHLObE=" />
        <t:AttachmentId Id="QuHSSmY=" />
        <t:AttachmentId Id="qf2KoPo=" />
        <t:AttachmentId Id="NFQMnMc=" />
        <t:AttachmentId Id="jJvbLXQ=" />
      </m:AttachmentIds>
    </m:DeleteAttachment>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud **DeleteAttachment** con un mensaje [DeleteAttachmentResponse](https://msdn.microsoft.com/library/24099a88-4ab6-4bf3-8ed5-efec8e07b9b9%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) de **NoError** para cada [DeleteAttachmentResponseMessage](https://msdn.microsoft.com/library/1edb085f-1674-48e5-8ec3-42351adeac7d%28Office.15%29.aspx), que indica que cada dato adjunto se eliminó correctamente. Los valores de algunos atributos se acortan para mejorar la legibilidad.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="939"
                         MinorBuildNumber="12"
                         Version="V2_11"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:DeleteAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
      </m:ResponseMessages>
    </m:DeleteAttachmentResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a>Ver también


- [Datos adjuntos y EWS en Exchange](attachments-and-ews-in-exchange.md)
    
- [Agregar datos adjuntos mediante EWS en Exchange](how-to-add-attachments-by-using-ews-in-exchange.md)
    
- [Obtener datos adjuntos mediante EWS en Exchange](how-to-get-attachments-by-using-ews-in-exchange.md)
    

