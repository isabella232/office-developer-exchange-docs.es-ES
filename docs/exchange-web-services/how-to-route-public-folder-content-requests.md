---
title: Redirigir solicitudes del contenido de carpetas públicas
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 59d2f05e-90fb-471e-ac06-70becc15b295
description: Todas las solicitudes de información de carpetas públicas que impliquen el contenido de la carpeta pública deben enrutrse al buzón de carpetas públicas que contiene el contenido de la carpeta de destino. Para enrutar las solicitudes a ese buzón, debe establecer los encabezados X-AnchorMailbox y X-PublicFolderMailbox en valores específicos.
ms.openlocfilehash: d5a066a63d9bc3b48c41473545343125538d856b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521105"
---
# <a name="route-public-folder-content-requests"></a>Redirigir solicitudes del contenido de carpetas públicas

Todas las solicitudes de información de carpetas públicas que impliquen el contenido de la carpeta pública deben enrutrse al buzón de carpetas públicas que contiene el contenido de la carpeta de destino. Para enrutar las solicitudes a ese buzón, debe establecer los encabezados **X-AnchorMailbox** y **X-PublicFolderMailbox** en valores específicos. 
  
En la tabla siguiente se proporciona información general sobre el proceso:
  
**Introducción a carpetas públicas**

|Encabezado|¿Qué necesito?|¿Cómo lo puedo obtener?|
|:-----|:-----|:-----|
|**X-AnchorMailbox** <br/> |1. [Los valores X-AnchorMailbox y X-PublicFolderInformation ](how-to-route-public-folder-hierarchy-requests.md) para el buzón de jerarquía de carpetas públicas.<br/><br/>2. GUID del buzón de carpetas públicas que contiene el contenido del buzón, que se envía al servicio de detección automática.<br/><br/>  **AutoDiscoverSMTPAddress en** la respuesta Autodisover se convierte en el valor del encabezado **X-AnchorMailbox.**  <br/> ![TODO](media/Ex15_PF_PFContent.png)| 1. Use el ejemplo de código de este artículo, que [implementa la API administrada ews](#bk_determineguidewsma). O [use EWS](#bk_determineguidews) y convierta los resultados para obtener un GUID.<br/><br/>2. [Realice una solicitud de detección automática](#bk_makeautodrequest) con el GUID más el nombre de dominio.<br/><br/>3. Use el valor del elemento **AutoDiscoverSMTPAddress** devuelto en la respuesta Detección automática para rellenar [el valor de los encabezados](#bk_setheadervalues).  <br/> |
|**X-PublicFolderMailbox** <br/> |El trabajo ha terminado, el valor X-PublicFolderMailbox es el mismo que el valor X-AnchorMailbox.  <br/> |Ya lo tienes.  <br/> |
   
Después de determinar los valores de encabezado, indónlos [al realizar solicitudes de contenido de carpetas públicas.](#bk_setheadervalues)
  
Los pasos de este artículo son específicos de las solicitudes de contenido de carpetas públicas. Para determinar si la solicitud es una jerarquía de carpetas públicas o una solicitud de contenido, vea [Routing public folder requests](public-folder-access-with-ews-in-exchange.md#bk_routing).

<a name="bk_determineguidewsma"> </a>

## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-the-ews-managed-api"></a>Determinar el GUID del buzón de carpetas públicas mediante la API administrada de EWS


Para determinar el GUID del buzón de contenido de carpetas públicas, use el siguiente ejemplo de código, que hace lo siguiente: 
  
- Usa los **encabezados X-AnchorMailbox** y **X-PublicFolderInformation** recuperados mediante el enrutamiento de solicitudes de jerarquía [de carpetas públicas](how-to-route-public-folder-hierarchy-requests.md).
    
- Llama al método [FindFolders](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) de la API administrada ews e incluye una solicitud para la **propiedad PR_REPLICA_LIST** (0x66980102) 
    
El **PR_REPLICA_LIST** identifica el GUID del buzón de correo del buzón de carpetas públicas que tiene el contenido de la carpeta. La **PR_REPLICA_LIST** es una matriz de bytes, pero se convierte como un GUID para este escenario. El GUID y el nombre de dominio se concatenan para formar la dirección en la que se debe llamar a Detección automática. 
  
En este ejemplo se supone que es el objeto ExchangeService para el usuario del buzón y que son los valores de los encabezados `service` [](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) `PFHAnchorHeader` `PFHMailboxHeader` **X-AnchorMailbox** y **X-PublicFolderMailbox,** y domain es el nombre de dominio usado por el inquilino. 
  
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

Si recibió el error "Error en la solicitud. Se cerró la conexión subyacente: no se pudo establecer una relación de confianza para el canal seguro SSL/TLS", deberá agregar una llamada a un método de devolución de llamada [de validación](how-to-validate-a-server-certificate-for-the-ews-managed-api.md). En el ejemplo de código se incluye un marcador de posición y un comentario para ese método.
  
Si el GUID del buzón es el mismo para todas las carpetas públicas bajo la raíz de carpetas públicas, el ejemplo indica la dirección que se usará al llamar a [Detección](#bk_makeautodrequest) automática en el resultado de la consola y como el valor devuelto. Si el GUID del buzón no es el mismo para todas [](#bk_makeautodrequest) las carpetas públicas en la raíz de carpetas públicas, debe realizar una solicitud de detección automática en la dirección asociada a la carpeta de la solicitud de contenido. 

<a name="bk_determineguidews"> </a>

## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-ews"></a>Determinar el GUID del buzón de carpetas públicas mediante EWS

En el ejemplo de código siguiente se muestra cómo recuperar el valor de la propiedad **PR_REPLICA_LIST** (0x66980102) mediante la operación [FindFolder de](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) EWS. Para el [elemento ExtendedFieldURI,](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) el atributo **PropertyTag** se establece en el valor decimal (26264) de la propiedad **PR_REPLICA_LIST** y el atributo **PropertyType** se establece en **Binary**.
  
También es la solicitud XML que envía la API administrada ews cuando se usa el método **FindFolders** para determinar el GUID del buzón de carpetas públicas mediante la [API administrada ews](#bk_determineguidewsma).
  
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
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

El servidor responde a la solicitud **FindFolder** con un mensaje [FindFolderResponse](https://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) que incluye el valor de la **PR_REPLICA_LIST** extendida. Tenga en cuenta que el valor de la propiedad aparece en la respuesta EWS como el formato de cadena de una matriz de bytes codificada en base 64. Algunos valores de encabezado de la respuesta se acortan para que sean legibles. 
  
```XML
<?xml version="1.0" encoding="utf-8"?><s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="1019" MinorBuildNumber="15" Version="V2_17" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body>
    <m:FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

Para usar el valor del **PR_REPLICA_LIST** devuelto en el XML, MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA==, para determinar el GUID del buzón, el valor debe convertirse en un GUID en un formato similar al que se convierte en el ejemplo de código de api administrada [ews](#bk_determineguidewsma). A continuación, el GUID se concatena con el nombre de dominio para crear una dirección SMTP, que se incluye en la [solicitud de detección automática](#bk_makeautodrequest).
  
## <a name="make-an-autodiscover-request"></a>Realizar una solicitud de detección automática
<a name="bk_makeautodrequest"> </a>

Use la dirección devuelta por el  `GetMailboxGuidAddress` método para llamar a Detección automática. Se recomienda usar el Exchange [2013:](https://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) Obtener la configuración del usuario con el ejemplo de código de detección automática para llamar al servicio de detección automática porque simplifica el proceso de detección automática. En este ejemplo de código se usan los argumentos de línea de comandos enumerados en la tabla siguiente para llamar al servicio de detección automática pox para recuperar el valor [AutoDiscoverSMTPAddress](https://msdn.microsoft.com/library/office/dn750991%28v=exchg.150%29.aspx) asociado al GUID del buzón. 

  
|**Argumento**|**Descripción**|
|:-----|:-----|
|emailAddress  <br/> |La dirección devuelta por el  `GetMailboxGuidAddress` método en Determine the GUID of the public folder [mailbox](#bk_determineguidewsma).  <br/> |
|-skipSOAP  <br/> |Indica que las solicitudes de detección automática de POX son necesarias.  <br/> |
|-auth authEmailAddress  <br/> |La dirección de correo electrónico del usuario del buzón, que se usa para la autenticación. Se le pedirá que escriba la contraseña del usuario del buzón cuando ejecute el ejemplo.  <br/> |
   
Por ejemplo, los argumentos de línea de comandos deben tener este aspecto:
  
`1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com -skipSOAP -auth sonyaf@contoso.com`

Dónde `1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com` está la dirección devuelta por el método **GetMailboxGuidAddress** y `sonyaf@contoso.com` es el usuario del buzón. 
  
Al ejecutar el Exchange **2013:** Obtener la configuración del usuario con el ejemplo de detección automática, la última respuesta de detección automática debe ser correcta e incluir toda la configuración de usuario asociada con el GUID del buzón. Guarde la **configuración de usuario AutoDiscoverSMTPAddress** localmente, ya que lo usará en el paso siguiente. 
  
Como alternativa, si no desea usar **Exchange 2013:** Obtener la configuración de usuario con el ejemplo de detección automática, puede obtener la configuración de usuario **AutoDiscoverSMTPAddress** mediante la generación de una lista de extremos de detección automática y, a continuación, enviar la siguiente solicitud de detección automática pox [a](how-to-generate-a-list-of-autodiscover-endpoints.md)cada dirección URL hasta que reciba una respuesta correcta.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com</EMailAddress>
    <AcceptableResponseSchema>https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

Para obtener más información sobre el proceso de detección automática, vea [Autodiscover for Exchange](autodiscover-for-exchange.md), [Generate a list of Autodiscover endpoints](how-to-generate-a-list-of-autodiscover-endpoints.md)y [Get user settings from Exchange by using Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).
  
## <a name="set-the-values-of-the-x-anchormailbox-and-x-publicfoldermailbox-headers"></a>Establecer los valores de los encabezados X-AnchorMailbox y X-PublicFolderMailbox
<a name="bk_setheadervalues"> </a>

Con el valor de **AutoDiscoverSMTPAddress** adquirido en [Make an Autodiscover request](#bk_makeautodrequest), establezca los valores de los encabezados **X-AnchorMailbox** y **X-PublicFolderMailbox** en la solicitud de contenido de la carpeta pública. 
  
Por ejemplo, dado un AutoDiscoverSMTPAddress de NewPublicFolder@contoso.com, incluya los siguientes encabezados al realizar llamadas a los siguientes métodos o operaciones.
  
`X-AnchorMailbox: NewPublicFolder@contoso.com`<br/>
`X-PublicFolderMailbox: NewPublicFolder@contoso.com`

**Llamadas a carpetas públicas que requieren los encabezados X-AncorMailbox y X-PublicFolder**

|**Métodos de administración de la API de EWS**|**Operaciones EWS**|
|:-----|:-----|
|[Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [Item.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> [Item.Copy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> [Item.Move](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> [Item.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> [Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> [Folder.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> [CopyItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> [MoveItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |
   
Para agregar estos encabezados mediante la API administrada ews, use el [método HttpHeaders.Add.](https://msdn.microsoft.com/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", "NewPublicFolder@contoso.com");
service.HttpHeaders.Add("X-PublicFolderMailbox", "NewPublicFolder@contoso.com");
```

El código siguiente muestra una solicitud [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) con el encabezado **X-AnchorMailbox** y **X-PublicFolderMailbox** establecidos en los valores recuperados en los ejemplos de este artículo. 
  
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
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

## <a name="see-also"></a>Ver también

- [Acceso a carpetas públicas con EWS en Exchange](public-folder-access-with-ews-in-exchange.md)    
- [Detección automática en Exchange](autodiscover-for-exchange.md)    
- [Generar una lista de extremos de detección automática](how-to-generate-a-list-of-autodiscover-endpoints.md)   
- [Obtener la configuración de usuario de Exchange mediante el uso de Detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
  
