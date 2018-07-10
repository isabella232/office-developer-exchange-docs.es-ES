---
title: Expandir grupos de distribución mediante el uso de EWS en Exchange 2013
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 25ee84e7-63bc-4f51-9b7d-e7f46fd574d5
description: Obtenga información sobre cómo expandir un grupo de distribución mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 0f9186fb71b3005c71a70e89aafb674ae15e4814
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763058"
---
# <a name="expand-distribution-groups-by-using-ews-in-exchange-2013"></a><span data-ttu-id="94e1e-103">Expandir grupos de distribución mediante el uso de EWS en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="94e1e-103">Expand distribution groups by using EWS in Exchange 2013</span></span>

<span data-ttu-id="94e1e-104">Obtenga información sobre cómo expandir un grupo de distribución mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="94e1e-104">Learn how to expand a distribution group by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="94e1e-105">Puede usar el método de la API administrada de EWS [ExchangeService.ExpandGroup](http://msdn.microsoft.com/es-es/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) o la operación de EWS [ExpandDL](http://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) para expandir un grupo de distribución para identificar a todos los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="94e1e-105">You can use the [ExchangeService.ExpandGroup](http://msdn.microsoft.com/es-es/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) EWS Managed API method or the [ExpandDL](http://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) EWS operation to expand a distribution group to identify all recipients.</span></span> 
  
<span data-ttu-id="94e1e-106">Debido a que el método [ExpandGroup](http://msdn.microsoft.com/es-es/library/office/ee344007%28v=exchg.80%29.aspx) está sobrecargado, puede llamar de varias maneras:</span><span class="sxs-lookup"><span data-stu-id="94e1e-106">Because the [ExpandGroup](http://msdn.microsoft.com/es-es/library/office/ee344007%28v=exchg.80%29.aspx) method is overloaded, you can call it in several ways:</span></span> 
  
- <span data-ttu-id="94e1e-107">[ExpandGroup(String)](http://msdn.microsoft.com/es-es/library/office/ee343988%28v=exchg.80%29.aspx) - expande un grupo identificado por una dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="94e1e-107">[ExpandGroup(String)](http://msdn.microsoft.com/es-es/library/office/ee343988%28v=exchg.80%29.aspx) - Expands a group identified by an SMTP address.</span></span> 
    
- <span data-ttu-id="94e1e-108">[ExpandGroup(EmailAddress)](http://msdn.microsoft.com/es-es/library/office/ee344007%28v=exchg.80%29.aspx) - expande un grupo identificado por una dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="94e1e-108">[ExpandGroup(EmailAddress)](http://msdn.microsoft.com/es-es/library/office/ee344007%28v=exchg.80%29.aspx) - Expands a group identified by an email address.</span></span> 
    
- <span data-ttu-id="94e1e-109">[ExpandGroup(ItemId)](http://msdn.microsoft.com/es-es/library/office/ee356407%28v=exchg.80%29.aspx) - expande un grupo identificado por un identificador de grupo.</span><span class="sxs-lookup"><span data-stu-id="94e1e-109">[ExpandGroup(ItemId)](http://msdn.microsoft.com/es-es/library/office/ee356407%28v=exchg.80%29.aspx) - Expands a group identified by a group ID.</span></span> 
    
- <span data-ttu-id="94e1e-110">[ExpanGroup (String, String)](http://msdn.microsoft.com/es-es/library/office/ee356468%28v=exchg.80%29.aspx) - expande un grupo identificado por una dirección SMTP y el tipo de distribución de esa dirección.</span><span class="sxs-lookup"><span data-stu-id="94e1e-110">[ExpanGroup(String, String)](http://msdn.microsoft.com/es-es/library/office/ee356468%28v=exchg.80%29.aspx) - Expands a group identified by an SMTP address and the routing type of that address.</span></span> 
    
## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews-managed-api"></a><span data-ttu-id="94e1e-111">Expanda un grupo de distribución universal o un grupo de seguridad mediante el uso de API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="94e1e-111">Expand a universal distribution group or security group by using EWS Managed API</span></span>
<span data-ttu-id="94e1e-112"><a name="bk_ExpandDGEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="94e1e-112"></span></span>

<span data-ttu-id="94e1e-113">En el ejemplo siguiente se muestra cómo expandir un grupo de distribución universal o un grupo de seguridad mediante el uso de una dirección de correo electrónico, que es el enfoque más sencillo.</span><span class="sxs-lookup"><span data-stu-id="94e1e-113">The following example shows how to expand a universal distribution group or security group by using an email address, which is the simplest approach.</span></span> <span data-ttu-id="94e1e-114">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="94e1e-114">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
// Return the expanded group.
   ExpandGroupResults myGroupMembers = service.ExpandGroup("employees@contoso.com");
// Display the group members.
   foreach (EmailAddress address in myGroupMembers.Members)
   {
      Console.WriteLine("Email Address: {0}", address);
   }

```

<span data-ttu-id="94e1e-115">Eso no es una gran cantidad de código, pero también es bastante básica y es posible que no dar a lo está buscando.</span><span class="sxs-lookup"><span data-stu-id="94e1e-115">That's not a lot of code, but it's also pretty basic and might not give you what you are looking for.</span></span> <span data-ttu-id="94e1e-116">Por lo que vamos a dar un paso más.</span><span class="sxs-lookup"><span data-stu-id="94e1e-116">So let's take it a step further.</span></span> <span data-ttu-id="94e1e-117">Grupos de distribución también pueden contener otros grupos de distribución.</span><span class="sxs-lookup"><span data-stu-id="94e1e-117">Distribution groups can also contain other distribution groups.</span></span> <span data-ttu-id="94e1e-118">Simplemente expandirlo se de resultados de la dirección de correo electrónico de los grupos de distribución contenido, pero no los expandir.</span><span class="sxs-lookup"><span data-stu-id="94e1e-118">Simply expanding it will output the email address of the contained distribution groups but not expand them.</span></span> <span data-ttu-id="94e1e-119">Mediante la adición de unas pocas líneas más de código, se puede de forma recursiva expandir los grupos para cada contacto de salida.</span><span class="sxs-lookup"><span data-stu-id="94e1e-119">By adding a few more lines of code, you can recursively expand the groups to output every contact.</span></span>
  
```cs
private static void ExpandDistributionLists(ExchangeService service, string Mailbox)
{
   // Return the expanded group.
      ExpandGroupResults myGroupMembers = service.ExpandGroup(Mailbox);
   // Display the group members.
      foreach (EmailAddress address in myGroupMembers.Members)
      {
         // Check to see if the mailbox is a public group
         if (address.MailboxType == MailboxType.PublicGroup)
      {
         // Call the function again to expand the contained
         // distribution group.
         ExpandDistributionLists(service, address.Address);
      }
      else
      {
         // Output the address of the mailbox.
         Console.WriteLine("Email Address: {0}", address);
      }
   }
}

```

<span data-ttu-id="94e1e-120">Y ahora se puede llamar a esta función nuevo el su código y expanda todos los grupos de distribución pública incluidos en el primero de ellos.</span><span class="sxs-lookup"><span data-stu-id="94e1e-120">And now you can call this new function in the your code and expand all the public distribution groups contained within the first one.</span></span>
  
```cs
ExpandDistributionLists(service, "employees@contoso.com");

```

## <a name="expand-a-contact-group-by-using-ews-managed-api"></a><span data-ttu-id="94e1e-121">Expanda un grupo de contactos mediante el uso de API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="94e1e-121">Expand a contact group by using EWS Managed API</span></span>
<span data-ttu-id="94e1e-122"><a name="bk_ExpandDGEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="94e1e-122"></span></span>

<span data-ttu-id="94e1e-123">Debido a que los grupos de contactos no tiene una dirección de correo electrónico asociadas, necesita expandir el grupo basado en el ItemId mediante el método [ExpandGroup(ItemId)](http://msdn.microsoft.com/es-es/library/office/ee356407%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="94e1e-123">Because contact groups do not have an associated email address, you need to expand the group based on the ItemId by using the [ExpandGroup(ItemId)](http://msdn.microsoft.com/es-es/library/office/ee356407%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="94e1e-124">Puede crear una función, tal como se muestra en el ejemplo anterior y cambie el segundo tipo de parámetro de una cadena a un [ItemId](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="94e1e-124">You can create a function, as shown in the previous example, and change the second parameter type from a string to an [ItemId](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx).</span></span>
  
```cs
private static void ExpandContactGroup(ExchangeService service, ItemId groupID)
{
   // Return the expanded group.
      ExpandGroupResults myGroupMembers = service.ExpandGroup(groupID);
   // Display the group members.
      foreach (EmailAddress address in myGroupMembers.Members)
      {
         if (address.MailboxType == MailboxType.PublicGroup)
         {
            ExpandDistributionLists(service, address.Address);
         }
         else
         {
            Console.WriteLine("Email Address: {0}", address);
         }
      }
}
```

<span data-ttu-id="94e1e-125">Ahora puede llamar a esta función mediante el objeto de servicio de Exchange y el **ItemId** del grupo de contactos.</span><span class="sxs-lookup"><span data-stu-id="94e1e-125">Now you can call this function by using the Exchange service object and the **ItemId** of the contact group.</span></span> <span data-ttu-id="94e1e-126">Tenga en cuenta que los **ItemId** en el ejemplo se acorta para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="94e1e-126">Note that the **ItemId** in the example is shortened for readability.</span></span> 
  
```cs
ExpandContactGroup(service, new ItemId("AAMkADBlY…");

```

## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews"></a><span data-ttu-id="94e1e-127">Expanda un grupo de distribución universal o un grupo de seguridad mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="94e1e-127">Expand a universal distribution group or security group by using EWS</span></span>
<span data-ttu-id="94e1e-128"><a name="bk_ExpandDGEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="94e1e-128"></span></span>

<span data-ttu-id="94e1e-129">En el ejemplo siguiente se muestra el mensaje de solicitud XML que se envía desde el cliente al servidor cuando se usa la operación de [ExpandDL](http://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="94e1e-129">The following example shows the XML request message that is sent from the client to the server when you use the [ExpandDL](http://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="94e1e-130">También es la solicitud XML que la API administrada de EWS envía al usar la API administrada de EWS para [expandir un grupo de distribución universal](#bk_ExpandDGEWSMA).</span><span class="sxs-lookup"><span data-stu-id="94e1e-130">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [expand a universal distribution group](#bk_ExpandDGEWSMA).</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <Mailbox>
        <t:EmailAddress>employees@contoso.com</t:EmailAddress>
      </Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="94e1e-131">En el ejemplo siguiente se muestra el mensaje de respuesta XML que se envía desde el servidor al cliente.</span><span class="sxs-lookup"><span data-stu-id="94e1e-131">The following example shows the XML response message that is sent from the server to the client.</span></span> <span data-ttu-id="94e1e-132">Tenga en cuenta que se devuelven los buzones de correo y grupos de distribución universal.</span><span class="sxs-lookup"><span data-stu-id="94e1e-132">Notice that both mailboxes and universal distribution groups are returned.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
     xmlns:xsd="http://www.w3.org/2001/XMLSchema">
<ExpandDLResponse xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                      xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <ResponseMessages xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
    <ExpandDLResponseMessage ResponseClass="Success">
      <ResponseCode>NoError</ResponseCode>
      <DLExpansion IncludesLastItemInRange="true" TotalItemsInView="4">
        <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Sadie Daniels</Name>
          <EmailAddress>sadie@contoso.com</EmailAddress>
          <RoutingType>SMTP</RoutingType>
          <MailboxType>Mailbox</MailboxType>
        </Mailbox>
        <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Alfred Welker</Name>
          <EmailAddress>alfred@contoso.com</EmailAddress>
          <RoutingType>SMTP</RoutingType>
          <MailboxType>Mailbox</MailboxType>
        </Mailbox>
        <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Contoso Sales</Name>
          <EmailAddress>sales@contoso.com</EmailAddress>
          <RoutingType>SMTP</RoutingType>
          <MailboxType>PublicDL</MailboxType>
        </Mailbox>
        <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Contoso Support</Name>
          <EmailAddress>support@contoso.com</EmailAddress>
          <RoutingType>SMTP</RoutingType>
          <MailboxType>PublicDL</MailboxType>
        </Mailbox>
      </DLExpansion>
    </ExpandDLResponseMessage>
  </ResponseMessages>
</ExpandDLResponse>
</s:Body>
</s:Envelope>
```

<span data-ttu-id="94e1e-133">A diferencia de cuando se utiliza la API administrada de EWS, al usar EWS para expandir un grupo de distribución universal, no se puede de forma recursiva expandir los grupos de distribución que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="94e1e-133">Unlike when you use the EWS Managed API, when you use EWS to expand a universal distribution group, you can't recursively expand the distribution groups that are returned.</span></span> <span data-ttu-id="94e1e-134">Debe enviar una solicitud adicional para expandir cada uno de los grupos de distribución que se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="94e1e-134">You will need to send an additional request to expand each of the distribution groups included in the response.</span></span>
  
## <a name="expand-a-contact-group-by-using-ews"></a><span data-ttu-id="94e1e-135">Expanda un grupo de contactos mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="94e1e-135">Expand a contact group by using EWS</span></span>
<span data-ttu-id="94e1e-136"><a name="bk_ExpandDGEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="94e1e-136"></span></span>

<span data-ttu-id="94e1e-137">La solicitud XML para expandir un grupo de contactos es similar a una solicitud para expandir un grupo de distribución.</span><span class="sxs-lookup"><span data-stu-id="94e1e-137">The XML request to expand a contact group is similar to a request to expand a distribution group.</span></span> <span data-ttu-id="94e1e-138">En lugar de una dirección de correo electrónico, use el [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) del grupo de contactos.</span><span class="sxs-lookup"><span data-stu-id="94e1e-138">Instead of an email address, you use the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the contact group.</span></span> <span data-ttu-id="94e1e-139">El **ItemId** en este ejemplo se acorta para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="94e1e-139">The **ItemId** in this example is shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <Mailbox>
         <ItemId xmlns="http://schemas.microsoft.com/exchange/services/2006/types" Id="AAMkADBlY…" />
      </Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="94e1e-140">La estructura de la respuesta XML a una solicitud para expandir un grupo de contactos es la misma que la respuesta a una solicitud para expandir un grupo de distribución universal.</span><span class="sxs-lookup"><span data-stu-id="94e1e-140">The structure of the XML response to a request to expand a contact group is the same as the response to a request to expand a universal distribution group.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="94e1e-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="94e1e-141">See also</span></span>


- [<span data-ttu-id="94e1e-142">Grupos de distribución y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="94e1e-142">Distribution groups and EWS in Exchange</span></span>](distribution-groups-and-ews-in-exchange.md)
    
- [<span data-ttu-id="94e1e-143">Crear grupos de contactos mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="94e1e-143">Create contact groups by using EWS in Exchange</span></span>](how-to-create-contact-groups-by-using-ews-in-exchange.md)
    

