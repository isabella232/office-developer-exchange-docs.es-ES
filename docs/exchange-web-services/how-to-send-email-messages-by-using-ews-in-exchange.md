---
title: Enviar mensajes de correo electrónico mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 5290fafe-8b51-4275-a27e-baf497fc969c
description: Obtenga información sobre cómo enviar mensajes de correo electrónico nuevos o borradores, o para enviar un mensaje de correo electrónico retrasado mediante la API administrada de EWS o EWS en Exchange.
localization_priority: Priority
ms.openlocfilehash: b73327cc69db37028c0508af788bf5294e79206a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527729"
---
# <a name="send-email-messages-by-using-ews-in-exchange"></a>Enviar mensajes de correo electrónico mediante EWS en Exchange

Obtenga información sobre cómo enviar mensajes de correo electrónico nuevos o borradores, o para enviar un mensaje de correo electrónico retrasado mediante la API administrada de EWS o EWS en Exchange.
  
Independientemente de si usa la API administrada de EWS o EWS, puede enviar mensajes de correo electrónico de dos maneras. Puede enviar un mensaje existente, como un mensaje almacenado en la carpeta Borradores, o puede crear y enviar un correo electrónico en un solo paso. Los métodos y las operaciones que se usan para enviar el mensaje son los mismos si envía un mensaje inmediatamente o envía un mensaje retrasado.
  
**Tabla 1. Métodos de API administrada de EWS y operaciones EWS para enviar mensajes de correo electrónico**

|**Tarea**|**Método de la API administrada de EWS**|**Operación de EWS**|
|:-----|:-----|:-----|
|Enviar un nuevo mensaje de correo electrónico  <br/> |[EmailMessage. SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|Enviar un mensaje de correo electrónico existente  <br/> |[EmailMessage. Send](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx) <br/> |[SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) <br/> |
   
## <a name="send-a-new-email-message-by-using-the-ews-managed-api"></a>Enviar un mensaje de correo electrónico nuevo mediante la API administrada de EWS
<a name="bk_sendnewewsma"> </a>

En el ejemplo de código siguiente se muestra cómo usar el objeto [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) para crear un mensaje de correo electrónico y el método [SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) para enviar el mensaje al destinatario y guardar el mensaje en la carpeta elementos enviados. 
  
En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange. 
  
```cs
// Create an email message and provide it with connection 
// configuration information by using an ExchangeService object named service.
EmailMessage message = new EmailMessage(service);
// Set properties on the email message.
message.Subject = "Company Soccer Team";
message.Body = "Are you interested in joining?";
message.ToRecipients.Add("sadie@contoso.com");
// Send the email message and save a copy.
// This method call results in a CreateItem call to EWS.
message.SendAndSaveCopy();
Console.WriteLine("An email with the subject '" + message.Subject + "' has been sent to '" + message.ToRecipients[0] + "' and saved in the SendItems folder.");
```

## <a name="send-a-new-email-message-by-using-ews"></a>Enviar un mensaje de correo electrónico nuevo mediante EWS
<a name="bk_sendnewews"> </a>

En el ejemplo de código siguiente se muestra cómo utilizar la operación [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) con un valor **MessageDisposition** de **SendAndSaveCopy** para crear un mensaje de correo electrónico, enviar el mensaje al destinatario y guardar el mensaje en la carpeta elementos enviados. También es la solicitud XML que la API administrada de EWS envía cuando envía [un nuevo mensaje de correo electrónico](#bk_sendnewewsma).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Company Soccer Team</t:Subject>
          <t:Body BodyType="HTML">Are you interested in joining?</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com </t:EmailAddress>
              </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud **CreateItem** con un mensaje [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) de **NoError**, que indica que el correo electrónico se ha creado correctamente y el [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) del mensaje recién creado. 
  
## <a name="send-a-draft-email-message-by-using-the-ews-managed-api"></a>Enviar un borrador de mensaje de correo electrónico mediante la API administrada de EWS
<a name="bk_senddraftewsma"> </a>

En el siguiente ejemplo de código se muestra cómo enviar un mensaje que se almacenó en la carpeta Borradores, como se muestra en [crear un mensaje de correo electrónico mediante la API administrada de EWS](email-and-ews-in-exchange.md#bk_createewsma). En primer lugar, use el método [BIND](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) para recuperar el mensaje y, a continuación, use el método [send](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx) para enviar el mensaje de correo electrónico, como se muestra en el siguiente ejemplo de código. Tenga en cuenta que este método no guarda el mensaje enviado en la carpeta elementos enviados. 
  
En este caso, las propiedades [EmailMessageSchema. Subject](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemschema.subject%28v=exchg.80%29.aspx) y [EmailMessageSchema. ToRecipients](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessageschema.torecipients%28v=exchg.80%29.aspx) se agregan a la [PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) para que los valores se puedan incluir en el resultado de la consola. 
  
En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange. 
  
```cs
// As a best practice, create a property set that limits the properties returned by the Bind method to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, EmailMessageSchema.ToRecipients);
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, propSet);
// Send the email message.
// This method call results in a SendItem call to EWS.
message.Send();
Console.WriteLine("An email with the subject '" + message.Subject + "' has been sent to '" + message.ToRecipients[0] + "'.");
```

## <a name="send-a-draft-email-message-by-using-ews"></a>Enviar un borrador de mensaje de correo electrónico mediante EWS
<a name="bk_senddraftews"> </a>

Los ejemplos de código siguientes muestran cómo enviar un mensaje que se almacenó anteriormente en la carpeta Borradores, como se muestra en [crear un mensaje de correo electrónico mediante EWS](email-and-ews-in-exchange.md#bk_createews). En primer lugar, use la operación [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) para recuperar el mensaje de correo electrónico que se va a enviar. A continuación, use la operación [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) para enviar el mensaje de correo electrónico a los destinatarios y guárdelo en la carpeta elementos enviados. 
  
El primer mensaje, el mensaje de solicitud **GetItem** , especifica el [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) del borrador del mensaje de correo electrónico al que se va a enlazar y los elementos del elemento [ItemShape](https://msdn.microsoft.com/library/c5604161-bbc0-40bc-ad75-ff7e837d745f%28Office.15%29.aspx) limitan los resultados para incluirlos en la respuesta **GetItem** . El elemento **ItemShape** tiene un [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) de **IdOnly**y el elemento [AdditionalProperties](https://msdn.microsoft.com/library/7a269aed-dcfd-4c3e-9e14-094e53828101%28Office.15%29.aspx) incluye los valores [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) de la propiedad **Subject** del esquema de elementos y la propiedad **ToRecipients** del esquema del mensaje, lo que significa que solo se devolverán al cliente los elementos **Itemid**, [Subject](https://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx)y [ToRecipients](https://msdn.microsoft.com/library/72dc3be8-30bb-4ae1-acf4-fb94ff490631%28Office.15%29.aspx) en la respuesta. Para obtener más información sobre cómo limitar los valores devueltos en las llamadas y el significado del elemento **BaseShape** , vea [Property sets and Response Shapes in EWS in Exchange](property-sets-and-response-shapes-in-ews-in-exchange.md).
  
Esta es también la solicitud XML que la API administrada de EWS envía al llamar al método [BIND](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) . Los valores de algunos atributos y elementos se han abreviado para facilitar su lectura. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="message:ToRecipients" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="AAMkADE4=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

En el ejemplo siguiente se muestra la respuesta XML que devuelve el servidor después de procesar la operación **GetItem** . La respuesta indica que el mensaje de correo electrónico se ha recuperado correctamente e incluye los elementos **Subject** y **ToRecipient** según se ha solicitado. Los valores de algunos atributos y elementos se han abreviado para facilitar su lectura. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="842"
                         MinorBuildNumber="10"
                         Version="V2_8"
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
              <t:ItemId Id="AAMkADE4="
                        ChangeKey="CQAAABYA" />
              <t:Subject>Project priorities</t:Subject>
              <t:ToRecipients>
                <t:Mailbox>
                  <t:Name>sadie@contoso.com</t:Name>
                  <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
                  <t:RoutingType>SMTP</t:RoutingType>
                  <t:MailboxType>OneOff</t:MailboxType>
                </t:Mailbox>
              </t:ToRecipients>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

El segundo mensaje, el mensaje de solicitud **SendItem** , especifica el [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) del mensaje de correo electrónico que se envía, así como la [SavedItemFolderId](https://msdn.microsoft.com/library/4b8b475c-9ca5-48c9-acb0-8848b53be1ce%28Office.15%29.aspx), que especifica la carpeta en la que se va a guardar el elemento enviado.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:SendItem SaveItemToFolder="true">
      <m:ItemIds>
        <t:ItemId Id="AAMkADE4="
                  ChangeKey="CQAAABYA" />
      </m:ItemIds>
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems" />
      </m:SavedItemFolderId>
    </m:SendItem>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud **SendItem** con un mensaje [SendItemResponse](https://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) que incluye un [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) valor de **NoError**, lo que indica que el correo electrónico se envió correctamente.
  
## <a name="send-a-delayed-email-message-by-using-the-ews-managed-api"></a>Enviar un mensaje de correo electrónico retrasado mediante la API administrada de EWS
<a name="bk_senddelayedewsma"> </a>

En el ejemplo de código siguiente se muestra cómo usar el objeto [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) para crear un mensaje de correo electrónico, la clase [ExtendedPropertyDefinition](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) para crear una definición de propiedad para la propiedad [PidTagDeferredSendTime](https://msdn.microsoft.com/library/cc840017.aspx) (0x3FEF0040) y el método [SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) para enviar un mensaje retrasado y guardar el mensaje en la carpeta elementos enviados. 
  
En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange. 
  
```cs
// Create a new email message. 
EmailMessage message = new EmailMessage(service);
// Specify the email recipient and subject. 
message.ToRecipients.Add("sadie@contoso.com");
message.Subject = "Delayed email";
// Identify the extended property that can be used to specify when to send the email. 
ExtendedPropertyDefinition PidTagDeferredSendTime = new ExtendedPropertyDefinition(16367, MapiPropertyType.SystemTime);
// Set the time that will be used to specify when the email is sent. 
// In this example, the email will be sent one minute after the next line executes, 
// provided that the message.SendAndSaveCopy request is processed by the server within one minute. 
string sendTime = DateTime.Now.AddMinutes(1).ToUniversalTime().ToString();
// Specify when to send the email by setting the value of the extended property. 
message.SetExtendedProperty(PidTagDeferredSendTime, sendTime);
// Specify the email body. 
StringBuilder str = new StringBuilder();
str.AppendLine("The client submitted the SendAndSaveCopy request at: " + DateTime.Now.ToUniversalTime().ToString() + ".");
str.AppendLine("The email message will be sent at: " + sendTime + ".");
message.Body = str.ToString();
Console.WriteLine("");
Console.WriteLine("The client submitted the SendAndSaveCopy request at: " + DateTime.Now.ToUniversalTime().ToString() + ".");
Console.WriteLine("The email message will be sent at: " + sendTime + ".");
// Submit the request to send the email message. 
message.SendAndSaveCopy();
```

## <a name="send-a-delayed-email-message-by-using-ews"></a>Enviar un mensaje de correo electrónico retrasado mediante EWS
<a name="bk_senddelayedews"> </a>

El siguiente ejemplo de código muestra cómo utilizar la operación [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) con un valor **MessageDisposition** de **SendAndSaveCopy** para crear un mensaje de correo electrónico, el elemento [las extendedproperty](https://msdn.microsoft.com/library/f9701409-b620-4afe-b9ee-4c1e95507af7%28Office.15%29.aspx) para crear una definición de propiedad para la propiedad [PidTagDeferredSendTime](https://msdn.microsoft.com/library/cc840017.aspx) (0x3FEF0040) para establecer una hora para enviar el mensaje y el elemento [SavedItemFolderId](https://msdn.microsoft.com/library/4b8b475c-9ca5-48c9-acb0-8848b53be1ce%28Office.15%29.aspx) para guardar el mensaje enviado en la carpeta elementos enviados. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange207_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Delayed email</t:Subject>
          <t:Body BodyType="HTML">
            The client submitted the SendAndSaveCopy request at: 1/2/2014 9:08:52 PM.
            The email message will be sent at: 1/2/2014 9:09:52 PM.
          </t:Body>
          <t:ExtendedProperty>
            <t:ExtendedFieldURI PropertyTag="16367"
                                PropertyType="SystemTime" />
            <t:Value>2014-01-02T21:09:52.000</t:Value>
          </t:ExtendedProperty>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud **CreateItem** con un mensaje [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que el correo electrónico se ha creado correctamente y el [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) del mensaje recién creado. 
  
## <a name="see-also"></a>Vea también


- [Correo electrónico y EWS en Exchange](email-and-ews-in-exchange.md)
    
- [Responder a mensajes de correo electrónico mediante EWS en Exchange](how-to-respond-to-email-messages-by-using-ews-in-exchange.md)
    

