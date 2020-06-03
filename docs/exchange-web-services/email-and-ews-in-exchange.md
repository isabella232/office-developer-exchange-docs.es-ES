---
title: Correo electrónico y EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 4d7bdb37-f7f1-409f-9749-f8bcde7dc52a
description: Descubra cómo trabajar con mensajes de correo electrónico, incluido cómo crear un correo electrónico y cómo realizar otras tareas relacionadas con el correo electrónico mediante la API administrada de EWS o EWS en Exchange.
localization_priority: Priority
ms.openlocfilehash: 323d9d2cc40aa86044a439ad53e53a4808916783
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455446"
---
# <a name="email-and-ews-in-exchange"></a>Correo electrónico y EWS en Exchange

Descubra cómo trabajar con mensajes de correo electrónico, incluido cómo crear un correo electrónico y cómo realizar otras tareas relacionadas con el correo electrónico mediante la API administrada de EWS o EWS en Exchange.
  

  
En esencia, Exchange trata de correo electrónico. Pero, ¿qué hace que un correo electrónico sea un correo electrónico? Bueno, los mensajes de correo electrónico son uno de los [elementos fuertemente tipados](folders-and-items-in-ews-in-exchange.md#bk_item) en Exchange, lo que significa que contienen un [conjunto determinado de propiedades](email-properties-and-elements-in-ews-in-exchange.md), incluso antes de que se envíen. Los mensajes de correo electrónico se representan mediante la clase [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) en la API administrada EWS y el elemento [Message](https://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) y sus elementos secundarios en EWS. 
  
En la API administrada de EWS, el objeto **EmailMessage** deriva del objeto [Item](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) . La clase **EmailMessage** amplía la clase de **elemento** proporcionando propiedades adicionales como [EmailMessage. Sender](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sender%28v=exchg.80%29.aspx) y [EmailMessage. IsRead](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.isread%28v=exchg.80%29.aspx), que ahora son comunes a casi todos los escenarios de mensajería. Cuando obtenga, actualice o elimine un mensaje de correo electrónico, en la mayoría de los casos puede hacerlo mediante el objeto **EmailMessage** o el objeto de **elemento** base, dependiendo de si las propiedades con las que está trabajando están en la [EmailMessageSchema](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessageschema%28v=exchg.80%29.aspx) o en la clase [ItemSchema](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemschema%28v=exchg.80%29.aspx) . La creación de elementos es diferente porque la clase de **elemento** no tiene un constructor, por lo que cuando esté creando un correo electrónico, usará el [constructor EmailMessage](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.emailmessage%28v=exchg.80%29.aspx) para crearlo y los métodos [EmailMessage. Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) o [EmailMessage. SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) para guardarlo, o enviarlo y guardarlo. 
  
De forma similar, en EWS, use la operación [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) con el elemento [Message](https://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) para crear un mensaje de correo electrónico. Para obtener, actualizar o eliminar correos electrónicos mediante EWS, el hecho de que el elemento que se modifica es un mensaje de correo electrónico no es importante, aparte del hecho de que hay propiedades adicionales disponibles en los mensajes de correo electrónico. Las mismas operaciones que se usan para otros elementos con establecimiento inflexible de tipos también se usan para los mensajes de correo electrónico. 
  
|**Tarea**|**Método de la API administrada de EWS**|**Operación de EWS**|
|:-----|:-----|:-----|
|Crear  <br/> |[EmailMessage. Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|Obtener  <br/> |[EmailMessage. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) <br/> |
|Actualizar  <br/> |[Item. Update](https://msdn.microsoft.com/library/dd635915%28v=exchg.80%29.aspx) <br/> |[UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Eliminar  <br/> |[Item. Delete](https://msdn.microsoft.com/library/dd635072%28v=exchg.80%29.aspx) <br/> |[DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
   
Como los mensajes de correo electrónico son simplemente [elementos con establecimiento inflexible de tipos](folders-and-items-in-ews-in-exchange.md#bk_item), en algunos casos se trabaja con ellos de la misma forma que se [trabaja con elementos genéricos](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md). 
  
## <a name="create-an-email-message-by-using-the-ews-managed-api"></a>Crear un mensaje de correo electrónico mediante la API administrada de EWS
<a name="bk_createewsma"> </a>

Puede crear un mensaje de correo electrónico mediante el método [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) de la API administrada de EWS, como se muestra en el código del ejemplo siguiente. Tenga en cuenta que en el ejemplo solo se guarda el mensaje en la carpeta Borradores, no se envía el mensaje. Para obtener información sobre cómo enviar el mensaje o crear y enviar el mensaje en un solo paso, vea [enviar mensajes de correo electrónico mediante EWS en Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md).
  
En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange. 
  
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

## <a name="create-an-email-message-by-using-ews"></a>Crear un mensaje de correo electrónico mediante EWS
<a name="bk_createews"> </a>

Puede crear un mensaje de correo electrónico mediante la operación de [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) de EWS, como se muestra en el ejemplo siguiente. También es la solicitud XML que la API administrada de EWS envía cuando se [crea un mensaje de correo electrónico](#bk_createewsma). Tenga en cuenta que el siguiente ejemplo solo guarda el mensaje en la carpeta Borradores, pero no envía el mensaje. Para obtener información acerca de cómo enviar el mensaje o crear y enviar el mensaje en un ste, vea [Send email messages by Using EWS in Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

El servidor responde a la solicitud **CreateItem** con un mensaje [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que el correo electrónico se ha creado correctamente y el [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) del mensaje recién creado. 
  
## <a name="get-update-and-delete-an-email-message-by-using-the-ews-managed-api"></a>Obtener, actualizar y eliminar un mensaje de correo electrónico mediante la API administrada de EWS
<a name="bk_getewsma"> </a>

Puede usar la API administrada de EWS para obtener, actualizar o eliminar un mensaje de correo electrónico de la misma manera que realiza estas acciones en cualquier elemento genérico del almacén de Exchange. Para obtener más información, vea [trabajar con elementos de buzón de Exchange mediante EWS en Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md).
  
Si está actualizando un mensaje de correo electrónico, consulte [propiedades y elementos de correo electrónico de EWS en Exchange](email-properties-and-elements-in-ews-in-exchange.md) para obtener una lista de las propiedades de los mensajes de correo electrónico que se puede escribir. Para enviar un borrador de mensaje después de actualizarlo, vea [Enviar un borrador de mensaje de correo electrónico mediante la API administrada de EWS](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftewsma).
  
## <a name="get-update-and-delete-an-email-message-by-using-ews"></a>Obtener, actualizar y eliminar un mensaje de correo electrónico mediante EWS
<a name="bk_getews"> </a>

Puede usar EWS para obtener, actualizar y eliminar un mensaje de correo electrónico de la misma forma que realiza estas acciones en cualquier elemento genérico del almacén de Exchange. Para obtener más información, vea [trabajar con elementos de buzón de Exchange mediante EWS en Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md).
  
Si está actualizando un mensaje de correo electrónico, consulte [propiedades y elementos de correo electrónico de EWS en Exchange](email-properties-and-elements-in-ews-in-exchange.md) para obtener una lista de las propiedades de los mensajes de correo electrónico que se puede escribir. Para enviar un borrador de mensaje después de actualizarlo, vea [Enviar un borrador de mensaje de correo electrónico mediante EWS](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftews).
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_inthissection"> </a>

- [Propiedades y elementos de correo electrónico de EWS en Exchange](email-properties-and-elements-in-ews-in-exchange.md)
    
- [Enviar mensajes de correo electrónico mediante EWS en Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md)
    
- [Responder a mensajes de correo electrónico mediante EWS en Exchange](how-to-respond-to-email-messages-by-using-ews-in-exchange.md)
    
- [Mover y copiar mensajes de correo electrónico mediante EWS en Exchange](how-to-move-and-copy-email-messages-by-using-ews-in-exchange.md)
    
- [Trabajar con conversaciones mediante EWS en Exchange](how-to-work-with-conversations-by-using-ews-in-exchange.md)
    
- [Extraer una entidad de un mensaje de correo electrónico mediante EWS en Exchange](how-to-extract-an-entity-from-an-email-message-by-using-ews-in-exchange.md)
    
- [Procesar mensajes de correo electrónico en lotes mediante EWS en Exchange](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Vea también


- [Desarrollar clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Carpetas y elementos de EWS en Exchange](folders-and-items-in-ews-in-exchange.md)
    

