---
title: Resolver nombres ambiguos mediante el uso de EWS en Exchange 2013
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1ba21c54-ecd2-4a1e-80d4-0f4171dea84f
description: Obtenga información sobre cómo usar la API administrada de EWS o EWS para resolver nombres ambiguos mediante la obtención de coincidencias posibles de los servicios de dominio de Active Directory (AD DS) o una carpeta de contactos en el buzón del usuario.
ms.openlocfilehash: 05a88043083a27d2e6d445cd71e5f3919c5a775d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763163"
---
# <a name="resolve-ambiguous-names-by-using-ews-in-exchange-2013"></a>Resolver nombres ambiguos mediante el uso de EWS en Exchange 2013

Obtenga información sobre cómo usar la API administrada de EWS o EWS para resolver nombres ambiguos mediante la obtención de coincidencias posibles de los servicios de dominio de Active Directory (AD DS) o una carpeta de contactos en el buzón del usuario.
  
Un usuario de la organización recibe una lista escrito a mano de nombres y direcciones para los empleados que asistieron a una sesión de aprendizaje. Que desean enviar un correo electrónico con información adicional a los usuarios en la lista, pero no pueden leer dirección de correo electrónico de todos los usuarios. Si desea resolver este problema para los usuarios en la aplicación, puede ayudar EWS. Puede usar el método de la API administrada de EWS [ExchangeService.ResolveName](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) o la operación de EWS [ResolveNames](http://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) para devolver una lista de posibles coincidencias para una selección de texto, como parte de un nombre de la última. Los elementos devueltos pueden ser buzones de usuarios públicos, grupos de distribución y contactos. 
  
Tenga en cuenta que Exchange guarda las direcciones de correo electrónico con tipos de enrutamiento de prefijo, como smtp o sip, en una matriz con varios valores. El método **ResolveName** y la operación **ResolveNames** realizar a una coincidencia parcial con respecto a cada valor de dicha matriz al agregar el tipo de distribución al principio del nombre sin resolver, como "sip: usuario1". Si no especifica un tipo de distribución, el método o la operación se smtp de forma predeterminada, match a una propiedad de dirección smtp principal y no buscar en la matriz con varios valores. Por ejemplo, si busca User1 y no incluya el prefijo de sip, no recibirá sip:User1@Contoso.com como resultado, incluso si es un buzón válido. 
  
Sólo se puede especificar un nombre ambiguo en una única solicitud. Si tiene una lista de nombres ambiguos para resolver, debe ejecutar un bucle en la lista y el método o la operación para cada entrada de llamadas. Candidatos desde la carpeta de contactos de un usuario tendrá un valor de identificador de elemento que no son null, que, a continuación, se puede usar en una llamada al método [Contact.Bind](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) o una solicitud de operación [GetItem](http://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) para recuperar información adicional. Si el candidato es un grupo de distribución, puede usar el método de la API administrada de EWS [ExpandGroup(ItemId)](http://msdn.microsoft.com/en-us/library/office/ee356407%28v=exchg.80%29.aspx) o la operación de EWS [ExpandDL](http://msdn.microsoft.com/library/affe84a5-ad98-4aba-83f4-8732938b763d%28Office.15%29.aspx) para obtener la lista de miembros. Si el parámetro _returnContactDetails_ o el atributo EWS **ReturnFullContactData** se establece en true, las entradas de Active Directory que se devuelven a través de un método **ResolveName** o **ResolveNames** operación incluirá propiedades adicionales que describen el contacto. El parámetro _returnContactDetails_ o el atributo **ReturnFullContactData** no afecta a los datos que se devuelven para los contactos y grupos de contactos. 
  
## <a name="resolve-ambiguous-names-by-using-ews-managed-api"></a>Resolver nombres ambiguos mediante el uso de API administrada de EWS
<a name="bk_EWSMA"> </a>

Puede usar el método [ResolveName](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) para buscar a candidatos que coinciden con el nombre ambiguo que pase. Puede utilizar sobrecargas del método **ResolveName** para buscar candidatos de cinco maneras diferentes. 
  
**La tabla 1. Métodos ResolveName sobrecargados**

|**M?todo**|**Cómo funciona**|
|:-----|:-----|
|[ResolveName(String)](http://msdn.microsoft.com/en-us/library/dd635548%28v=exchg.80%29.aspx) <br/> |Busca los contactos en la carpeta de contactos del usuario y la lista Global de direcciones (GAL), en ese orden. La variable de cadena es el nombre ambiguo que intenta resolver.  <br/> |
|[ResolveName (String, ResolveNameSearchLocation, Boolean)](http://msdn.microsoft.com/en-us/library/dd634595%28v=exchg.80%29.aspx) <br/> |Busca los contactos en la carpeta Contactos predeterminada y en la lista Global de direcciones (GAL). El valor de cadena es el nombre ambiguo, la ubicación de búsqueda especifica la carpeta de contactos o la lista global de direcciones y el valor de tipo Boolean indica si se debe devolver la información de contacto.  <br/> |
|[ResolveName (String, ResolveNameSearchLocation, Boolean, PropertySet)](http://msdn.microsoft.com/en-us/library/hh532803%28v=exchg.80%29.aspx) <br/> |Busca los contactos en la carpeta Contactos predeterminada y la lista Global de direcciones (GAL). Este método le permite establecer las propiedades que se devuelven.  <br/> |
|[ResolveName (cadena, IEnumerable\<FolderId\>, ResolveNameSearchLocation, Boolean)](http://msdn.microsoft.com/en-us/library/dd636014%28v=exchg.80%29.aspx) <br/> |Busca los contactos en las carpetas de contacto especificadas o en la lista Global de direcciones (GAL). Puede usar este método para pasar de una colección de carpetas de búsqueda. Esto le permite buscar en carpetas de contactos que no sea la carpeta Contactos predeterminada.  <br/> |
|[ResolveName (cadena, IEnumerable\<FolderId\>, ResolveNameSearchLocation, Boolean, PropertySet)](http://msdn.microsoft.com/en-us/library/hh532581%28v=exchg.80%29.aspx) <br/> |Busca los contactos en la lista Global de direcciones (GAL) o en carpetas específicas de contacto. Este método le permite establecer las propiedades que se devuelven.  <br/> |
   
Vamos a comenzar con un ejemplo sencillo. En el ejemplo siguiente se muestra cómo resolver la cadena de texto "dan" y el nombre y el correo electrónico de cada candidato que se encuentra de salida. En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange. 
  
```cs
// Resolve the ambiguous name "dan".
   NameResolutionCollection resolvedNames = service.ResolveName("dan");
   // Output the list of candidates.
   foreach (NameResolution nameRes in resolvedNames)
   {
      Console.WriteLine("Contact name: " + nameRes.Mailbox.Name);
      Console.WriteLine("Contact e-mail address: " + nameRes.Mailbox.Address);
      Console.WriteLine("Mailbox type: " + nameRes.Mailbox.MailboxType);
   }

```

La respuesta devuelve un máximo de 100 candidatos, aunque puede haber más de 100 candidatos posibles. Para determinar si se han devuelto sólo los primeros 100 candidatos de un número mayor de candidatos, compruebe el valor de [IncludesAllResolutions](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.includesallresolutions%28v=exchg.80%29.aspx) en el objeto [NameResolutionCollection](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) . Si el valor es true, no hay más no posibles candidatos; Si el valor es false, el método sólo devuelve los 100 primeros de un número mayor de candidatos posibles. 
  
Si trabaja en una organización grande, es probable que un nombre como "dan" devolverá el número máximo de 100 candidatos. Para reducir el número de candidatos devuelto, limitar donde buscar. En el ejemplo siguiente se usa la enumeración [ResolveNameSearchLocation](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.resolvenamesearchlocation%28v=exchg.80%29.aspx) para especificar dónde buscar para resolver el nombre ambiguo. 
  
```cs
// Resolve the ambiguous name "dan".
// Only use the Contacts folder.
   NameResolutionCollection resolvedNames = service.ResolveName("dan", ResolveNameSearchLocation.ContactsOnly, false);
   // Output the list of candidates.   
   foreach (NameResolution nameRes in resolvedNames)
   {
      Console.WriteLine("Contact name: " + nameRes.Mailbox.Name);
      Console.WriteLine("Contact e-mail address: " + nameRes.Mailbox.Address);
      Console.WriteLine("Mailbox type: " + nameRes.Mailbox.MailboxType);
   }

```

Si almacena los contactos en una carpeta distinta de la carpeta de contactos Well-known, use uno de los métodos sobrecargados para especificar dónde buscar candidatos. En el ejemplo siguiente se crea una lista de carpetas para el método **ResolveName** según el identificador de la carpeta. Se ha reducido el **FolderId** para mejorar la legibilidad. 
  
```cs
// Create a list to store folders to search.
List<FolderId> folders = new List<FolderId>();
// Add a folder to the list based on the FolderId.
folders.Add(new FolderId("AABR8mboAAA="));
// Resolve the ambiguous name "dan".
// Only use the folders specified.
NameResolutionCollection resolvedNames = service.ResolveName("dan", folders, ResolveNameSearchLocation.ContactsOnly, false);
   foreach (NameResolution nameRes in resolvedNames)
   {
      Console.WriteLine("Contact name: " + nameRes.Mailbox.Name);
      Console.WriteLine("Contact e-mail address: " + nameRes.Mailbox.Address);
      Console.WriteLine("Mailbox type: " + nameRes.Mailbox.MailboxType);
   }

```

Si aplica filtros y no se devuelven candidatos, el [NameResolutionCollection](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) va a contener cero entradas. Para comprobar esto examinando la propiedad [Count](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.count%28v=exchg.80%29.aspx) de la colección. 
  
## <a name="resolve-ambiguous-names-by-using-ews"></a>Resolver nombres ambiguos mediante el uso de EWS
<a name="bk_EWSMA"> </a>

Puede usar la operación de EWS [ResolveNames](http://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) para identificar a posibles candidatos para un nombre ambiguo. El elemento [UnresolvedEntry](http://msdn.microsoft.com/library/5ac6116a-3b24-40f8-a877-dbe9a6935919%28Office.15%29.aspx) contiene el nombre ambiguo que desea resolver. En el ejemplo siguiente se muestra cómo resolver el nombre Sadie. También es la solicitud XML que se utiliza la API administrada de EWS cuando se [Utilice el método ResolveName](#bk_EWSMA), excepto en que utiliza un nombre distinto para ver ejemplos de salida válido.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ResolveNames xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                  ReturnFullContactData="true">
      <UnresolvedEntry>Sadie</UnresolvedEntry>
    </ResolveNames>
  </soap:Body>
</soap:Envelope>
```

La respuesta devuelve un máximo de 100 candidatos, aunque puede haber más de 100 posibles candidatos para determinar si se han devuelto sólo los primeros 100 candidatos de un número mayor de candidatos, compruebe el valor de la [IncludesLastItemInRange](http://msdn.microsoft.com/library/e7d6c7d3-548e-48b0-a313-bfef81e4832a%28Office.15%29.aspx) atributo del elemento [ResolutionSet](http://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) . Si el valor es true, no hay más no posibles candidatos; Si el valor es false, la operación sólo devuelve los 100 primeros de un número mayor de candidatos posibles. 
  
En el ejemplo siguiente se muestra la respuesta XML cuando se encuentra un candidato. Recuerde que la [ResolutionSet](http://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) puede contener hasta 100 candidatos, cada uno de ellos representado por el elemento de la [solución](http://msdn.microsoft.com/library/573bed4b-d7b1-4baf-b16f-0795cdebf1a7%28Office.15%29.aspx) y sus elementos secundarios. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ResolutionSet TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Resolution>
              <t:Mailbox>
                <t:Name>Sadie Daniels</t:Name>
                <t:EmailAddress>Sadie@Contoso.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Mailbox</t:MailboxType>
              </t:Mailbox>
              <t:Contact>
                <t:DisplayName>Sadie Daniels</t:DisplayName>
                <t:EmailAddresses>
                  <t:Entry Key="EmailAddress1">SMTP:Sadie@Contoso.com</t:Entry>
                </t:EmailAddresses>
                <t:ContactSource>ActiveDirectory</t:ContactSource>
              </t:Contact>
            </t:Resolution>
          </m:ResolutionSet>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </ResolveNamesResponse>
  </soap:Body>
</soap:Envelope>
```

No siempre va a surgen con candidatos para su nombre ambiguo. En el ejemplo siguiente se muestra la respuesta XML, como un error, cuando no se encuentran candidatos.
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Error">
          <m:MessageText>No results were found.</m:MessageText>
          <m:ResponseCode>ErrorNameResolutionNoResults</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </ResolveNamesResponse>
  </soap:Body>
</soap:Envelope>

```

## <a name="see-also"></a>Ver también


- [Las personas y los contactos de EWS en Exchange](people-and-contacts-in-ews-in-exchange.md)
    
- [Expandir grupos de distribución mediante el uso de EWS en Exchange 2013](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    

