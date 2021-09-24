---
title: Aprovisionar encabezados x mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 45a99a14-a85f-47f8-af48-18eb6c6cc230
description: Obtenga información sobre cómo aprovisionar encabezados x para un buzón mediante la API administrada ews o EWS en Exchange.
ms.openlocfilehash: e60092e0d40d5815cdf3fd4ed588e2f74978c245
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521119"
---
# <a name="provision-x-headers-by-using-ews-in-exchange"></a>Aprovisionar encabezados x mediante EWS en Exchange

Obtenga información sobre cómo aprovisionar encabezados x para un buzón mediante la API administrada ews o EWS en Exchange.
  
Los encabezados X son encabezados no estándar que se agregan a la colección de encabezados de un correo electrónico para comunicar información. Por ejemplo, Exchange marca los mensajes con el encabezado **X-MS-Exchange-Organization-SCL** para indicar el nivel de confianza de correo no deseado (SCL) atribuido al correo electrónico. Los clientes de correo electrónico como Outlook pueden usar esa información para determinar qué tipo de acción realizar en el correo electrónico (por ejemplo, Outlook puede impedir que se muestren imágenes a menos que el usuario haga una acción). 
  
Exchange agrega encabezados x entrantes al esquema de buzón como una propiedad con nombre la primera vez que recibe un correo electrónico con ese encabezado x. El valor del encabezado x no se guarda en ese primer correo electrónico; sin embargo, se guarda en todos los correos electrónicos posteriores que incluyen el encabezado x. Por este motivo, la aplicación debe aprovisionar encabezados x antes de esperar usarlos. La asignación entre una propiedad con nombre y un encabezado X se produce en la entrega de transporte del correo electrónico al buzón. Esto significa que debe recibir el correo electrónico a través de la entrega de transporte; no puede guardar un correo electrónico que incluya el encabezado x en un buzón para crear la asignación a una propiedad con nombre.
  
> [!NOTE]
> Si encuentra que los encabezados x no se [](https://code.msdn.microsoft.com/Exchange-2013-Build-an-32f62f5a) guardan, determine si un agente de transporte o [firewall](https://technet.microsoft.com/library/bb232136%28v=exchg.150%29.aspx) de encabezado está filtrando los encabezados x antes de que lleguen al buzón. r
  
## <a name="provision-an-x-header-by-using-the-ews-managed-api"></a>Aprovisionar un encabezado x mediante la API administrada ews
<a name="bk_example1"> </a>

En el siguiente ejemplo de código se muestra cómo usar el método [EmailMessage.Send](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx) de la API administrada ews para aprovisionar un encabezado x para un buzón. En este ejemplo se supone que **el servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el buzón de destino no ha excedido la cuota [de propiedades con nombre.](https://technet.microsoft.com/library/bb851492%28v=EXCHG.80%29.aspx)
  
```cs
private static void ProvisionCustomXHeaderByEmail(ExchangeService service)
{
    // Create a definition for an extended property that will represent a custom x-header. X-headers must be created in the
    // InternetHeaders property set. The x-header name must match the name of the x-header sent in the subsequent emails so
    // the x-header and value are saved on the email.
    ExtendedPropertyDefinition xExperimentalHeader = new ExtendedPropertyDefinition(DefaultExtendedPropertySet.InternetHeaders,
                                                                                            "X-Experimental",
                                                                                            MapiPropertyType.String);
    // Create an item that is used to provision the custom x-header.
    EmailMessage email = new EmailMessage(service);
    email.ToRecipients.Add("user@contoso.com");
    email.SetExtendedProperty(xExperimentalHeader, "Provision X-Experimental Internet message header");
    try
    {
        // The mapping of the named property happens in transport delivery.
        email.Send();
        if (service.ServerInfo.MajorVersion == 12)
        {
            Console.WriteLine("Provisioned the X-Experimental across the mailbox database that hosts the user's mailbox.");
        }
        else // For versions of Exchange starting with Exchange 2010
        {
            Console.WriteLine("Provisioned the X-Experimental for the user's mailbox. You will need to run this " +
                                "for each mailbox that needs to process this x-header.");
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error: {0}", ex.Message);
    }
}
```

## <a name="provision-an-x-header-by-using-ews"></a>Aprovisionar un encabezado x mediante EWS
<a name="bk_example1"> </a>

En el siguiente ejemplo de código se muestra cómo usar la operación [CreateItem de](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS para crear y enviar un correo electrónico para aprovisionar un buzón con un encabezado x. Esta es la solicitud XML que envía la API administrada ews al aprovisionar un encabezado x mediante la [API administrada ews](#bk_example1).
  
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
    <m:CreateItem MessageDisposition="SendOnly">
      <m:Items>
        <t:Message>
          <t:ExtendedProperty>
            <t:ExtendedFieldURI DistinguishedPropertySetId="InternetHeaders"
                                PropertyName="X-Experimental"
                                PropertyType="String" />
            <t:Value>Provision X-Experimental Internet message header</t:Value>
          </t:ExtendedProperty>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>user@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>

```

## <a name="version-differences"></a>Diferencias de versión
<a name="bk_example1"> </a>

La primera vez que aprovisiona un encabezado x en Exchange Online, Exchange Online como parte de Office 365 o una versión local de Exchange a partir de Exchange Server 2010, el valor de un nuevo encabezado x personalizado no se escribirá en el mensaje almacenado. Esto se debe a que el encabezado x debe asignarse primero a una propiedad con nombre en el buzón del usuario. La asignación se produce tras la primera solicitud para agregar las propiedades con nombre. Cuando se produce una solicitud posterior para crear la propiedad con nombre, la propiedad y el valor se almacenan en el mensaje. En Exchange 2007, la primera vez que se escribe un encabezado X en una base de datos de buzones de correo, se crea una asignación para el encabezado x a una propiedad con nombre en toda la base de datos de buzones. Cuando se produce una solicitud posterior para crear la propiedad con nombre, el encabezado x se procesa y almacena para cualquier buzón de la base de datos Exchange 2007.
  
## <a name="next-steps"></a>Pasos siguientes
<a name="bk_example1"> </a>

En este artículo se muestra cómo aprovisionar un encabezado x para un único buzón enviando un correo electrónico a un usuario. También puede aprovisionar un encabezado x para muchos usuarios enviando un correo electrónico por [lotes a](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md) una lista de destinatarios de la organización del autor de la llamada. 
  
## <a name="see-also"></a>Ver también


- [Propiedades y propiedades extendidas de EWS en Exchange](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [Exchange 2013: Aprovisionar encabezados X personalizados mediante programación](https://code.msdn.microsoft.com/exchange/Exchange-2013-Provision-d4ef5719)
    
- [Propiedades con nombre, encabezados X y you](https://blogs.technet.com/b/exchange/archive/2009/04/06/3407221.aspx)
    
- [Propiedades con nombre, Ronda 2: Lo que queda por delante](https://blogs.technet.com/b/exchange/archive/2009/06/12/3407672.aspx)
    
- [Firewall de encabezado](https://technet.microsoft.com/library/bb232136%28v=exchg.150%29.aspx)
    
- [EWS, MIME y los encabezados de mensajes de Internet que faltan](https://msdn.microsoft.com/library/office/hh545614%28v=exchg.140%29.aspx)
    
- [Procesar mensajes de correo electrónico en lotes mediante EWS en Exchange](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    

