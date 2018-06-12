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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763058"
---
# <a name="expand-distribution-groups-by-using-ews-in-exchange-2013"></a>Expandir grupos de distribución mediante el uso de EWS en Exchange 2013

Obtenga información sobre cómo expandir un grupo de distribución mediante la API administrada de EWS o EWS en Exchange.
  
Puede usar el método de la API administrada de EWS [ExchangeService.ExpandGroup](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) o la operación de EWS [ExpandDL](http://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) para expandir un grupo de distribución para identificar a todos los destinatarios. 
  
Debido a que el método [ExpandGroup](http://msdn.microsoft.com/en-us/library/office/ee344007%28v=exchg.80%29.aspx) está sobrecargado, puede llamar de varias maneras: 
  
- [ExpandGroup(String)](http://msdn.microsoft.com/en-us/library/office/ee343988%28v=exchg.80%29.aspx) - expande un grupo identificado por una dirección SMTP. 
    
- [ExpandGroup(EmailAddress)](http://msdn.microsoft.com/en-us/library/office/ee344007%28v=exchg.80%29.aspx) - expande un grupo identificado por una dirección de correo electrónico. 
    
- [ExpandGroup(ItemId)](http://msdn.microsoft.com/en-us/library/office/ee356407%28v=exchg.80%29.aspx) - expande un grupo identificado por un identificador de grupo. 
    
- [ExpanGroup (String, String)](http://msdn.microsoft.com/en-us/library/office/ee356468%28v=exchg.80%29.aspx) - expande un grupo identificado por una dirección SMTP y el tipo de distribución de esa dirección. 
    
## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews-managed-api"></a>Expanda un grupo de distribución universal o un grupo de seguridad mediante el uso de API administrada de EWS
<a name="bk_ExpandDGEWSMA"> </a>

En el ejemplo siguiente se muestra cómo expandir un grupo de distribución universal o un grupo de seguridad mediante el uso de una dirección de correo electrónico, que es el enfoque más sencillo. En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange. 
  
```cs
// Return the expanded group.
   ExpandGroupResults myGroupMembers = service.ExpandGroup("employees@contoso.com");
// Display the group members.
   foreach (EmailAddress address in myGroupMembers.Members)
   {
      Console.WriteLine("Email Address: {0}", address);
   }

```

Eso no es una gran cantidad de código, pero también es bastante básica y es posible que no dar a lo está buscando. Por lo que vamos a dar un paso más. Grupos de distribución también pueden contener otros grupos de distribución. Simplemente expandirlo se de resultados de la dirección de correo electrónico de los grupos de distribución contenido, pero no los expandir. Mediante la adición de unas pocas líneas más de código, se puede de forma recursiva expandir los grupos para cada contacto de salida.
  
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

Y ahora se puede llamar a esta función nuevo el su código y expanda todos los grupos de distribución pública incluidos en el primero de ellos.
  
```cs
ExpandDistributionLists(service, "employees@contoso.com");

```

## <a name="expand-a-contact-group-by-using-ews-managed-api"></a>Expanda un grupo de contactos mediante el uso de API administrada de EWS
<a name="bk_ExpandDGEWSMA"> </a>

Debido a que los grupos de contactos no tiene una dirección de correo electrónico asociadas, necesita expandir el grupo basado en el ItemId mediante el método [ExpandGroup(ItemId)](http://msdn.microsoft.com/en-us/library/office/ee356407%28v=exchg.80%29.aspx) . Puede crear una función, tal como se muestra en el ejemplo anterior y cambie el segundo tipo de parámetro de una cadena a un [ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx).
  
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

Ahora puede llamar a esta función mediante el objeto de servicio de Exchange y el **ItemId** del grupo de contactos. Tenga en cuenta que los **ItemId** en el ejemplo se acorta para mejorar la legibilidad. 
  
```cs
ExpandContactGroup(service, new ItemId("AAMkADBlY…");

```

## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews"></a>Expanda un grupo de distribución universal o un grupo de seguridad mediante el uso de EWS
<a name="bk_ExpandDGEWSMA"> </a>

En el ejemplo siguiente se muestra el mensaje de solicitud XML que se envía desde el cliente al servidor cuando se usa la operación de [ExpandDL](http://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) . También es la solicitud XML que la API administrada de EWS envía al usar la API administrada de EWS para [expandir un grupo de distribución universal](#bk_ExpandDGEWSMA). 
  
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

En el ejemplo siguiente se muestra el mensaje de respuesta XML que se envía desde el servidor al cliente. Tenga en cuenta que se devuelven los buzones de correo y grupos de distribución universal.
  
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

A diferencia de cuando se utiliza la API administrada de EWS, al usar EWS para expandir un grupo de distribución universal, no se puede de forma recursiva expandir los grupos de distribución que se devuelven. Debe enviar una solicitud adicional para expandir cada uno de los grupos de distribución que se incluye en la respuesta.
  
## <a name="expand-a-contact-group-by-using-ews"></a>Expanda un grupo de contactos mediante el uso de EWS
<a name="bk_ExpandDGEWSMA"> </a>

La solicitud XML para expandir un grupo de contactos es similar a una solicitud para expandir un grupo de distribución. En lugar de una dirección de correo electrónico, use el [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) del grupo de contactos. El **ItemId** en este ejemplo se acorta para mejorar la legibilidad. 
  
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

La estructura de la respuesta XML a una solicitud para expandir un grupo de contactos es la misma que la respuesta a una solicitud para expandir un grupo de distribución universal.
  
## <a name="see-also"></a>Ver también


- [Grupos de distribución y EWS en Exchange](distribution-groups-and-ews-in-exchange.md)
    
- [Crear grupos de contactos mediante el uso de EWS en Exchange](how-to-create-contact-groups-by-using-ews-in-exchange.md)
    

