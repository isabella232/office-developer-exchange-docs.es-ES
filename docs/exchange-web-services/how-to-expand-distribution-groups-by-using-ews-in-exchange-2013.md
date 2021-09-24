---
title: Expandir grupos de distribución mediante EWS en Exchange 2013
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 25ee84e7-63bc-4f51-9b7d-e7f46fd574d5
description: Obtenga información sobre cómo expandir un grupo de distribución mediante la API administrada ews o EWS en Exchange.
ms.openlocfilehash: 6aeebbd14604295bce46049f0e383663414c01a0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513188"
---
# <a name="expand-distribution-groups-by-using-ews-in-exchange-2013"></a>Expandir grupos de distribución mediante EWS en Exchange 2013

Obtenga información sobre cómo expandir un grupo de distribución mediante la API administrada ews o EWS en Exchange.
  
Puede usar el método de API administrada EWS [ExchangeService.ExpandGroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) o la operación [EWS ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) para expandir un grupo de distribución para identificar todos los destinatarios. 
  
Dado que [el método ExpandGroup](https://msdn.microsoft.com/library/office/ee344007%28v=exchg.80%29.aspx) está sobrecargado, puede llamarlo de varias maneras: 
  
- [ExpandGroup(String):](https://msdn.microsoft.com/library/office/ee343988%28v=exchg.80%29.aspx) expande un grupo identificado por una dirección SMTP. 
    
- [ExpandGroup(EmailAddress):](https://msdn.microsoft.com/library/office/ee344007%28v=exchg.80%29.aspx) expande un grupo identificado por una dirección de correo electrónico. 
    
- [ExpandGroup(ItemId):](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) expande un grupo identificado por un identificador de grupo. 
    
- [ExpanGroup(String, String):](https://msdn.microsoft.com/library/office/ee356468%28v=exchg.80%29.aspx) expande un grupo identificado por una dirección SMTP y el tipo de enrutamiento de esa dirección. 
    
## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews-managed-api"></a>Expandir un grupo de distribución universal o un grupo de seguridad mediante la API administrada de EWS
<a name="bk_ExpandDGEWSMA"> </a>

En el ejemplo siguiente se muestra cómo expandir un grupo de distribución universal o un grupo de seguridad mediante una dirección de correo electrónico, que es el enfoque más sencillo. En este ejemplo se supone que **el servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un Exchange servidor. 
  
```cs
// Return the expanded group.
   ExpandGroupResults myGroupMembers = service.ExpandGroup("employees@contoso.com");
// Display the group members.
   foreach (EmailAddress address in myGroupMembers.Members)
   {
      Console.WriteLine("Email Address: {0}", address);
   }

```

No es mucho código, pero también es bastante básico y puede que no le dé lo que está buscando. Así que vamos a dar un paso más allá. Los grupos de distribución también pueden contener otros grupos de distribución. Al expandirlo, se mostrará la dirección de correo electrónico de los grupos de distribución contenidos, pero no se expandirán. Al agregar algunas líneas de código más, puede expandir los grupos de forma recursiva para generar cada contacto.
  
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

Ahora puede llamar a esta nueva función en el código y expandir todos los grupos de distribución públicos incluidos en la primera.
  
```cs
ExpandDistributionLists(service, "employees@contoso.com");

```

## <a name="expand-a-contact-group-by-using-ews-managed-api"></a>Expandir un grupo de contactos mediante la API administrada de EWS
<a name="bk_ExpandDGEWSMA"> </a>

Dado que los grupos de contactos no tienen una dirección de correo electrónico asociada, debe expandir el grupo en función del ItemId mediante el método [ExpandGroup(ItemId).](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) Puede crear una función, como se muestra en el ejemplo anterior, y cambiar el segundo tipo de parámetro de una cadena a [un ItemId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx).
  
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

Ahora puede llamar a esta función mediante el Exchange de servicio y **el ItemId** del grupo de contactos. Tenga en cuenta **que itemid** en el ejemplo se abrevia para la legibilidad. 
  
```cs
ExpandContactGroup(service, new ItemId("AAMkADBlY…");

```

## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews"></a>Expandir un grupo de distribución universal o un grupo de seguridad mediante EWS
<a name="bk_ExpandDGEWSMA"> </a>

En el ejemplo siguiente se muestra el mensaje de solicitud XML que se envía desde el cliente al servidor cuando se usa la [operación ExpandDL.](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) Esta es también la solicitud XML que envía la API administrada ews cuando se usa la API administrada ews para [expandir un grupo de distribución universal.](#bk_ExpandDGEWSMA) 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <Mailbox>
        <t:EmailAddress>employees@contoso.com</t:EmailAddress>
      </Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

En el ejemplo siguiente se muestra el mensaje de respuesta XML que se envía desde el servidor al cliente. Tenga en cuenta que se devuelven tanto buzones como grupos de distribución universales.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
     xmlns:xsd="http://www.w3.org/2001/XMLSchema">
<ExpandDLResponse xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                      xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <ResponseMessages xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
    <ExpandDLResponseMessage ResponseClass="Success">
      <ResponseCode>NoError</ResponseCode>
      <DLExpansion IncludesLastItemInRange="true" TotalItemsInView="4">
        <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Sadie Daniels</Name>
          <EmailAddress>sadie@contoso.com</EmailAddress>
          <RoutingType>SMTP</RoutingType>
          <MailboxType>Mailbox</MailboxType>
        </Mailbox>
        <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Alfred Welker</Name>
          <EmailAddress>alfred@contoso.com</EmailAddress>
          <RoutingType>SMTP</RoutingType>
          <MailboxType>Mailbox</MailboxType>
        </Mailbox>
        <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Contoso Sales</Name>
          <EmailAddress>sales@contoso.com</EmailAddress>
          <RoutingType>SMTP</RoutingType>
          <MailboxType>PublicDL</MailboxType>
        </Mailbox>
        <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

A diferencia de cuando se usa la API administrada ews, cuando se usa EWS para expandir un grupo de distribución universal, no se pueden expandir recursivamente los grupos de distribución que se devuelven. Deberá enviar una solicitud adicional para expandir cada uno de los grupos de distribución incluidos en la respuesta.
  
## <a name="expand-a-contact-group-by-using-ews"></a>Expandir un grupo de contactos mediante EWS
<a name="bk_ExpandDGEWSMA"> </a>

La solicitud XML para expandir un grupo de contactos es similar a una solicitud para expandir un grupo de distribución. En lugar de una dirección de correo electrónico, use [el ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) del grupo de contactos. El **ItemId de** este ejemplo se abrevia para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <Mailbox>
         <ItemId xmlns="https://schemas.microsoft.com/exchange/services/2006/types" Id="AAMkADBlY…" />
      </Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

La estructura de la respuesta XML a una solicitud para expandir un grupo de contactos es la misma que la respuesta a una solicitud para expandir un grupo de distribución universal.
  
## <a name="see-also"></a>Ver también


- [Grupos de distribución y EWS en Exchange](distribution-groups-and-ews-in-exchange.md)
    
- [Crear grupos de contactos mediante EWS en Exchange](how-to-create-contact-groups-by-using-ews-in-exchange.md)
    

