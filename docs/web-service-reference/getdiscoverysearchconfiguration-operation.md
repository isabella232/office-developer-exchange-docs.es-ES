---
title: Operación GetDiscoverySearchConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8a54a6dc-110c-4972-a8bc-5ddb43c4b857
description: Busque información sobre la EWS GetDiscoverySearchConfiguration operación.
ms.openlocfilehash: a50463e575bf5a4ffdafc357d91563b0ca0486f4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764805"
---
# <a name="getdiscoverysearchconfiguration-operation"></a>Operación GetDiscoverySearchConfiguration

Obtenga información acerca de la operación de EWS **GetDiscoverySearchConfiguration** . 
  
La operación **GetDiscoverySearchConfiguration** devuelve contiene información de configuración de en contexto, guarda las búsquedas de detección y los buzones de correo que están habilitados para la búsqueda de detección. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-getdiscoverysearchconfiguration-operation"></a>Mediante la operación GetDiscoverySearchConfiguration

La operación **GetDiscoverySearchConfiguration** proporciona información de configuración de búsqueda de detección. Las solicitudes de pueden contener uno o varios de los argumentos siguientes: 
  
1. [El identificador de búsqueda](searchid.md) : identifica una búsqueda de descubrimiento guardados. Si este argumento se envía en la solicitud, se omiten los valores de los demás argumentos. 
    
2. [ExpandGroupMembership](expandgroupmembership.md) : indica si se expande la pertenencia a grupos en la respuesta. Un valor de **true** indica que se expande la pertenencia a grupos para que se devuelvan todos los buzones que se puede buscar en la respuesta. Un valor de **false** indica que se devuelve sólo el grupo en la respuesta. 
    
3. [InPlaceHoldConfigurationOnly](inplaceholdconfigurationonly.md) : indica si se devuelven todos los buzones que admite búsquedos además de la configuración de suspensión en contexto. Un valor de **true** indica que se devuelven sólo las configuraciones de suspensión en contexto. Un valor de **false** indica que se devuelven todos los identificadores de buzón de correo que admite búsquedas además de los identificadores de suspensión en contexto. Si este elemento no está presente, el comportamiento predeterminado es el equivalente del valor **false**. 
    
### <a name="getdiscoverysearchconfiguration-operation-soap-headers"></a>Encabezados SOAP de operación de GetDiscoverySearchConfiguration

La operación de **GetDiscoverySearchConfiguration** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla. 
  
|**Nombre de encabezado**|**Element**|**Descripción**|
|:-----|:-----|:-----|
|**ManagementRole** <br/> |[ManagementRole](managementrole.md) <br/> |Identifica las funciones de servidor que son necesarias en orden para el autor de la llamada realizar la solicitud. Este encabezado es aplicable a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de la operación. Este encabezado es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que ha respondido a la solicitud. Este encabezado es aplicable a una respuesta.  <br/> |
   
## <a name="getdiscoverysearchconfiguration-operation-request-example-get-the-discovery-search-configuration-for-a-saved-search"></a>Ejemplo de solicitud de operación de GetDiscoverySearchConfiguration: obtener la configuración de búsqueda de detección para una búsqueda guardada

El siguiente ejemplo de una solicitud de operación **GetDiscoverySearchConfiguration** muestra cómo solicitar la configuración de una búsqueda guardada que se denomina "MyDiscSearchFor-sbrown". Se omiten los argumentos para los elementos de [InPlaceHoldConfigurationOnly](inplaceholdconfigurationonly.md) y [ExpandGroupMembership](expandgroupmembership.md) . 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetDiscoverySearchConfiguration>
         <m:SearchId>MyDiscSearchFor-sbrown</m:SearchId>
         <m:ExpandGroupMembership>true</m:ExpandGroupMembership>
         <m:InPlaceHoldConfigurationOnly>false</m:InPlaceHoldConfigurationOnly>
      </m:GetDiscoverySearchConfiguration>
   </soap:Body>
</soap:Envelope>

```

La solicitud SOAP body contiene los siguientes elementos:
  
- [GetDiscoverySearchConfiguration](getdiscoverysearchconfiguration.md)
    
- [Identificador de búsqueda](searchid.md)
    
- [ExpandGroupMembership](expandgroupmembership.md)
    
- [InPlaceHoldConfigurationOnly](inplaceholdconfigurationonly.md)
    
## <a name="successful-getdiscoverysearchconfiguration-operation-response-request-for-a-single-saved-search"></a>La respuesta es correcta de operación GetDiscoverySearchConfiguration: solicitud para una sola búsqueda guardada

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **GetDiscoverySearchConfiguration** para obtener la configuración de una búsqueda guardada que se denomina "MyDiscSearchFor-sbrown". 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="526" MinorBuildNumber="0" Version="Exchange2013" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetDiscoverySearchConfigurationResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <DiscoverySearchConfigurations>
        <DiscoverySearchConfiguration xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <SearchId>MyDiscSearchFor-sbrown</SearchId>
          <SearchQuery>test item</SearchQuery>
          <SearchableMailboxes>
            <SearchableMailbox>
              <Guid>3c620d04-8b22-432e-92be-5b9321599576</Guid>
              <PrimarySmtpAddress>SBrown@contoso.com</PrimarySmtpAddress>
              <IsExternalMailbox>false</IsExternalMailbox>
              <ExternalEmailAddress/>
              <DisplayName>Steven Brown</DisplayName>
              <IsMembershipGroup>false</IsMembershipGroup>
              <ReferenceId>/o=First/ou=Exchange(FYDILT)/cn=Recipients/cn=313ecf-Steve</ReferenceId>
            </SearchableMailbox>
          </SearchableMailboxes>
        </DiscoverySearchConfiguration>
      </DiscoverySearchConfigurations>
    </GetDiscoverySearchConfigurationResponse>
  </s:Body>
</s:Envelope>
```

La respuesta SOAP body contiene los siguientes elementos:
  
- [GetDiscoverySearchConfigurationResponse](getdiscoverysearchconfigurationresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [DiscoverySearchConfigurations](discoverysearchconfigurations.md)
    
- [DiscoverySearchConfiguration](discoverysearchconfiguration.md)
    
- [Identificador de búsqueda](searchid.md)
    
- [SearchQuery](searchquery.md)
    
- [SearchableMailboxes](searchablemailboxes.md)
    
- [SearchableMailbox](searchablemailbox.md)
    
- [GUID](guid-ex15websvcsotherref.md)
    
- [PrimarySmtpAddress (cadena)](primarysmtpaddress-string.md)
    
- [IsExternalMailbox](isexternalmailbox.md)
    
- [ExternalEmailAddress](externalemailaddress.md)
    
- [DisplayName (cadena)](displayname-string.md)
    
- [IsMembershipGroup](ismembershipgroup.md)
    
- [ReferenceId](referenceid.md)
    
## <a name="successful-getdiscoverysearchconfiguration-operation-response-request-for-in-place-holds"></a>La respuesta es correcta de operación GetDiscoverySearchConfiguration: solicitud de suspensiones en contexto

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **GetDiscoverySearchConfiguration** para sólo obtener en contexto contiene. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetDiscoverySearchConfigurationResponse ResponseClass="Success" 
                                               xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <DiscoverySearchConfigurations>
            <DiscoverySearchConfiguration xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <SearchId>MyDiscSearchFor-sbrown</SearchId>
               <SearchQuery>test item</SearchQuery>
               <InPlaceHoldIdentity>3f37d90f53144558a80814ef0272749a9</InPlaceHoldIdentity>
               <ManagedByOrganization/>
            </DiscoverySearchConfiguration>
            <DiscoverySearchConfiguration xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <SearchId>MyDiscSearch</SearchId>
               <SearchQuery>test</SearchQuery>
               <InPlaceHoldIdentity>6ea486f0f3f140efb044682a2e782abdf</InPlaceHoldIdentity>
               <ManagedByOrganization/>
            </DiscoverySearchConfiguration>
         </DiscoverySearchConfigurations>
      </GetDiscoverySearchConfigurationResponse>
   </s:Body>
</s:Envelope>

```

La respuesta SOAP body contiene los siguientes elementos:
  
- [GetDiscoverySearchConfigurationResponse](getdiscoverysearchconfigurationresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [DiscoverySearchConfigurations](discoverysearchconfigurations.md)
    
- [DiscoverySearchConfiguration](discoverysearchconfiguration.md)
    
- [Identificador de búsqueda](searchid.md)
    
- [SearchQuery](searchquery.md)
    
- [InPlaceHoldIdentity](inplaceholdidentity.md)
    
- [ManagedByOrganization](managedbyorganization.md)
    
## <a name="successful-getdiscoverysearchconfiguration-operation-response-request-for-all-saved-discovery-search-configurations"></a>La respuesta es correcta de operación GetDiscoverySearchConfiguration: solicitud de todos los guardan detección configuraciones de búsqueda

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **GetDiscoverySearchConfiguration** para obtener todas las búsquedas de descubrimiento guardados. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetDiscoverySearchConfigurationResponse ResponseClass="Success" 
                                               xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <DiscoverySearchConfigurations>
            <DiscoverySearchConfiguration xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <SearchId>MyDiscSearchFor-sbrown</SearchId>
               <SearchQuery>test item</SearchQuery>
               <SearchableMailboxes>
                  <SearchableMailbox>
                     <Guid>3c620d04-8b33-435e-95be-5b9351599576</Guid>
                     <PrimarySmtpAddress>SBrown@contoso.com</PrimarySmtpAddress>
                     <IsExternalMailbox>false</IsExternalMailbox>
                     <ExternalEmailAddress/>
                     <DisplayName>Steven Brown</DisplayName>
                     <IsMembershipGroup>false</IsMembershipGroup>
                     <ReferenceId>/o=First/ou=Exchange (FYLT)/cn=Recipients/cn=35381a742f0e47e395c8601a60d13ecz-Steve</ReferenceId>
                  </SearchableMailbox>
               </SearchableMailboxes>
            </DiscoverySearchConfiguration>
            <DiscoverySearchConfiguration xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <SearchId>MyDiscSearch</SearchId>
               <SearchQuery>test</SearchQuery>
               <SearchableMailboxes>
                  <SearchableMailbox>
                     <Guid>e788c4b0-54a2-458c-83b2-22d5bb02b23f</Guid>
                     <PrimarySmtpAddress>Administrator@contoso.com</PrimarySmtpAddress>
                     <IsExternalMailbox>false</IsExternalMailbox>
                     <ExternalEmailAddress/>
                     <DisplayName>Administrator</DisplayName>
                     <IsMembershipGroup>false</IsMembershipGroup>
                     <ReferenceId>/o=First/ou=Exchange (FYLT)/cn=Recipients/cn=ebez7871332d4595abe1c62962911a58-Admin</ReferenceId>
                  </SearchableMailbox>
                  <SearchableMailbox>
                     <Guid>6f6cff39-8967-4a60-b43f-328413c25199</Guid>
                     <PrimarySmtpAddress>ADavis@contoso.com</PrimarySmtpAddress>
                     <IsExternalMailbox>false</IsExternalMailbox>
                     <ExternalEmailAddress/>
                     <DisplayName>Anthony Davis</DisplayName>
                     <IsMembershipGroup>false</IsMembershipGroup>
                     <ReferenceId>/o=First/ou=Exchange (FYLT)/cn=Recipients/cn=f10c9f70519844beb04101d8f40c572z-Antho</ReferenceId>
                  </SearchableMailbox>
               </SearchableMailboxes>
            </DiscoverySearchConfiguration>
         </DiscoverySearchConfigurations>
      </GetDiscoverySearchConfigurationResponse>
   </s:Body>
</s:Envelope>
```

La respuesta SOAP body contiene los siguientes elementos:
  
- [GetDiscoverySearchConfigurationResponse](getdiscoverysearchconfigurationresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [DiscoverySearchConfigurations](discoverysearchconfigurations.md)
    
- [DiscoverySearchConfiguration](discoverysearchconfiguration.md)
    
- [Identificador de búsqueda](searchid.md)
    
- [SearchQuery](searchquery.md)
    
- [SearchableMailboxes](searchablemailboxes.md)
    
- [SearchableMailbox](searchablemailbox.md)
    
- [GUID](guid-ex15websvcsotherref.md)
    
- [PrimarySmtpAddress (cadena)](primarysmtpaddress-string.md)
    
- [IsExternalMailbox](isexternalmailbox.md)
    
- [ExternalEmailAddress](externalemailaddress.md)
    
- [DisplayName (cadena)](displayname-string.md)
    
- [IsMembershipGroup](ismembershipgroup.md)
    
- [ReferenceId](referenceid.md)
    
## <a name="getdiscoverysearchconfiguration-operation-error-response"></a>Respuesta de error de la operación de GetDiscoverySearchConfiguration

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **GetDiscoverySearchConfiguration** . Esta es una respuesta a una solicitud para obtener una búsqueda guardada que no se encuentra en el servidor. 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetDiscoverySearchConfigurationResponse ResponseClass="Error" 
                                               xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Search configuration corresponding to the search id was not found.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         <DiscoverySearchConfigurations/>
      </GetDiscoverySearchConfigurationResponse>
   </s:Body>
</s:Envelope>

```

La respuesta de error SOAP body contiene los siguientes elementos:
  
- [GetDiscoverySearchConfigurationResponse](getdiscoverysearchconfigurationresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [DiscoverySearchConfigurations](discoverysearchconfigurations.md)
    
Para códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Vea también

- [Operaciones de EWS en Exchange](ews-operations-in-exchange.md)
    
- [GetSearchableMailboxes](getsearchablemailboxes.md)
    
- [SearchMailboxes](searchmailboxes.md)
    
- [GetHoldOnMailboxes](getholdonmailboxes.md)
    
- [SetHoldOnMailboxes](setholdonmailboxes.md)
    
- [GetNonIndexableItemDetails](getnonindexableitemdetails.md)
    
- [GetNonIndexableItemStatistics](getnonindexableitemstatistics.md)
    

