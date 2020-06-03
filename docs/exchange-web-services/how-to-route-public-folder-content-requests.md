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
# <a name="route-public-folder-content-requests"></a><span data-ttu-id="00933-104">Enrutar solicitudes de contenido de carpetas públicas</span><span class="sxs-lookup"><span data-stu-id="00933-104">Route public folder content requests</span></span>

<span data-ttu-id="00933-105">Todas las solicitudes de información de carpetas públicas que impliquen el contenido de la carpeta pública deben enrutarse al buzón de la carpeta pública que contiene el contenido de la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="00933-105">All requests for public folder information that involve the content of the public folder need to be routed to the public folder mailbox that holds the content for the target folder.</span></span> <span data-ttu-id="00933-106">Para enrutar las solicitudes a ese buzón de correo, debe establecer los encabezados **x-AnchorMailbox** y **x-PublicFolderMailbox** en valores específicos.</span><span class="sxs-lookup"><span data-stu-id="00933-106">To route the requests to that mailbox, you need to set the **X-AnchorMailbox** and **X-PublicFolderMailbox** headers to specific values.</span></span> 
  
<span data-ttu-id="00933-107">En la tabla siguiente se proporciona información general sobre el proceso:</span><span class="sxs-lookup"><span data-stu-id="00933-107">The following table provides an overview of the process:</span></span>
  
<span data-ttu-id="00933-108">**Introducción a la carpeta pública**</span><span class="sxs-lookup"><span data-stu-id="00933-108">**Public folder overview**</span></span>

|<span data-ttu-id="00933-109">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00933-109">Header</span></span>|<span data-ttu-id="00933-110">¿Qué necesito?</span><span class="sxs-lookup"><span data-stu-id="00933-110">What do I need?</span></span>|<span data-ttu-id="00933-111">¿Cómo puedo obtenerlo?</span><span class="sxs-lookup"><span data-stu-id="00933-111">How do I get it?</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="00933-112">**X-AnchorMailbox**</span><span class="sxs-lookup"><span data-stu-id="00933-112">**X-AnchorMailbox**</span></span> <br/> |<span data-ttu-id="00933-113">1. [los valores x-AnchorMailbox y x-PublicFolderInformation](how-to-route-public-folder-hierarchy-requests.md) para el buzón de la jerarquía de carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="00933-113">1. [The X-AnchorMailbox and X-PublicFolderInformation values ](how-to-route-public-folder-hierarchy-requests.md) for the public folder hierarchy mailbox.</span></span><br/><br/><span data-ttu-id="00933-114">2. el GUID del buzón de carpeta pública que contiene el contenido del buzón, que se envía al servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="00933-114">2. The GUID of the public folder mailbox that contains the mailbox content, which is sent to the Autodiscover service.</span></span><br/><br/>  <span data-ttu-id="00933-115">La **AutoDiscoverSMTPAddress** en la respuesta de Autodisover se convierte en el valor del encabezado **X-AnchorMailbox** .</span><span class="sxs-lookup"><span data-stu-id="00933-115">The **AutoDiscoverSMTPAddress** in the Autodisover response becomes the value of the **X-AnchorMailbox** header.</span></span>  <br/> <span data-ttu-id="00933-116">![TODO](media/Ex15_PF_PFContent.png)</span><span class="sxs-lookup"><span data-stu-id="00933-116">![TODO](media/Ex15_PF_PFContent.png)</span></span>| <span data-ttu-id="00933-117">1. Use el ejemplo de código de este artículo, que [implementa la API administrada de EWS](#bk_determineguidewsma).</span><span class="sxs-lookup"><span data-stu-id="00933-117">1. Use the code example in this article, which [implements the EWS Managed API](#bk_determineguidewsma).</span></span> <span data-ttu-id="00933-118">O bien, [use EWS](#bk_determineguidews) y convierta los resultados para obtener un GUID.</span><span class="sxs-lookup"><span data-stu-id="00933-118">Or [use EWS](#bk_determineguidews) and convert your results to obtain a GUID.</span></span><br/><br/><span data-ttu-id="00933-119">2. [realice una solicitud de detección automática](#bk_makeautodrequest) usando el GUID y el nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="00933-119">2. [Make an Autodiscover request](#bk_makeautodrequest) by using the GUID plus the domain name.</span></span><br/><br/><span data-ttu-id="00933-120">3. Use el valor del elemento **AutoDiscoverSMTPAddress** devuelto en la respuesta de detección automática para [rellenar el valor de los encabezados](#bk_setheadervalues).</span><span class="sxs-lookup"><span data-stu-id="00933-120">3. Use the value of the **AutoDiscoverSMTPAddress** element returned in the Autodiscover response to [populate the value of the headers](#bk_setheadervalues).</span></span>  <br/> |
|<span data-ttu-id="00933-121">**X-PublicFolderMailbox**</span><span class="sxs-lookup"><span data-stu-id="00933-121">**X-PublicFolderMailbox**</span></span> <br/> |<span data-ttu-id="00933-122">El trabajo se ha realizado, el valor X-PublicFolderMailbox es el mismo que el valor X-AnchorMailbox</span><span class="sxs-lookup"><span data-stu-id="00933-122">Your work is done, the X-PublicFolderMailbox value is the same as the X-AnchorMailbox value!</span></span>  <br/> |<span data-ttu-id="00933-123">Ya lo ha hecho.</span><span class="sxs-lookup"><span data-stu-id="00933-123">You already have it!</span></span>  <br/> |
   
<span data-ttu-id="00933-124">Una vez que haya determinado los valores de encabezado, incluidos [al realizar solicitudes de contenido de carpetas públicas](#bk_setheadervalues).</span><span class="sxs-lookup"><span data-stu-id="00933-124">After you have determined the header values, include them [when you make public folder content requests](#bk_setheadervalues).</span></span>
  
<span data-ttu-id="00933-125">Los pasos de este artículo son específicos de las solicitudes de contenido de carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="00933-125">The steps in this article are specific to public folder content requests.</span></span> <span data-ttu-id="00933-126">Para determinar si su solicitud es una jerarquía de carpetas públicas o una solicitud de contenido, consulte [enrutamiento de solicitudes de carpetas públicas](public-folder-access-with-ews-in-exchange.md#bk_routing).</span><span class="sxs-lookup"><span data-stu-id="00933-126">To determine whether your request is a public folder hierarchy or content request, see [Routing public folder requests](public-folder-access-with-ews-in-exchange.md#bk_routing).</span></span>

<span data-ttu-id="00933-127"><a name="bk_determineguidewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="00933-127"><a name="bk_determineguidewsma"> </a></span></span>

## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-the-ews-managed-api"></a><span data-ttu-id="00933-128">Determinación del GUID del buzón de carpetas públicas mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="00933-128">Determine the GUID of the public folder mailbox by using the EWS Managed API</span></span>


<span data-ttu-id="00933-129">Para determinar el GUID del buzón de contenido de la carpeta pública, use el siguiente ejemplo de código, que hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="00933-129">To determine the GUID of the public folder content mailbox, use the following code example, which does the following:</span></span> 
  
- <span data-ttu-id="00933-130">Usa los encabezados **x-AnchorMailbox** y **x-PublicFolderInformation** que recuperó mediante el [enrutamiento de solicitudes de jerarquía de carpetas públicas](how-to-route-public-folder-hierarchy-requests.md).</span><span class="sxs-lookup"><span data-stu-id="00933-130">Uses the **X-AnchorMailbox** and **X-PublicFolderInformation** headers you retrieved by [routing public folder hierarchy requests](how-to-route-public-folder-hierarchy-requests.md).</span></span>
    
- <span data-ttu-id="00933-131">Llama al método [FindFolders](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) de la API administrada de EWS e incluye una solicitud para la propiedad **PR_REPLICA_LIST** (0x66980102).</span><span class="sxs-lookup"><span data-stu-id="00933-131">Calls the EWS Managed API [FindFolders](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) method, and includes a request for the **PR_REPLICA_LIST** (0x66980102) property</span></span> 
    
<span data-ttu-id="00933-132">El valor **PR_REPLICA_LIST** identifica el GUID del buzón de correo de la carpeta pública que tiene el contenido de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="00933-132">The **PR_REPLICA_LIST** value identifies the mailbox GUID of the public folder mailbox that has the content for the folder.</span></span> <span data-ttu-id="00933-133">La propiedad **PR_REPLICA_LIST** es una matriz de bytes, pero se convierte en un GUID para este escenario.</span><span class="sxs-lookup"><span data-stu-id="00933-133">The **PR_REPLICA_LIST** property is a byte array, but is cast as a GUID for this scenario.</span></span> <span data-ttu-id="00933-134">El GUID y el nombre de dominio se concatenan para formar la dirección en la que se va a llamar a detección automática.</span><span class="sxs-lookup"><span data-stu-id="00933-134">The GUID and the domain name are concatenated to form the address on which to call Autodiscover.</span></span> 
  
<span data-ttu-id="00933-135">En este ejemplo se supone que `service` es el objeto [ExchangeService](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) para el usuario de buzón de correo, `PFHAnchorHeader` y `PFHMailboxHeader` son los valores de los encabezados **x-AnchorMailbox** y **x-PublicFolderMailbox** , y domain es el nombre de dominio que usa el inquilino.</span><span class="sxs-lookup"><span data-stu-id="00933-135">This example assumes that  `service` is the [ExchangeService](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox user,  `PFHAnchorHeader` and  `PFHMailboxHeader` are the values of the **X-AnchorMailbox** and **X-PublicFolderMailbox** headers, and domain is the domain name used by the tenant.</span></span> 
  
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

<span data-ttu-id="00933-136">Si recibió el error "error en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="00933-136">If you received the error "The request failed.</span></span> <span data-ttu-id="00933-137">Se cerró la conexión subyacente: no se pudo establecer una relación de confianza para el canal seguro SSL/TLS ", tendrá que [Agregar una llamada a un método de devolución de llamada de validación](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span><span class="sxs-lookup"><span data-stu-id="00933-137">The underlying connection was closed: Could not establish trust relationship for the SSL/TLS secure channel", you'll need to [add a call to a validation callback method](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span></span> <span data-ttu-id="00933-138">En el ejemplo de código se incluye un marcador de posición y un comentario para ese método.</span><span class="sxs-lookup"><span data-stu-id="00933-138">A placeholder and comment for that method is included in the code example.</span></span>
  
<span data-ttu-id="00933-139">Si el GUID del buzón es el mismo para todas las carpetas públicas de la raíz de la carpeta pública, el ejemplo indica la dirección que se va a usar al [llamar a detección automática](#bk_makeautodrequest) en el resultado de la consola y como el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="00933-139">If the mailbox GUID is the same for all the public folders under the public folder root, the example indicates the address to use when [calling Autodiscover](#bk_makeautodrequest) in the console output and as the return value.</span></span> <span data-ttu-id="00933-140">Si el GUID del buzón no es el mismo para todas las carpetas públicas en la raíz de la carpeta pública, debe [realizar una solicitud de detección automática](#bk_makeautodrequest) en la dirección asociada a la carpeta en la solicitud de contenido.</span><span class="sxs-lookup"><span data-stu-id="00933-140">If the mailbox GUID is not the same for all public folders under the public folder root, you need to [Make an Autodiscover request](#bk_makeautodrequest) on the address associated with the folder in your content request.</span></span> 

<span data-ttu-id="00933-141"><a name="bk_determineguidews"> </a></span><span class="sxs-lookup"><span data-stu-id="00933-141"><a name="bk_determineguidews"> </a></span></span>

## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-ews"></a><span data-ttu-id="00933-142">Determinación del GUID del buzón de carpetas públicas mediante EWS</span><span class="sxs-lookup"><span data-stu-id="00933-142">Determine the GUID of the public folder mailbox by using EWS</span></span>

<span data-ttu-id="00933-143">En el ejemplo de código siguiente se muestra cómo recuperar el valor de la propiedad **PR_REPLICA_LIST** (0x66980102) mediante la operación [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) de EWS.</span><span class="sxs-lookup"><span data-stu-id="00933-143">The following code example shows how retrieve the value of the **PR_REPLICA_LIST** (0x66980102) property by using the EWS [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="00933-144">En el caso del elemento [ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) , el atributo **PropertyTag** se establece en el valor decimal (26264) de la propiedad **PR_REPLICA_LIST** y el atributo **PropertyType** se establece en **Binary**.</span><span class="sxs-lookup"><span data-stu-id="00933-144">For the [ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) element, the **PropertyTag** attribute is set to the decimal value (26264) of the **PR_REPLICA_LIST** property, and the **PropertyType** attribute is set to **Binary**.</span></span>
  
<span data-ttu-id="00933-145">También es la solicitud XML que la API administrada de EWS envía cuando usa el método **FindFolders** para [determinar el GUID del buzón de carpetas públicas mediante la API administrada de EWS](#bk_determineguidewsma).</span><span class="sxs-lookup"><span data-stu-id="00933-145">This is also the XML request that the EWS Managed API sends when you use the **FindFolders** method to [determine the GUID of the public folder mailbox by using the EWS Managed API](#bk_determineguidewsma).</span></span>
  
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

<span data-ttu-id="00933-146">El servidor responde a la solicitud **FindFolder** con un mensaje [FindFolderResponse](https://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) que incluye el valor de la propiedad extendida **PR_REPLICA_LIST** .</span><span class="sxs-lookup"><span data-stu-id="00933-146">The server responds to the **FindFolder** request with a [FindFolderResponse](https://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) message that includes the value of the **PR_REPLICA_LIST** extended property.</span></span> <span data-ttu-id="00933-147">Tenga en cuenta que el valor de la propiedad aparece en la respuesta de EWS como el formato de cadena de una matriz de bytes codificada en base 64.</span><span class="sxs-lookup"><span data-stu-id="00933-147">Note that the value of the property appears on the EWS response as the string format of a base-64 encoded byte array.</span></span> <span data-ttu-id="00933-148">Algunos valores de encabezado de la respuesta se acortan para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="00933-148">Some header values in the response are shortened for readability.</span></span> 
  
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

<span data-ttu-id="00933-149">Para usar el valor de la **PR_REPLICA_LIST** devuelta en el XML, MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA = =, para determinar el GUID de buzón, el valor debe convertirse en un GUID en un formato similar al de la conversión del valor en el ejemplo de código de la [API administrada de EWS](#bk_determineguidewsma).</span><span class="sxs-lookup"><span data-stu-id="00933-149">In order to use the value of the **PR_REPLICA_LIST** returned in the XML, MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA==, to determine the mailbox GUID, the value must be converted into a GUID in a format similar to how the value is converted in the [EWS Managed API code example](#bk_determineguidewsma).</span></span> <span data-ttu-id="00933-150">A continuación, el GUID se concatena con el nombre de dominio para crear una dirección SMTP, que se incluye en la [solicitud de detección automática](#bk_makeautodrequest).</span><span class="sxs-lookup"><span data-stu-id="00933-150">The GUID is then concatenated with the domain name to create an SMTP address, which is included in the [Autodiscover request](#bk_makeautodrequest).</span></span>
  
## <a name="make-an-autodiscover-request"></a><span data-ttu-id="00933-151">Realizar una solicitud de detección automática</span><span class="sxs-lookup"><span data-stu-id="00933-151">Make an Autodiscover request</span></span>
<span data-ttu-id="00933-152"><a name="bk_makeautodrequest"> </a></span><span class="sxs-lookup"><span data-stu-id="00933-152"><a name="bk_makeautodrequest"> </a></span></span>

<span data-ttu-id="00933-153">Use la dirección devuelta por el `GetMailboxGuidAddress` método para llamar a detección automática.</span><span class="sxs-lookup"><span data-stu-id="00933-153">Use the address returned by the  `GetMailboxGuidAddress` method to call Autodiscover.</span></span> <span data-ttu-id="00933-154">Le recomendamos que use el ejemplo de código [Exchange 2013: obtener configuración de usuario con detección automática](https://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) para llamar al servicio Detección automática porque optimiza el proceso de detección automática por usted.</span><span class="sxs-lookup"><span data-stu-id="00933-154">We recommend that you use the [Exchange 2013: Get user settings with Autodiscover](https://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) code sample to call the Autodiscover service because it streamlines the Autodiscover process for you.</span></span> <span data-ttu-id="00933-155">Este ejemplo de código usa los argumentos de línea de comandos enumerados en la siguiente tabla para llamar al servicio Detección automática de POX para recuperar el valor [AutoDiscoverSMTPAddress](https://msdn.microsoft.com/library/office/dn750991%28v=exchg.150%29.aspx) asociado al GUID de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="00933-155">This code sample uses the command-line arguments listed in the following table to call the POX Autodiscover service to retrieve the [AutoDiscoverSMTPAddress](https://msdn.microsoft.com/library/office/dn750991%28v=exchg.150%29.aspx) value associated with the mailbox GUID.</span></span> 

  
|<span data-ttu-id="00933-156">**Argumento**</span><span class="sxs-lookup"><span data-stu-id="00933-156">**Argument**</span></span>|<span data-ttu-id="00933-157">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="00933-157">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00933-158">emailAddress</span><span class="sxs-lookup"><span data-stu-id="00933-158">emailAddress</span></span>  <br/> |<span data-ttu-id="00933-159">La dirección devuelta por el `GetMailboxGuidAddress` método para [determinar el GUID del buzón de carpetas públicas](#bk_determineguidewsma).</span><span class="sxs-lookup"><span data-stu-id="00933-159">The address returned by the  `GetMailboxGuidAddress` method in [Determine the GUID of the public folder mailbox](#bk_determineguidewsma).</span></span>  <br/> |
|<span data-ttu-id="00933-160">-skipSOAP</span><span class="sxs-lookup"><span data-stu-id="00933-160">-skipSOAP</span></span>  <br/> |<span data-ttu-id="00933-161">Indica que las solicitudes de detección automática de POX son necesarias.</span><span class="sxs-lookup"><span data-stu-id="00933-161">Indicates that POX Autodiscover requests are required.</span></span>  <br/> |
|<span data-ttu-id="00933-162">-auth authEmailAddress</span><span class="sxs-lookup"><span data-stu-id="00933-162">-auth authEmailAddress</span></span>  <br/> |<span data-ttu-id="00933-163">La dirección de correo electrónico del usuario del buzón, que se usa para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="00933-163">The mailbox user's email address, which is used for authentication.</span></span> <span data-ttu-id="00933-164">Al ejecutar el ejemplo, se le pedirá que escriba la contraseña del usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="00933-164">You will be prompted to enter the mailbox user's password when you run the sample.</span></span>  <br/> |
   
<span data-ttu-id="00933-165">Por ejemplo, los argumentos de la línea de comandos deben tener el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="00933-165">For example, the command-line arguments should look like this:</span></span>
  
`1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com -skipSOAP -auth sonyaf@contoso.com`

<span data-ttu-id="00933-166">Donde `1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com` es la dirección devuelta por el método **GetMailboxGuidAddress** y `sonyaf@contoso.com` es el usuario del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="00933-166">Where `1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com` is the address returned by the **GetMailboxGuidAddress** method, and `sonyaf@contoso.com` is the mailbox user.</span></span> 
  
<span data-ttu-id="00933-167">Al ejecutar el ejemplo **Exchange 2013: obtener configuración de usuario con detección automática** , la última respuesta de detección automática debería ser correcta e incluir todas las configuraciones de usuario asociadas con el GUID de buzón.</span><span class="sxs-lookup"><span data-stu-id="00933-167">When you run the **Exchange 2013: Get user settings with Autodiscover** sample, the last Autodiscover response should be successful and include all the user settings associated with the mailbox GUID.</span></span> <span data-ttu-id="00933-168">Guarde la configuración de usuario **AutoDiscoverSMTPAddress** de forma local, como la usará en el paso siguiente.</span><span class="sxs-lookup"><span data-stu-id="00933-168">Save the **AutoDiscoverSMTPAddress** user setting locally, as you'll use that in the next step.</span></span> 
  
<span data-ttu-id="00933-169">Como alternativa, si no quiere usar **Exchange 2013: obtener configuración de usuario con la detección automática** , puede obtener la configuración de usuario **AutoDiscoverSMTPAddress** [generando una lista de extremos de detección automática](how-to-generate-a-list-of-autodiscover-endpoints.md)y, a continuación, enviando la siguiente solicitud de detección automática de POX a cada dirección URL hasta que reciba una respuesta correcta.</span><span class="sxs-lookup"><span data-stu-id="00933-169">Alternatively, if you do not want to use **Exchange 2013: Get user settings with Autodiscover** sample, you can get the **AutoDiscoverSMTPAddress** user setting by [generating a list of Autodiscover endpoints](how-to-generate-a-list-of-autodiscover-endpoints.md), and then sending the following POX Autodiscover request to each URL until you receive a successful response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com</EMailAddress>
    <AcceptableResponseSchema>https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

<span data-ttu-id="00933-170">Para obtener más información sobre el proceso de detección automática, consulte [detección automática para Exchange](autodiscover-for-exchange.md), [generar una lista de extremos de detección automática](how-to-generate-a-list-of-autodiscover-endpoints.md)y [obtener la configuración de usuario de Exchange mediante detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).</span><span class="sxs-lookup"><span data-stu-id="00933-170">For more information about the Autodiscover process, see [Autodiscover for Exchange](autodiscover-for-exchange.md), [Generate a list of Autodiscover endpoints](how-to-generate-a-list-of-autodiscover-endpoints.md), and [Get user settings from Exchange by using Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).</span></span>
  
## <a name="set-the-values-of-the-x-anchormailbox-and-x-publicfoldermailbox-headers"></a><span data-ttu-id="00933-171">Establecer los valores de los encabezados X-AnchorMailbox y X-PublicFolderMailbox</span><span class="sxs-lookup"><span data-stu-id="00933-171">Set the values of the X-AnchorMailbox and X-PublicFolderMailbox headers</span></span>
<span data-ttu-id="00933-172"><a name="bk_setheadervalues"> </a></span><span class="sxs-lookup"><span data-stu-id="00933-172"><a name="bk_setheadervalues"> </a></span></span>

<span data-ttu-id="00933-173">Con el valor de **AutoDiscoverSMTPAddress** adquirido en [realizar una solicitud de detección automática](#bk_makeautodrequest), establezca los valores de los encabezados **x-AnchorMailbox** y **x-PublicFolderMailbox** en la solicitud de contenido de la carpeta pública.</span><span class="sxs-lookup"><span data-stu-id="00933-173">Using the value for the **AutoDiscoverSMTPAddress** acquired in [Make an Autodiscover request](#bk_makeautodrequest), set the values of the **X-AnchorMailbox** and **X-PublicFolderMailbox** headers in your public folder content request.</span></span> 
  
<span data-ttu-id="00933-174">Por ejemplo, dada una AutoDiscoverSMTPAddress de NewPublicFolder@contoso.com, incluya los siguientes encabezados al realizar llamadas a los siguientes métodos u operaciones.</span><span class="sxs-lookup"><span data-stu-id="00933-174">For example, given an AutoDiscoverSMTPAddress of NewPublicFolder@contoso.com, include the following headers when making calls to the following methods or operations.</span></span>
  
`X-AnchorMailbox: NewPublicFolder@contoso.com`<br/>
`X-PublicFolderMailbox: NewPublicFolder@contoso.com`

<span data-ttu-id="00933-175">**Llamadas a carpetas públicas que requieren los encabezados X-AncorMailbox y X-PublicFolder**</span><span class="sxs-lookup"><span data-stu-id="00933-175">**Public folder calls that require the X-AncorMailbox and X-PublicFolder headers**</span></span>

|<span data-ttu-id="00933-176">**Métodos de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="00933-176">**EWS Managed API methods**</span></span>|<span data-ttu-id="00933-177">**Operaciones de EWS**</span><span class="sxs-lookup"><span data-stu-id="00933-177">**EWS operations**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="00933-178">Item. bind</span><span class="sxs-lookup"><span data-stu-id="00933-178">Item.Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="00933-179">Item. Update</span><span class="sxs-lookup"><span data-stu-id="00933-179">Item.Update</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="00933-180">Item. Copy</span><span class="sxs-lookup"><span data-stu-id="00933-180">Item.Copy</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="00933-181">Item. Move</span><span class="sxs-lookup"><span data-stu-id="00933-181">Item.Move</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="00933-182">Item. Delete</span><span class="sxs-lookup"><span data-stu-id="00933-182">Item.Delete</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="00933-183">Folder. bind</span><span class="sxs-lookup"><span data-stu-id="00933-183">Folder.Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="00933-184">Folder. FindItems</span><span class="sxs-lookup"><span data-stu-id="00933-184">Folder.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="00933-185">CreateItem</span><span class="sxs-lookup"><span data-stu-id="00933-185">CreateItem</span></span>](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> [<span data-ttu-id="00933-186">GetItem</span><span class="sxs-lookup"><span data-stu-id="00933-186">GetItem</span></span>](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> [<span data-ttu-id="00933-187">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="00933-187">UpdateItem</span></span>](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> [<span data-ttu-id="00933-188">CopyItem</span><span class="sxs-lookup"><span data-stu-id="00933-188">CopyItem</span></span>](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> [<span data-ttu-id="00933-189">MoveItem</span><span class="sxs-lookup"><span data-stu-id="00933-189">MoveItem</span></span>](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> [<span data-ttu-id="00933-190">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="00933-190">DeleteItem</span></span>](../web-service-reference/deleteitem-operation.md) <br/> [<span data-ttu-id="00933-191">GetFolder</span><span class="sxs-lookup"><span data-stu-id="00933-191">GetFolder</span></span>](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> [<span data-ttu-id="00933-192">FindItem</span><span class="sxs-lookup"><span data-stu-id="00933-192">FindItem</span></span>](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="00933-193">Para agregar estos encabezados mediante la API administrada de EWS, use el método [HttpHeaders. Add](https://msdn.microsoft.com/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="00933-193">To add these headers by using the EWS Managed API, use the [HttpHeaders.Add](https://msdn.microsoft.com/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) method.</span></span> 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", "NewPublicFolder@contoso.com");
service.HttpHeaders.Add("X-PublicFolderMailbox", "NewPublicFolder@contoso.com");
```

<span data-ttu-id="00933-194">El siguiente código muestra una solicitud [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) con el encabezado **x-AnchorMailbox** y **x-PublicFolderMailbox** establecido en los valores que se han recuperado en los ejemplos de este artículo.</span><span class="sxs-lookup"><span data-stu-id="00933-194">The following code shows a [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) request with the **X-AnchorMailbox** and **X-PublicFolderMailbox** header set to the values retrieved in the examples in this article.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="00933-195">Vea también</span><span class="sxs-lookup"><span data-stu-id="00933-195">See also</span></span>

- [<span data-ttu-id="00933-196">Acceso a carpetas públicas con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="00933-196">Public folder access with EWS in Exchange</span></span>](public-folder-access-with-ews-in-exchange.md)    
- [<span data-ttu-id="00933-197">Detección automática en Exchange</span><span class="sxs-lookup"><span data-stu-id="00933-197">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)    
- [<span data-ttu-id="00933-198">Generar una lista de extremos de detección automática</span><span class="sxs-lookup"><span data-stu-id="00933-198">Generate a list of Autodiscover endpoints</span></span>](how-to-generate-a-list-of-autodiscover-endpoints.md)   
- [<span data-ttu-id="00933-199">Obtener la configuración de usuario de Exchange mediante el uso de detección automática</span><span class="sxs-lookup"><span data-stu-id="00933-199">Get user settings from Exchange by using Autodiscover</span></span>](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
  