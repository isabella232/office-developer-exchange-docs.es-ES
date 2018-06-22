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
# <a name="route-public-folder-content-requests"></a><span data-ttu-id="1d96e-104">Enrutar las solicitudes de contenido de carpetas públicas</span><span class="sxs-lookup"><span data-stu-id="1d96e-104">Route public folder content requests</span></span>

<span data-ttu-id="1d96e-105">Todas las solicitudes de información de carpetas públicas que implican el contenido de la necesidad de carpetas públicas se enrutan al buzón de carpeta pública contiene el contenido de la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="1d96e-105">All requests for public folder information that involve the content of the public folder need to be routed to the public folder mailbox that holds the content for the target folder.</span></span> <span data-ttu-id="1d96e-106">Para enrutar las solicitudes a ese buzón, debe establecer los encabezados **X-AnchorMailbox** y **X-PublicFolderMailbox** a valores específicos.</span><span class="sxs-lookup"><span data-stu-id="1d96e-106">To route the requests to that mailbox, you need to set the **X-AnchorMailbox** and **X-PublicFolderMailbox** headers to specific values.</span></span> 
  
<span data-ttu-id="1d96e-107">En la siguiente tabla se proporciona información general sobre el proceso:</span><span class="sxs-lookup"><span data-stu-id="1d96e-107">The following table provides an overview of the process:</span></span>
  
<span data-ttu-id="1d96e-108">**Introducción a la carpeta pública**</span><span class="sxs-lookup"><span data-stu-id="1d96e-108">**Public folder overview**</span></span>

|<span data-ttu-id="1d96e-109">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d96e-109">Header</span></span>|<span data-ttu-id="1d96e-110">¿Qué es necesario?</span><span class="sxs-lookup"><span data-stu-id="1d96e-110">What do I need?</span></span>|<span data-ttu-id="1d96e-111">¿Cómo se puede obtener?</span><span class="sxs-lookup"><span data-stu-id="1d96e-111">How do I get it?</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1d96e-112">**X-AnchorMailbox**</span><span class="sxs-lookup"><span data-stu-id="1d96e-112">**X-AnchorMailbox**</span></span> <br/> |<span data-ttu-id="1d96e-113">1. [los X-AnchorMailbox y los valores de X-PublicFolderInformation](how-to-route-public-folder-hierarchy-requests.md) para el buzón de la jerarquía de carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="1d96e-113">1. [The X-AnchorMailbox and X-PublicFolderInformation values ](how-to-route-public-folder-hierarchy-requests.md) for the public folder hierarchy mailbox.</span></span><br/><br/><span data-ttu-id="1d96e-114">2. el GUID del buzón de carpeta pública que contiene el contenido del buzón de correo, que se envía al servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="1d96e-114">2. The GUID of the public folder mailbox that contains the mailbox content, which is sent to the Autodiscover service.</span></span><br/><br/>  <span data-ttu-id="1d96e-115">El **AutoDiscoverSMTPAddress** en la respuesta de Autodisover se convierte en el valor del encabezado **X-AnchorMailbox** .</span><span class="sxs-lookup"><span data-stu-id="1d96e-115">The **AutoDiscoverSMTPAddress** in the Autodisover response becomes the value of the **X-AnchorMailbox** header.</span></span>  <br/> <span data-ttu-id="1d96e-116">![TODO](media/Ex15_PF_PFContent.png)</span><span class="sxs-lookup"><span data-stu-id="1d96e-116">![TODO](media/Ex15_PF_PFContent.png)</span></span>| <span data-ttu-id="1d96e-117">1. use el ejemplo de código de este artículo, que [implementa la API administrada de EWS](#bk_determineguidewsma).</span><span class="sxs-lookup"><span data-stu-id="1d96e-117">1. Use the code example in this article, which [implements the EWS Managed API](#bk_determineguidewsma).</span></span> <span data-ttu-id="1d96e-118">O bien [usar EWS](#bk_determineguidews) y convertir los resultados para obtener un GUID.</span><span class="sxs-lookup"><span data-stu-id="1d96e-118">Or [use EWS](#bk_determineguidews) and convert your results to obtain a GUID.</span></span><br/><br/><span data-ttu-id="1d96e-119">2. [realizar una solicitud de detección automática](#bk_makeautodrequest) mediante el GUID y el nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="1d96e-119">2. [Make an Autodiscover request](#bk_makeautodrequest) by using the GUID plus the domain name.</span></span><br/><br/><span data-ttu-id="1d96e-120">3. use el valor del elemento **AutoDiscoverSMTPAddress** devuelto en la respuesta de detección automática para [rellenar el valor de los encabezados](#bk_setheadervalues).</span><span class="sxs-lookup"><span data-stu-id="1d96e-120">3. Use the value of the **AutoDiscoverSMTPAddress** element returned in the Autodiscover response to [populate the value of the headers](#bk_setheadervalues).</span></span>  <br/> |
|<span data-ttu-id="1d96e-121">**X-PublicFolderMailbox**</span><span class="sxs-lookup"><span data-stu-id="1d96e-121">**X-PublicFolderMailbox**</span></span> <br/> |<span data-ttu-id="1d96e-122">Se realiza el trabajo, el valor de X-PublicFolderMailbox es el mismo que el valor de X-AnchorMailbox!</span><span class="sxs-lookup"><span data-stu-id="1d96e-122">Your work is done, the X-PublicFolderMailbox value is the same as the X-AnchorMailbox value!</span></span>  <br/> |<span data-ttu-id="1d96e-123">Ya lo tiene.</span><span class="sxs-lookup"><span data-stu-id="1d96e-123">You already have it!</span></span>  <br/> |
   
<span data-ttu-id="1d96e-124">Una vez que haya determinado los valores de encabezado, incluirlos [cuando realiza las solicitudes de contenido de carpetas públicas](#bk_setheadervalues).</span><span class="sxs-lookup"><span data-stu-id="1d96e-124">After you have determined the header values, include them [when you make public folder content requests](#bk_setheadervalues).</span></span>
  
<span data-ttu-id="1d96e-125">Los pasos descritos en este artículo son específicos de las solicitudes de contenido de carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="1d96e-125">The steps in this article are specific to public folder content requests.</span></span> <span data-ttu-id="1d96e-126">Para determinar si la solicitud es una solicitud de contenido o la jerarquía de carpetas públicas, vea [las solicitudes de carpetas públicas de enrutamiento](public-folder-access-with-ews-in-exchange.md#bk_routing).</span><span class="sxs-lookup"><span data-stu-id="1d96e-126">To determine whether your request is a public folder hierarchy or content request, see [Routing public folder requests](public-folder-access-with-ews-in-exchange.md#bk_routing).</span></span>
  
## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-the-ews-managed-api"></a><span data-ttu-id="1d96e-127">Determinar el GUID del buzón de carpetas públicas mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="1d96e-127">Determine the GUID of the public folder mailbox by using the EWS Managed API</span></span>
<span data-ttu-id="1d96e-128"><a name="bk_determineguidewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="1d96e-128"></span></span>

<span data-ttu-id="1d96e-129">Para determinar el GUID del buzón de contenido de carpetas públicas, use el siguiente ejemplo de código, que hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="1d96e-129">To determine the GUID of the public folder content mailbox, use the following code example, which does the following:</span></span> 
  
- <span data-ttu-id="1d96e-130">Usa los encabezados **X-AnchorMailbox** y **X-PublicFolderInformation** recuperado por el [enrutamiento de las solicitudes de jerarquía de carpetas públicas](how-to-route-public-folder-hierarchy-requests.md).</span><span class="sxs-lookup"><span data-stu-id="1d96e-130">Uses the **X-AnchorMailbox** and **X-PublicFolderInformation** headers you retrieved by [routing public folder hierarchy requests](how-to-route-public-folder-hierarchy-requests.md).</span></span>
    
- <span data-ttu-id="1d96e-131">Llama al método de la API administrada de EWS [FindFolders](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) e incluye una solicitud para la propiedad **PR_REPLICA_LIST** (0x66980102)</span><span class="sxs-lookup"><span data-stu-id="1d96e-131">Calls the EWS Managed API [FindFolders](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) method, and includes a request for the **PR_REPLICA_LIST** (0x66980102) property</span></span> 
    
<span data-ttu-id="1d96e-132">El valor **PR_REPLICA_LIST** identifica el GUID del buzón de carpeta pública que tiene el contenido de la carpeta de buzón.</span><span class="sxs-lookup"><span data-stu-id="1d96e-132">The **PR_REPLICA_LIST** value identifies the mailbox GUID of the public folder mailbox that has the content for the folder.</span></span> <span data-ttu-id="1d96e-133">La propiedad **PR_REPLICA_LIST** es una matriz de bytes, pero se convierte como un GUID para este escenario.</span><span class="sxs-lookup"><span data-stu-id="1d96e-133">The **PR_REPLICA_LIST** property is a byte array, but is cast as a GUID for this scenario.</span></span> <span data-ttu-id="1d96e-134">El GUID y el nombre de dominio se concatenen para formar la dirección en la que se llama a la detección automática.</span><span class="sxs-lookup"><span data-stu-id="1d96e-134">The GUID and the domain name are concatenated to form the address on which to call Autodiscover.</span></span> 
  
<span data-ttu-id="1d96e-135">En este ejemplo se da por supuesto que `service` es el objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) para el usuario de buzón de correo, `PFHAnchorHeader` y `PFHMailboxHeader` son los valores de los encabezados **X-AnchorMailbox** y **X-PublicFolderMailbox** y dominio es el nombre de dominio utilizado por el inquilino.</span><span class="sxs-lookup"><span data-stu-id="1d96e-135">This example assumes that  `service` is the [ExchangeService](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox user,  `PFHAnchorHeader` and  `PFHMailboxHeader` are the values of the **X-AnchorMailbox** and **X-PublicFolderMailbox** headers, and domain is the domain name used by the tenant.</span></span> 
  
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

<span data-ttu-id="1d96e-136">Si ha recibido el error "Error en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1d96e-136">If you received the error "The request failed.</span></span> <span data-ttu-id="1d96e-137">Se cerró la conexión subyacente: no se pude establecer una relación de confianza para el canal seguro SSL/TLS ", debe [Agregar una llamada a un método de devolución de llamada de validación](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span><span class="sxs-lookup"><span data-stu-id="1d96e-137">The underlying connection was closed: Could not establish trust relationship for the SSL/TLS secure channel", you'll need to [add a call to a validation callback method](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span></span> <span data-ttu-id="1d96e-138">Un marcador de posición y un comentario para este método se incluye en el ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="1d96e-138">A placeholder and comment for that method is included in the code example.</span></span>
  
<span data-ttu-id="1d96e-139">Si el GUID de buzón es el mismo para todas las carpetas públicas en la raíz de la carpeta pública, en el ejemplo se indica la dirección para usar al [llamar a la detección automática](#bk_makeautodrequest) en la consola de salida y como el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="1d96e-139">If the mailbox GUID is the same for all the public folders under the public folder root, the example indicates the address to use when [calling Autodiscover](#bk_makeautodrequest) in the console output and as the return value.</span></span> <span data-ttu-id="1d96e-140">Si el GUID de buzón no es el mismo para todas las carpetas públicas en la raíz de carpetas públicas, debe [realizar una solicitud de detección automática](#bk_makeautodrequest) en la dirección asociada a la carpeta en su solicitud de contenido.</span><span class="sxs-lookup"><span data-stu-id="1d96e-140">If the mailbox GUID is not the same for all public folders under the public folder root, you need to [Make an Autodiscover request](#bk_makeautodrequest) on the address associated with the folder in your content request.</span></span> 
  
## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-ews"></a><span data-ttu-id="1d96e-141">Determinar el GUID del buzón de carpetas públicas mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="1d96e-141">Determine the GUID of the public folder mailbox by using EWS</span></span>
<span data-ttu-id="1d96e-142"><a name="bk_determineguidews"> </a></span><span class="sxs-lookup"><span data-stu-id="1d96e-142"></span></span>

<span data-ttu-id="1d96e-143">El ejemplo de código siguiente se muestra cómo recuperar el valor de la propiedad **PR_REPLICA_LIST** (0x66980102) mediante el uso de la operación de EWS [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="1d96e-143">The following code example shows how retrieve the value of the **PR_REPLICA_LIST** (0x66980102) property by using the EWS [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="1d96e-144">Para el elemento [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) , el atributo **PropertyTag** se establece en el valor decimal (26264) de la propiedad **PR_REPLICA_LIST** y se establece el atributo **PropertyType** en **binario**.</span><span class="sxs-lookup"><span data-stu-id="1d96e-144">For the [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) element, the **PropertyTag** attribute is set to the decimal value (26264) of the **PR_REPLICA_LIST** property, and the **PropertyType** attribute is set to **Binary**.</span></span>
  
<span data-ttu-id="1d96e-145">También es la solicitud XML que la API administrada de EWS envía cuando se utiliza el método **FindFolders** para [determinar el GUID del buzón de carpetas públicas mediante el uso de la API administrada de EWS](#bk_determineguidewsma).</span><span class="sxs-lookup"><span data-stu-id="1d96e-145">This is also the XML request that the EWS Managed API sends when you use the **FindFolders** method to [determine the GUID of the public folder mailbox by using the EWS Managed API](#bk_determineguidewsma).</span></span>
  
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

<span data-ttu-id="1d96e-146">El servidor responde a la solicitud de **FindFolder** con un mensaje de [FindFolderResponse](http://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) que incluye el valor de la **PR_REPLICA_LIST** propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="1d96e-146">The server responds to the **FindFolder** request with a [FindFolderResponse](http://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) message that includes the value of the **PR_REPLICA_LIST** extended property.</span></span> <span data-ttu-id="1d96e-147">Tenga en cuenta que el valor de la propiedad aparece en la respuesta EWS como el formato de cadena de un valor de base-64 codificada matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="1d96e-147">Note that the value of the property appears on the EWS response as the string format of a base-64 encoded byte array.</span></span> <span data-ttu-id="1d96e-148">Algunos valores de encabezado en la respuesta se acortan para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="1d96e-148">Some header values in the response are shortened for readability.</span></span> 
  
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

<span data-ttu-id="1d96e-149">Para poder usar el valor de la **PR_REPLICA_LIST** devuelto en el XML, MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA ==, para determinar el GUID de buzón, el valor se debe convertir en un GUID en un formato similar a cómo se convierte el valor en el [Ejemplo de código de API administrada de EWS](#bk_determineguidewsma).</span><span class="sxs-lookup"><span data-stu-id="1d96e-149">In order to use the value of the **PR_REPLICA_LIST** returned in the XML, MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA==, to determine the mailbox GUID, the value must be converted into a GUID in a format similar to how the value is converted in the [EWS Managed API code example](#bk_determineguidewsma).</span></span> <span data-ttu-id="1d96e-150">El GUID, a continuación, se concatena con el nombre de dominio para crear una dirección SMTP, que se incluye en la [solicitud de detección automática](#bk_makeautodrequest).</span><span class="sxs-lookup"><span data-stu-id="1d96e-150">The GUID is then concatenated with the domain name to create an SMTP address, which is included in the [Autodiscover request](#bk_makeautodrequest).</span></span>
  
## <a name="make-an-autodiscover-request"></a><span data-ttu-id="1d96e-151">Para realizar una solicitud de detección automática</span><span class="sxs-lookup"><span data-stu-id="1d96e-151">Make an Autodiscover request</span></span>
<span data-ttu-id="1d96e-152"><a name="bk_makeautodrequest"> </a></span><span class="sxs-lookup"><span data-stu-id="1d96e-152"></span></span>

<span data-ttu-id="1d96e-153">Usar la dirección devuelta por la `GetMailboxGuidAddress` método para llamar a la detección automática.</span><span class="sxs-lookup"><span data-stu-id="1d96e-153">Use the address returned by the  `GetMailboxGuidAddress` method to call Autodiscover.</span></span> <span data-ttu-id="1d96e-154">Se recomienda que use la [Exchange 2013: obtener la configuración de usuario con detección automática](http://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) ejemplo de código para llamar al servicio de detección automática debido a que optimiza el proceso de detección automática para usted.</span><span class="sxs-lookup"><span data-stu-id="1d96e-154">We recommend that you use the [Exchange 2013: Get user settings with Autodiscover](http://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) code sample to call the Autodiscover service because it streamlines the Autodiscover process for you.</span></span> <span data-ttu-id="1d96e-155">Este ejemplo de código usa los argumentos de línea de comandos que aparecen en la tabla siguiente para llamar al servicio de detección automática de POX para recuperar el valor de [AutoDiscoverSMTPAddress](http://msdn.microsoft.com/en-us/library/office/dn750991%28v=exchg.150%29.aspx) asociado con el GUID de buzón.</span><span class="sxs-lookup"><span data-stu-id="1d96e-155">This code sample uses the command-line arguments listed in the following table to call the POX Autodiscover service to retrieve the [AutoDiscoverSMTPAddress](http://msdn.microsoft.com/en-us/library/office/dn750991%28v=exchg.150%29.aspx) value associated with the mailbox GUID.</span></span> 
  
|<span data-ttu-id="1d96e-156">**Argumento**</span><span class="sxs-lookup"><span data-stu-id="1d96e-156">**Argument**</span></span>|<span data-ttu-id="1d96e-157">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d96e-157">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1d96e-158">emailAddress</span><span class="sxs-lookup"><span data-stu-id="1d96e-158">emailAddress</span></span>  <br/> |<span data-ttu-id="1d96e-159">La dirección devuelta por la `GetMailboxGuidAddress` método en [Determine el GUID del buzón de carpetas públicas](http://msdn.microsoft.com/library/bk_determineguidewsma.aspx).</span><span class="sxs-lookup"><span data-stu-id="1d96e-159">The address returned by the  `GetMailboxGuidAddress` method in [Determine the GUID of the public folder mailbox](http://msdn.microsoft.com/library/bk_determineguidewsma.aspx).</span></span>  <br/> |
|<span data-ttu-id="1d96e-160">-skipSOAP</span><span class="sxs-lookup"><span data-stu-id="1d96e-160">-skipSOAP</span></span>  <br/> |<span data-ttu-id="1d96e-161">Indica que las solicitudes de detección automática de POX son necesarias.</span><span class="sxs-lookup"><span data-stu-id="1d96e-161">Indicates that POX Autodiscover requests are required.</span></span>  <br/> |
|<span data-ttu-id="1d96e-162">authEmailAddress - auth</span><span class="sxs-lookup"><span data-stu-id="1d96e-162">-auth authEmailAddress</span></span>  <br/> |<span data-ttu-id="1d96e-163">Dirección de correo electrónico del usuario de buzón de correo, que se usa para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="1d96e-163">The mailbox user's email address, which is used for authentication.</span></span> <span data-ttu-id="1d96e-164">Se le pedirá para escribir la contraseña del usuario de buzón de correo al ejecutar el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1d96e-164">You will be prompted to enter the mailbox user's password when you run the sample.</span></span>  <br/> |
   
<span data-ttu-id="1d96e-165">Por ejemplo, los argumentos de línea de comandos deben tener un aspecto similar:</span><span class="sxs-lookup"><span data-stu-id="1d96e-165">For example, the command-line arguments should look like this:</span></span>
  
`1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com -skipSOAP -auth sonyaf@contoso.com`

<span data-ttu-id="1d96e-166">Donde `1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com` es la dirección devuelta por el método **GetMailboxGuidAddress** , y `sonyaf@contoso.com` es el usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="1d96e-166">Where `1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com` is the address returned by the **GetMailboxGuidAddress** method, and `sonyaf@contoso.com` is the mailbox user.</span></span> 
  
<span data-ttu-id="1d96e-167">Al ejecutar el **Exchange 2013: obtener la configuración de usuario con detección automática** ejemplo, la última respuesta de detección automática debe ser correcta e incluir todos los la configuración del usuario asociada con el GUID de buzón.</span><span class="sxs-lookup"><span data-stu-id="1d96e-167">When you run the **Exchange 2013: Get user settings with Autodiscover** sample, the last Autodiscover response should be successful and include all the user settings associated with the mailbox GUID.</span></span> <span data-ttu-id="1d96e-168">Guardar usuario **AutoDiscoverSMTPAddress** establecer localmente, como se usará que en el paso siguiente.</span><span class="sxs-lookup"><span data-stu-id="1d96e-168">Save the **AutoDiscoverSMTPAddress** user setting locally, as you'll use that in the next step.</span></span> 
  
<span data-ttu-id="1d96e-169">Como alternativa, si no desea usar **Exchange 2013: obtener la configuración de usuario con detección automática** ejemplo, puede obtener el usuario **AutoDiscoverSMTPAddress** establecer mediante la [generación de una lista de extremos de detección automática de](how-to-generate-a-list-of-autodiscover-endpoints.md)y, a continuación, enviar lo siguiente Solicitud de detección automática POX a cada dirección URL hasta que recibe una respuesta correcta.</span><span class="sxs-lookup"><span data-stu-id="1d96e-169">Alternatively, if you do not want to use **Exchange 2013: Get user settings with Autodiscover** sample, you can get the **AutoDiscoverSMTPAddress** user setting by [generating a list of Autodiscover endpoints](how-to-generate-a-list-of-autodiscover-endpoints.md), and then sending the following POX Autodiscover request to each URL until you receive a successful response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com</EMailAddress>
    <AcceptableResponseSchema>http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

<span data-ttu-id="1d96e-170">Para obtener más información acerca del proceso de detección automática, vea [detección automática de Exchange](autodiscover-for-exchange.md), [generar una lista de extremos de detección automática](how-to-generate-a-list-of-autodiscover-endpoints.md)y [obtener la configuración de usuario de Exchange mediante el uso de detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).</span><span class="sxs-lookup"><span data-stu-id="1d96e-170">For more information about the Autodiscover process, see [Autodiscover for Exchange](autodiscover-for-exchange.md), [Generate a list of Autodiscover endpoints](how-to-generate-a-list-of-autodiscover-endpoints.md), and [Get user settings from Exchange by using Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).</span></span>
  
## <a name="set-the-values-of-the-x-anchormailbox-and-x-publicfoldermailbox-headers"></a><span data-ttu-id="1d96e-171">Establezca los valores de los encabezados X-AnchorMailbox y X-PublicFolderMailbox</span><span class="sxs-lookup"><span data-stu-id="1d96e-171">Set the values of the X-AnchorMailbox and X-PublicFolderMailbox headers</span></span>
<span data-ttu-id="1d96e-172"><a name="bk_setheadervalues"> </a></span><span class="sxs-lookup"><span data-stu-id="1d96e-172"></span></span>

<span data-ttu-id="1d96e-173">Con el valor de la **AutoDiscoverSMTPAddress** adquirido en [realizar una solicitud de detección automática](#bk_makeautodrequest), establezca los valores de los encabezados **X-AnchorMailbox** y **X-PublicFolderMailbox** en su solicitud de contenido de carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="1d96e-173">Using the value for the **AutoDiscoverSMTPAddress** acquired in [Make an Autodiscover request](#bk_makeautodrequest), set the values of the **X-AnchorMailbox** and **X-PublicFolderMailbox** headers in your public folder content request.</span></span> 
  
<span data-ttu-id="1d96e-174">Por ejemplo, dado un AutoDiscoverSMTPAddress de NewPublicFolder@contoso.com, debe incluir los encabezados siguientes cuando efectúe llamadas a las operaciones o los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="1d96e-174">For example, given an AutoDiscoverSMTPAddress of NewPublicFolder@contoso.com, include the following headers when making calls to the following methods or operations.</span></span>
  
`X-AnchorMailbox: NewPublicFolder@contoso.com`<br/>
`X-PublicFolderMailbox: NewPublicFolder@contoso.com`

<span data-ttu-id="1d96e-175">**Llamadas de carpeta pública que requieren los encabezados X-AncorMailbox y X-PublicFolder**</span><span class="sxs-lookup"><span data-stu-id="1d96e-175">**Public folder calls that require the X-AncorMailbox and X-PublicFolder headers**</span></span>

|<span data-ttu-id="1d96e-176">**Métodos de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="1d96e-176">**EWS Managed API methods**</span></span>|<span data-ttu-id="1d96e-177">**Operaciones de EWS**</span><span class="sxs-lookup"><span data-stu-id="1d96e-177">**EWS operations**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d96e-178">Item.Bind</span><span class="sxs-lookup"><span data-stu-id="1d96e-178">Item.Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="1d96e-179">Item.Update</span><span class="sxs-lookup"><span data-stu-id="1d96e-179">Item.Update</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="1d96e-180">Item.Copy</span><span class="sxs-lookup"><span data-stu-id="1d96e-180">Item.Copy</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="1d96e-181">Item.Move</span><span class="sxs-lookup"><span data-stu-id="1d96e-181">Item.Move</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="1d96e-182">Item.Delete</span><span class="sxs-lookup"><span data-stu-id="1d96e-182">Item.Delete</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="1d96e-183">Folder.Bind</span><span class="sxs-lookup"><span data-stu-id="1d96e-183">Folder.Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="1d96e-184">Folder.FindItems</span><span class="sxs-lookup"><span data-stu-id="1d96e-184">Folder.FindItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="1d96e-185">CreateItem</span><span class="sxs-lookup"><span data-stu-id="1d96e-185">CreateItem</span></span>](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> [<span data-ttu-id="1d96e-186">GetItem</span><span class="sxs-lookup"><span data-stu-id="1d96e-186">GetItem</span></span>](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> [<span data-ttu-id="1d96e-187">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="1d96e-187">UpdateItem</span></span>](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> [<span data-ttu-id="1d96e-188">CopyItem</span><span class="sxs-lookup"><span data-stu-id="1d96e-188">CopyItem</span></span>](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> [<span data-ttu-id="1d96e-189">MoveItem</span><span class="sxs-lookup"><span data-stu-id="1d96e-189">MoveItem</span></span>](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> [<span data-ttu-id="1d96e-190">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="1d96e-190">DeleteItem</span></span>](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> [<span data-ttu-id="1d96e-191">GetFolder</span><span class="sxs-lookup"><span data-stu-id="1d96e-191">GetFolder</span></span>](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> [<span data-ttu-id="1d96e-192">FindItem</span><span class="sxs-lookup"><span data-stu-id="1d96e-192">FindItem</span></span>](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="1d96e-193">Para agregar estos encabezados mediante el uso de la API administrada de EWS, use el método [HttpHeaders.Add](http://msdn.microsoft.com/en-us/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="1d96e-193">To add these headers by using the EWS Managed API, use the [HttpHeaders.Add](http://msdn.microsoft.com/en-us/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) method.</span></span> 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", "NewPublicFolder@contoso.com");
service.HttpHeaders.Add("X-PublicFolderMailbox", "NewPublicFolder@contoso.com");
```

<span data-ttu-id="1d96e-194">El código siguiente muestra una solicitud [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) con el encabezado **X-AnchorMailbox** y **X-PublicFolderMailbox** establecido en los valores recuperados en los ejemplos de este artículo.</span><span class="sxs-lookup"><span data-stu-id="1d96e-194">The following code shows a [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) request with the **X-AnchorMailbox** and **X-PublicFolderMailbox** header set to the values retrieved in the examples in this article.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="1d96e-195">Ver también</span><span class="sxs-lookup"><span data-stu-id="1d96e-195">See also</span></span>

- [<span data-ttu-id="1d96e-196">Carpetas públicas en Exchange obtener acceso con EWS</span><span class="sxs-lookup"><span data-stu-id="1d96e-196">Public folder access with EWS in Exchange</span></span>](public-folder-access-with-ews-in-exchange.md)    
- [<span data-ttu-id="1d96e-197">Detección automática de Exchange</span><span class="sxs-lookup"><span data-stu-id="1d96e-197">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)    
- [<span data-ttu-id="1d96e-198">Generar una lista de extremos de detección automática</span><span class="sxs-lookup"><span data-stu-id="1d96e-198">Generate a list of Autodiscover endpoints</span></span>](how-to-generate-a-list-of-autodiscover-endpoints.md)   
- [<span data-ttu-id="1d96e-199">Obtener la configuración de usuario de Exchange mediante el uso de detección automática</span><span class="sxs-lookup"><span data-stu-id="1d96e-199">Get user settings from Exchange by using Autodiscover</span></span>](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    

