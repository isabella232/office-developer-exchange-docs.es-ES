---
title: Enrutar las solicitudes de jerarquía de carpetas públicas
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ec35df8e-4d75-4aa1-8b9c-ae1db7e05772
description: Todas las solicitudes de información de carpetas públicas que requieren conocimientos de la jerarquía de carpetas públicas, como mover, actualizar, eliminar o buscar carpetas públicas, es necesario distribuir para el buzón de jerarquía de carpetas públicas predeterminado para el usuario determinado. Para enrutar las solicitudes a ese buzón, debe establecer los encabezados X-AnchorMailbox y X-PublicFolderMailbox a determinados valores devueltos por el servicio Detección automática.
ms.openlocfilehash: 983431864729edbb040a7206dae416d10bfb2b7a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763174"
---
# <a name="route-public-folder-hierarchy-requests"></a>Enrutar las solicitudes de jerarquía de carpetas públicas

Todas las solicitudes de información de carpetas públicas que requieren conocimientos de la jerarquía de carpetas públicas, como mover, actualizar, eliminar o buscar carpetas públicas, es necesario distribuir para el buzón de jerarquía de carpetas públicas predeterminado para el usuario determinado. Para enrutar las solicitudes a ese buzón, debe establecer los encabezados **X-AnchorMailbox** y **X-PublicFolderMailbox** a determinados valores devueltos por el servicio Detección automática. 
  
**Información general de las carpetas públicas**

|Encabezado|¿Qué es necesario?|¿Cómo se puede obtener?|
|:-----|:-----|:-----|
|**X-AnchorMailbox** <br/> |El valor [PublicFolderInformation](http://msdn.microsoft.com/en-us/library/dn751006%28v=exchg.150%29.aspx) desde una respuesta SOAP de detección automática, [GetUserSettings](http://msdn.microsoft.com/en-us/library/office/dd877096%28v=exchg.150%29.aspx) , que se convierte en el valor del encabezado **X-AnchorMailbox** .<br/><br/> ![TODO](media/Ex15_PF_PFH_Anchor.png)| 1. enviar una solicitud de **GetUserSetting** con la dirección SMTP para el buzón del usuario.<br/><br/>2. el valor del elemento **PublicFolderInformation** que devuelve el servicio Detección automática de la memoria caché. Esto puede ser una caché desde una llamada de detección automática existente en su código, o una nueva [llamada API GetUserSettings administrada de EWS](#bk_getpfinfoewsma) o una [solicitud SOAP GetUserSettings](#bk_getpfinfoews).  <br/><br/>3. use el elemento **PublicFolderInformation** para rellenar el valor del encabezado **X-AnchorMailbox** . El valor del elemento **PublicFolderInformation** es una dirección SMTP.  <br/> |
|**X-PublicFolderMailbox** <br/> |El valor de [servidor](http://msdn.microsoft.com/en-us/library/bb204084%28v=exchg.150%29.aspx) desde una [respuesta de detección automática de POX](http://msdn.microsoft.com/en-us/library/bb204082%28v=exchg.150%29.aspx), que se convierte en el valor del encabezado **X-PublicFolderMailbox** .<br/><br/> ![TODO](media/Ex15_PF_PFH_PFMailbox.png)|1. el servicio de [llamada a la detección automática POX](#bk_makeautodrequest) utilizando la dirección de correo electrónico **X-AnchorMailbox** .  <br/><br/>2. Utilice el elemento de **servidor** devuelto por el servicio de detección automática para rellenar el valor del encabezado **X-PublicFolderMailbox** . El valor de la **X-PublicFolderMailbox** es una dirección SMTP donde el nombre de usuario es un GUID.  <br/> |

<br/>

Una vez que haya determinado los valores de encabezado, incluirlos [cuando realiza las solicitudes de jerarquía de carpetas públicas](#bk_setheadervalues).
  
Los pasos descritos en este artículo son específicos de las solicitudes de jerarquía de carpetas públicas. Para determinar si la solicitud es una solicitud de contenido o la jerarquía de carpetas públicas, vea [las solicitudes de carpetas públicas de enrutamiento](public-folder-access-with-ews-in-exchange.md#bk_routing).
  
## <a name="determine-the-value-of-the-x-anchormailbox-header-by-using-the-ews-managed-api"></a>Determinar el valor del encabezado X-AnchorMailbox mediante el uso de la API administrada de EWS
<a name="bk_getpfinfoewsma"> </a>

Para recuperar el valor de [PublicFolderInformation (POX)](http://msdn.microsoft.com/library/a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6%28Office.15%29.aspx) mediante el uso de la API administrada de EWS, puede almacenar en caché el valor del elemento **PublicFolderInformation** que devuelve una llamada existente para el servicio Detección automática, o realizar una nueva llamada. 
  
Si está realizando una llamada nueva, se puede [obtener la configuración de usuario mediante el uso de la API administrada de EWS](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)[obtener la configuración de usuario mediante el uso de la API administrada de EWS](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed) para el código y, a continuación, llame el **GetUserSettings** de ejemplo (método) mediante el código siguiente, que recupera el valor del elemento **PublicFolderInformation** . Incluir la dirección SMTP del usuario de buzón de correo como un parámetro de entrada. 
  
```cs
GetUserSettingsResponse userResponse = GetUserSettings(adservice, "sonyaf@contoso.com", 3, UserSettingName.PublicFolderInformation);
Console.WriteLine("X-AnchorMailbox value for public folder hierarchy requests: {0}", userResponse.Settings[UserSettingName.PublicFolderInformation]);
```

Después de ejecutar el código, se muestra la siguiente información en la consola:
  
`X-AnchorMailbox for public folder hierarchy requests: SharedPublicFolder@contoso.com`

Ahora que tiene el valor **PublicFolderInformation** , incluir como el valor para el encabezado X-AnchorMailbox en todas las solicitudes de jerarquía de carpetas públicas. 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com`

## <a name="determine-the-value-of-the-x-anchormailbox-header-using-soap"></a>Determinar el valor del encabezado X-AnchorMailbox usa SOAP
<a name="bk_getpfinfoews"> </a>

En el ejemplo de código siguiente se muestra cómo recuperar el valor de **PublicFolderInformation** mediante el uso de la operación de SOAP [GetUserSettings](http://msdn.microsoft.com/en-us/library/dd877096%28v=exchg.150%29.aspx) . El usuario del buzón está especificado en el elemento de [buzón de correo](http://msdn.microsoft.com/en-us/library/dd877076%28v=exchg.150%29.aspx) , y el elemento [RequestedSettings](http://msdn.microsoft.com/en-us/library/office/dd877107%28v=exchg.150%29.aspx) limita la respuesta en el valor de [PublicFolderInformation](http://msdn.microsoft.com/en-us/library/dn751006%28v=exchg.150%29.aspx) . 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover"
               xmlns:wsa="http://www.w3.org/2005/08/addressing"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2007_SP1</a:RequestedServerVersion>
    <wsa:Action>http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
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

La respuesta incluye el valor de **PublicFolderInformation** . 
  
```XML
<UserSetting i:type="StringSetting">
    <Name>PublicFolderInformation</Name>
    <Value>SharedPublicFolder@contoso.com</Value>
</UserSetting>
```

Ahora que tiene el valor **PublicFolderInformation** , incluir como el valor para el encabezado X-AnchorMailbox en todas las solicitudes de jerarquía de carpetas públicas. 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com`

## <a name="make-an-autodiscover-request-to-determine-the-x-publicfolderinformation-value"></a>Para realizar una solicitud de detección automática para determinar el valor de X-PublicFolderInformation
<a name="bk_makeautodrequest"> </a>

Realizar una solicitud de detección automática mediante el uso de la dirección SMTP de **PublicFolderInformation** , que ahora se utiliza como el valor de **X-AnchorMailbox** . Usar el [Exchange 2013: obtener la configuración de usuario con detección automática](http://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) ejemplo de código para llamar al servicio de detección automática debido a que optimiza el proceso de detección automática para usted. Este ejemplo de código usa los argumentos de línea de comandos que aparecen en la tabla siguiente para llamar al servicio de detección automática de POX en la dirección SMTP de **PublicFolderInformation** . 
  
|**Argumento de línea de comandos**|**Descripción**|
|:-----|:-----|
|emailAddress  <br/> |La dirección **PublicFolderInformation** SMTP.  <br/> |
|-skipSOAP  <br/> | Usar solicitudes de detección automática de POX para este escenario.  <br/> |
|authEmailAddress - auth  <br/> |Dirección de correo electrónico del usuario de buzón de correo, que se usa para la autenticación. Se le pedirá para escribir la contraseña del usuario de buzón de correo al ejecutar el ejemplo.  <br/> |
   
Por ejemplo, cuando SharedPublicFolder@contoso.com es la dirección SMTP del elemento **PublicFolderInformation** y sonyaf@contoso.com es el usuario de buzón de correo, los argumentos de línea de comandos deben tener un aspecto similar. 
  
`SharedPublicFolder@contoso.com -skipSOAP -auth sonyaf@contoso.com`

Al ejecutar el **Exchange 2013: obtener la configuración de usuario con detección automática** ejemplo, la última respuesta de detección automática debe ser correcta e incluir todos los la configuración del usuario asociada con el GUID de buzón. El valor de [servidor](http://msdn.microsoft.com/en-us/library/bb204084%28v=exchg.150%29.aspx) asociado con el elemento de [protocolo](http://msdn.microsoft.com/en-us/library/bb204278%28v=exchg.150%29.aspx)EXCH[tipo](http://msdn.microsoft.com/en-us/library/office/bb204223%28v=exchg.150%29.aspx) es el valor de encabezado **X-PublicFolderInformation** . 
  
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

Como alternativa, si no desea usar el **Exchange 2013: obtener la configuración de usuario con detección automática** ejemplo, puede obtener el valor de **servidor de** [generación de una lista de extremos de detección automática](how-to-generate-a-list-of-autodiscover-endpoints.md)y, a continuación, enviando la detección automática POX siguiente solicitar a cada dirección URL hasta que recibe una respuesta correcta. SharedPublicFolder@contoso.com es el valor del encabezado **X-PublicFolderMailbox** . 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>SharedPublicFolder@contoso.com</EMailAddress>
    <AcceptableResponseSchema>http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

Para obtener más información acerca del proceso de detección automática, vea [detección automática de Exchange](autodiscover-for-exchange.md), [generar una lista de extremos de detección automática](how-to-generate-a-list-of-autodiscover-endpoints.md)y [obtener la configuración de usuario de Exchange mediante el uso de detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).
  
## <a name="set-the-values-of-the-x-anchormailbox-and-x-publicfoldermailbox-headers"></a>Establezca los valores de los encabezados X-AnchorMailbox y X-PublicFolderMailbox
<a name="bk_setheadervalues"> </a>

Con el valor de la dirección de **PublicFolderInformation** SMTP adquirido en [determinar el valor del encabezado X-AnchorMailbox mediante el uso de la API administrada de EWS](#bk_getpfinfoewsma) o [determinar el valor del encabezado X-AnchorMailbox mediante SOAP](#bk_getpfinfoews) y el servidor de ** **valor adquirido en [realizar una solicitud de detección automática para determinar el valor de X-PublicFolderInformation](#bk_makeautodrequest), establezca los valores de los encabezados **X-AnchorMailbox** y **X-PublicFolderMailbox** en su solicitud de contenido de carpetas públicas. 
  
Por ejemplo, dada una dirección de **PublicFolderInformation** SMTP de SharedPublicFolder@contoso.com y el valor de un **servidor** de 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com, incluir los encabezados siguientes al realizar llamadas a la siguiente los métodos u operaciones. 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com` <br/>
`X-PublicFolderMailbox: 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com`

**Llamadas de carpeta pública que requieren los encabezados X-AnchorMailbox y X-PublicFolder**

|**Métodos de la API administrada de EWS**|**Operaciones de EWS**|
|:-----|:-----|
|[Folder.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> [Folder.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> [Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> [Folder.Move](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.move%28v=exchg.80%29.aspx) <br/> |[CreateFolder](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> [DeleteFolder](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> [MoveFolder](http://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <br/> |
   
Para agregar estos encabezados mediante el uso de la API administrada de EWS, use el método [HttpHeaders.Add](http://msdn.microsoft.com/en-us/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) . 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", "SharedPublicFolder@contoso.com");service.HttpHeaders.Add("X-PublicFolderMailbox", "1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com");
```

Por ejemplo, el código siguiente muestra una solicitud [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) con el encabezado **X-AnchorMailbox** y **X-PublicFolderMailbox** establecido en los valores recuperados en los ejemplos de este artículo. 
  
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

## <a name="see-also"></a>Vea también

- [Carpetas públicas en Exchange obtener acceso con EWS](public-folder-access-with-ews-in-exchange.md)    
- [Enrutar las solicitudes de contenido de carpetas públicas](how-to-route-public-folder-content-requests.md)    
- [Obtener la configuración de usuario mediante el uso de la API administrada de EWS](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)
    

