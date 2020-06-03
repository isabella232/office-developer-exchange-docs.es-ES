---
title: Enrutar solicitudes de contenido de carpetas públicas
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 59d2f05e-90fb-471e-ac06-70becc15b295
description: Todas las solicitudes de información de carpetas públicas que impliquen el contenido de la carpeta pública deben enrutarse al buzón de la carpeta pública que contiene el contenido de la carpeta de destino. Para enrutar las solicitudes a ese buzón de correo, debe establecer los encabezados X-AnchorMailbox y X-PublicFolderMailbox en valores específicos.
ms.openlocfilehash: 523b9c8efc65253f7970fffeb5800e451784522d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527739"
---
# <a name="route-public-folder-content-requests"></a>Enrutar solicitudes de contenido de carpetas públicas

Todas las solicitudes de información de carpetas públicas que impliquen el contenido de la carpeta pública deben enrutarse al buzón de la carpeta pública que contiene el contenido de la carpeta de destino. Para enrutar las solicitudes a ese buzón de correo, debe establecer los encabezados **x-AnchorMailbox** y **x-PublicFolderMailbox** en valores específicos. 
  
En la tabla siguiente se proporciona información general sobre el proceso:
  
**Introducción a la carpeta pública**

|Encabezado|¿Qué necesito?|¿Cómo puedo obtenerlo?|
|:-----|:-----|:-----|
|**X-AnchorMailbox** <br/> |1. [los valores x-AnchorMailbox y x-PublicFolderInformation](how-to-route-public-folder-hierarchy-requests.md) para el buzón de la jerarquía de carpetas públicas.<br/><br/>2. el GUID del buzón de carpeta pública que contiene el contenido del buzón, que se envía al servicio Detección automática.<br/><br/>  La **AutoDiscoverSMTPAddress** en la respuesta de Autodisover se convierte en el valor del encabezado **X-AnchorMailbox** .  <br/> ![TODO](media/Ex15_PF_PFContent.png)| 1. Use el ejemplo de código de este artículo, que [implementa la API administrada de EWS](#bk_determineguidewsma). O bien, [use EWS](#bk_determineguidews) y convierta los resultados para obtener un GUID.<br/><br/>2. [realice una solicitud de detección automática](#bk_makeautodrequest) usando el GUID y el nombre de dominio.<br/><br/>3. Use el valor del elemento **AutoDiscoverSMTPAddress** devuelto en la respuesta de detección automática para [rellenar el valor de los encabezados](#bk_setheadervalues).  <br/> |
|**X-PublicFolderMailbox** <br/> |El trabajo se ha realizado, el valor X-PublicFolderMailbox es el mismo que el valor X-AnchorMailbox  <br/> |Ya lo ha hecho.  <br/> |
   
Una vez que haya determinado los valores de encabezado, incluidos [al realizar solicitudes de contenido de carpetas públicas](#bk_setheadervalues).
  
Los pasos de este artículo son específicos de las solicitudes de contenido de carpetas públicas. Para determinar si su solicitud es una jerarquía de carpetas públicas o una solicitud de contenido, consulte [enrutamiento de solicitudes de carpetas públicas](public-folder-access-with-ews-in-exchange.md#bk_routing).

<a name="bk_determineguidewsma"> </a>

## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-the-ews-managed-api"></a>Determinación del GUID del buzón de carpetas públicas mediante la API administrada de EWS


Para determinar el GUID del buzón de contenido de la carpeta pública, use el siguiente ejemplo de código, que hace lo siguiente: 
  
- Usa los encabezados **x-AnchorMailbox** y **x-PublicFolderInformation** que recuperó mediante el [enrutamiento de solicitudes de jerarquía de carpetas públicas](how-to-route-public-folder-hierarchy-requests.md).
    
- Llama al método [FindFolders](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) de la API administrada de EWS e incluye una solicitud para la propiedad **PR_REPLICA_LIST** (0x66980102). 
    
El valor **PR_REPLICA_LIST** identifica el GUID del buzón de correo de la carpeta pública que tiene el contenido de la carpeta. La propiedad **PR_REPLICA_LIST** es una matriz de bytes, pero se convierte en un GUID para este escenario. El GUID y el nombre de dominio se concatenan para formar la dirección en la que se va a llamar a detección automática. 
  
En este ejemplo se supone que `service` es el objeto [ExchangeService](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) para el usuario de buzón de correo, `PFHAnchorHeader` y `PFHMailboxHeader` son los valores de los encabezados **x-AnchorMailbox** y **x-PublicFolderMailbox** , y domain es el nombre de dominio que usa el inquilino. 
  
```cs
public static string GetMailboxGuidAddress(ExchangeService service, String PFHAnchorHeader, String PFHMailboxHeader, String domain)
{
    // Create a new folder view, and pass in the maximum number of folders to return.
    FolderView view = new FolderView(10);
    // Create an extended property definition for the PR_REPLICA_LIST property.
    ExtendedPropertyDefinition PR_REPLICA_LIST = new ExtendedPropertyDefinition(0x6698, MapiPropertyType.Binary);
    // As a best practice, limit the properties returned to only those required.
    // In this case, return the folder ID, the folder display name, and 
    // the value of the PR_REPLICA_LIST extended property definition.
    view.PropertySet = new PropertySet(BasePropertySet.IdOnly, FolderSchema.DisplayName, PR_REPLICA_LIST);
    service.HttpHeaders.Add("X-AnchorMailbox", PFHAnchorHeader);
    service.HttpHeaders.Add("X-PublicFolderMailbox", PFHMailboxHeader);
    // Add a call to the CertificateValidationCallback method here if needed.
    // ServicePointManager.ServerCertificateValidationCallback = CertificateValidationCallBack;
    // Call FindFolders to retrieve the folder hierarchy, starting with the PublicFolderRoot folder.
    // This method call results in a FindFolder call to EWS.
    FindFoldersResults findResults = service.FindFolders(WellKnownFolderName.PublicFoldersRoot, view);
    string GuidAsString = null;
    List<string> Guids = new List<string>();
    // For each folder under the root, display the name, and copy the value of the 
    // PR_REPLICA_LIST byte array to a string value. 
    foreach (Folder folder in findResults.Folders)
    {
        Console.WriteLine("Public folder display name: {0}", folder.DisplayName);
        byte[] ByteArr = (byte[])folder.ExtendedProperties[0].Value;
        GuidAsString = System.Text.Encoding.ASCII.GetString(ByteArr, 0, 36);
        Guids.Add(GuidAsString);
        Console.WriteLine("Address for Autodiscover: {0}.{1}\r\n", GuidAsString, domain);
    }
    // Concatenate the GUID value of the PR_REPLICA_LIST with the domain name to generate the 
    // SMTP address to use for the AutoDiscover request for the public folder content mailbox.
    string AutoDSMTPAddress = GuidAsString + "@" + domain;
    // Check that all folders have the same GUID value. If they do not, use the GUID value of the
    // folder that you're requesting content for.
    string commonGuid = CompareGuidsForEquality(Guids);
    if (commonGuid == "Not Equal")
    {
        Console.WriteLine("The GUIDs for all the folders in the hierarchy are not the same. Run the Autodiscover sample using the address returned above that is associated with the folder in your hierarchy request.", AutoDSMTPAddress);
        return null;
    }
    else
    {
        Console.WriteLine("The GUIDs for all public folders in the hierarchy are the same. Run the Autodiscover sample using the {0} address.", AutoDSMTPAddress);
        return AutoDSMTPAddress;
    }
}
// Method to compare the GUID for each folder under the public folder root.
// If each GUID is the same, return the GUID.
// If the GUIDs are not the same, return "Not equal".
public static string CompareGuidsForEquality(List<string> list)
{
    string NotEqual = "Not equal";
    string first = list.First();
    return list.All(x => x == first) ? first : NotEqual;
}
```

Si recibió el error "error en la solicitud. Se cerró la conexión subyacente: no se pudo establecer una relación de confianza para el canal seguro SSL/TLS ", tendrá que [Agregar una llamada a un método de devolución de llamada de validación](how-to-validate-a-server-certificate-for-the-ews-managed-api.md). En el ejemplo de código se incluye un marcador de posición y un comentario para ese método.
  
Si el GUID del buzón es el mismo para todas las carpetas públicas de la raíz de la carpeta pública, el ejemplo indica la dirección que se va a usar al [llamar a detección automática](#bk_makeautodrequest) en el resultado de la consola y como el valor devuelto. Si el GUID del buzón no es el mismo para todas las carpetas públicas en la raíz de la carpeta pública, debe [realizar una solicitud de detección automática](#bk_makeautodrequest) en la dirección asociada a la carpeta en la solicitud de contenido. 

<a name="bk_determineguidews"> </a>

## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-ews"></a>Determinación del GUID del buzón de carpetas públicas mediante EWS

En el ejemplo de código siguiente se muestra cómo recuperar el valor de la propiedad **PR_REPLICA_LIST** (0x66980102) mediante la operación [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) de EWS. En el caso del elemento [ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) , el atributo **PropertyTag** se establece en el valor decimal (26264) de la propiedad **PR_REPLICA_LIST** y el atributo **PropertyType** se establece en **Binary**.
  
También es la solicitud XML que la API administrada de EWS envía cuando usa el método **FindFolders** para [determinar el GUID del buzón de carpetas públicas mediante la API administrada de EWS](#bk_determineguidewsma).
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
Accept: text/xml
User-Agent: ExchangeServicesClient/15.00.0913.015
Accept-Encoding: gzip,deflate
Authorization: Basic c29ueWFmQGNvbnRvc28xMDAwLm9ubWljcm9zb2Z0LmNvbTpFWENIIzIwMTQ=
Host: outlook.office365.com
Cookie: ClientId=KZPBLKA9ZMPXAQDW
Content-Length: 1005
Expect: 100-continue
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindFolder Traversal="Shallow">
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="folder:DisplayName" />
          <t:ExtendedFieldURI PropertyTag="26264" PropertyType="Binary" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:IndexedPageFolderView MaxEntriesReturned="10" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="publicfoldersroot" />
      </m:ParentFolderIds>
    </m:FindFolder>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud **FindFolder** con un mensaje [FindFolderResponse](https://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) que incluye el valor de la propiedad extendida **PR_REPLICA_LIST** . Tenga en cuenta que el valor de la propiedad aparece en la respuesta de EWS como el formato de cadena de una matriz de bytes codificada en base 64. Algunos valores de encabezado de la respuesta se acortan para facilitar su lectura. 
  
```XML
<?xml version="1.0" encoding="utf-8"?><s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="1019" MinorBuildNumber="15" Version="V2_17" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body>
    <m:FindFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="2" TotalItemsInView="2" IncludesLastItemInRange="true">
            <t:Folders>
              <t:ContactsFolder>
                <t:FolderId Id="AAEuAAAAAADL8shaNEKnQYVvRbpoY9vDAQBGDloItRzyTrAt+XVzRr/YAABdofPkAAA=" ChangeKey="AwAAABYAAABGDloItRzyTrAt+XVzRr/YAABdo/2h"/>
                <t:DisplayName>My Public Contacts</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x6698" PropertyType="Binary"/>
                  <t:Value>MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA==</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:Folder>
                <t:FolderId Id="AQEuAAADy/LIWjRCp0GFb0W6aGPbwwEARg5aCLUc8k6wLfl1c0a/2AAAAxEAAAA=" ChangeKey="AQAAABYAAABGDloItRzyTrAt+XVzRr/YAABdo/W/"/>
                <t:DisplayName>SampleFolder</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x6698" PropertyType="Binary"/>
                  <t:Value>MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA==</t:Value>
                </t:ExtendedProperty>
              </t:Folder>
            </t:Folders>
          </m:RootFolder>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </m:FindFolderResponse>
  </s:Body>
</s:Envelope>
```

Para usar el valor de la **PR_REPLICA_LIST** devuelta en el XML, MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA = =, para determinar el GUID de buzón, el valor debe convertirse en un GUID en un formato similar al de la conversión del valor en el ejemplo de código de la [API administrada de EWS](#bk_determineguidewsma). A continuación, el GUID se concatena con el nombre de dominio para crear una dirección SMTP, que se incluye en la [solicitud de detección automática](#bk_makeautodrequest).
  
## <a name="make-an-autodiscover-request"></a>Realizar una solicitud de detección automática
<a name="bk_makeautodrequest"> </a>

Use la dirección devuelta por el `GetMailboxGuidAddress` método para llamar a detección automática. Le recomendamos que use el ejemplo de código [Exchange 2013: obtener configuración de usuario con detección automática](https://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) para llamar al servicio Detección automática porque optimiza el proceso de detección automática por usted. Este ejemplo de código usa los argumentos de línea de comandos enumerados en la siguiente tabla para llamar al servicio Detección automática de POX para recuperar el valor [AutoDiscoverSMTPAddress](https://msdn.microsoft.com/library/office/dn750991%28v=exchg.150%29.aspx) asociado al GUID de buzón de correo. 

  
|**Argumento**|**Descripción**|
|:-----|:-----|
|emailAddress  <br/> |La dirección devuelta por el `GetMailboxGuidAddress` método para [determinar el GUID del buzón de carpetas públicas](#bk_determineguidewsma).  <br/> |
|-skipSOAP  <br/> |Indica que las solicitudes de detección automática de POX son necesarias.  <br/> |
|-auth authEmailAddress  <br/> |La dirección de correo electrónico del usuario del buzón, que se usa para la autenticación. Al ejecutar el ejemplo, se le pedirá que escriba la contraseña del usuario del buzón.  <br/> |
   
Por ejemplo, los argumentos de la línea de comandos deben tener el siguiente aspecto:
  
`1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com -skipSOAP -auth sonyaf@contoso.com`

Donde `1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com` es la dirección devuelta por el método **GetMailboxGuidAddress** y `sonyaf@contoso.com` es el usuario del buzón de correo. 
  
Al ejecutar el ejemplo **Exchange 2013: obtener configuración de usuario con detección automática** , la última respuesta de detección automática debería ser correcta e incluir todas las configuraciones de usuario asociadas con el GUID de buzón. Guarde la configuración de usuario **AutoDiscoverSMTPAddress** de forma local, como la usará en el paso siguiente. 
  
Como alternativa, si no quiere usar **Exchange 2013: obtener configuración de usuario con la detección automática** , puede obtener la configuración de usuario **AutoDiscoverSMTPAddress** [generando una lista de extremos de detección automática](how-to-generate-a-list-of-autodiscover-endpoints.md)y, a continuación, enviando la siguiente solicitud de detección automática de POX a cada dirección URL hasta que reciba una respuesta correcta.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com</EMailAddress>
    <AcceptableResponseSchema>https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

Para obtener más información sobre el proceso de detección automática, consulte [detección automática para Exchange](autodiscover-for-exchange.md), [generar una lista de extremos de detección automática](how-to-generate-a-list-of-autodiscover-endpoints.md)y [obtener la configuración de usuario de Exchange mediante detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).
  
## <a name="set-the-values-of-the-x-anchormailbox-and-x-publicfoldermailbox-headers"></a>Establecer los valores de los encabezados X-AnchorMailbox y X-PublicFolderMailbox
<a name="bk_setheadervalues"> </a>

Con el valor de **AutoDiscoverSMTPAddress** adquirido en [realizar una solicitud de detección automática](#bk_makeautodrequest), establezca los valores de los encabezados **x-AnchorMailbox** y **x-PublicFolderMailbox** en la solicitud de contenido de la carpeta pública. 
  
Por ejemplo, dada una AutoDiscoverSMTPAddress de NewPublicFolder@contoso.com, incluya los siguientes encabezados al realizar llamadas a los siguientes métodos u operaciones.
  
`X-AnchorMailbox: NewPublicFolder@contoso.com`<br/>
`X-PublicFolderMailbox: NewPublicFolder@contoso.com`

**Llamadas a carpetas públicas que requieren los encabezados X-AncorMailbox y X-PublicFolder**

|**Métodos de la API administrada de EWS**|**Operaciones de EWS**|
|:-----|:-----|
|[Item. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [Item. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> [Item. Copy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> [Item. Move](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> [Item. Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> [Folder. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> [Folder. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> [CopyItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> [MoveItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |
   
Para agregar estos encabezados mediante la API administrada de EWS, use el método [HttpHeaders. Add](https://msdn.microsoft.com/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) . 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", "NewPublicFolder@contoso.com");
service.HttpHeaders.Add("X-PublicFolderMailbox", "NewPublicFolder@contoso.com");
```

El siguiente código muestra una solicitud [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) con el encabezado **x-AnchorMailbox** y **x-PublicFolderMailbox** establecido en los valores que se han recuperado en los ejemplos de este artículo. 
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
User-Agent: SoapSender1.0
X-AnchorMailbox: NewPublicFolder@contoso.com
X-PublicFolderMailbox: NewPublicFolder@contoso.com
Authorization: Basic c29ueWFmQGNvbnRvc28xMDAwLm9ubWljcm9zb2Z0LmNvbTpFWENIIzIwMTQ=
Host: outlook.office365.com
Content-Length: 688
Expect: 100-continue
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetFolder>
      <m:FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </m:FolderShape>
      <m:FolderIds>
        <t:DistinguishedFolderId Id="publicfoldersroot" />
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Vea también

- [Acceso a carpetas públicas con EWS en Exchange](public-folder-access-with-ews-in-exchange.md)    
- [Detección automática en Exchange](autodiscover-for-exchange.md)    
- [Generar una lista de extremos de detección automática](how-to-generate-a-list-of-autodiscover-endpoints.md)   
- [Obtener la configuración de usuario de Exchange mediante el uso de detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
  