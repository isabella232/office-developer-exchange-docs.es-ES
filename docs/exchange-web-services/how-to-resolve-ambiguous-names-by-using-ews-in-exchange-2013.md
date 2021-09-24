---
title: Resolver nombres ambiguos mediante EWS en Exchange 2013
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 1ba21c54-ecd2-4a1e-80d4-0f4171dea84f
description: Obtenga información sobre cómo usar la API administrada ews o EWS para resolver nombres ambiguos obteniendo posibles coincidencias de Servicios de dominio de Active Directory (AD DS) o una carpeta de contactos en el buzón del usuario.
ms.openlocfilehash: 5946dad32639b454b3961eaa172b6069ce118b58
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521126"
---
# <a name="resolve-ambiguous-names-by-using-ews-in-exchange-2013"></a>Resolver nombres ambiguos mediante EWS en Exchange 2013

Obtenga información sobre cómo usar la API administrada ews o EWS para resolver nombres ambiguos obteniendo posibles coincidencias de Servicios de dominio de Active Directory (AD DS) o una carpeta de contactos en el buzón del usuario.
  
A un usuario de su organización se le da una lista escrita a mano de nombres y direcciones para los empleados que han asistido a una sesión de formación. Quieren enviar un correo electrónico con información adicional a los usuarios de la lista, pero no pueden leer la dirección de correo electrónico de todos. Si desea solucionar este problema para los usuarios de la aplicación, EWS puede ayudarle. Puede usar el método de API administrada EWS [ExchangeService.ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) o la operación EWS ResolveNames para devolver una lista de [posibles coincidencias](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) para una selección de texto, como parte de un apellido. Los elementos devueltos pueden ser buzones de usuario públicos, grupos de distribución y contactos. 
  
Tenga en Exchange guardar direcciones de correo electrónico con tipos de enrutamiento con prefijo, como smtp o sip, en una matriz de varios valores. El **método ResolveName** y la operación **ResolveNames** realizan una coincidencia parcial con cada valor de esa matriz al agregar el tipo de enrutamiento al principio del nombre no resuelto, como "sip:User1". Si no especifica un tipo de enrutamiento, el método o la operación serán smtp de forma predeterminada, lo coincidirán con una propiedad de dirección smtp principal y no buscarán en la matriz de varios valores. Por ejemplo, si busca User1 y no incluye el prefijo sip, no recibirá sip:User1@Contoso.com como resultado, incluso si se trata de un buzón válido. 
  
Solo puede especificar un nombre ambiguo en una sola solicitud. Si tiene una lista de nombres ambiguos que resolver, deberá recorrer la lista en bucle y llamar al método u operación de cada entrada. Los candidatos de la carpeta Contactos de un usuario tendrán un valor de identificador de elemento que no sea nulo, que se puede usar en una llamada al método [Contact.Bind](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) o en una solicitud de operación [GetItem](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) para recuperar información adicional. Si el candidato es un grupo de distribución, puede usar el método de API administrada ews [ExpandGroup(ItemId)](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) o la operación [EWS ExpandDL](https://msdn.microsoft.com/library/affe84a5-ad98-4aba-83f4-8732938b763d%28Office.15%29.aspx) para obtener la lista de miembros. Si el  _parámetro returnContactDetails_ o el atributo **EWS ReturnFullContactData** se establece en true, las entradas de Active Directory devueltas a través de un método **ResolveName** o una operación **ResolveNames** incluirán propiedades adicionales que describen el contacto. El  _parámetro returnContactDetails_ o el atributo **ReturnFullContactData** no afectan a los datos devueltos para contactos y grupos de contactos. 
  
## <a name="resolve-ambiguous-names-by-using-ews-managed-api"></a>Resolver nombres ambiguos con la API administrada de EWS
<a name="bk_EWSMA"> </a>

Puede usar el método [ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) para buscar candidatos que coincidan con el nombre ambiguo que pase. Puede usar sobrecargas del método **ResolveName** para buscar candidatos de cinco maneras diferentes. 
  
**Tabla 1. Métodos ResolveName sobrecargados**

|**Método**|**Funcionamiento**|
|:-----|:-----|
|[ResolveName(String)](https://msdn.microsoft.com/library/dd635548%28v=exchg.80%29.aspx) <br/> |Busca contactos en la carpeta Contactos del usuario y en la Lista global de direcciones (GAL) en ese orden. La variable de cadena es el nombre ambiguo que está intentando resolver.  <br/> |
|[ResolveName(String, ResolveNameSearchLocation, Boolean)](https://msdn.microsoft.com/library/dd634595%28v=exchg.80%29.aspx) <br/> |Busca contactos en la carpeta contactos predeterminada o en la lista global de direcciones (GAL). El valor de cadena es el nombre ambiguo, la ubicación de búsqueda especifica la carpeta Contactos o la GAL y el valor booleano indica si se devuelve la información de contacto completa.  <br/> |
|[ResolveName(String, ResolveNameSearchLocation, Boolean, PropertySet)](https://msdn.microsoft.com/library/hh532803%28v=exchg.80%29.aspx) <br/> |Busca contactos en la carpeta contactos predeterminada o en la lista global de direcciones (GAL). Este método permite establecer las propiedades que se devuelven.  <br/> |
|[ResolveName(String, IEnumerable \<FolderId\> , ResolveNameSearchLocation, Boolean)](https://msdn.microsoft.com/library/dd636014%28v=exchg.80%29.aspx) <br/> |Busca contactos en carpetas de contactos especificadas o en la Lista global de direcciones (GAL). Puede usar este método para pasar una colección de carpetas para buscar. Esto le permite buscar en carpetas de contactos que no sea la carpeta contactos predeterminada.  <br/> |
|[ResolveName(String, IEnumerable \<FolderId\> , ResolveNameSearchLocation, Boolean, PropertySet)](https://msdn.microsoft.com/library/hh532581%28v=exchg.80%29.aspx) <br/> |Busca contactos en la lista global de direcciones (GAL) o en carpetas de contactos específicas. Este método permite establecer las propiedades que se devuelven.  <br/> |
   
Empecemos con un ejemplo sencillo. En el ejemplo siguiente se muestra cómo resolver la cadena de texto "dan" y cómo generar el nombre y la dirección de correo electrónico de cada candidato encontrado. En este ejemplo se supone que **el servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un Exchange servidor. 
  
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

La respuesta devuelve un máximo de 100 candidatos, aunque puede haber más de 100 candidatos potenciales. Para determinar si solo se devolvieron los primeros 100 candidatos de un número mayor de candidatos, compruebe el valor de [IncludesAllResolutions](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.includesallresolutions%28v=exchg.80%29.aspx) en el [objeto NameResolutionCollection.](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) Si el valor es true, no hay más candidatos posibles; si el valor es false, el método solo devuelve los primeros 100 de un número mayor de posibles candidatos. 
  
Si trabaja en una organización grande, es probable que un nombre como "dan" devuelva el número máximo de 100 candidatos. Para reducir el número de candidatos devueltos, limite la búsqueda. En el siguiente ejemplo se [usa la enumeración ResolveNameSearchLocation](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.resolvenamesearchlocation%28v=exchg.80%29.aspx) para especificar dónde buscar para resolver el nombre ambiguo. 
  
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

Si almacena los contactos en una carpeta que no sea la carpeta Contactos conocida, use uno de los métodos sobrecargados para especificar dónde buscar candidatos. En el siguiente ejemplo se crea una lista de carpetas para el **método ResolveName** basándose en el identificador de carpeta. **FolderId** se ha acortado para mejorar la legibilidad. 
  
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

Si aplica filtros y no se devuelve ningún candidato, [NameResolutionCollection](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) contendrá cero entradas. Para comprobar esto, consulte la [propiedad Count](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.count%28v=exchg.80%29.aspx) de la colección. 
  
## <a name="resolve-ambiguous-names-by-using-ews"></a>Resolver nombres ambiguos mediante EWS
<a name="bk_EWSMA"> </a>

Puede usar la operación [EWS ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) para identificar posibles candidatos para un nombre ambiguo. El [elemento UnresolvedEntry](https://msdn.microsoft.com/library/5ac6116a-3b24-40f8-a877-dbe9a6935919%28Office.15%29.aspx) contiene el nombre ambiguo que desea resolver. En el ejemplo siguiente se muestra cómo resolver el nombre Sadie. Esta es también la solicitud XML que usa la API administrada ews cuando se usa el método [ResolveName](#bk_EWSMA), excepto que usa un nombre diferente para ejemplos de salida válidos.
  
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

La respuesta devuelve un máximo de 100 candidatos, aunque puede haber más de 100 candidatos potenciales Para determinar si solo se han devuelto los primeros 100 candidatos de un número mayor de candidatos, compruebe el valor del atributo [IncludesLastItemInRange](https://msdn.microsoft.com/library/e7d6c7d3-548e-48b0-a313-bfef81e4832a%28Office.15%29.aspx) del elemento [ResolutionSet.](https://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) Si el valor es true, no hay más candidatos posibles; si el valor es false, la operación solo devuelve los primeros 100 de un número mayor de posibles candidatos. 
  
En el siguiente ejemplo se muestra la respuesta XML cuando se encuentra un candidato. Recuerde que [ResolutionSet](https://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) puede contener hasta 100 candidatos, cada uno representado por el elemento [Resolution](https://msdn.microsoft.com/library/573bed4b-d7b1-4baf-b16f-0795cdebf1a7%28Office.15%29.aspx) y sus elementos secundarios. 
  
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

No siempre vas a encontrar candidatos para tu nombre ambiguo. En el ejemplo siguiente se muestra la respuesta XML, como un error, cuando no se encuentra ningún candidato.
  
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

## <a name="see-also"></a>Ver también


- [Personas y contactos de EWS en Exchange](people-and-contacts-in-ews-in-exchange.md)
    
- [Expandir grupos de distribución mediante EWS en Exchange 2013](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    

