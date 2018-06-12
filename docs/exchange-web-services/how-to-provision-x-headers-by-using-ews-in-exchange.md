---
title: Encabezados x de aprovisionamiento mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 45a99a14-a85f-47f8-af48-18eb6c6cc230
description: Obtenga información sobre cómo aprovisionar los encabezados x para un buzón de correo mediante el uso de la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: de572764921da432cfa203b3dcf166d1d34dd0cd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763157"
---
# <a name="provision-x-headers-by-using-ews-in-exchange"></a>Encabezados x de aprovisionamiento mediante el uso de EWS en Exchange

Obtenga información sobre cómo aprovisionar los encabezados x para un buzón de correo mediante el uso de la API administrada de EWS o EWS en Exchange.
  
Encabezados X son los encabezados no estándar que se agregan a la colección de encabezado de un correo electrónico para transmitir la información. Por ejemplo, intercambiar mensajes de las marcas con el encabezado **X-MS-Exchange-organización-SCL** para indicar el nivel de con nivel de confianza de correo no deseado (SCL) atribuido para el correo electrónico. Los clientes de correo electrónico como Outlook puede usar esa información para determinar qué tipo de acción que debe realizarse en el correo electrónico (por ejemplo, Outlook puede evitar que las imágenes muestre a menos que el usuario realiza una acción). 
  
Exchange agrega entrantes a los encabezados x para el esquema del buzón como una hora de la propiedad con nombre de la primera recibe un correo electrónico con ese encabezado de x. El valor de encabezado de x no se guarda en ese correo electrónico primera; Sin embargo, se guarda en todos los siguientes mensajes de correo electrónico que incluyan el encabezado de x. Por este motivo, la aplicación debe aprovisionar a los encabezados x antes de esperar a usarlas. La asignación entre una propiedad con nombre y un encabezado x se produce en la entrega de transporte del correo electrónico para el buzón de correo. Esto significa que es necesario recibir el correo electrónico a través de entrega de transporte; simplemente no se puede guardar un correo electrónico que incluya el encabezado x a un buzón de correo para crear la asignación a una propiedad con nombre.
  
> [!NOTE]
> Si observa que no se está guardando encabezados x, determinar si un [agente de transporte](http://code.msdn.microsoft.com/Exchange-2013-Build-an-32f62f5a) o [firewall de encabezados](http://technet.microsoft.com/en-us/library/bb232136%28v=exchg.150%29.aspx) está filtrando los encabezados x antes de que se incluyen en el buzón de correo. 
  
## <a name="provision-an-x-header-by-using-the-ews-managed-api"></a>Aprovisionar un encabezado x mediante el uso de la API administrada de EWS
<a name="bk_example1"> </a>

En el ejemplo de código siguiente se muestra cómo utilizar el método de la API administrada de EWS [EmailMessage.Send](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx) para aprovisionar un encabezado x para un buzón de correo. En este ejemplo se da por supuesto que **servicio** se válida objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) y que el buzón de destino no ha superado la [cuota de las propiedades con nombre](http://technet.microsoft.com/en-us/library/bb851492%28v=EXCHG.80%29.aspx).
  
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

## <a name="provision-an-x-header-by-using-ews"></a>Aprovisionar un encabezado x mediante el uso de EWS
<a name="bk_example1"> </a>

En el ejemplo de código siguiente se muestra cómo usar la operación de EWS [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) para crear y enviar un correo electrónico para aprovisionar un buzón de correo con un encabezado x. Se trata de la solicitud XML que se envía por la API administrada de EWS cuando se [debe aprovisionar un encabezado x mediante el uso de la API administrada de EWS](#bk_example1).
  
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

La primera vez que aprovisione un encabezado x en Exchange Online, Exchange Online como parte de Office 365 o una versión local de Exchange a partir de Exchange Server 2010, el valor de un nuevo encabezado x personalizado no se escribirá al mensaje almacenado. Esto es debido a que el encabezado de x en primer lugar debe asignarse a una propiedad con nombre en el buzón del usuario. La asignación se produce tras la primera solicitud para agregar las propiedades con nombre. Cuando se produce una solicitud subsiguiente para crear la propiedad con nombre, la propiedad y el valor se almacenan en el mensaje. En Exchange 2007, la primera vez que se escribe un encabezado x en una base de datos de buzones de correo, se crea una asignación para el encabezado de x a una propiedad con nombre a través de la base de datos de buzón de correo. Cuando se produce una solicitud subsiguiente para crear la propiedad con nombre, el encabezado de x se procesan y se almacena para cualquier buzón de correo en la base de datos de Exchange 2007.
  
## <a name="next-steps"></a>Siguientes pasos
<a name="bk_example1"> </a>

En este artículo se muestra cómo aprovisionar un encabezado x para un solo buzón mediante el envío de un correo electrónico a un usuario. También puede aprovisionar un encabezado x para muchos usuarios mediante el [envío de un correo electrónico de lote a una lista de destinatarios](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md) en la organización el autor de la llamada. 
  
## <a name="see-also"></a>Ver también


- [Propiedades y propiedades extendidas de EWS en Exchange](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [Exchange 2013: Aprovisionar encabezados X personalizados mediante programación](http://code.msdn.microsoft.com/exchange/Exchange-2013-Provision-d4ef5719)
    
- [Propiedades, con nombre a los encabezados X y](http://blogs.technet.com/b/exchange/archive/2009/04/06/3407221.aspx)
    
- [Propiedades con nombre, Round 2: Lo que hay delante](http://blogs.technet.com/b/exchange/archive/2009/06/12/3407672.aspx)
    
- [Firewall de encabezado](http://technet.microsoft.com/en-us/library/bb232136%28v=exchg.150%29.aspx)
    
- [EWS, MIME y los encabezados de mensaje de Internet que faltan](http://msdn.microsoft.com/library/office/hh545614%28v=exchg.140%29.aspx)
    
- [Mensajes de correo electrónico de proceso por lotes mediante el uso de EWS en Exchange](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    

