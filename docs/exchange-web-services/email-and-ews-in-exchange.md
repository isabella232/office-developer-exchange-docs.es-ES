---
title: Correo electrónico y EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d7bdb37-f7f1-409f-9749-f8bcde7dc52a
description: Obtenga información acerca de cómo trabajar con mensajes de correo electrónico, incluido cómo crear un correo electrónico y cómo realizar otras tareas relacionadas con el correo electrónico mediante el uso de la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: d222be7409a3c3f4613a2be39b83b977fabb09e8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763002"
---
# <a name="email-and-ews-in-exchange"></a>Correo electrónico y EWS en Exchange

Obtenga información acerca de cómo trabajar con mensajes de correo electrónico, incluido cómo crear un correo electrónico y cómo realizar otras tareas relacionadas con el correo electrónico mediante el uso de la API administrada de EWS o EWS en Exchange.
  

  
En esencia, Exchange es acerca del correo electrónico. Pero ¿qué hace un correo electrónico de un correo electrónico? Bueno, mensajes de correo electrónico están uno de [los elementos con establecimiento inflexible de tipos](folders-and-items-in-ews-in-exchange.md#bk_item) en Exchange, lo que significa que contienen un determinado [conjunto de propiedades](email-properties-and-elements-in-ews-in-exchange.md), incluso antes de que se envían. Mensajes de correo electrónico están representados por la clase [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) en la API administrada de EWS y en el elemento de [mensaje](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) y sus elementos secundarios en EWS. 
  
En la API administrada de EWS, el objeto **EmailMessage** se deriva el objeto de [elemento](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) . La clase **EmailMessage** extiende la clase de **elemento** proporcionando propiedades adicionales como [EmailMessage.Sender](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sender%28v=exchg.80%29.aspx) y [EmailMessage.IsRead](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.isread%28v=exchg.80%29.aspx), que ahora son comunes a casi todos los escenarios de mensajería. Al obtener, actualizar o eliminar un mensaje de correo electrónico, en la mayoría de los casos que puede hacerlo mediante el objeto **EmailMessage** o el objeto de **elemento** base, en función de si las propiedades que se está trabajando con están en la [EmailMessageSchema](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessageschema%28v=exchg.80%29.aspx) o la [ ItemSchema](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemschema%28v=exchg.80%29.aspx) clase. Creación de elemento es diferente porque la clase de **elemento** no tiene un constructor, por lo que si se está creando un correo electrónico, se usará el [constructor EmailMessage](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.emailmessage%28v=exchg.80%29.aspx) para crear y el [EmailMessage.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) o [EmailMessage.SendAndSaveCopy ](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx)métodos para guardarlo, o enviarlo y vuelva a guardarla. 
  
De forma similar, en EWS, use la operación [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) con el elemento de [mensaje](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) para crear un mensaje de correo electrónico. Para obtener, actualizar o eliminar mensajes de correo electrónico mediante el uso de EWS, el hecho de que el elemento que se modifica es un mensaje de correo electrónico no es importante, aparte del hecho de que las propiedades adicionales están disponibles en los mensajes de correo electrónico. También se usan las mismas operaciones que se usan para otros elementos fuertemente tipados para mensajes de correo electrónico. 
  
|**Tarea**|**Método de la API administrada de EWS**|**Operación de EWS**|
|:-----|:-----|:-----|
|Crear  <br/> |[EmailMessage.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) <br/> |[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|Obtener  <br/> |[EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) <br/> |
|Actualizar  <br/> |[Item.Update](http://msdn.microsoft.com/en-us/library/dd635915%28v=exchg.80%29.aspx) <br/> |[UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Eliminar  <br/> |[Item.Delete](http://msdn.microsoft.com/en-us/library/dd635072%28v=exchg.80%29.aspx) <br/> |[DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |
   
Debido a que los mensajes de correo electrónico son simplemente [elementos con establecimiento inflexible de tipos](folders-and-items-in-ews-in-exchange.md#bk_item), en algunos casos trabaja con ellos de la misma manera que [trabajar con los elementos genéricos](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md). 
  
## <a name="create-an-email-message-by-using-the-ews-managed-api"></a>Crear un mensaje de correo electrónico mediante el uso de la API administrada de EWS
<a name="bk_createewsma"> </a>

Puede crear un mensaje de correo electrónico mediante el método API administrada de EWS [Guardar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) , tal como se muestra en el código en el siguiente ejemplo. Tenga en cuenta que sólo en el ejemplo se guarda el mensaje en la carpeta Borradores, no envía el mensaje. Para obtener información acerca de cómo enviar el mensaje o crear y enviar el mensaje en un solo paso, consulte [enviar mensajes de correo electrónico mediante el uso de EWS en Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md).
  
En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange. 
  
```cs
// Create a new email message.
EmailMessage message = new EmailMessage(service);
// Set properties on the email message.
message.ToRecipients.Add("mack@contoso.com");
message.Subject = "Project priorities";
message.Body = "(1) Buy pizza, (2) Eat pizza";
// Save the email message to the Drafts folder (where it can be retrieved, updated, and sent at a later time).
// This method call results in a CreateItem call to EWS.
message.Save(WellKnownFolderName.Drafts);
Console.WriteLine("A draft email message with the subject '" + message.Subject + "' has been saved to the Drafts folder.");
```

## <a name="create-an-email-message-by-using-ews"></a>Crear un mensaje de correo electrónico mediante el uso de EWS
<a name="bk_createews"> </a>

Puede crear un mensaje de correo electrónico mediante el uso de la operación EWS [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) , tal como se muestra en el siguiente ejemplo. Esto también es la solicitud XML que la API administrada de EWS envía al [crear un mensaje de correo electrónico](#bk_createewsma). Tenga en cuenta que sólo en el ejemplo siguiente se guarda el mensaje en la carpeta Borradores, no envía el mensaje. Para obtener información acerca de cómo enviar el mensaje o crear y enviar el mensaje en uno ste, vea [enviar mensajes de correo electrónico mediante el uso de EWS en Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP2" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="drafts" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Project priorities</t:Subject>
          <t:Body BodyType="HTML">(1) Buy pizza, (2) Eat pizza</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>mack@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>

```

El servidor responde a la solicitud **CreateItem** con un mensaje de [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **NoError**, lo que indica que el correo electrónico se ha creado correctamente y la [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) de la recientemente mensaje de creación. 
  
## <a name="get-update-and-delete-an-email-message-by-using-the-ews-managed-api"></a>Obtener, actualizar y eliminar un mensaje de correo electrónico mediante el uso de la API administrada de EWS
<a name="bk_getewsma"> </a>

Puede usar la API administrada de EWS para obtener, actualizar o eliminar un mensaje de correo electrónico de la misma manera que se realizan estas acciones con cualquier elemento genérico desde el almacén de Exchange. Para obtener más información, vea [trabajar con elementos de buzón de correo de Exchange mediante el uso de EWS en Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md).
  
Si está actualizando un mensaje de correo electrónico, vea [de correo electrónico las propiedades y los elementos de EWS en Exchange](email-properties-and-elements-in-ews-in-exchange.md) para obtener una lista de propiedades del mensaje de correo electrónico puede escribir. Para enviar un borrador de mensaje después de que lo haya actualizado, vea [Enviar un borrador de mensaje de correo electrónico mediante el uso de la API administrada de EWS](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftewsma).
  
## <a name="get-update-and-delete-an-email-message-by-using-ews"></a>Obtener, actualizar y eliminar un mensaje de correo electrónico mediante el uso de EWS
<a name="bk_getews"> </a>

Puede usar EWS para obtener, actualizar y eliminar un mensaje de correo electrónico de la misma manera que se realizan estas acciones con cualquier elemento genérico desde el almacén de Exchange. Para obtener más información, vea [trabajar con elementos de buzón de correo de Exchange mediante el uso de EWS en Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md).
  
Si está actualizando un mensaje de correo electrónico, vea [de correo electrónico las propiedades y los elementos de EWS en Exchange](email-properties-and-elements-in-ews-in-exchange.md) para obtener una lista de propiedades del mensaje de correo electrónico puede escribir. Para enviar un borrador de mensaje después de que lo haya actualizado, vea [Enviar un borrador de mensaje de correo electrónico mediante el uso de EWS](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftews).
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_inthissection"> </a>

- [Correo electrónico de las propiedades y los elementos de EWS en Exchange](email-properties-and-elements-in-ews-in-exchange.md)
    
- [Enviar mensajes de correo electrónico mediante el uso de EWS en Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md)
    
- [Responder a mensajes de correo electrónico mediante el uso de EWS en Exchange](how-to-respond-to-email-messages-by-using-ews-in-exchange.md)
    
- [Mover y copiar los mensajes de correo electrónico mediante el uso de EWS en Exchange](how-to-move-and-copy-email-messages-by-using-ews-in-exchange.md)
    
- [Trabajar con las conversaciones con EWS en Exchange](how-to-work-with-conversations-by-using-ews-in-exchange.md)
    
- [Extraer una entidad de un mensaje de correo electrónico mediante el uso de EWS en Exchange](how-to-extract-an-entity-from-an-email-message-by-using-ews-in-exchange.md)
    
- [Mensajes de correo electrónico de proceso por lotes mediante el uso de EWS en Exchange](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Vea también


- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Las carpetas y elementos de EWS en Exchange](folders-and-items-in-ews-in-exchange.md)
    

