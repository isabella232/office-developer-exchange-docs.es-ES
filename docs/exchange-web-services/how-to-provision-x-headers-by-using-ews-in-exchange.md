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
# <a name="provision-x-headers-by-using-ews-in-exchange"></a><span data-ttu-id="82ee6-103">Encabezados x de aprovisionamiento mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="82ee6-103">Provision x-headers by using EWS in Exchange</span></span>

<span data-ttu-id="82ee6-104">Obtenga información sobre cómo aprovisionar los encabezados x para un buzón de correo mediante el uso de la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="82ee6-104">Learn how to provision x-headers for a mailbox by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="82ee6-105">Encabezados X son los encabezados no estándar que se agregan a la colección de encabezado de un correo electrónico para transmitir la información.</span><span class="sxs-lookup"><span data-stu-id="82ee6-105">X-headers are non-standard headers that are added to the header collection of an email to communicate information.</span></span> <span data-ttu-id="82ee6-106">Por ejemplo, intercambiar mensajes de las marcas con el encabezado **X-MS-Exchange-organización-SCL** para indicar el nivel de con nivel de confianza de correo no deseado (SCL) atribuido para el correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="82ee6-106">For example, Exchange stamps messages with the **X-MS-Exchange-Organization-SCL** header to indicate the spam confidence level (SCL) attributed to the email.</span></span> <span data-ttu-id="82ee6-107">Los clientes de correo electrónico como Outlook puede usar esa información para determinar qué tipo de acción que debe realizarse en el correo electrónico (por ejemplo, Outlook puede evitar que las imágenes muestre a menos que el usuario realiza una acción).</span><span class="sxs-lookup"><span data-stu-id="82ee6-107">Email clients like Outlook can use that information to determine what type of action to take on the email (for example, Outlook can prevent images from displaying unless the user takes an action).</span></span> 
  
<span data-ttu-id="82ee6-108">Exchange agrega entrantes a los encabezados x para el esquema del buzón como una hora de la propiedad con nombre de la primera recibe un correo electrónico con ese encabezado de x.</span><span class="sxs-lookup"><span data-stu-id="82ee6-108">Exchange adds incoming x-headers to the mailbox schema as a named property the first time it receives an email with that x-header.</span></span> <span data-ttu-id="82ee6-109">El valor de encabezado de x no se guarda en ese correo electrónico primera; Sin embargo, se guarda en todos los siguientes mensajes de correo electrónico que incluyan el encabezado de x.</span><span class="sxs-lookup"><span data-stu-id="82ee6-109">The x-header value is not saved on that first email; however, it is saved on all subsequent emails that include the x-header.</span></span> <span data-ttu-id="82ee6-110">Por este motivo, la aplicación debe aprovisionar a los encabezados x antes de esperar a usarlas.</span><span class="sxs-lookup"><span data-stu-id="82ee6-110">For this reason, your application should provision x-headers before you expect to use them.</span></span> <span data-ttu-id="82ee6-111">La asignación entre una propiedad con nombre y un encabezado x se produce en la entrega de transporte del correo electrónico para el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="82ee6-111">The mapping between a named property and an x-header occurs in the transport delivery of the email to the mailbox.</span></span> <span data-ttu-id="82ee6-112">Esto significa que es necesario recibir el correo electrónico a través de entrega de transporte; simplemente no se puede guardar un correo electrónico que incluya el encabezado x a un buzón de correo para crear la asignación a una propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="82ee6-112">This means that you need to receive the email via transport delivery; you cannot just save an email that includes the x-header to a mailbox to create the mapping to a named property.</span></span>
  
> [!NOTE]
> <span data-ttu-id="82ee6-113">Si observa que no se está guardando encabezados x, determinar si un [agente de transporte](http://code.msdn.microsoft.com/Exchange-2013-Build-an-32f62f5a) o [firewall de encabezados](http://technet.microsoft.com/en-us/library/bb232136%28v=exchg.150%29.aspx) está filtrando los encabezados x antes de que se incluyen en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="82ee6-113">If you find that x-headers aren't being saved, determine whether a [transport agent](http://code.msdn.microsoft.com/Exchange-2013-Build-an-32f62f5a) or [header firewall](http://technet.microsoft.com/en-us/library/bb232136%28v=exchg.150%29.aspx) is filtering out your x-headers before they get to the mailbox.</span></span> 
  
## <a name="provision-an-x-header-by-using-the-ews-managed-api"></a><span data-ttu-id="82ee6-114">Aprovisionar un encabezado x mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="82ee6-114">Provision an x-header by using the EWS Managed API</span></span>
<span data-ttu-id="82ee6-115"><a name="bk_example1"> </a></span><span class="sxs-lookup"><span data-stu-id="82ee6-115"></span></span>

<span data-ttu-id="82ee6-116">En el ejemplo de código siguiente se muestra cómo utilizar el método de la API administrada de EWS [EmailMessage.Send](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx) para aprovisionar un encabezado x para un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="82ee6-116">The following code example shows how to use the EWS Managed API [EmailMessage.Send](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx) method to provision an x-header for a mailbox.</span></span> <span data-ttu-id="82ee6-117">En este ejemplo se da por supuesto que **servicio** se válida objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) y que el buzón de destino no ha superado la [cuota de las propiedades con nombre](http://technet.microsoft.com/en-us/library/bb851492%28v=EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="82ee6-117">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the target mailbox hasn't exceeded the [quota for named properties](http://technet.microsoft.com/en-us/library/bb851492%28v=EXCHG.80%29.aspx).</span></span>
  
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

## <a name="provision-an-x-header-by-using-ews"></a><span data-ttu-id="82ee6-118">Aprovisionar un encabezado x mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="82ee6-118">Provision an x-header by using EWS</span></span>
<span data-ttu-id="82ee6-119"><a name="bk_example1"> </a></span><span class="sxs-lookup"><span data-stu-id="82ee6-119"></span></span>

<span data-ttu-id="82ee6-120">En el ejemplo de código siguiente se muestra cómo usar la operación de EWS [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) para crear y enviar un correo electrónico para aprovisionar un buzón de correo con un encabezado x.</span><span class="sxs-lookup"><span data-stu-id="82ee6-120">The following code example shows how to use the EWS [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) operation to create and send an email to provision a mailbox with an x-header.</span></span> <span data-ttu-id="82ee6-121">Se trata de la solicitud XML que se envía por la API administrada de EWS cuando se [debe aprovisionar un encabezado x mediante el uso de la API administrada de EWS](#bk_example1).</span><span class="sxs-lookup"><span data-stu-id="82ee6-121">This is the XML request that is sent by the EWS Managed API when you [Provision an x-header by using the EWS Managed API](#bk_example1).</span></span>
  
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

## <a name="version-differences"></a><span data-ttu-id="82ee6-122">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="82ee6-122">Version differences</span></span>
<span data-ttu-id="82ee6-123"><a name="bk_example1"> </a></span><span class="sxs-lookup"><span data-stu-id="82ee6-123"></span></span>

<span data-ttu-id="82ee6-124">La primera vez que aprovisione un encabezado x en Exchange Online, Exchange Online como parte de Office 365 o una versión local de Exchange a partir de Exchange Server 2010, el valor de un nuevo encabezado x personalizado no se escribirá al mensaje almacenado.</span><span class="sxs-lookup"><span data-stu-id="82ee6-124">The first time that you provision an x-header in Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange Server 2010, the value of a new custom x-header will not be written to the stored message.</span></span> <span data-ttu-id="82ee6-125">Esto es debido a que el encabezado de x en primer lugar debe asignarse a una propiedad con nombre en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="82ee6-125">This is because the x-header must first be mapped to a named property in the user's mailbox.</span></span> <span data-ttu-id="82ee6-126">La asignación se produce tras la primera solicitud para agregar las propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="82ee6-126">The mapping occurs upon the first request to add the named properties.</span></span> <span data-ttu-id="82ee6-127">Cuando se produce una solicitud subsiguiente para crear la propiedad con nombre, la propiedad y el valor se almacenan en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="82ee6-127">When a subsequent request to create the named property occurs, the property and value are stored on the message.</span></span> <span data-ttu-id="82ee6-128">En Exchange 2007, la primera vez que se escribe un encabezado x en una base de datos de buzones de correo, se crea una asignación para el encabezado de x a una propiedad con nombre a través de la base de datos de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="82ee6-128">In Exchange 2007, the first time an x-header is written to a mailbox database, a mapping is created for the x-header to a named property across the mailbox database.</span></span> <span data-ttu-id="82ee6-129">Cuando se produce una solicitud subsiguiente para crear la propiedad con nombre, el encabezado de x se procesan y se almacena para cualquier buzón de correo en la base de datos de Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="82ee6-129">When a subsequent request to create the named property occurs, the x-header is processed and stored for any mailbox in the Exchange 2007 database.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="82ee6-130">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="82ee6-130">Next steps</span></span>
<span data-ttu-id="82ee6-131"><a name="bk_example1"> </a></span><span class="sxs-lookup"><span data-stu-id="82ee6-131"></span></span>

<span data-ttu-id="82ee6-132">En este artículo se muestra cómo aprovisionar un encabezado x para un solo buzón mediante el envío de un correo electrónico a un usuario.</span><span class="sxs-lookup"><span data-stu-id="82ee6-132">This article shows you how to provision an x-header for a single mailbox by sending an email to a user.</span></span> <span data-ttu-id="82ee6-133">También puede aprovisionar un encabezado x para muchos usuarios mediante el [envío de un correo electrónico de lote a una lista de destinatarios](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md) en la organización el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="82ee6-133">You can also provision an x-header for many users by [sending a batch email to a list of recipients](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md) in the caller's organization.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="82ee6-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="82ee6-134">See also</span></span>


- [<span data-ttu-id="82ee6-135">Propiedades y propiedades extendidas de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="82ee6-135">Properties and extended properties in EWS in Exchange</span></span>](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [<span data-ttu-id="82ee6-136">Exchange 2013: Aprovisionar encabezados X personalizados mediante programación</span><span class="sxs-lookup"><span data-stu-id="82ee6-136">Exchange 2013: Provision custom X-headers programmatically</span></span>](http://code.msdn.microsoft.com/exchange/Exchange-2013-Provision-d4ef5719)
    
- [<span data-ttu-id="82ee6-137">Propiedades, con nombre a los encabezados X y</span><span class="sxs-lookup"><span data-stu-id="82ee6-137">Named Properties, X-Headers, and You</span></span>](http://blogs.technet.com/b/exchange/archive/2009/04/06/3407221.aspx)
    
- [<span data-ttu-id="82ee6-138">Propiedades con nombre, Round 2: Lo que hay delante</span><span class="sxs-lookup"><span data-stu-id="82ee6-138">Named Properties, Round 2: What lies Ahead</span></span>](http://blogs.technet.com/b/exchange/archive/2009/06/12/3407672.aspx)
    
- [<span data-ttu-id="82ee6-139">Firewall de encabezado</span><span class="sxs-lookup"><span data-stu-id="82ee6-139">Header Firewall</span></span>](http://technet.microsoft.com/en-us/library/bb232136%28v=exchg.150%29.aspx)
    
- [<span data-ttu-id="82ee6-140">EWS, MIME y los encabezados de mensaje de Internet que faltan</span><span class="sxs-lookup"><span data-stu-id="82ee6-140">EWS, MIME, and the missing Internet message headers</span></span>](http://msdn.microsoft.com/library/office/hh545614%28v=exchg.140%29.aspx)
    
- [<span data-ttu-id="82ee6-141">Mensajes de correo electrónico de proceso por lotes mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="82ee6-141">Process email messages in batches by using EWS in Exchange</span></span>](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    

