---
title: Aprovisionar encabezados x mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 45a99a14-a85f-47f8-af48-18eb6c6cc230
description: Obtenga información sobre cómo aprovisionar encabezados x para un buzón de correo mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 409ddb944bbac7a60242de39cdf7ae13b17cc76a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527771"
---
# <a name="provision-x-headers-by-using-ews-in-exchange"></a><span data-ttu-id="01655-103">Aprovisionar encabezados x mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="01655-103">Provision x-headers by using EWS in Exchange</span></span>

<span data-ttu-id="01655-104">Obtenga información sobre cómo aprovisionar encabezados x para un buzón de correo mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="01655-104">Learn how to provision x-headers for a mailbox by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="01655-105">Los encabezados X son encabezados no estándar que se agregan a la colección de encabezados de un correo electrónico para comunicar la información.</span><span class="sxs-lookup"><span data-stu-id="01655-105">X-headers are non-standard headers that are added to the header collection of an email to communicate information.</span></span> <span data-ttu-id="01655-106">Por ejemplo, Exchange marca los mensajes con el encabezado **X-MS-Exchange-Organization-SCL** para indicar el nivel de confianza contra correo no deseado (SCL) atribuido al correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="01655-106">For example, Exchange stamps messages with the **X-MS-Exchange-Organization-SCL** header to indicate the spam confidence level (SCL) attributed to the email.</span></span> <span data-ttu-id="01655-107">Los clientes de correo electrónico como Outlook pueden usar esta información para determinar el tipo de acción que se realizará en el correo electrónico (por ejemplo, Outlook puede impedir que se muestren las imágenes a menos que el usuario realice alguna acción).</span><span class="sxs-lookup"><span data-stu-id="01655-107">Email clients like Outlook can use that information to determine what type of action to take on the email (for example, Outlook can prevent images from displaying unless the user takes an action).</span></span> 
  
<span data-ttu-id="01655-108">Exchange agrega encabezados x entrantes al esquema de buzones como una propiedad con nombre la primera vez que recibe un correo electrónico con ese encabezado x.</span><span class="sxs-lookup"><span data-stu-id="01655-108">Exchange adds incoming x-headers to the mailbox schema as a named property the first time it receives an email with that x-header.</span></span> <span data-ttu-id="01655-109">El valor del encabezado x no se guarda en ese primer correo electrónico; sin embargo, se guarda en todos los correos electrónicos posteriores que incluyan el encabezado x.</span><span class="sxs-lookup"><span data-stu-id="01655-109">The x-header value is not saved on that first email; however, it is saved on all subsequent emails that include the x-header.</span></span> <span data-ttu-id="01655-110">Por este motivo, la aplicación debe aprovisionar encabezados x antes de que se espere usarlos.</span><span class="sxs-lookup"><span data-stu-id="01655-110">For this reason, your application should provision x-headers before you expect to use them.</span></span> <span data-ttu-id="01655-111">La asignación entre una propiedad con nombre y un encabezado x se produce en la entrega de transporte del correo electrónico al buzón.</span><span class="sxs-lookup"><span data-stu-id="01655-111">The mapping between a named property and an x-header occurs in the transport delivery of the email to the mailbox.</span></span> <span data-ttu-id="01655-112">Esto significa que debe recibir el correo electrónico a través de la entrega del transporte; no se puede guardar simplemente un correo electrónico que incluya el encabezado x en un buzón para crear la asignación a una propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="01655-112">This means that you need to receive the email via transport delivery; you cannot just save an email that includes the x-header to a mailbox to create the mapping to a named property.</span></span>
  
> [!NOTE]
> <span data-ttu-id="01655-113">Si observa que los encabezados x no se están guardando, determine si un [agente de transporte](https://code.msdn.microsoft.com/Exchange-2013-Build-an-32f62f5a) o un firewall de [encabezado](https://technet.microsoft.com/library/bb232136%28v=exchg.150%29.aspx) filtra los encabezados x antes de que lleguen al buzón.</span><span class="sxs-lookup"><span data-stu-id="01655-113">If you find that x-headers aren't being saved, determine whether a [transport agent](https://code.msdn.microsoft.com/Exchange-2013-Build-an-32f62f5a) or [header firewall](https://technet.microsoft.com/library/bb232136%28v=exchg.150%29.aspx) is filtering out your x-headers before they get to the mailbox.</span></span> <span data-ttu-id="01655-114">r</span><span class="sxs-lookup"><span data-stu-id="01655-114">r</span></span>
  
## <a name="provision-an-x-header-by-using-the-ews-managed-api"></a><span data-ttu-id="01655-115">Aprovisionamiento de un encabezado x mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="01655-115">Provision an x-header by using the EWS Managed API</span></span>
<span data-ttu-id="01655-116"><a name="bk_example1"> </a></span><span class="sxs-lookup"><span data-stu-id="01655-116"><a name="bk_example1"> </a></span></span>

<span data-ttu-id="01655-117">En el siguiente ejemplo de código se muestra cómo usar el método [EmailMessage. Send](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx) de la API administrada de EWS para aprovisionar un encabezado x para un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="01655-117">The following code example shows how to use the EWS Managed API [EmailMessage.Send](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx) method to provision an x-header for a mailbox.</span></span> <span data-ttu-id="01655-118">En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el buzón de destino no ha excedido la [cuota para las propiedades con nombre](https://technet.microsoft.com/library/bb851492%28v=EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="01655-118">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the target mailbox hasn't exceeded the [quota for named properties](https://technet.microsoft.com/library/bb851492%28v=EXCHG.80%29.aspx).</span></span>
  
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

## <a name="provision-an-x-header-by-using-ews"></a><span data-ttu-id="01655-119">Aprovisionamiento de un encabezado x mediante EWS</span><span class="sxs-lookup"><span data-stu-id="01655-119">Provision an x-header by using EWS</span></span>
<span data-ttu-id="01655-120"><a name="bk_example1"> </a></span><span class="sxs-lookup"><span data-stu-id="01655-120"><a name="bk_example1"> </a></span></span>

<span data-ttu-id="01655-121">En el siguiente ejemplo de código se muestra cómo usar la operación de EWS [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) para crear y enviar un correo electrónico para aprovisionar un buzón con un encabezado x.</span><span class="sxs-lookup"><span data-stu-id="01655-121">The following code example shows how to use the EWS [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) operation to create and send an email to provision a mailbox with an x-header.</span></span> <span data-ttu-id="01655-122">Esta es la solicitud XML que la API administrada de EWS envía al [aprovisionar un encabezado x mediante la API administrada de EWS](#bk_example1).</span><span class="sxs-lookup"><span data-stu-id="01655-122">This is the XML request that is sent by the EWS Managed API when you [Provision an x-header by using the EWS Managed API](#bk_example1).</span></span>
  
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

## <a name="version-differences"></a><span data-ttu-id="01655-123">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="01655-123">Version differences</span></span>
<span data-ttu-id="01655-124"><a name="bk_example1"> </a></span><span class="sxs-lookup"><span data-stu-id="01655-124"><a name="bk_example1"> </a></span></span>

<span data-ttu-id="01655-125">La primera vez que aprovisione un encabezado x en Exchange Online, Exchange online como parte de Office 365 o una versión local de Exchange a partir de Exchange Server 2010, el valor de un nuevo encabezado x personalizado no se escribirá en el mensaje almacenado.</span><span class="sxs-lookup"><span data-stu-id="01655-125">The first time that you provision an x-header in Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange Server 2010, the value of a new custom x-header will not be written to the stored message.</span></span> <span data-ttu-id="01655-126">Esto se debe a que el encabezado x primero debe asignarse a una propiedad con nombre en el buzón de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="01655-126">This is because the x-header must first be mapped to a named property in the user's mailbox.</span></span> <span data-ttu-id="01655-127">La asignación se produce después de la primera solicitud para agregar las propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="01655-127">The mapping occurs upon the first request to add the named properties.</span></span> <span data-ttu-id="01655-128">Cuando se produce una solicitud posterior para crear la propiedad con nombre, la propiedad y el valor se almacenan en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="01655-128">When a subsequent request to create the named property occurs, the property and value are stored on the message.</span></span> <span data-ttu-id="01655-129">En Exchange 2007, la primera vez que se escribe un encabezado x en una base de datos de buzones de correo, se crea una asignación para el encabezado x a una propiedad con nombre en la base de datos de buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="01655-129">In Exchange 2007, the first time an x-header is written to a mailbox database, a mapping is created for the x-header to a named property across the mailbox database.</span></span> <span data-ttu-id="01655-130">Cuando se produce una solicitud posterior para crear la propiedad con nombre, el encabezado x se procesa y se almacena para cualquier buzón de correo en la base de datos de Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="01655-130">When a subsequent request to create the named property occurs, the x-header is processed and stored for any mailbox in the Exchange 2007 database.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="01655-131">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="01655-131">Next steps</span></span>
<span data-ttu-id="01655-132"><a name="bk_example1"> </a></span><span class="sxs-lookup"><span data-stu-id="01655-132"><a name="bk_example1"> </a></span></span>

<span data-ttu-id="01655-133">En este artículo se muestra cómo aprovisionar un encabezado x para un solo buzón mediante el envío de un correo electrónico a un usuario.</span><span class="sxs-lookup"><span data-stu-id="01655-133">This article shows you how to provision an x-header for a single mailbox by sending an email to a user.</span></span> <span data-ttu-id="01655-134">También puede aprovisionar un encabezado x para muchos usuarios mediante el [envío de un correo electrónico de lote a una lista de destinatarios](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md) de la organización del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="01655-134">You can also provision an x-header for many users by [sending a batch email to a list of recipients](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md) in the caller's organization.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="01655-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="01655-135">See also</span></span>


- [<span data-ttu-id="01655-136">Propiedades y propiedades extendidas de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="01655-136">Properties and extended properties in EWS in Exchange</span></span>](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [<span data-ttu-id="01655-137">Exchange 2013: aprovisionar encabezados X personalizados mediante programación</span><span class="sxs-lookup"><span data-stu-id="01655-137">Exchange 2013: Provision custom X-headers programmatically</span></span>](https://code.msdn.microsoft.com/exchange/Exchange-2013-Provision-d4ef5719)
    
- [<span data-ttu-id="01655-138">Propiedades con nombre, encabezados X y se</span><span class="sxs-lookup"><span data-stu-id="01655-138">Named Properties, X-Headers, and You</span></span>](https://blogs.technet.com/b/exchange/archive/2009/04/06/3407221.aspx)
    
- [<span data-ttu-id="01655-139">Propiedades con nombre, 2: significado hacia delante</span><span class="sxs-lookup"><span data-stu-id="01655-139">Named Properties, Round 2: What lies Ahead</span></span>](https://blogs.technet.com/b/exchange/archive/2009/06/12/3407672.aspx)
    
- [<span data-ttu-id="01655-140">Firewall de encabezado</span><span class="sxs-lookup"><span data-stu-id="01655-140">Header Firewall</span></span>](https://technet.microsoft.com/library/bb232136%28v=exchg.150%29.aspx)
    
- [<span data-ttu-id="01655-141">EWS, MIME y los encabezados de mensajes de Internet que faltan</span><span class="sxs-lookup"><span data-stu-id="01655-141">EWS, MIME, and the missing Internet message headers</span></span>](https://msdn.microsoft.com/library/office/hh545614%28v=exchg.140%29.aspx)
    
- [<span data-ttu-id="01655-142">Procesar mensajes de correo electrónico en lotes mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="01655-142">Process email messages in batches by using EWS in Exchange</span></span>](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    

