---
title: Obtener la configuración de usuario de Exchange mediante el uso de detección automática
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 6d90c305-4802-4e18-8d52-f60349feaa8d
description: Obtenga información sobre cómo obtener la configuración de usuario de un servidor de Exchange mediante detección automática.
localization_priority: Priority
ms.openlocfilehash: 5f7ea04e6b04f674d4cb481cf9243d46437d6950
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528002"
---
# <a name="get-user-settings-from-exchange-by-using-autodiscover"></a>Obtener la configuración de usuario de Exchange mediante el uso de detección automática

Obtenga información sobre cómo obtener la configuración de usuario de un servidor de Exchange mediante detección automática.
  
La detección automática simplifica la configuración de las aplicaciones al facilitar el acceso a la información de configuración del usuario usando solo la dirección de correo electrónico y la contraseña del usuario. Hay disponible una [serie de opciones de configuración de usuario](https://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) a través de la detección automática, como el nombre para mostrar del usuario o la dirección URL del servicio Web externo. 
  
Puede usar una de las siguientes tecnologías de desarrollo para recuperar la configuración de usuario del servicio Detección automática:
  
- Introducción [a las aplicaciones de cliente de la API administrada de EWS](get-started-with-ews-managed-api-client-applications.md)
    
- El [servicio Web de detección automática de SOAP](https://msdn.microsoft.com/library/61c21ea9-7fea-4f56-8ada-bf80e1e6b074%28Office.15%29.aspx)
    
- El [servicio Web detección automática de POX](https://msdn.microsoft.com/library/877152f0-f4b1-4f63-b2ce-924f4bdf2d20%28Office.15%29.aspx)
    
La API administrada de EWS proporciona una interfaz basada en objetos para recuperar la configuración de usuario. Si su aplicación cliente usa un código administrado, le recomendamos que use la API administrada de EWS. Si usa la API administrada de EWS, determine si la configuración que necesita está disponible en la enumeración [Microsoft. Exchange. webservices. Autodiscover. UserSettingName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.usersettingname%28v=EXCHG.80%29.aspx) . Si no es así, es posible que quiera usar los servicios de detección automática de POX o SOAP. 
  
Si usa un servicio Web, le sugerimos que use el servicio de detección automática de SOAP, ya que admite un conjunto de características más amplio que el servicio Detección automática de POX. Si el servicio Detección automática de SOAP no está disponible, el servicio Detección automática de POX es una buena alternativa.
  
## <a name="set-up-to-get-user-settings"></a>Configurar para obtener la configuración del usuario
<a name="bk_Prereq"> </a>

Antes de obtener la configuración de usuario mediante el servicio Detección automática, asegúrese de que tiene acceso a lo siguiente:
  
- Si usa la API administrada de EWS o el servicio de detección automática basado en POX, Exchange Online, Exchange online como parte de Office 365, o un servidor que ejecute una versión de Exchange a partir de Exchange 2007 SP1. 
    
- Si usa el servicio de detección automática basado en SOAP, Exchange online o una versión de Exchange que empiece por Exchange 2010.
    
> [!NOTE]
> Si usa la API administrada de EWS, tendrá que [proporcionar un método de devolución de llamada de validación de certificados](how-to-validate-a-server-certificate-for-the-ews-managed-api.md) en algunas circunstancias. También es posible que necesite un método de devolución de llamada de validación de certificados con algunas bibliotecas de proxy generadas, como las creadas por Visual Studio. 
  
## <a name="get-user-settings-by-using-the-ews-managed-api"></a>Obtener la configuración de usuario mediante la API administrada de EWS
<a name="bk_Managed"> </a>

Puede usar el método [GetUserSettings](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice.getusersettings%28v=exchg.80%29.aspx) para recuperar la información de configuración de un usuario, como se muestra en el ejemplo siguiente. En este ejemplo, puede especificar una matriz de opciones de configuración de usuario para devolver (de la que están disponibles en la enumeración [UserSettingName](https://msdn.microsoft.com/library/exchange/microsoft.exchange.webservices.autodiscover.usersettingname%28v=exchg.80%29.aspx) ) y el método seguirá las respuestas de redirección del servidor de Exchange. 
  
```cs
using System;
using System.Net;
using Microsoft.Exchange.WebServices.Autodiscover;
public static GetUserSettingsResponse GetUserSettings(
    AutodiscoverService service,
    string emailAddress,
    int maxHops,
    params UserSettingName[] settings)
{
    Uri url = null;
    GetUserSettingsResponse response = null;
    for (int attempt = 0; attempt < maxHops; attempt++)
    {
        service.Url = url;
        service.EnableScpLookup = (attempt < 2);
        response = service.GetUserSettings(emailAddress, settings);
        if (response.ErrorCode == AutodiscoverErrorCode.RedirectAddress)
        {
            url = new Uri(response.RedirectTarget);
        }
        else if (response.ErrorCode == AutodiscoverErrorCode.RedirectUrl)
        {
            url = new Uri(response.RedirectTarget);
        }
        else
        {
            return response;
        }
    }
    throw new Exception("No suitable Autodiscover endpoint was found.");
}
```

Puede analizar la colección devuelta para obtener acceso a cada par clave-valor de la matriz de configuración del usuario. En el siguiente ejemplo se muestra cómo analizar mediante cada elemento devuelto y mostrar el nombre y el valor de cada par clave-valor.
  
```cs
// Display each retrieved value. The settings are part of a key/value pair.
// userresponse is a GetUserSettingsResonse object.
foreach (KeyValuePair<UserSettingName, Object> usersetting in userresponse.Settings)
{
    Console.WriteLine(usersetting.Key.ToString() + ": " + usersetting.Value);
}
```

De manera alternativa, puede obtener el valor de una configuración específica. En el siguiente ejemplo, se muestra la configuración **UserDisplayName** . 
  
```cs
// Display a specific setting, such as UserDisplayName.
Console.WriteLine(userresponse.Settings[UserSettingName.UserDisplayName]);
```

## <a name="get-user-settings-by-using-soap-autodiscover"></a>Obtener la configuración del usuario mediante la detección automática de SOAP
<a name="bk_SOAP"> </a>

Si no está usando la API administrada de EWS, le recomendamos que use el servicio Web de detección automática de SOAP. Use el servicio Web de detección automática de POX si el servicio Web de detección automática de SOAP produce un error o no está disponible. 
  
Para obtener la configuración del usuario, use la [operación GetUserSettings (SOAP)](https://msdn.microsoft.com/library/758d965c-ef63-4de4-9120-e293abf14ff8%28Office.15%29.aspx). La configuración solicitada se devuelve como [elementos UserSetting](https://msdn.microsoft.com/library/aac6dc31-edd2-49d7-b845-1df4d77da58c%28Office.15%29.aspx).
  
En el ejemplo siguiente se muestra una solicitud de detección automática de SOAP para obtener la configuración del usuario del servidor.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>mara@contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>UserDisplayName</a:Setting>
          <a:Setting>UserDN</a:Setting>
          <a:Setting>UserDeploymentId</a:Setting>
          <a:Setting>InternalMailboxServer</a:Setting>
          <a:Setting>MailboxDN</a:Setting>
          <a:Setting>PublicFolderServer</a:Setting>
          <a:Setting>ActiveDirectoryServer</a:Setting>
          <a:Setting>ExternalMailboxServer</a:Setting>
          <a:Setting>EcpDeliveryReportUrlFragment</a:Setting>
          <a:Setting>EcpPublishingUrlFragment</a:Setting>
          <a:Setting>EcpTextMessagingUrlFragment</a:Setting>
          <a:Setting>ExternalEwsUrl</a:Setting>
          <a:Setting>CasVersion</a:Setting>
          <a:Setting>EwsSupportedSchemas</a:Setting>
          <a:Setting>GroupingInformation</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>
```

En el ejemplo siguiente se muestra la respuesta SOAP que devuelve el servidor después de analizar la solicitud del cliente. La respuesta contiene solo la configuración solicitada, si existe.
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/" xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>15</h:MajorVersion>
      <h:MinorVersion>0</h:MinorVersion>
      <h:MajorBuildNumber>160</h:MajorBuildNumber>
      <h:MinorBuildNumber>4</h:MinorBuildNumber>
      <h:Version>Exchange2013</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover">
      <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
        <ErrorCode>NoError</ErrorCode>
        <ErrorMessage />
        <UserResponses>
          <UserResponse>
            <ErrorCode>NoError</ErrorCode>
            <ErrorMessage>No error.</ErrorMessage>
            <RedirectTarget i:nil="true" />
            <UserSettingErrors />
            <UserSettings>
              <UserSetting i:type="StringSetting">
                <Name>UserDisplayName</Name>
                <Value>Mara Whitley</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>UserDN</Name>
                <Value>/o=microsoft/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=mara</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>UserDeploymentId</Name>
                <Value>649d50b8-a1ce-4bac-8ace-2321   e463f701</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>CasVersion</Name>
                <Value>15.01.0160.004</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>EwsSupportedSchemas</Name>
                <Value>Exchange2007, Exchange2007_SP1, Exchange2010, Exchange2010_SP1, Exchange2010_SP2, Exchange2013</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>InternalMailboxServer</Name>
                <Value>mail.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>ActiveDirectoryServer</Name>
                <Value>dc.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>MailboxDN</Name>
                <Value>/o=microsoft/ou=Exchange Administrative Group 
                  (FYDIBOHF23SPDLT)/cn=Configuration/cn=Servers/cn=mail.contoso.com/cn=Contoso Private MDB</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>PublicFolderServer</Name>
                <Value>public.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>EcpDeliveryReportUrlFragment</Name>
                <Value>PersonalSettings/DeliveryReport.aspx?exsvurl=1&amp;amp;IsOWA=&amp;lt;IsOWA&amp;gt;&amp;amp;MsgID=&amp;lt;MsgID&amp;gt;&amp;amp;Mbx=&amp;lt;Mbx&amp;gt;</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>EcpTextMessagingUrlFragment</Name>
                <Value>?p=sms/textmessaging.slab&amp;amp;exsvurl=1</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>EcpPublishingUrlFragment</Name>
                <Value>customize/calendarpublishing.slab?exsvurl=1&amp;amp;FldID=&amp;lt;FldID&amp;gt;</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>ExternalEwsUrl</Name>
                <Value>https://mail.contoso.com/EWS/Exchange.asmx</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>ExternalMailboxServer</Name>
                <Value>mail.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>GroupingInformation</Name>
                <Value>CONTOSO-1</Value>
              </UserSetting>
            </UserSettings>
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope
```

## <a name="get-user-settings-by-using-pox-autodiscover"></a>Obtener la configuración de usuario mediante detección automática de POX
<a name="bk_POX"> </a>

Aunque se recomienda usar el servicio Web de detección automática de SOAP, el servicio Web de detección automática de POX es una buena opción de copia de seguridad para los momentos en los que SOAP no está disponible. Por ejemplo, Exchange 2007 no admite el servicio Web de detección automática de SOAP, por lo que si el destino es Exchange 2007, tiene que usar el servicio Web detección automática de POX. A diferencia del servicio Web de detección automática de SOAP, el servicio Detección automática de POX no permite solicitar una configuración específica. En su lugar, el servidor devuelve una lista completa de las opciones de configuración disponibles como elementos secundarios del [elemento Protocol](https://msdn.microsoft.com/library/f77e4d66-6fdd-4999-9339-f7d7f9c86f44%28Office.15%29.aspx).
  
En el ejemplo siguiente se muestra una solicitud de detección automática de POX para obtener la configuración del usuario del servidor. El siguiente XML se envía al servidor a través de un HTTP POST.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>mara@contoso.com</EMailAddress>
    <AcceptableResponseSchema>https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

En el ejemplo siguiente se muestra la respuesta de POX que devuelve el servidor.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    <User>
      <DisplayName>Mara Whitley</DisplayName>
      <LegacyDN>/o=First Organization/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=f5eeabead90d4b6fb51d6379474692cd-Mara</LegacyDN>
      <AutoDiscoverSMTPAddress>mara@contoso.com</AutoDiscoverSMTPAddress>
      <DeploymentId>50817eff-b925-4578-a0db-13bfc635e7a5</DeploymentId>
    </User>
    <Account>
      <AccountType>email</AccountType>
      <Action>settings</Action>
      <MicrosoftOnline>False</MicrosoftOnline>
      <Protocol>
        <Type>EXCH</Type>
        <Server>5f76be3c-9138-4f66-85e0-21bc23ca35f0@contoso.com</Server>
        <ServerDN>/o=First Organization/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Configuration/cn=Servers/cn=5f76be3c-9138-4f66-85e0-21bc23ca35f0@contoso.com</ServerDN>
        <ServerVersion>73C08204</ServerVersion>
        <MdbDN>/o=First Organization/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Configuration/cn=Servers/cn=5f76be3c-9138-4f66-85e0-21bc23ca35f0@contoso.com/cn=Microsoft Private MDB</MdbDN>
        <PublicFolderServer>public.contoso.com</PublicFolderServer>
        <AD>dc.contoso.com</AD>
        <ASUrl>https://mail.contoso.com/EWS/Exchange.asmx</ASUrl>
        <EwsUrl>https://mail.contoso.com/EWS/Exchange.asmx</EwsUrl>
        <EmwsUrl>https://mail.contoso.com/EWS/Exchange.asmx</EmwsUrl>
        <EcpUrl>https://mail.contoso.com/ecp/</EcpUrl>
        <EcpUrl-um>?rfr=olk&amp;amp;p=customize/voicemail.aspx&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-um>
        <EcpUrl-aggr>?rfr=olk&amp;amp;p=personalsettings/EmailSubscriptions.slab&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-aggr>
        <EcpUrl-mt>PersonalSettings/DeliveryReport.aspx?rfr=olk&amp;amp;exsvurl=1&amp;amp;IsOWA=&amp;lt;IsOWA&amp;gt;&amp;amp;MsgID=&amp;lt;MsgID&amp;gt;&amp;amp;Mbx=&amp;lt;Mbx&amp;gt;&amp;amp;realm=contoso.com</EcpUrl-mt>
        <EcpUrl-ret>?rfr=olk&amp;amp;p=organize/retentionpolicytags.slab&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-ret>
        <EcpUrl-sms>?rfr=olk&amp;amp;p=sms/textmessaging.slab&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-sms>
        <EcpUrl-publish>customize/calendarpublishing.slab?rfr=olk&amp;amp;exsvurl=1&amp;amp;FldID=&amp;lt;FldID&amp;gt;&amp;amp;realm=contoso.com</EcpUrl-publish>
        <EcpUrl-photo>PersonalSettings/EditAccount.aspx?rfr=olk&amp;amp;chgPhoto=1&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-photo>
        <EcpUrl-tm>?rfr=olk&amp;amp;ftr=TeamMailbox&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-tm>
        <EcpUrl-tmCreating>?rfr=olk&amp;amp;ftr=TeamMailboxCreating&amp;amp;SPUrl=&amp;lt;SPUrl&amp;gt;&amp;amp;Title=&amp;lt;Title&amp;gt;&amp;amp;SPTMAppUrl=&amp;lt;SPTMAppUrl&amp;gt;&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-tmCreating>
        <EcpUrl-tmEditing>?rfr=olk&amp;amp;ftr=TeamMailboxEditing&amp;amp;Id=&amp;lt;Id&amp;gt;&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-tmEditing>
        <EcpUrl-extinstall>Extension/InstalledExtensions.slab?rfr=olk&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-extinstall>
        <OOFUrl>https://mail.contoso.com/EWS/Exchange.asmx</OOFUrl>
        <UMUrl>https://mail.contoso.com/EWS/UM2007Legacy.asmx</UMUrl>
        <OABUrl>https://mail.contoso.com/OAB/c21c7bc2-53b3-4ddc-ad89-1219b486c37c/</OABUrl>
        <ServerExclusiveConnect>off</ServerExclusiveConnect>
      </Protocol>
      <Protocol>
        <Type>EXPR</Type>
        <Server>mail.contoso.com</Server>
        <SSL>Off</SSL>
        <AuthPackage>Ntlm</AuthPackage>
        <ServerExclusiveConnect>on</ServerExclusiveConnect>
        <CertPrincipalName>None</CertPrincipalName>
      </Protocol>
      <Protocol>
        <Type>WEB</Type>
        <Internal>
          <OWAUrl AuthenticationMethod="Basic, Fba">https://mail.contoso.com/owa/</OWAUrl>
          <Protocol>
            <Type>EXCH</Type>
            <ASUrl>https://mail.contoso.com/EWS/Exchange.asmx</ASUrl>
          </Protocol>
        </Internal>
      </Protocol>
    </Account>
  </Response>
</Autodiscover>
```

## <a name="next-steps"></a>Siguientes pasos
<a name="bk_Next"> </a>

Una vez que haya recuperado los detalles de configuración necesarios para el usuario desde el servidor, estará preparado para comunicarse con Exchange y realizar las acciones que debe realizar la aplicación. Lo que haga a continuación depende de cómo se comunique con Exchange y lo que desea conseguir. Si necesita cierta inspiración y está usando EWS, puede explorar los ejemplos de código de [Exchange 101](https://code.msdn.microsoft.com/exchange/Exchange-2013-101-Code-3c38582c) para algunas ideas. 
  
## <a name="see-also"></a>Vea también


- [Detección automática en Exchange](autodiscover-for-exchange.md)
    
- [API administrada Servicios Web Exchange (EWS)](https://msdn.microsoft.com/library/exchange/jj220535%28v=exchg.80%29.aspx)
    
- [Referencia del servicio Web de detección automática de SOAP para Exchange](https://msdn.microsoft.com/library/61c21ea9-7fea-4f56-8ada-bf80e1e6b074%28Office.15%29.aspx)
    
- [Referencia de servicio Web de detección automática de POX para Exchange](https://msdn.microsoft.com/library/877152f0-f4b1-4f63-b2ce-924f4bdf2d20%28Office.15%29.aspx)
    

