---
title: Enrutar solicitudes de jerarquía de carpetas públicas
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ec35df8e-4d75-4aa1-8b9c-ae1db7e05772
description: Todas las solicitudes de información de carpetas públicas que requieran conocimiento de la jerarquía de carpetas públicas, como mover, actualizar, eliminar o buscar carpetas públicas, se deben enrutar al buzón de jerarquía de carpetas públicas predeterminado para el usuario determinado. Para enrutar las solicitudes a ese buzón de correo, debe establecer los encabezados X-AnchorMailbox y X-PublicFolderMailbox en valores específicos devueltos por el servicio Detección automática.
ms.openlocfilehash: 2773aa3ab29868c69d1fb088deb6c8a96dfb9ecc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455704"
---
# <a name="route-public-folder-hierarchy-requests"></a><span data-ttu-id="7fa32-104">Enrutar solicitudes de jerarquía de carpetas públicas</span><span class="sxs-lookup"><span data-stu-id="7fa32-104">Route public folder hierarchy requests</span></span>

<span data-ttu-id="7fa32-105">Todas las solicitudes de información de carpetas públicas que requieran conocimiento de la jerarquía de carpetas públicas, como mover, actualizar, eliminar o buscar carpetas públicas, se deben enrutar al buzón de jerarquía de carpetas públicas predeterminado para el usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="7fa32-105">All requests for public folder information that require knowledge of the public folder hierarchy, such as moving, updating, deleting, or finding public folders, need to be routed to the default public folder hierarchy mailbox for the given user.</span></span> <span data-ttu-id="7fa32-106">Para enrutar las solicitudes a ese buzón de correo, debe establecer los encabezados **x-AnchorMailbox** y **x-PublicFolderMailbox** en valores específicos devueltos por el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="7fa32-106">To route the requests to that mailbox, you need to set the **X-AnchorMailbox** and **X-PublicFolderMailbox** headers to specific values returned by the Autodiscover service.</span></span> 
  
<span data-ttu-id="7fa32-107">**Información general sobre las carpetas públicas**</span><span class="sxs-lookup"><span data-stu-id="7fa32-107">**Overview of public folders**</span></span>

|<span data-ttu-id="7fa32-108">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7fa32-108">Header</span></span>|<span data-ttu-id="7fa32-109">¿Qué necesito?</span><span class="sxs-lookup"><span data-stu-id="7fa32-109">What do I need?</span></span>|<span data-ttu-id="7fa32-110">¿Cómo puedo obtenerlo?</span><span class="sxs-lookup"><span data-stu-id="7fa32-110">How do I get it?</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7fa32-111">**X-AnchorMailbox**</span><span class="sxs-lookup"><span data-stu-id="7fa32-111">**X-AnchorMailbox**</span></span> <br/> |<span data-ttu-id="7fa32-112">El valor [PublicFolderInformation](https://msdn.microsoft.com/library/dn751006%28v=exchg.150%29.aspx) de una respuesta SOAP de detección automática de [GetUserSettings](https://msdn.microsoft.com/library/office/dd877096%28v=exchg.150%29.aspx) , que se convierte en el valor del encabezado **X-AnchorMailbox** .</span><span class="sxs-lookup"><span data-stu-id="7fa32-112">The [PublicFolderInformation](https://msdn.microsoft.com/library/dn751006%28v=exchg.150%29.aspx) value from a [GetUserSettings](https://msdn.microsoft.com/library/office/dd877096%28v=exchg.150%29.aspx) Autodiscover SOAP response, which becomes the value of the **X-AnchorMailbox** header.</span></span><br/><br/> <span data-ttu-id="7fa32-113">![TODO](media/Ex15_PF_PFH_Anchor.png)</span><span class="sxs-lookup"><span data-stu-id="7fa32-113">![TODO](media/Ex15_PF_PFH_Anchor.png)</span></span>| <span data-ttu-id="7fa32-114">1. enviar una solicitud de **GetUserSetting** con la dirección SMTP del buzón de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="7fa32-114">1. Send a **GetUserSetting** request with the SMTP address for the user's mailbox.</span></span><br/><br/><span data-ttu-id="7fa32-115">2. Almacene en caché el valor del elemento **PublicFolderInformation** que devuelve el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="7fa32-115">2. Cache the value of the **PublicFolderInformation** element that the Autodiscover service returns.</span></span> <span data-ttu-id="7fa32-116">Puede ser un servicio en caché de una llamada de detección automática existente en el código, o una nueva llamada de GetUserSettings de la [API administrada de EWS](#bk_getpfinfoewsma) o una [solicitud SOAP de GetUserSettings](#bk_getpfinfoews).</span><span class="sxs-lookup"><span data-stu-id="7fa32-116">This can be a cached from an existing Autodiscover call in your code, or a new [EWS Managed API GetUserSettings call](#bk_getpfinfoewsma) or a [GetUserSettings SOAP request](#bk_getpfinfoews).</span></span>  <br/><br/><span data-ttu-id="7fa32-117">3. Use el elemento **PublicFolderInformation** para rellenar el valor del encabezado **X-AnchorMailbox** .</span><span class="sxs-lookup"><span data-stu-id="7fa32-117">3. Use the **PublicFolderInformation** element to populate the value of the **X-AnchorMailbox** header.</span></span> <span data-ttu-id="7fa32-118">El valor del elemento **PublicFolderInformation** es una dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="7fa32-118">The value of the **PublicFolderInformation** element is an SMTP address.</span></span>  <br/> |
|<span data-ttu-id="7fa32-119">**X-PublicFolderMailbox**</span><span class="sxs-lookup"><span data-stu-id="7fa32-119">**X-PublicFolderMailbox**</span></span> <br/> |<span data-ttu-id="7fa32-120">El valor del [servidor](https://msdn.microsoft.com/library/bb204084%28v=exchg.150%29.aspx) de una [respuesta de detección automática de POX](https://msdn.microsoft.com/library/bb204082%28v=exchg.150%29.aspx), que se convierte en el valor del encabezado **X-PublicFolderMailbox** .</span><span class="sxs-lookup"><span data-stu-id="7fa32-120">The [Server](https://msdn.microsoft.com/library/bb204084%28v=exchg.150%29.aspx) value from a [POX Autodiscover response](https://msdn.microsoft.com/library/bb204082%28v=exchg.150%29.aspx), which becomes the value of the **X-PublicFolderMailbox** header.</span></span><br/><br/> <span data-ttu-id="7fa32-121">![TODO](media/Ex15_PF_PFH_PFMailbox.png)</span><span class="sxs-lookup"><span data-stu-id="7fa32-121">![TODO](media/Ex15_PF_PFH_PFMailbox.png)</span></span>|<span data-ttu-id="7fa32-122">1. [llamar al servicio Detección automática de POX](#bk_makeautodrequest) usando la dirección de correo electrónico **X-AnchorMailbox** .</span><span class="sxs-lookup"><span data-stu-id="7fa32-122">1. [Call the POX Autodiscover](#bk_makeautodrequest) service using the **X-AnchorMailbox** email address.</span></span>  <br/><br/><span data-ttu-id="7fa32-123">2. Use el elemento **Server** devuelto por el servicio de detección automática para rellenar el valor del encabezado **X-PublicFolderMailbox** .</span><span class="sxs-lookup"><span data-stu-id="7fa32-123">2. Use the **Server** element returned by the Autodiscover service to populate the value of the **X-PublicFolderMailbox** header.</span></span> <span data-ttu-id="7fa32-124">El valor de **X-PublicFolderMailbox** es una dirección SMTP en la que el nombre de usuario es un GUID.</span><span class="sxs-lookup"><span data-stu-id="7fa32-124">The value of the **X-PublicFolderMailbox** is an SMTP address where the username is a GUID.</span></span>  <br/> |

<br/>

<span data-ttu-id="7fa32-125">Una vez que haya determinado los valores de encabezado, incluidos [al realizar solicitudes de jerarquía de carpetas públicas](#bk_setheadervalues).</span><span class="sxs-lookup"><span data-stu-id="7fa32-125">After you have determined the header values, include them [when you make public folder hierarchy requests](#bk_setheadervalues).</span></span>
  
<span data-ttu-id="7fa32-126">Los pasos de este artículo son específicos de las solicitudes de jerarquía de carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="7fa32-126">The steps in this article are specific to public folder hierarchy requests.</span></span> <span data-ttu-id="7fa32-127">Para determinar si su solicitud es una jerarquía de carpetas públicas o una solicitud de contenido, consulte [enrutamiento de solicitudes de carpetas públicas](public-folder-access-with-ews-in-exchange.md#bk_routing).</span><span class="sxs-lookup"><span data-stu-id="7fa32-127">To determine whether your request is a public folder hierarchy or content request, see [Routing public folder requests](public-folder-access-with-ews-in-exchange.md#bk_routing).</span></span>
  
## <a name="determine-the-value-of-the-x-anchormailbox-header-by-using-the-ews-managed-api"></a><span data-ttu-id="7fa32-128">Determinar el valor del encabezado X-AnchorMailbox mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="7fa32-128">Determine the value of the X-AnchorMailbox header by using the EWS Managed API</span></span>
<span data-ttu-id="7fa32-129"><a name="bk_getpfinfoewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="7fa32-129"><a name="bk_getpfinfoewsma"> </a></span></span>

<span data-ttu-id="7fa32-130">Para recuperar el valor de [PublicFolderInformation (POX)](https://msdn.microsoft.com/library/a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6%28Office.15%29.aspx) mediante la API administrada de EWS, puede almacenar en caché el valor del elemento **PublicFolderInformation** que una llamada existente al servicio Detección automática devuelve o realizar una nueva llamada.</span><span class="sxs-lookup"><span data-stu-id="7fa32-130">To retrieve the [PublicFolderInformation (POX)](https://msdn.microsoft.com/library/a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6%28Office.15%29.aspx) value by using the EWS Managed API, you can either cache the value of the **PublicFolderInformation** element that an existing call to the Autodiscover service returns, or make a new call.</span></span> 
  
<span data-ttu-id="7fa32-131">Si realiza una nueva llamada, puede [obtener la configuración de usuario con la configuración de usuario de la API administrada de EWS](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)mediante la[API administrada de EWS](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed) al código y, a continuación, llamar al método de ejemplo **GetUserSettings** con el siguiente código, que recupera solo el valor del elemento **PublicFolderInformation** .</span><span class="sxs-lookup"><span data-stu-id="7fa32-131">If you're making a new call, you can [Get user settings by using the EWS Managed API](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)[Get user settings by using the EWS Managed API](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed) to your code, and then call the **GetUserSettings** sample method by using the following code, which retrieves only the value of the **PublicFolderInformation** element.</span></span> <span data-ttu-id="7fa32-132">Incluya la dirección SMTP del usuario del buzón de correo como un parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="7fa32-132">Include the SMTP address of the mailbox user as an input parameter.</span></span> 
  
```cs
GetUserSettingsResponse userResponse = GetUserSettings(adservice, "sonyaf@contoso.com", 3, UserSettingName.PublicFolderInformation);
Console.WriteLine("X-AnchorMailbox value for public folder hierarchy requests: {0}", userResponse.Settings[UserSettingName.PublicFolderInformation]);
```

<span data-ttu-id="7fa32-133">Después de ejecutar el código, se muestra la siguiente información en la consola:</span><span class="sxs-lookup"><span data-stu-id="7fa32-133">After running the code, the following information is displayed on the console:</span></span>
  
`X-AnchorMailbox for public folder hierarchy requests: SharedPublicFolder@contoso.com`

<span data-ttu-id="7fa32-134">Ahora que tiene el valor **PublicFolderInformation** , debe incluirlo como valor para el encabezado X-AnchorMailbox en todas las solicitudes de jerarquía de carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="7fa32-134">Now that you have the **PublicFolderInformation** value, include it as the value for the X-AnchorMailbox header in all public folder hierarchy requests.</span></span> 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com`

## <a name="determine-the-value-of-the-x-anchormailbox-header-using-soap"></a><span data-ttu-id="7fa32-135">Determinar el valor del encabezado X-AnchorMailbox mediante SOAP</span><span class="sxs-lookup"><span data-stu-id="7fa32-135">Determine the value of the X-AnchorMailbox header using SOAP</span></span>
<span data-ttu-id="7fa32-136"><a name="bk_getpfinfoews"> </a></span><span class="sxs-lookup"><span data-stu-id="7fa32-136"><a name="bk_getpfinfoews"> </a></span></span>

<span data-ttu-id="7fa32-137">En el ejemplo de código siguiente se muestra cómo recuperar el valor de **PublicFolderInformation** mediante la operación SOAP de [GetUserSettings](https://msdn.microsoft.com/library/dd877096%28v=exchg.150%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7fa32-137">The following code example shows how to retrieve the **PublicFolderInformation** value by using the [GetUserSettings](https://msdn.microsoft.com/library/dd877096%28v=exchg.150%29.aspx) SOAP operation.</span></span> <span data-ttu-id="7fa32-138">El usuario del buzón de correo se especifica en el elemento [Mailbox](https://msdn.microsoft.com/library/dd877076%28v=exchg.150%29.aspx) y el elemento [RequestedSettings](https://msdn.microsoft.com/library/office/dd877107%28v=exchg.150%29.aspx) limita la respuesta al valor [PublicFolderInformation](https://msdn.microsoft.com/library/dn751006%28v=exchg.150%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7fa32-138">The mailbox user is specified in the [Mailbox](https://msdn.microsoft.com/library/dd877076%28v=exchg.150%29.aspx) element, and the [RequestedSettings](https://msdn.microsoft.com/library/office/dd877107%28v=exchg.150%29.aspx) element limits the response to the [PublicFolderInformation](https://msdn.microsoft.com/library/dn751006%28v=exchg.150%29.aspx) value.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover"
               xmlns:wsa="http://www.w3.org/2005/08/addressing"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2007_SP1</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://pod51042.outlook.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover">
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

<span data-ttu-id="7fa32-139">La respuesta incluye el valor **PublicFolderInformation** .</span><span class="sxs-lookup"><span data-stu-id="7fa32-139">The response includes the **PublicFolderInformation** value.</span></span> 
  
```XML
<UserSetting i:type="StringSetting">
    <Name>PublicFolderInformation</Name>
    <Value>SharedPublicFolder@contoso.com</Value>
</UserSetting>
```

<span data-ttu-id="7fa32-140">Ahora que tiene el valor **PublicFolderInformation** , debe incluirlo como valor para el encabezado X-AnchorMailbox en todas las solicitudes de jerarquía de carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="7fa32-140">Now that you have the **PublicFolderInformation** value, include it as the value for the X-AnchorMailbox header in all public folder hierarchy requests.</span></span> 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com`

## <a name="make-an-autodiscover-request-to-determine-the-x-publicfolderinformation-value"></a><span data-ttu-id="7fa32-141">Realizar una solicitud de detección automática para determinar el valor X-PublicFolderInformation</span><span class="sxs-lookup"><span data-stu-id="7fa32-141">Make an Autodiscover request to determine the X-PublicFolderInformation value</span></span>
<span data-ttu-id="7fa32-142"><a name="bk_makeautodrequest"> </a></span><span class="sxs-lookup"><span data-stu-id="7fa32-142"><a name="bk_makeautodrequest"> </a></span></span>

<span data-ttu-id="7fa32-143">Realice una solicitud de detección automática usando la dirección SMTP de **PublicFolderInformation** , que ahora se usa como el valor **X-AnchorMailbox** .</span><span class="sxs-lookup"><span data-stu-id="7fa32-143">Make an Autodiscover request by using the **PublicFolderInformation** SMTP address, which is now being used as the **X-AnchorMailbox** value.</span></span> <span data-ttu-id="7fa32-144">Use el ejemplo de código [Exchange 2013: obtener configuración de usuario con detección automática](https://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) para llamar al servicio Detección automática porque optimiza el proceso de detección automática por usted.</span><span class="sxs-lookup"><span data-stu-id="7fa32-144">Use the [Exchange 2013: Get user settings with Autodiscover](https://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) code sample to call the Autodiscover service because it streamlines the Autodiscover process for you.</span></span> <span data-ttu-id="7fa32-145">Este ejemplo de código usa los argumentos de la línea de comandos enumerados en la siguiente tabla para llamar al servicio Detección automática de POX en la dirección SMTP **PublicFolderInformation** .</span><span class="sxs-lookup"><span data-stu-id="7fa32-145">This code sample uses the command line arguments listed in the following table to call the POX Autodiscover service on the **PublicFolderInformation** SMTP address.</span></span> 
  
|<span data-ttu-id="7fa32-146">**Argumento de línea de comandos**</span><span class="sxs-lookup"><span data-stu-id="7fa32-146">**Command-line argument**</span></span>|<span data-ttu-id="7fa32-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7fa32-147">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7fa32-148">emailAddress</span><span class="sxs-lookup"><span data-stu-id="7fa32-148">emailAddress</span></span>  <br/> |<span data-ttu-id="7fa32-149">La dirección SMTP de **PublicFolderInformation** .</span><span class="sxs-lookup"><span data-stu-id="7fa32-149">The **PublicFolderInformation** SMTP address.</span></span>  <br/> |
|<span data-ttu-id="7fa32-150">-skipSOAP</span><span class="sxs-lookup"><span data-stu-id="7fa32-150">-skipSOAP</span></span>  <br/> | <span data-ttu-id="7fa32-151">Use las solicitudes de detección automática de POX para este escenario.</span><span class="sxs-lookup"><span data-stu-id="7fa32-151">Use POX Autodiscover requests for this scenario.</span></span>  <br/> |
|<span data-ttu-id="7fa32-152">-auth authEmailAddress</span><span class="sxs-lookup"><span data-stu-id="7fa32-152">-auth authEmailAddress</span></span>  <br/> |<span data-ttu-id="7fa32-153">La dirección de correo electrónico del usuario del buzón, que se usa para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="7fa32-153">The mailbox user's email address, which is used for authentication.</span></span> <span data-ttu-id="7fa32-154">Al ejecutar el ejemplo, se le pedirá que escriba la contraseña del usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="7fa32-154">You will be prompted to enter the mailbox user's password when you run the sample.</span></span>  <br/> |
   
<span data-ttu-id="7fa32-155">Por ejemplo, cuando SharedPublicFolder@contoso.com es la dirección SMTP del elemento **PublicFolderInformation** y sonyaf@contoso.com es el usuario del buzón de correo, los argumentos de la línea de comandos deben tener el siguiente aspecto.</span><span class="sxs-lookup"><span data-stu-id="7fa32-155">For example, when SharedPublicFolder@contoso.com is the SMTP address of the **PublicFolderInformation** element, and sonyaf@contoso.com is the mailbox user, the command-line arguments should look like this.</span></span> 
  
`SharedPublicFolder@contoso.com -skipSOAP -auth sonyaf@contoso.com`

<span data-ttu-id="7fa32-156">Al ejecutar el ejemplo **Exchange 2013: obtener configuración de usuario con detección automática** , la última respuesta de detección automática debería ser correcta e incluir todas las configuraciones de usuario asociadas con el GUID de buzón.</span><span class="sxs-lookup"><span data-stu-id="7fa32-156">When you run the **Exchange 2013: Get user settings with Autodiscover** sample, the last Autodiscover response should be successful and include all the user settings associated with the mailbox GUID.</span></span> <span data-ttu-id="7fa32-157">El valor de [servidor](https://msdn.microsoft.com/library/bb204084%28v=exchg.150%29.aspx) asociado con el elemento de[tipo](https://msdn.microsoft.com/library/office/bb204223%28v=exchg.150%29.aspx) de [Protocolo](https://msdn.microsoft.com/library/bb204278%28v=exchg.150%29.aspx)EXCH es el valor de encabezado **X-PublicFolderInformation** .</span><span class="sxs-lookup"><span data-stu-id="7fa32-157">The [Server](https://msdn.microsoft.com/library/bb204084%28v=exchg.150%29.aspx) value associated with the EXCH [Protocol](https://msdn.microsoft.com/library/bb204278%28v=exchg.150%29.aspx)[Type](https://msdn.microsoft.com/library/office/bb204223%28v=exchg.150%29.aspx) element is the **X-PublicFolderInformation** header value.</span></span> 
  
```XML
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    …
    <Account>
      <AccountType>email</AccountType>
      <Action>settings</Action>
      <Protocol>
        <Type>EXCH</Type>
        <Server>1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com</Server>

```

<span data-ttu-id="7fa32-158">Como alternativa, si no desea usar el ejemplo **Exchange 2013: obtener configuración de usuario con detección automática** , puede obtener el valor del **servidor** [generando una lista de extremos de detección automática](how-to-generate-a-list-of-autodiscover-endpoints.md)y, a continuación, enviando la siguiente solicitud de detección automática de POX a cada dirección URL hasta que reciba una respuesta correcta.</span><span class="sxs-lookup"><span data-stu-id="7fa32-158">Alternatively, if you do not want to use the **Exchange 2013: Get user settings with Autodiscover** sample, you can get the **Server** value by [generating a list of Autodiscover endpoints](how-to-generate-a-list-of-autodiscover-endpoints.md), and then sending the following POX Autodiscover request to each URL until you receive a successful response.</span></span> <span data-ttu-id="7fa32-159">SharedPublicFolder@contoso.com es el valor del encabezado **X-PublicFolderMailbox** .</span><span class="sxs-lookup"><span data-stu-id="7fa32-159">SharedPublicFolder@contoso.com is the value of the **X-PublicFolderMailbox** header.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>SharedPublicFolder@contoso.com</EMailAddress>
    <AcceptableResponseSchema>https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

<span data-ttu-id="7fa32-160">Para obtener más información sobre el proceso de detección automática, consulte [detección automática para Exchange](autodiscover-for-exchange.md), [generar una lista de extremos de detección automática](how-to-generate-a-list-of-autodiscover-endpoints.md)y [obtener la configuración de usuario de Exchange mediante detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).</span><span class="sxs-lookup"><span data-stu-id="7fa32-160">For more information about the Autodiscover process, see [Autodiscover for Exchange](autodiscover-for-exchange.md), [Generate a list of Autodiscover endpoints](how-to-generate-a-list-of-autodiscover-endpoints.md), and [Get user settings from Exchange by using Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).</span></span>
  
## <a name="set-the-values-of-the-x-anchormailbox-and-x-publicfoldermailbox-headers"></a><span data-ttu-id="7fa32-161">Establecer los valores de los encabezados X-AnchorMailbox y X-PublicFolderMailbox</span><span class="sxs-lookup"><span data-stu-id="7fa32-161">Set the values of the X-AnchorMailbox and X-PublicFolderMailbox headers</span></span>
<span data-ttu-id="7fa32-162"><a name="bk_setheadervalues"> </a></span><span class="sxs-lookup"><span data-stu-id="7fa32-162"><a name="bk_setheadervalues"> </a></span></span>

<span data-ttu-id="7fa32-163">Con el valor de la dirección SMTP de **PublicFolderInformation** adquirida en [determinar el valor del encabezado x-ANCHORMAILBOX mediante la API administrada de EWS](#bk_getpfinfoewsma) o [determinar el valor del encabezado x-AnchorMailbox mediante SOAP](#bk_getpfinfoews) y el valor **Server** adquirido en [realizar una solicitud de detección automática para determinar el valor x-PublicFolderInformation](#bk_makeautodrequest), establezca los valores de los encabezados **x-AnchorMailbox** y **x-PublicFolderMailbox** en la solicitud de contenido de carpeta pública</span><span class="sxs-lookup"><span data-stu-id="7fa32-163">Using the value of the **PublicFolderInformation** SMTP address acquired in [Determine the value of the X-AnchorMailbox header by using the EWS Managed API](#bk_getpfinfoewsma) or [Determine the value of the X-AnchorMailbox header using SOAP](#bk_getpfinfoews) and the **Server** value acquired in [Make an Autodiscover request to determine the X-PublicFolderInformation value](#bk_makeautodrequest), set the values of **X-AnchorMailbox** and **X-PublicFolderMailbox** headers in your public folder content request.</span></span> 
  
<span data-ttu-id="7fa32-164">Por ejemplo, dada una dirección SMTP de **PublicFolderInformation** de SharedPublicFolder@contoso.com y un valor de **servidor** de 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com, se incluyen los siguientes encabezados cuando se realizan llamadas a los siguientes métodos u operaciones.</span><span class="sxs-lookup"><span data-stu-id="7fa32-164">For example, given a **PublicFolderInformation** SMTP address of SharedPublicFolder@contoso.com and a **Server** value of 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com, include the following headers when making calls to the following methods or operations.</span></span> 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com` <br/>
`X-PublicFolderMailbox: 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com`

<span data-ttu-id="7fa32-165">**Llamadas a carpetas públicas que requieren los encabezados X-AnchorMailbox y X-PublicFolder**</span><span class="sxs-lookup"><span data-stu-id="7fa32-165">**Public folder calls that require the X-AnchorMailbox and X-PublicFolder headers**</span></span>

|<span data-ttu-id="7fa32-166">**Métodos de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="7fa32-166">**EWS Managed API methods**</span></span>|<span data-ttu-id="7fa32-167">**Operaciones de EWS**</span><span class="sxs-lookup"><span data-stu-id="7fa32-167">**EWS operations**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7fa32-168">Folder. FindFolders</span><span class="sxs-lookup"><span data-stu-id="7fa32-168">Folder.FindFolders</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="7fa32-169">Folder. Delete</span><span class="sxs-lookup"><span data-stu-id="7fa32-169">Folder.Delete</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="7fa32-170">Folder. Update</span><span class="sxs-lookup"><span data-stu-id="7fa32-170">Folder.Update</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="7fa32-171">Folder. Move</span><span class="sxs-lookup"><span data-stu-id="7fa32-171">Folder.Move</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.move%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="7fa32-172">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="7fa32-172">CreateFolder</span></span>](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> [<span data-ttu-id="7fa32-173">FindFolder</span><span class="sxs-lookup"><span data-stu-id="7fa32-173">FindFolder</span></span>](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> [<span data-ttu-id="7fa32-174">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="7fa32-174">DeleteFolder</span></span>](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> [<span data-ttu-id="7fa32-175">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="7fa32-175">UpdateFolder</span></span>](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> [<span data-ttu-id="7fa32-176">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="7fa32-176">MoveFolder</span></span>](https://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="7fa32-177">Para agregar estos encabezados mediante la API administrada de EWS, use el método [HttpHeaders. Add](https://msdn.microsoft.com/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7fa32-177">To add these headers by using the EWS Managed API, use the [HttpHeaders.Add](https://msdn.microsoft.com/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) method.</span></span> 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", "SharedPublicFolder@contoso.com");service.HttpHeaders.Add("X-PublicFolderMailbox", "1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com");
```

<span data-ttu-id="7fa32-178">Por ejemplo, el siguiente código muestra una solicitud [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) con el encabezado **x-AnchorMailbox** y **x-PublicFolderMailbox** establecido en los valores recuperados en los ejemplos de este artículo.</span><span class="sxs-lookup"><span data-stu-id="7fa32-178">For example, the following code shows a [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) request with the **X-AnchorMailbox** and **X-PublicFolderMailbox** header set to the values retrieved in the examples in this article.</span></span> 
  
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
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

## <a name="see-also"></a><span data-ttu-id="7fa32-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fa32-179">See also</span></span>

- [<span data-ttu-id="7fa32-180">Acceso a carpetas públicas con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="7fa32-180">Public folder access with EWS in Exchange</span></span>](public-folder-access-with-ews-in-exchange.md)    
- [<span data-ttu-id="7fa32-181">Enrutar solicitudes de contenido de carpetas públicas</span><span class="sxs-lookup"><span data-stu-id="7fa32-181">Route public folder content requests</span></span>](how-to-route-public-folder-content-requests.md)    
- [<span data-ttu-id="7fa32-182">Obtener la configuración de usuario mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="7fa32-182">Get user settings by using the EWS Managed API</span></span>](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)
    

