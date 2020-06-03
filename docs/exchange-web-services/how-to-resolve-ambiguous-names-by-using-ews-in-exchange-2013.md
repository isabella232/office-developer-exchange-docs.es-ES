---
title: Resolver nombres ambiguos mediante EWS en Exchange 2013
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1ba21c54-ecd2-4a1e-80d4-0f4171dea84f
description: Obtenga información sobre cómo usar la API administrada de EWS o EWS para resolver nombres ambiguos al obtener posibles coincidencias de los servicios de dominio de Active Directory (AD DS) o de una carpeta de contactos en el buzón de correo del usuario.
ms.openlocfilehash: 5e30e268f54e6ca257e188592e49d168e64332ff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527750"
---
# <a name="resolve-ambiguous-names-by-using-ews-in-exchange-2013"></a>Resolver nombres ambiguos mediante EWS en Exchange 2013

Obtenga información sobre cómo usar la API administrada de EWS o EWS para resolver nombres ambiguos al obtener posibles coincidencias de los servicios de dominio de Active Directory (AD DS) o de una carpeta de contactos en el buzón de correo del usuario.
  
Un usuario de la organización recibe una lista de nombres y direcciones que se escriben a mano para los empleados que hayan asistido a una sesión de formación. Quieren enviar un mensaje de correo electrónico con información adicional a las personas de la lista, pero no pueden leer la dirección de correo electrónico de todos los usuarios. Si desea solucionar este problema para los usuarios de su aplicación, EWS puede ayudarle. Puede usar el método de la API administrada de EWS [ExchangeService. ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) o la operación de EWS [ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) para devolver una lista de posibles coincidencias para una selección de texto, como parte de un apellido. Los elementos devueltos pueden ser buzones de usuario públicos, grupos de distribución y contactos. 
  
Tenga en cuenta que Exchange guarda direcciones de correo electrónico con tipos de enrutamiento con prefijo, como SMTP o SIP, en una matriz de varios valores. El método **ResolveName** y la operación **ResolveNames** realizan una coincidencia parcial con cada valor de la matriz cuando se agrega el tipo de enrutamiento al principio del nombre sin resolver, como "SIP: user1". Si no especifica un tipo de enrutamiento, el método o la operación tomarán el valor predeterminado SMTP, se hará coincidir con una propiedad de dirección SMTP principal y no buscarán en la matriz de varios valores. Por ejemplo, si busca user1 y no incluye el prefijo SIP, no recibirá sip:User1@Contoso.com como resultado, incluso si es un buzón válido. 
  
Solo se puede especificar un nombre ambiguo en una sola solicitud. Si tiene una lista de nombres ambiguos que se van a resolver, deberá recorrer la lista y llamar al método o la operación para cada entrada. Los candidatos de la carpeta de contactos de un usuario tendrán un valor de identificador de elemento no NULL, que se puede usar en una llamada al método [Contact. bind](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) o en una solicitud de operación [GetItem](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) para recuperar información adicional. Si el candidato es un grupo de distribución, puede usar el método de la API administrada EWS de [ExpandGroup (Itemid)](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) o la operación de EWS [ExpandDL](https://msdn.microsoft.com/library/affe84a5-ad98-4aba-83f4-8732938b763d%28Office.15%29.aspx) para obtener la lista de miembros. Si el parámetro _returnContactDetails_ o el atributo EWS **ReturnFullContactData** está establecido en true, las entradas de Active Directory devueltas a través de un método **ResolveName** o una operación **ResolveNames** incluirán propiedades adicionales que describen el contacto. El parámetro _returnContactDetails_ o el atributo **ReturnFullContactData** no afectan a los datos que se devuelven para contactos y grupos de contactos. 
  
## <a name="resolve-ambiguous-names-by-using-ews-managed-api"></a>Resolución de nombres ambiguos mediante la API administrada de EWS
<a name="bk_EWSMA"> </a>

Puede usar el método [ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) para buscar candidatos que coinciden con el nombre ambiguo que ha pasado. Puede usar sobrecargas del método **ResolveName** para buscar candidatos de cinco maneras diferentes. 
  
**Tabla 1. Métodos ResolveName sobrecargados**

|**Método**|**Funcionamiento**|
|:-----|:-----|
|[ResolveName (cadena)](https://msdn.microsoft.com/library/dd635548%28v=exchg.80%29.aspx) <br/> |Busca contactos en la carpeta de contactos del usuario y en la lista global de direcciones (GAL), en ese orden. La variable de cadena es el nombre ambiguo que está intentando resolver.  <br/> |
|[ResolveName (String, ResolveNameSearchLocation, Boolean)](https://msdn.microsoft.com/library/dd634595%28v=exchg.80%29.aspx) <br/> |Busca contactos en la carpeta contactos predeterminada o en la lista global de direcciones (GAL). El valor de cadena es el nombre ambiguo, la ubicación de búsqueda especifica la carpeta de contactos o la GAL, y el valor booleano indica si se debe devolver la información de contacto completa.  <br/> |
|[ResolveName (String, ResolveNameSearchLocation, Boolean, PropertySet)](https://msdn.microsoft.com/library/hh532803%28v=exchg.80%29.aspx) <br/> |Busca contactos en la carpeta contactos predeterminada o en la lista global de direcciones (GAL). Este método permite establecer las propiedades que se devuelven.  <br/> |
|[ResolveName (String, IEnumerable \<FolderId\> , ResolveNameSearchLocation, Boolean)](https://msdn.microsoft.com/library/dd636014%28v=exchg.80%29.aspx) <br/> |Busca contactos en las carpetas de contactos especificadas o en la lista global de direcciones (GAL). Puede usar este método para pasar una colección de carpetas para buscar. Esto le permite buscar en carpetas de contactos distintas de la carpeta de contactos predeterminada.  <br/> |
|[ResolveName (String, IEnumerable \<FolderId\> , ResolveNameSearchLocation, Boolean, PropertySet)](https://msdn.microsoft.com/library/hh532581%28v=exchg.80%29.aspx) <br/> |Busca contactos en la lista global de direcciones (GAL) o en carpetas de contactos específicas. Este método permite establecer las propiedades que se devuelven.  <br/> |
   
Comencemos con un ejemplo sencillo. En el siguiente ejemplo, se muestra cómo resolver la cadena de texto "dan" y se muestra el nombre y la dirección de correo electrónico de cada candidato encontrado. En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange. 
  
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

La respuesta devuelve un máximo de 100 candidatos, aunque podría haber más de 100 candidatos potenciales. Para determinar si solo se devolvieron los primeros 100 candidatos de un número mayor de candidatos, compruebe el valor de [IncludesAllResolutions](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.includesallresolutions%28v=exchg.80%29.aspx) en el objeto [NameResolutionCollection](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) Si el valor es true, no hay más candidatos posibles; Si el valor es false, el método sólo devuelve el primer 100 de un número mayor de candidatos potenciales. 
  
Si trabaja en una organización de gran tamaño, es probable que un nombre como "dan" devuelva el número máximo de 100 candidatos. Para reducir el número de candidatos devueltos, limite dónde realiza la búsqueda. El siguiente ejemplo usa la enumeración [ResolveNameSearchLocation](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.resolvenamesearchlocation%28v=exchg.80%29.aspx) para especificar dónde buscar para resolver el nombre ambiguo. 
  
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

Si almacena los contactos en una carpeta que no sea la carpeta de contactos conocida, use uno de los métodos sobrecargados para especificar dónde buscar candidatos. En el ejemplo siguiente se crea una lista de carpetas para el método **ResolveName** basándose en el identificador de la carpeta. La **FolderId** se ha abreviado para facilitar la legibilidad. 
  
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

Si se aplican filtros y no se devuelven candidatos, el [NameResolutionCollection](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) no contendrá ninguna entrada. Puede comprobarlo observando la propiedad [Count](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.count%28v=exchg.80%29.aspx) de la colección. 
  
## <a name="resolve-ambiguous-names-by-using-ews"></a>Resolución de nombres ambiguos mediante EWS
<a name="bk_EWSMA"> </a>

Puede usar la operación de EWS de [ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) para identificar posibles candidatos para un nombre ambiguo. El elemento [UnresolvedEntry](https://msdn.microsoft.com/library/5ac6116a-3b24-40f8-a877-dbe9a6935919%28Office.15%29.aspx) contiene el nombre ambiguo que desea resolver. En el siguiente ejemplo, se muestra cómo resolver el nombre Sadie. También es la solicitud XML que usa la API administrada de EWS cuando usa [el método ResolveName](#bk_EWSMA), excepto que usa un nombre diferente para los ejemplos de resultados válidos.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ResolveNames xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                  ReturnFullContactData="true">
      <UnresolvedEntry>Sadie</UnresolvedEntry>
    </ResolveNames>
  </soap:Body>
</soap:Envelope>
```

La respuesta devuelve un máximo de 100 candidatos, aunque es posible que haya más de 100 candidatos potenciales para determinar si solo se devolvieron los primeros 100 candidatos de un número mayor de candidatos, compruebe el valor del atributo [IncludesLastItemInRange](https://msdn.microsoft.com/library/e7d6c7d3-548e-48b0-a313-bfef81e4832a%28Office.15%29.aspx) del elemento [ResolutionSet](https://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) . Si el valor es true, no hay más candidatos posibles; Si el valor es false, la operación sólo devuelve el primer 100 de un número mayor de candidatos potenciales. 
  
En el ejemplo siguiente se muestra la respuesta XML cuando se encuentra un candidato. Recuerde que [ResolutionSet](https://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) puede contener hasta 100 candidatos, cada uno de los cuales está representado por el elemento [Resolution](https://msdn.microsoft.com/library/573bed4b-d7b1-4baf-b16f-0795cdebf1a7%28Office.15%29.aspx) y sus elementos secundarios. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

No siempre irá a los candidatos para su nombre ambiguo. En el ejemplo siguiente se muestra la respuesta XML, como un error, cuando no se encuentran candidatos.
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="see-also"></a>Vea también


- [Personas y contactos de EWS en Exchange](people-and-contacts-in-ews-in-exchange.md)
    
- [Expandir grupos de distribución mediante EWS en Exchange 2013](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    

