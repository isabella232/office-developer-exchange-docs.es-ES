---
title: Redirigir solicitudes de la jerarquía de carpetas públicas
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: ec35df8e-4d75-4aa1-8b9c-ae1db7e05772
description: Todas las solicitudes de información de carpetas públicas que requieren conocimiento de la jerarquía de carpetas públicas, como mover, actualizar, eliminar o buscar carpetas públicas, deben enrutándose al buzón de jerarquía de carpetas públicas predeterminado para el usuario determinado. Para enrutar las solicitudes a ese buzón, debe establecer los encabezados X-AnchorMailbox y X-PublicFolderMailbox en valores específicos devueltos por el servicio de detección automática.
ms.openlocfilehash: e86e1956db33b7ad8e654a22b980900b4f59dd87
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513125"
---
# <a name="route-public-folder-hierarchy-requests"></a>Redirigir solicitudes de la jerarquía de carpetas públicas

Todas las solicitudes de información de carpetas públicas que requieren conocimiento de la jerarquía de carpetas públicas, como mover, actualizar, eliminar o buscar carpetas públicas, deben enrutándose al buzón de jerarquía de carpetas públicas predeterminado para el usuario determinado. Para enrutar las solicitudes a ese buzón, debe establecer los encabezados **X-AnchorMailbox** y **X-PublicFolderMailbox** en valores específicos devueltos por el servicio de detección automática. 
  
**Información general sobre carpetas públicas**

|Encabezado|¿Qué necesito?|¿Cómo lo puedo obtener?|
|:-----|:-----|:-----|
|**X-AnchorMailbox** <br/> |El [valor PublicFolderInformation](https://msdn.microsoft.com/library/dn751006%28v=exchg.150%29.aspx) de una respuesta SOAP de Detección automática de [GetUserSettings,](https://msdn.microsoft.com/library/office/dd877096%28v=exchg.150%29.aspx) que se convierte en el valor del encabezado **X-AnchorMailbox.**<br/><br/> ![Respuesta X-AnchorMailbox](media/Ex15_PF_PFH_Anchor.png)| 1. Envíe una **solicitud GetUserSetting** con la dirección SMTP del buzón del usuario.<br/><br/>2. Almacenar en caché el valor del **elemento PublicFolderInformation** que devuelve el servicio de detección automática. Puede ser una caché de una llamada de detección automática existente en el código, una nueva llamada [GetUserSettings](#bk_getpfinfoewsma) de la API administrada ews o una [solicitud SOAP GetUserSettings](#bk_getpfinfoews).  <br/><br/>3. Use el **elemento PublicFolderInformation** para rellenar el valor del **encabezado X-AnchorMailbox.** El valor del elemento **PublicFolderInformation** es una dirección SMTP.  <br/> |
|**X-PublicFolderMailbox** <br/> |Valor [de](https://msdn.microsoft.com/library/bb204084%28v=exchg.150%29.aspx) servidor de una [respuesta de detección](https://msdn.microsoft.com/library/bb204082%28v=exchg.150%29.aspx)automática pox , que se convierte en el valor del encabezado **X-PublicFolderMailbox.**<br/><br/> ![Respuesta X-PublicFolderMailbox](media/Ex15_PF_PFH_PFMailbox.png)|1. Llame al servicio de detección [automática de POX](#bk_makeautodrequest) con la dirección **de correo electrónico X-AnchorMailbox.**  <br/><br/>2. Use el **elemento Server** devuelto por el servicio de detección automática para rellenar el valor del encabezado **X-PublicFolderMailbox.** El valor de **X-PublicFolderMailbox** es una dirección SMTP donde el nombre de usuario es un GUID.  <br/> |

<br/>

Después de determinar los valores de encabezado, indónlos al realizar solicitudes de jerarquía de [carpetas públicas.](#bk_setheadervalues)
  
Los pasos de este artículo son específicos de las solicitudes de jerarquía de carpetas públicas. Para determinar si la solicitud es una jerarquía de carpetas públicas o una solicitud de contenido, vea [Routing public folder requests](public-folder-access-with-ews-in-exchange.md#bk_routing).
  
## <a name="determine-the-value-of-the-x-anchormailbox-header-by-using-the-ews-managed-api"></a>Determinar el valor del encabezado X-AnchorMailbox mediante la API administrada ews
<a name="bk_getpfinfoewsma"> </a>

Para recuperar el valor [PublicFolderInformation (POX)](https://msdn.microsoft.com/library/a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6%28Office.15%29.aspx) mediante la API administrada ews, puede almacenar en caché el valor del elemento **PublicFolderInformation** que devuelve una llamada existente al servicio de detección automática o realizar una nueva llamada. 
  
Si realiza una nueva llamada, puede obtener la configuración de usuario mediante la [API](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)administrada ews Obtener la configuración de usuario mediante la [API](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed) administrada ews en el código y, a continuación, llamar al método de ejemplo **GetUserSettings** mediante el código siguiente, que recupera solo el valor del elemento **PublicFolderInformation.** Incluya la dirección SMTP del usuario del buzón como parámetro de entrada. 
  
```cs
GetUserSettingsResponse userResponse = GetUserSettings(adservice, "sonyaf@contoso.com", 3, UserSettingName.PublicFolderInformation);
Console.WriteLine("X-AnchorMailbox value for public folder hierarchy requests: {0}", userResponse.Settings[UserSettingName.PublicFolderInformation]);
```

Después de ejecutar el código, se muestra la siguiente información en la consola:
  
`X-AnchorMailbox for public folder hierarchy requests: SharedPublicFolder@contoso.com`

Ahora que tiene el valor **PublicFolderInformation,** indúzcalo como el valor del encabezado X-AnchorMailbox en todas las solicitudes de jerarquía de carpetas públicas. 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com`

## <a name="determine-the-value-of-the-x-anchormailbox-header-using-soap"></a>Determinar el valor del encabezado X-AnchorMailbox mediante SOAP
<a name="bk_getpfinfoews"> </a>

En el siguiente ejemplo de código se muestra cómo recuperar el **valor PublicFolderInformation** mediante la [operación SOAP GetUserSettings.](https://msdn.microsoft.com/library/dd877096%28v=exchg.150%29.aspx) El usuario del buzón se especifica en el elemento [Mailbox](https://msdn.microsoft.com/library/dd877076%28v=exchg.150%29.aspx) y el [elemento RequestedSettings](https://msdn.microsoft.com/library/office/dd877107%28v=exchg.150%29.aspx) limita la respuesta al [valor PublicFolderInformation.](https://msdn.microsoft.com/library/dn751006%28v=exchg.150%29.aspx) 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover"
               xmlns:wsa="http://www.w3.org/2005/08/addressing"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2007_SP1</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://pod51042.outlook.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>sonyaf@contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>PublicFolderInformation</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>
```

La respuesta incluye el **valor PublicFolderInformation.** 
  
```XML
<UserSetting i:type="StringSetting">
    <Name>PublicFolderInformation</Name>
    <Value>SharedPublicFolder@contoso.com</Value>
</UserSetting>
```

Ahora que tiene el valor **PublicFolderInformation,** indúzcalo como el valor del encabezado X-AnchorMailbox en todas las solicitudes de jerarquía de carpetas públicas. 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com`

## <a name="make-an-autodiscover-request-to-determine-the-x-publicfolderinformation-value"></a>Realizar una solicitud de detección automática para determinar el valor X-PublicFolderInformation
<a name="bk_makeautodrequest"> </a>

Realice una solicitud de detección automática mediante la dirección SMTP **PublicFolderInformation,** que ahora se usa como valor **X-AnchorMailbox.** Use el [Exchange 2013:](https://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) Obtener la configuración del usuario con el ejemplo de código de detección automática para llamar al servicio de detección automática porque simplifica el proceso de detección automática. En este ejemplo de código se usan los argumentos de línea de comandos enumerados en la tabla siguiente para llamar al servicio de detección automática POX en la dirección SMTP **PublicFolderInformation.** 
  
|**Argumento de línea de comandos**|**Descripción**|
|:-----|:-----|
|emailAddress  <br/> |La **dirección SMTP PublicFolderInformation.**  <br/> |
|-skipSOAP  <br/> | Use solicitudes de detección automática de POX para este escenario.  <br/> |
|-auth authEmailAddress  <br/> |La dirección de correo electrónico del usuario del buzón, que se usa para la autenticación. Se le pedirá que escriba la contraseña del usuario del buzón cuando ejecute el ejemplo.  <br/> |
   
Por ejemplo, cuando SharedPublicFolder@contoso.com es la dirección SMTP del elemento **PublicFolderInformation** y sonyaf@contoso.com es el usuario del buzón, los argumentos de línea de comandos deben tener este aspecto. 
  
`SharedPublicFolder@contoso.com -skipSOAP -auth sonyaf@contoso.com`

Al ejecutar el Exchange **2013:** Obtener la configuración del usuario con el ejemplo de detección automática, la última respuesta de detección automática debe ser correcta e incluir toda la configuración de usuario asociada con el GUID del buzón. El [valor de](https://msdn.microsoft.com/library/bb204084%28v=exchg.150%29.aspx) Servidor asociado al elemento [Tipo de protocolo](https://msdn.microsoft.com/library/bb204278%28v=exchg.150%29.aspx)[](https://msdn.microsoft.com/library/office/bb204223%28v=exchg.150%29.aspx) EXCH es el valor de encabezado **X-PublicFolderInformation.** 
  
```XML
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    …
    <Account>
      <AccountType>email</AccountType>
      <Action>settings</Action>
      <Protocol>
        <Type>EXCH</Type>
        <Server>1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com</Server>

```

Como alternativa, si no desea usar el ejemplo **Exchange 2013:** Obtener la configuración de usuario con detección automática, puede obtener el valor de **Servidor** generando una lista de extremos de detección automática y, a continuación, enviando la siguiente solicitud de detección automática de POX [a](how-to-generate-a-list-of-autodiscover-endpoints.md)cada dirección URL hasta que reciba una respuesta correcta. SharedPublicFolder@contoso.com es el valor del encabezado **X-PublicFolderMailbox.** 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>SharedPublicFolder@contoso.com</EMailAddress>
    <AcceptableResponseSchema>https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

Para obtener más información sobre el proceso de detección automática, vea [Autodiscover for Exchange](autodiscover-for-exchange.md), [Generate a list of Autodiscover endpoints](how-to-generate-a-list-of-autodiscover-endpoints.md)y [Get user settings from Exchange by using Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).
  
## <a name="set-the-values-of-the-x-anchormailbox-and-x-publicfoldermailbox-headers"></a>Establecer los valores de los encabezados X-AnchorMailbox y X-PublicFolderMailbox
<a name="bk_setheadervalues"> </a>

Uso del valor de la dirección SMTP **PublicFolderInformation** adquirida en [Determine the value of the X-AnchorMailbox header by using the EWS Managed API](#bk_getpfinfoewsma) or Determine the value of the [X-AnchorMailbox header using SOAP](#bk_getpfinfoews) and the **Server** value acquired in Make [an Autodiscover request to determine the X-PublicFolderInformation value](#bk_makeautodrequest), set the values of **X-AnchorMailbox** and **X-PublicFolderMailbox** headers in your public folder content request. 
  
Por ejemplo, teniendo en cuenta una dirección SMTP **PublicFolderInformation** de SharedPublicFolder@contoso.com y un valor server de 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com, incluya los siguientes encabezados al realizar llamadas **a** los siguientes métodos o operaciones. 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com` <br/>
`X-PublicFolderMailbox: 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com`

**Llamadas a carpetas públicas que requieren los encabezados X-AnchorMailbox y X-PublicFolder**

|**Métodos de administración de la API de EWS**|**Operaciones EWS**|
|:-----|:-----|
|[Folder.FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> [Folder.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> [Folder.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> [Folder.Move](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.move%28v=exchg.80%29.aspx) <br/> |[CreateFolder](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> [DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> [MoveFolder](https://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <br/> |
   
Para agregar estos encabezados mediante la API administrada ews, use el [método HttpHeaders.Add.](https://msdn.microsoft.com/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", "SharedPublicFolder@contoso.com");service.HttpHeaders.Add("X-PublicFolderMailbox", "1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com");
```

Por ejemplo, el siguiente código muestra una solicitud [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) con el encabezado **X-AnchorMailbox** y **X-PublicFolderMailbox** establecidos en los valores recuperados en los ejemplos de este artículo. 
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
User-Agent: SoapSender1.0
X-AnchorMailbox: SharedPublicFolder@contoso.com
X-PublicFolderMailbox: 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com
Host: outlook.office365.com
Content-Length: 1174
Expect: 100-continue
Connection: Keep-Alive
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindFolder Traversal="Shallow">
      <m:FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </m:FolderShape>
      <m:IndexedPageFolderView MaxEntriesReturned="1" Offset="0" BasePoint="Beginning" />
      <m:Restriction>
        <t:IsEqualTo>
          <t:FieldURI FieldURI="folder:DisplayName" />
          <t:FieldURIOrConstant>
            <t:Constant Value="My Public Contacts" />
          </t:FieldURIOrConstant>
        </t:IsEqualTo>
      </m:Restriction>
      <m:ParentFolderIds>
        <t:FolderId Id="AQEuAAADy/LIWjRCp0GFb0W6aGPbwwEARg5aCLUc8k6wLfl1c0a/2AAAAwIAAAA=" ChangeKey="AQAAABYAAABGDloItRzyTrAt+XVzRr/YAABdo/XB" />
      </m:ParentFolderIds>
    </m:FindFolder>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Ver también

- [Acceso a carpetas públicas con EWS en Exchange](public-folder-access-with-ews-in-exchange.md)    
- [Redirigir solicitudes del contenido de carpetas públicas](how-to-route-public-folder-content-requests.md)    
- [Obtener la configuración del usuario mediante la API administrada de EWS](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)
    

