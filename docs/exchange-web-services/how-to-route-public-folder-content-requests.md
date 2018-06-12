---
title: Enrutar las solicitudes de contenido de carpetas públicas
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 59d2f05e-90fb-471e-ac06-70becc15b295
description: Todas las solicitudes de información de carpetas públicas que implican el contenido de la necesidad de carpetas públicas se enrutan al buzón de carpeta pública contiene el contenido de la carpeta de destino. Para enrutar las solicitudes a ese buzón, debe establecer los encabezados X-AnchorMailbox y X-PublicFolderMailbox a valores específicos.
ms.openlocfilehash: ad36c1526a24d815ec690879d633774d429ed36c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763181"
---
# <a name="route-public-folder-content-requests"></a>Enrutar las solicitudes de contenido de carpetas públicas

Todas las solicitudes de información de carpetas públicas que implican el contenido de la necesidad de carpetas públicas se enrutan al buzón de carpeta pública contiene el contenido de la carpeta de destino. Para enrutar las solicitudes a ese buzón, debe establecer los encabezados **X-AnchorMailbox** y **X-PublicFolderMailbox** a valores específicos. 
  
En la siguiente tabla se proporciona información general sobre el proceso:
  
**Introducción a la carpeta pública**

|Encabezado|¿Qué es necesario?|¿Cómo se puede obtener?|
|:-----|:-----|:-----|
|**X-AnchorMailbox** <br/> |1. [los X-AnchorMailbox y los valores de X-PublicFolderInformation](how-to-route-public-folder-hierarchy-requests.md) para el buzón de la jerarquía de carpetas públicas.<br/><br/>2. el GUID del buzón de carpeta pública que contiene el contenido del buzón de correo, que se envía al servicio de detección automática.<br/><br/>  El **AutoDiscoverSMTPAddress** en la respuesta de Autodisover se convierte en el valor del encabezado **X-AnchorMailbox** .  <br/> ![TODO](media/Ex15_PF_PFContent.png)| 1. use el ejemplo de código de este artículo, que [implementa la API administrada de EWS](#bk_determineguidewsma). O bien [usar EWS](#bk_determineguidews) y convertir los resultados para obtener un GUID.<br/><br/>2. [realizar una solicitud de detección automática](#bk_makeautodrequest) mediante el GUID y el nombre de dominio.<br/><br/>3. use el valor del elemento **AutoDiscoverSMTPAddress** devuelto en la respuesta de detección automática para [rellenar el valor de los encabezados](#bk_setheadervalues).  <br/> |
|**X-PublicFolderMailbox** <br/> |Se realiza el trabajo, el valor de X-PublicFolderMailbox es el mismo que el valor de X-AnchorMailbox!  <br/> |Ya lo tiene.  <br/> |
   
Una vez que haya determinado los valores de encabezado, incluirlos [cuando realiza las solicitudes de contenido de carpetas públicas](#bk_setheadervalues).
  
Los pasos descritos en este artículo son específicos de las solicitudes de contenido de carpetas públicas. Para determinar si la solicitud es una solicitud de contenido o la jerarquía de carpetas públicas, vea [las solicitudes de carpetas públicas de enrutamiento](public-folder-access-with-ews-in-exchange.md#bk_routing).
  
## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-the-ews-managed-api"></a>Determinar el GUID del buzón de carpetas públicas mediante el uso de la API administrada de EWS
<a name="bk_determineguidewsma"> </a>

Para determinar el GUID del buzón de contenido de carpetas públicas, use el siguiente ejemplo de código, que hace lo siguiente: 
  
- Usa los encabezados **X-AnchorMailbox** y **X-PublicFolderInformation** recuperado por el [enrutamiento de las solicitudes de jerarquía de carpetas públicas](how-to-route-public-folder-hierarchy-requests.md).
    
- Llama al método de la API administrada de EWS [FindFolders](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) e incluye una solicitud para la propiedad **PR_REPLICA_LIST** (0x66980102) 
    
El valor **PR_REPLICA_LIST** identifica el GUID del buzón de carpeta pública que tiene el contenido de la carpeta de buzón. La propiedad **PR_REPLICA_LIST** es una matriz de bytes, pero se convierte como un GUID para este escenario. El GUID y el nombre de dominio se concatenen para formar la dirección en la que se llama a la detección automática. 
  
En este ejemplo se da por supuesto que `service` es el objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) para el usuario de buzón de correo, `PFHAnchorHeader` y `PFHMailboxHeader` son los valores de los encabezados **X-AnchorMailbox** y **X-PublicFolderMailbox** y dominio es el nombre de dominio utilizado por el inquilino. 
  
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

Si ha recibido el error "Error en la solicitud. Se cerró la conexión subyacente: no se pude establecer una relación de confianza para el canal seguro SSL/TLS ", debe [Agregar una llamada a un método de devolución de llamada de validación](how-to-validate-a-server-certificate-for-the-ews-managed-api.md). Un marcador de posición y un comentario para este método se incluye en el ejemplo de código.
  
Si el GUID de buzón es el mismo para todas las carpetas públicas en la raíz de la carpeta pública, en el ejemplo se indica la dirección para usar al [llamar a la detección automática](#bk_makeautodrequest) en la consola de salida y como el valor devuelto. Si el GUID de buzón no es el mismo para todas las carpetas públicas en la raíz de carpetas públicas, debe [realizar una solicitud de detección automática](#bk_makeautodrequest) en la dirección asociada a la carpeta en su solicitud de contenido. 
  
## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-ews"></a>Determinar el GUID del buzón de carpetas públicas mediante el uso de EWS
<a name="bk_determineguidews"> </a>

El ejemplo de código siguiente se muestra cómo recuperar el valor de la propiedad **PR_REPLICA_LIST** (0x66980102) mediante el uso de la operación de EWS [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) . Para el elemento [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) , el atributo **PropertyTag** se establece en el valor decimal (26264) de la propiedad **PR_REPLICA_LIST** y se establece el atributo **PropertyType** en **binario**.
  
También es la solicitud XML que la API administrada de EWS envía cuando se utiliza el método **FindFolders** para [determinar el GUID del buzón de carpetas públicas mediante el uso de la API administrada de EWS](#bk_determineguidewsma).
  
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

El servidor responde a la solicitud de **FindFolder** con un mensaje de [FindFolderResponse](http://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) que incluye el valor de la **PR_REPLICA_LIST** propiedad extendida. Tenga en cuenta que el valor de la propiedad aparece en la respuesta EWS como el formato de cadena de un valor de base-64 codificada matriz de bytes. Algunos valores de encabezado en la respuesta se acortan para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?><s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
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

Para poder usar el valor de la **PR_REPLICA_LIST** devuelto en el XML, MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA ==, para determinar el GUID de buzón, el valor se debe convertir en un GUID en un formato similar a cómo se convierte el valor en el [Ejemplo de código de API administrada de EWS](#bk_determineguidewsma). El GUID, a continuación, se concatena con el nombre de dominio para crear una dirección SMTP, que se incluye en la [solicitud de detección automática](#bk_makeautodrequest).
  
## <a name="make-an-autodiscover-request"></a>Para realizar una solicitud de detección automática
<a name="bk_makeautodrequest"> </a>

Usar la dirección devuelta por la `GetMailboxGuidAddress` método para llamar a la detección automática. Se recomienda que use la [Exchange 2013: obtener la configuración de usuario con detección automática](http://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) ejemplo de código para llamar al servicio de detección automática debido a que optimiza el proceso de detección automática para usted. Este ejemplo de código usa los argumentos de línea de comandos que aparecen en la tabla siguiente para llamar al servicio de detección automática de POX para recuperar el valor de [AutoDiscoverSMTPAddress](http://msdn.microsoft.com/en-us/library/office/dn750991%28v=exchg.150%29.aspx) asociado con el GUID de buzón. 
  
|**Argumento**|**Descripción**|
|:-----|:-----|
|emailAddress  <br/> |La dirección devuelta por la `GetMailboxGuidAddress` método en [Determine el GUID del buzón de carpetas públicas](http://msdn.microsoft.com/library/bk_determineguidewsma.aspx).  <br/> |
|-skipSOAP  <br/> |Indica que las solicitudes de detección automática de POX son necesarias.  <br/> |
|authEmailAddress - auth  <br/> |Dirección de correo electrónico del usuario de buzón de correo, que se usa para la autenticación. Se le pedirá para escribir la contraseña del usuario de buzón de correo al ejecutar el ejemplo.  <br/> |
   
Por ejemplo, los argumentos de línea de comandos deben tener un aspecto similar:
  
`1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com -skipSOAP -auth sonyaf@contoso.com`

Donde `1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com` es la dirección devuelta por el método **GetMailboxGuidAddress** , y `sonyaf@contoso.com` es el usuario de buzón de correo. 
  
Al ejecutar el **Exchange 2013: obtener la configuración de usuario con detección automática** ejemplo, la última respuesta de detección automática debe ser correcta e incluir todos los la configuración del usuario asociada con el GUID de buzón. Guardar usuario **AutoDiscoverSMTPAddress** establecer localmente, como se usará que en el paso siguiente. 
  
Como alternativa, si no desea usar **Exchange 2013: obtener la configuración de usuario con detección automática** ejemplo, puede obtener el usuario **AutoDiscoverSMTPAddress** establecer mediante la [generación de una lista de extremos de detección automática de](how-to-generate-a-list-of-autodiscover-endpoints.md)y, a continuación, enviar lo siguiente Solicitud de detección automática POX a cada dirección URL hasta que recibe una respuesta correcta.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com</EMailAddress>
    <AcceptableResponseSchema>http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

Para obtener más información acerca del proceso de detección automática, vea [detección automática de Exchange](autodiscover-for-exchange.md), [generar una lista de extremos de detección automática](how-to-generate-a-list-of-autodiscover-endpoints.md)y [obtener la configuración de usuario de Exchange mediante el uso de detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).
  
## <a name="set-the-values-of-the-x-anchormailbox-and-x-publicfoldermailbox-headers"></a>Establezca los valores de los encabezados X-AnchorMailbox y X-PublicFolderMailbox
<a name="bk_setheadervalues"> </a>

Con el valor de la **AutoDiscoverSMTPAddress** adquirido en [realizar una solicitud de detección automática](#bk_makeautodrequest), establezca los valores de los encabezados **X-AnchorMailbox** y **X-PublicFolderMailbox** en su solicitud de contenido de carpetas públicas. 
  
Por ejemplo, dado un AutoDiscoverSMTPAddress de NewPublicFolder@contoso.com, debe incluir los encabezados siguientes cuando efectúe llamadas a las operaciones o los métodos siguientes.
  
`X-AnchorMailbox: NewPublicFolder@contoso.com`<br/>
`X-PublicFolderMailbox: NewPublicFolder@contoso.com`

**Llamadas de carpeta pública que requieren los encabezados X-AncorMailbox y X-PublicFolder**

|**Métodos de la API administrada de EWS**|**Operaciones de EWS**|
|:-----|:-----|
|[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [Item.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> [Item.Copy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> [Item.Move](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> [Item.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> [Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> |[CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> [CopyItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> [MoveItem](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |
   
Para agregar estos encabezados mediante el uso de la API administrada de EWS, use el método [HttpHeaders.Add](http://msdn.microsoft.com/en-us/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) . 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", "NewPublicFolder@contoso.com");
service.HttpHeaders.Add("X-PublicFolderMailbox", "NewPublicFolder@contoso.com");
```

El código siguiente muestra una solicitud [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) con el encabezado **X-AnchorMailbox** y **X-PublicFolderMailbox** establecido en los valores recuperados en los ejemplos de este artículo. 
  
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

- [Carpetas públicas en Exchange obtener acceso con EWS](public-folder-access-with-ews-in-exchange.md)    
- [Detección automática de Exchange](autodiscover-for-exchange.md)    
- [Generar una lista de extremos de detección automática](how-to-generate-a-list-of-autodiscover-endpoints.md)   
- [Obtener la configuración de usuario de Exchange mediante el uso de detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    

