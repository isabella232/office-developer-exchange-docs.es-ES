---
title: Usar autodetección para buscar puntos de conexión
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 03896542-549b-4c45-973c-98f9025ea26c
description: Descubra cómo usar el servicio de detección automática para dirigir la aplicación cliente al servidor Exchange correcto.
localization_priority: Priority
ms.openlocfilehash: c1895fa0d2cce489467a726614e9457052624ef6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527596"
---
# <a name="use-autodiscover-to-find-connection-points"></a>Usar autodetección para buscar puntos de conexión

Descubra cómo usar el servicio de detección automática para dirigir la aplicación cliente al servidor Exchange correcto.
  
El servicio Detección automática de Exchange proporciona a la aplicación cliente opciones de configuración para las cuentas de correo electrónico que se hospedan en Exchange Online, Exchange online como parte de Office 365, o un servidor de Exchange que ejecuta una versión de Exchange que empieza por Exchange 2013. El servicio de detección automática es un servicio Web que proporciona opciones de configuración. El servicio de detección automática es un servicio Web que proporciona información de configuración de Exchange Server a la aplicación cliente. Las aplicaciones cliente usan detección automática para determinar el punto final del servicio Detección automática para un buzón específico. En este artículo se explica cómo seguir las respuestas de un servidor de Exchange para encontrar el punto de conexión correcto. 
  
Para obtener información sobre cómo obtener las opciones de configuración de direcciones de correo electrónico, consulte [obtener configuración de usuario de Exchange mediante la detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) y [obtener la configuración de dominio de un servidor de Exchange](how-to-get-domain-settings-from-an-exchange-server.md).
  
> [!NOTE]
> El proceso para buscar el punto de conexión correcto forma parte de la solicitud de configuración de usuario o dominio. El servicio Detección automática usa una serie de respuestas de redirección para enviar la aplicación cliente al punto de conexión correcto para una dirección de correo electrónico. 
  
Puede usar una de las siguientes tecnologías de desarrollo de Exchange para tener acceso al servicio de detección automática:

- La API administrada de servicios Web Exchange (EWS)
    
- EWS
    
Si usa EWS, puede usar los métodos siguientes para recuperar la configuración de usuario:
    
- El servicio Detección automática basado en SOAP
    
- El servicio Detección automática XML (POX)
    
- Un proxy generado automáticamente se ha generado del servicio Detección automática de XML o SOAP
    
Para obtener más información sobre estos métodos, vea [Detección automática en Exchange](autodiscover-for-exchange.md).

Para obtener más información sobre estas tecnologías de desarrollo de Exchange, vea [explorar la API administrada de EWS, EWS y servicios Web de Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md). 

La API administrada de EWS proporciona una interfaz basada en objetos para recuperar la configuración de usuario. Si su aplicación cliente usa un código administrado, le recomendamos que use la API administrada de EWS. La interfaz de la API administrada de EWS está mejor optimizada para un modelo de objetos simples que el típico proxy de servicio web generado automáticamente.  
  
Si está usando EWS, le sugerimos que use el servicio Detección automática de SOAP, ya que admite un conjunto superior de características que el servicio Detección automática de POX.
  
## <a name="prerequisites-for-finding-an-endpoint"></a>Requisitos previos para buscar un extremo
<a name="bk_Prereq"> </a>

Antes de crear una aplicación cliente que use el servicio de detección automática, debe tener acceso a lo siguiente:
  
- Exchange online o un servidor que ejecute una versión de Exchange a partir de Exchange 2007 SP1. Si usa el servicio de detección automática basado en SOAP, Exchange online o una versión de Exchange que empiece por Exchange 2010.
    
- Un servidor Exchange que está configurado para aceptar conexiones de su aplicación cliente. Para obtener información sobre cómo configurar su servidor de Exchange, vea [Controlar el acceso de la aplicación de cliente a EWS en Exchange](controlling-client-application-access-to-ews-in-exchange.md).
    
- Una cuenta que esté autorizada para usar EWS. Para obtener información sobre cómo configurar una cuenta, vea [Controlar el acceso de la aplicación de cliente a EWS en Exchange](controlling-client-application-access-to-ews-in-exchange.md).
    
> [!NOTE]
> Si está usando la API administrada de EWS, debe proporcionar una devolución de llamada de validación de certificado en algunas circunstancias. También puede necesitar una devolución de llamada de validación de certificado con algunas bibliotecas de proxy generadas, como las que se han creado mediante Visual Studio. Para obtener más información, vea [Validar un certificado de servidor de la API de administración de EWS](how-to-validate-a-server-certificate-for-the-ews-managed-api.md). 
  
### <a name="core-concepts-for-finding-an-endpoint"></a>Conceptos básicos para buscar un extremo
<a name="bk_Core"> </a>

Antes de usar la detección automática para buscar un extremo, debe estar familiarizado con los conceptos que se enumeran en la siguiente tabla.
  
|**Concepto**|**Descripción**|
|:-----|:-----|
|[Detección automática en Exchange](autodiscover-for-exchange.md) <br/> |Proporciona información general del funcionamiento del servicio Detección automática.  <br/> |
   
Si usa la API administrada de EWS, usa la clase [Microsoft.Exchange.WebServices.Data.ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) del espacio de nombres [Microsoft.Exchange.WebServices.Data](https://msdn.microsoft.com/library/dd633907%28v=exchg.80%29.aspx) para administrar la conexión con EWS. Para usar los ejemplos de código de la API administrada de EWS de este artículo, debe hacer referencia a los siguientes espacios de nombres en el código: 
  
- **System.Net**
    
- **Microsoft.Exchange.WebServices.Data.ExchangeService**
    
## <a name="find-the-correct-endpoint-by-using-the-ews-managed-api"></a>Buscar el punto de conexión correcto mediante la API administrada de EWS
<a name="bk_Managed"> </a>

Si usa la API administrada de EWS, las llamadas al servicio Detección automática se administran mediante la clase **ExchangeService** . Para determinar el punto de conexión correcto de una cuenta de correo electrónico, llame al método **AutodiscoverUrl** en un objeto **[ExchangeService]** . En el siguiente ejemplo de código se muestra cómo establecer el extremo del servicio Web EWS para una dirección de correo electrónico en el archivo Exchange. asmx en el servidor de acceso de cliente correcto mediante la API administrada de EWS. 
  
```cs
NetworkCredential credentials = new NetworkCredential(securelyStoredEmail, securelyStoredPassword);
ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2013);
service.Credentials = credentials;
service.AutodiscoverUrl("User1@contoso.com");
```

## <a name="find-the-correct-endpoint-by-using-ews"></a>Buscar el punto de conexión correcto mediante EWS
<a name="bk_SOAP"> </a>

El servicio Detección automática de SOAP puede usar una serie de solicitudes y respuestas para dirigir la aplicación al punto de conexión correcto de EWS. Para obtener información acerca del proceso para determinar el punto de conexión correcto para una cuenta de correo electrónico, consulte [detección automática de Exchange](autodiscover-for-exchange.md). Los siguientes ejemplos de XML muestran la serie de solicitudes y respuestas que puede esperar al realizar una solicitud de detección automática de SOAP para encontrar el punto de conexión correcto.
  
### <a name="soap-autodiscover-endpoint-request"></a>Solicitud de extremo de detección automática de SOAP

En el ejemplo siguiente se muestra una solicitud XML que se envía al servicio de detección automática para encontrar el punto de conexión correcto.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://mail.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>User1@Contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>InternalEwsUrl</a:Setting>
          <a:Setting>ExternalEwsUrl</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>

```

### <a name="soap-autodiscover-redirection-response"></a>Respuesta de redireccionamiento de detección automática de SOAP

El servicio Detección automática puede responder con una de dos respuestas de redirección: una redirección HTTP 302 o una respuesta de redireccionamiento SOAP. Si la respuesta del servidor de Exchange es una redirección HTTP 302, la aplicación cliente debe validar que la dirección de redireccionamiento es aceptable y, a continuación, seguir la respuesta de redireccionamiento.
  
> [!IMPORTANT]
> Para consultar los criterios para validar una respuesta de redireccionamiento, consulte [detección automática de Exchange](autodiscover-for-exchange.md). 
  
Si el servicio Detección automática devuelve una respuesta de redirección, indicada por el elemento [ErrorCode](https://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) del elemento **UserResponse** , la aplicación cliente debe usar el elemento **RedirectTarget** para construir una nueva solicitud de configuración que se envía al servidor especificado en la respuesta de redireccionamiento. En el ejemplo siguiente se muestra una respuesta de redirección del servidor. 
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/" xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>15</h:MajorVersion>
      <h:MinorVersion>0</h:MinorVersion>
      <h:MajorBuildNumber>682</h:MajorBuildNumber>
      <h:MinorBuildNumber>1</h:MinorBuildNumber>
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
            <ErrorCode>RedirectAddress</ErrorCode>
            <ErrorMessage>Redirection address.</ErrorMessage>
            <RedirectTarget>User1@mail.Contoso.com</RedirectTarget>
            <UserSettingErrors />
            <UserSettings />
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope>

```

Después de una redirección, el cliente usa la dirección URL de redireccionamiento para preparar otra solicitud. El siguiente código muestra un ejemplo de la solicitud que ha creado a partir de la respuesta de redireccionamiento.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>User1@mail.Contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>InternalEwsUrl</a:Setting>
          <a:Setting>ExternalEwsUrl</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>

```

Cuando la aplicación cliente se haya redirigido al punto de conexión correcto del servicio Detección automática, el servidor enviará una respuesta con el elemento [ErrorCode](https://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) del elemento **UserResponse** establecido en **NoError** y que contenga la configuración de usuario solicitada. Solo se devuelven las configuraciones de usuario solicitadas, **InternalEwsUrl** y **ExternalEwsUrl**. En el ejemplo siguiente se muestra la respuesta del servidor. 
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/" 
        xmlns:a="http://www.w3.org/2005/08/addressing">
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
                <Name>InternalEwsUrl</Name>
                <Value>https://server.Contoso.com/ews/exchange.asmx</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>ExternalEwsUrl</Name>
                <Value>https://server.Contoso.com/ews/exchange.asmx</Value>
              </UserSetting>
            </UserSettings>
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope>
```

## <a name="next-steps"></a>Siguientes pasos
<a name="bk_Next"> </a>

La búsqueda del extremo siguiendo el proceso de detección automática devuelve la configuración de dominio o usuario solicitada. Para obtener información sobre cómo realizar una solicitud para una configuración específica, vea los siguientes artículos:
  
- [Obtener la configuración de dominio de un servidor de Exchange](how-to-get-domain-settings-from-an-exchange-server.md)    
- [Obtener la configuración de usuario de Exchange mediante el uso de detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
## <a name="see-also"></a>Vea también

- [Configurar la aplicación EWS](setting-up-your-ews-application.md)   
- [Detección automática en Exchange](autodiscover-for-exchange.md)    
- [Referencia del servicio web de Detección automática para Exchange](https://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)    
- [Referencia EWS para Exchange](https://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx)
    

