---
title: Empezar a trabajar con aplicaciones de cliente de la API administrada de EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: c2267733-6f4f-49e5-9614-1e4a24c3af1a
description: Desarrolle una sencilla aplicación cliente de correo electrónico Hola a todos para Exchange mediante la API administrada EWS.
ms.openlocfilehash: dafc8cbbf172ad725ab83c93553464ba96ef33b8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763026"
---
# <a name="get-started-with-ews-managed-api-client-applications"></a><span data-ttu-id="a6d61-103">Empezar a trabajar con aplicaciones de cliente de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="a6d61-103">Get started with EWS Managed API client applications</span></span>

<span data-ttu-id="a6d61-104">Este documento puede incluir contenido relacionado con funciones o productos preliminares que pueden cambiar mucho antes del lanzamiento comercial final. Este documento se proporciona "tal cual" solamente con fines informativos y Microsoft no realiza ninguna garantía, explícita ni implícita, en el documento. Desarrolle una sencilla aplicación cliente de correo electrónico Hola a todos para Exchange mediante la API administrada EWS.</span><span class="sxs-lookup"><span data-stu-id="a6d61-104">Develop a simple Hello World email client application for Exchange by using the EWS Managed API.</span></span> 
  
<span data-ttu-id="a6d61-p101">La [API administrada EWS](http://aka.ms/ews-managed-api-readme) proporciona un modelo de objetos intuitivo y fácil de usar para enviar y recibir mensajes de servicios web desde aplicaciones cliente, aplicaciones de portal y aplicaciones de servicio. Puede tener acceso a casi toda la información almacenada en un buzón de correo de Exchange Online, Exchange Online como parte de Office 365 o Exchange Server mediante la API administrada EWS. Puede usar la información de este artículo como ayuda para desarrollar su primera aplicación cliente de la API administrada EWS.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p101">The [EWS Managed API](http://aka.ms/ews-managed-api-readme) provides an intuitive, easy-to-use object model for sending and receiving web service messages from client applications, portal applications, and service applications. You can access almost all the information stored in an Exchange Online, Exchange Online as part of Office 365, or an Exchange server mailbox by using the EWS Managed API. You can use the information in this article to help you develop your first EWS Managed API client application.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a6d61-p102"> La API administrada EWS ya está disponible como un proyecto de código abierto en [GitHub](https://github.com/officedev/ews-managed-api). Puede usar la biblioteca de código abierto para: >  Contribuir con correcciones de errores y mejoras a la API. >  Obtener correcciones y mejoras antes de que estén disponibles en una versión oficial. >  Tener acceso a una implementación más completa y actualizada de la API, para usarla como referencia o para crear nuevas bibliotecas en nuevas plataformas. >  Le agradecemos las [aportaciones](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) que realice a través de GitHub.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p102">The EWS Managed API is now available as an open source project on [GitHub](https://github.com/officedev/ews-managed-api). You can use the open source library to: >  Contribute bug fixes and enhancements to the API. >  Get fixes and enhancements before they are available in an official release. >  Access the most comprehensive and up-to-date implementation of the API, to use as a reference or to create new libraries on new platforms. >  We welcome your [contributions](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) via GitHub.</span></span> 
  
## <a name="youll-need-an-exchange-server"></a><span data-ttu-id="a6d61-113">Necesitará un servidor de Exchange</span><span class="sxs-lookup"><span data-stu-id="a6d61-113">You'll need an Exchange server</span></span>
<span data-ttu-id="a6d61-114"><a name="NeedExchange"> </a></span><span class="sxs-lookup"><span data-stu-id="a6d61-114"></span></span>

<span data-ttu-id="a6d61-p103">Si ya tiene una cuenta de buzón de Exchange, puede omitir esta sección. En caso contrario, dispone de las opciones siguientes para configurar un buzón de Exchange para su primera aplicación cliente EWS:</span><span class="sxs-lookup"><span data-stu-id="a6d61-p103">If you already have an Exchange mailbox account, you can skip this section. Otherwise, you have the following options for setting up an Exchange mailbox for your first EWS client application:</span></span>
  
- <span data-ttu-id="a6d61-p104">Obtener un [sitio para desarrolladores de Office 365](http://msdn.microsoft.com/es-es/library/office/fp179924.aspx) (recomendado). Esta es la forma más rápida de configurar un buzón de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p104">Get an [Office 365 Developer Site](http://msdn.microsoft.com/es-es/library/office/fp179924.aspx) (recommended). This is the quickest way for you to set up an Exchange mailbox.</span></span> 
    
- <span data-ttu-id="a6d61-119">Descargar [Exchange Server](http://office.microsoft.com/en-us/exchange/microsoft-exchange-try-or-buy-exchange-we-can-help-you-decide-FX103746846.aspx?WT%2Eintid1=ODC%5FENUS%5FFX103472230%5FXT103965589).</span><span class="sxs-lookup"><span data-stu-id="a6d61-119">Download [Exchange Server](http://office.microsoft.com/en-us/exchange/microsoft-exchange-try-or-buy-exchange-we-can-help-you-decide-FX103746846.aspx?WT%2Eintid1=ODC%5FENUS%5FFX103472230%5FXT103965589).</span></span>
    
<span data-ttu-id="a6d61-p105">Una vez que haya comprobado que puede enviar y recibir correo electrónico desde Exchange, estará listo para configurar el entorno de desarrollo. Puede usar [Outlook Web App](http://technet.microsoft.com/es-es/library/jj657718%28v=exchg.150%29.aspx) del cliente web de Exchange para comprobar que puede enviar correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p105">After you have verified that you can send and receive email from Exchange, you are ready to set up your development environment. You can use the Exchange web client [Outlook Web App](http://technet.microsoft.com/es-es/library/jj657718%28v=exchg.150%29.aspx) to verify that you can send email.</span></span> 
  
## <a name="set-up-your-development-environment"></a><span data-ttu-id="a6d61-122">Configurar el entorno de desarrollo</span><span class="sxs-lookup"><span data-stu-id="a6d61-122">Set up your development environment</span></span>
<span data-ttu-id="a6d61-123"><a name="Setup"> </a></span><span class="sxs-lookup"><span data-stu-id="a6d61-123"></span></span>

<span data-ttu-id="a6d61-124">Asegúrese de que tiene acceso a los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="a6d61-124">Make sure that you have access to the following:</span></span>
  
- <span data-ttu-id="a6d61-p106">Cualquier versión de [Visual Studio](http://www.visualstudio.com/en-us/downloads/download-visual-studio-vs.aspx) que sea compatible con .NET Framework 4. Aunque técnicamente no se necesita Visual Studio porque se puede usar cualquier compilador de C#, recomendamos que lo use.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p106">Any version of [Visual Studio](http://www.visualstudio.com/en-us/downloads/download-visual-studio-vs.aspx) that supports the .NET Framework 4. Although technically, you don't need Visual Studio because you can use any C# compiler, we recommend that you use it.</span></span> 
    
- <span data-ttu-id="a6d61-p107">La [API administrada EWS](http://aka.ms/ews-managed-api-readme). Puede usar la versión de 64 o 32 bits, en función de su sistema. Use la ubicación de instalación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p107">The [EWS Managed API](http://aka.ms/ews-managed-api-readme). You can use either the 64-bit or 32-bit version, depending on your system. Use the default installation location.</span></span> 
    
## <a name="create-your-first-ews-managed-api-application"></a><span data-ttu-id="a6d61-130">Crear la primera aplicación de API administrada EWS</span><span class="sxs-lookup"><span data-stu-id="a6d61-130">Create your first EWS Managed API application</span></span>
<span data-ttu-id="a6d61-131"><a name="Create"> </a></span><span class="sxs-lookup"><span data-stu-id="a6d61-131"></span></span>

<span data-ttu-id="a6d61-p108">En estos pasos se da por supuesto que ha configurado un sitio para desarrolladores de Office 365. Si ha descargado e instalado Exchange, deberá [instalar un certificado válido](http://technet.microsoft.com/es-es/library/bb310769%28v=exchg.141%29.aspx) en el servidor de Exchange o [implementar una devolución de llamada de validación de certificado](how-to-validate-a-server-certificate-for-the-ews-managed-api.md) para un certificado autofirmado proporcionado de forma predeterminada. Tenga en cuenta también que estos pasos pueden variar ligeramente según la versión de Visual Studio que use.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p108">These steps assume that you set up an Office 365 Developer Site. If you downloaded and installed Exchange, you will need to [install a valid certificate](http://technet.microsoft.com/es-es/library/bb310769%28v=exchg.141%29.aspx) on your Exchange server or [implement a certificate validation](how-to-validate-a-server-certificate-for-the-ews-managed-api.md) callback for a self-signed certificate that is provided by default. Also note that these steps might vary slightly depending on the version of Visual Studio that you are using.</span></span> 
  
### <a name="step-1-create-a-project-in-visual-studio"></a><span data-ttu-id="a6d61-135">Paso 1: crear un proyecto en Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a6d61-135">Step 1: Create a project in Visual Studio</span></span>

1. <span data-ttu-id="a6d61-p109">En Visual Studio, en el menú **Archivo**, seleccione **Nuevo** y después elija **Proyecto**. Se abre el cuadro de diálogo **Nuevo proyecto**.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p109">In Visual Studio, on the **File** menu, choose **New**, and then choose **Project**. The **New Project** dialog box opens.</span></span> 
    
2. <span data-ttu-id="a6d61-p110">Cree una **aplicación de consola de C#**. En el panel **Plantillas**, elija **Visual C#** y luego **Aplicación de consola**.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p110">Create a **C# Console Application**. From the **Templates** pane, choose **Visual C#**, and then choose **Console Application**.</span></span> 
    
3. <span data-ttu-id="a6d61-140">Indique HelloWorld como nombre del proyecto y después elija **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="a6d61-140">Name the project HelloWorld, and then choose **OK**.</span></span>
    
<span data-ttu-id="a6d61-141">Visual Studio crea el proyecto y abre la ventana de documento de código Program.cs.</span><span class="sxs-lookup"><span data-stu-id="a6d61-141">Visual Studio creates the project and opens the Program.cs code document window.</span></span>

### <a name="step-2-add-a-reference-to-the-ews-managed-api"></a><span data-ttu-id="a6d61-142">Paso 2: agregar una referencia a la API administrada EWS</span><span class="sxs-lookup"><span data-stu-id="a6d61-142">Step 2: Add a reference to the EWS Managed API</span></span>

1. <span data-ttu-id="a6d61-p111">Si la ventana **Explorador de soluciones** ya está abierta, omita este paso y vaya al paso 2. Para abrir la ventana **Explorador de soluciones**, en el menú **Vista**, elija **Explorador de soluciones**.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p111">If the **Solution Explorer** window is already open, skip this step and proceed to step 2. To open the **Solution Explorer** window, on the **View** menu, choose **Solution Explorer**.</span></span> 
    
2. <span data-ttu-id="a6d61-p112">En el **Explorador de soluciones** y en el proyecto **HelloWorld**, abra el menú contextual (botón derecho) de **Referencias** y elija **Agregar referencia** en el menú contextual. Se abrirá un cuadro de diálogo para administrar las referencias del proyecto.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p112">In the **Solution Explorer** and the **HelloWorld** project, open the shortcut menu (right-click) for **References** and choose **Add Reference** from the context menu. A dialog box for managing project references will open.</span></span> 
    
3. <span data-ttu-id="a6d61-p113">Elija la opción **Examinar**. Vaya a la ubicación donde instaló el archivo DLL de la API administrada EWS. La ruta de acceso predeterminada que establece el programa de instalación es la siguiente: C:\Archivos de programa\Microsoft\Exchange\Web Services\<versión>\. La ruta de acceso puede variar en función de si descarga la versión de 32 o de 64 bits del archivo Microsoft.Exchange.WebServices.dll. Elija **Microsoft.Exchange.WebServices.dll** y seleccione **Aceptar** o **Agregar**. Esto agrega la referencia de la API administrada EWS a su proyecto.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p113">Choose the **Browse** option. Browse to the location where you installed the EWS Managed API DLL. The default path set by the installer is the following: C:\Program Files\Microsoft\Exchange\Web Services\<version>\. The path can vary based on whether you download the 32 or 64 bit version of the Microsoft.Exchange.WebServices.dll. Choose **Microsoft.Exchange.WebServices.dll** and select **OK** or **Add**. This adds the EWS Managed API reference to your project.</span></span> 
    
4. <span data-ttu-id="a6d61-p114">Si usa la API administrada 2.0 EWS, cambie el destino del proyecto HelloWorld a .NET Framework 4. Otras versiones de la API administrada EWS podrían usar una versión de destino diferente de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p114">If you are using EWS Managed API 2.0, change the HelloWorld project to target the .NET Framework 4. Other versions of the EWS Managed API might use a different target version of the .NET Framework.</span></span>
    
5. <span data-ttu-id="a6d61-p115">Confirme que usa la versión de destino correcta de .NET Framework. Abra el menú contextual (botón derecho) del proyecto **HelloWorld** en el **Explorador de soluciones** y elija **Propiedades**. Compruebe que está seleccionado **.NET Framework 4** en el cuadro desplegable **Versión de .NET Framework de destino**.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p115">Confirm that you are using the correct target version of the .NET Framework. Open the shortcut menu (right-click) for your **HelloWorld** project in the **Solution Explorer**, and choose **Properties**. Verify that the **.NET Framework 4** is selected in the **Target framework** drop-down box.</span></span> 
    
<span data-ttu-id="a6d61-158">Ahora que ha configurado el proyecto y que ha creado una referencia a la API administrada EWS, está listo para crear su primera aplicación.</span><span class="sxs-lookup"><span data-stu-id="a6d61-158">Now that you have your project set up and you created a reference to the EWS Managed API, you are ready to create your first application.</span></span> <span data-ttu-id="a6d61-159">Para simplificar las cosas, agregue el código al archivo Program.cs.</span><span class="sxs-lookup"><span data-stu-id="a6d61-159">To keep things simple, add your code to the Program.cs file.</span></span> <span data-ttu-id="a6d61-160">Leer la [referencia del ensamblado de la API administrada de EWS](how-to-reference-the-ews-managed-api-assembly.md) para obtener más información acerca de cómo hacer referencia a la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="a6d61-160">Read [Reference the EWS Managed API assembly](how-to-reference-the-ews-managed-api-assembly.md) for more information about referencing the EWS Managed API.</span></span> <span data-ttu-id="a6d61-161">En el paso siguiente, desarrollará el código básico para escribir la mayoría de las aplicaciones cliente de la API administrada EWS.</span><span class="sxs-lookup"><span data-stu-id="a6d61-161">In the next step, you will develop the basic code to write most EWS Managed API client applications.</span></span> 
### <a name="step-3-set-up-url-redirection-validation-for-autodiscover"></a><span data-ttu-id="a6d61-162">Paso 3: configurar la validación del redireccionamiento de la dirección URL para la Detección automática</span><span class="sxs-lookup"><span data-stu-id="a6d61-162">Step 3: Set up URL redirection validation for Autodiscover</span></span>

- <span data-ttu-id="a6d61-p117">Agregue el siguiente método de devolución de llamada para la validación del redireccionamiento después del método **Main(string[] args)**. Esto valida si las direcciones URL redirigidas que devuelve la [Detección automática](autodiscover-for-exchange.md) representan un extremo HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p117">Add the following redirection validation callback method after the **Main(string[] args)** method. This validates whether redirected URLs returned by [Autodiscover](autodiscover-for-exchange.md) represent an HTTPS endpoint.</span></span> 
    
  ```cs
  private static bool RedirectionUrlValidationCallback(string redirectionUrl)
  {
     // The default for the validation callback is to reject the URL.
     bool result = false;
     Uri redirectionUri = new Uri(redirectionUrl);
     // Validate the contents of the redirection URL. In this simple validation
     // callback, the redirection URL is considered valid if it is using HTTPS
     // to encrypt the authentication credentials. 
     if (redirectionUri.Scheme == "https")
     {
        result = true;
     }
     return result;
  }
  ```

<span data-ttu-id="a6d61-p118">Esta devolución de llamada de validación se pasará al objeto **ExchangeService** en el paso 4. Esto es necesario para que la aplicación confíe y siga los redireccionamientos de la Detección automática, ya que los resultados del redireccionamiento de la Detección automática proporcionan el extremo EWS para nuestra aplicación.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p118">This validation callback will be passed to the **ExchangeService** object in step 4. You need this so that your application will trust and follow Autodiscover redirects - the results of the Autodiscover redirect provides the EWS endpoint for our application.</span></span> 

### <a name="step-4-prepare-the-exchangeservice-object"></a><span data-ttu-id="a6d61-167">Paso 4: preparar el objeto ExchangeService</span><span class="sxs-lookup"><span data-stu-id="a6d61-167">Step 4: Prepare the ExchangeService object</span></span>

1. <span data-ttu-id="a6d61-p119">Agregue una referencia de directiva **using** a la API administrada EWS. Agregue el código siguiente después de la última directiva **using** en la parte superior de Program.cs.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p119">Add a **using** directive reference to the EWS Managed API. Add the following code after the last **using** directive at the top of Program.cs.</span></span> 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

2. <span data-ttu-id="a6d61-p120">En el método **Main**, cree una instancia del objeto [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) con la versión del servicio que quiere tener como destino. En este ejemplo el destino es la versión más antigua del esquema EWS.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p120">In the **Main** method, instantiate the [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object with the service version you intend to target. This example targets the earliest version of the EWS schema.</span></span> 
    
   ```cs
    ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2007_SP1);
   ```

3. <span data-ttu-id="a6d61-p121">Si tiene como destino un servidor de Exchange local y el cliente está unido al dominio, vaya al paso 4. Si el cliente tiene como destino un buzón del sitio para desarrolladores de Exchange Online u Office 365, deberá pasar credenciales explícitas. Agregue el código siguiente después de crear instancias del objeto **ExchangeService** y establezca las credenciales de su cuenta de buzón. El nombre de usuario debe ser el nombre principal del usuario. Vaya al paso 5.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p121">If you are targeting an on-premises Exchange server and your client is domain joined, proceed to step 4. If you client is targeting an Exchange Online or Office 365 Developer Site mailbox, you have to pass explicit credentials. Add the following code after the instantiation of the **ExchangeService** object and set the credentials for your mailbox account. The user name should be the user principal name. Proceed to step 5.</span></span> 
    
   ```cs
    service.Credentials = new WebCredentials("user1@contoso.com", "password");
   ```

4. <span data-ttu-id="a6d61-p122">Los clientes unidos al dominio que tengan como destino un servidor de Exchange local pueden usar las credenciales predeterminadas del usuario que haya iniciado sesión, siempre y cuando dichas credenciales estén asociadas con un buzón. Agregue el código siguiente después de crear instancias del objeto **ExchangeService**.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p122">Domain-joined clients that target an on-premises Exchange server can use the default credentials of the user who is logged on, assuming the credentials are associated with a mailbox. Add the following code after the instantiation of the **ExchangeService** object.</span></span> 
    
   ```cs
    service.UseDefaultCredentials = true;
   ```

   <span data-ttu-id="a6d61-p123">Si el cliente tiene como destino un buzón del sitio para desarrolladores de Exchange Online u Office 365, compruebe que [UseDefaultCredentials](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservicebase.usedefaultcredentials%28v=exchg.80%29.aspx) esté establecido en **false**, que es el valor predeterminado. El cliente está listo para realizar la primera llamada al servicio Detección automática para obtener la dirección URL del servicio para realizar llamadas al servicio EWS.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p123">If your client targets an Exchange Online or Office 365 Developer Site mailbox, verify that [UseDefaultCredentials](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservicebase.usedefaultcredentials%28v=exchg.80%29.aspx) is set to **false**, which is the default value. Your client is ready to make the first call to the Autodiscover service to get the service URL for calls to the EWS service.</span></span>
    
5. <span data-ttu-id="a6d61-p124">El método **AutodiscoverUrl** del objeto **ExchangeService** realiza una serie de llamadas al servicio Detección automática para obtener la dirección URL del servicio. Si esta llamada de método se realiza correctamente, la propiedad URL del objeto **ExchangeService** se establecerá con la dirección URL del servicio. Pase la dirección de correo electrónico del usuario y el objeto **RedirectionUrlValidationCallback** al método **AutodiscoverUrl**. Agregue el código siguiente después de especificar las credenciales en el paso 3 o 4. Cambie  `user1@contoso.com` a su dirección de correo electrónico de modo que el servicio Detección automática encuentre su extremo EWS.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p124">The **AutodiscoverUrl** method on the **ExchangeService** object performs a series of calls to the Autodiscover service to get the service URL. If this method call is successful, the URL property on the **ExchangeService** object will be set with the service URL. Pass the user's email address and the **RedirectionUrlValidationCallback** to the **AutodiscoverUrl** method. Add the following code after the credentials have been specified in step 3 or 4. Change  `user1@contoso.com` to your email address so that the Autodiscover service finds your EWS endpoint.</span></span> 
    
   ```cs
    service.AutodiscoverUrl("user1@contoso.com", RedirectionUrlValidationCallback);
   ```

<span data-ttu-id="a6d61-186">En este momento, el cliente está configurado para hacer llamadas a EWS para tener acceso a los datos del buzón.</span><span class="sxs-lookup"><span data-stu-id="a6d61-186">At this point, your client is set up to make calls to EWS to access mailbox data.</span></span> <span data-ttu-id="a6d61-187">Si ejecuta ahora el código, comprobará que la llamada de método **AutodiscoverUrl** funcionó si examina el contenido de la propiedad [ExchangeService.Url](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a6d61-187">If you run your code now, you can verify that the **AutodiscoverUrl** method call worked by examining the contents of the [ExchangeService.Url](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) property.</span></span> <span data-ttu-id="a6d61-188">Si esta propiedad contiene una dirección URL, la llamada se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a6d61-188">If this property contains a URL, your call was a success!</span></span> <span data-ttu-id="a6d61-189">Esto significa que la aplicación se autenticó correctamente con el servicio y que detectó el extremo EWS de su buzón.</span><span class="sxs-lookup"><span data-stu-id="a6d61-189">This means that your application successfully authenticated with the service and discovered the EWS endpoint for your mailbox.</span></span> <span data-ttu-id="a6d61-190">Ahora ya puede realizar las primeras llamadas a EWS.</span><span class="sxs-lookup"><span data-stu-id="a6d61-190">Now you are ready to make your first calls to EWS.</span></span> <span data-ttu-id="a6d61-191">Para obtener más información acerca de cómo establecer la dirección URL de EWS, lea [establecer la dirección URL de servicio EWS mediante el uso de la API administrada de EWS](how-to-set-the-ews-service-url-by-using-the-ews-managed-api.md) .</span><span class="sxs-lookup"><span data-stu-id="a6d61-191">Read [Set the EWS service URL by using the EWS Managed API](how-to-set-the-ews-service-url-by-using-the-ews-managed-api.md) for more information about setting the EWS URL.</span></span> 

### <a name="step-6-create-your-first-hello-world-email-message"></a><span data-ttu-id="a6d61-192">Paso 6: crear el primer mensaje de correo electrónico de Hola a todos</span><span class="sxs-lookup"><span data-stu-id="a6d61-192">Step 6: Create your first Hello World email message</span></span>

1. <span data-ttu-id="a6d61-193">Después de la llamada de método **AutodiscoverUrl**, cree una instancia de un nuevo objeto **EmailMessage** y pase el objeto de servicio que ha creado.</span><span class="sxs-lookup"><span data-stu-id="a6d61-193">After the **AutodiscoverUrl** method call, instantiate a new **EmailMessage** object and pass in the service object you created.</span></span> 
    
   ```cs
    EmailMessage email = new EmailMessage(service);
   ```

   <span data-ttu-id="a6d61-p126">Ahora tiene un mensaje de correo electrónico en el que se ha establecido el enlace al servicio. Todas las llamadas iniciadas en el objeto **EmailMessage** tendrán el servicio como destino.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p126">You now have an email message on which the service binding is set. Any calls initiated on the **EmailMessage** object will be targeted at the service.</span></span> 
    
2. <span data-ttu-id="a6d61-p127">Ahora establezca el destinatario de la línea Para: del mensaje de correo electrónico. Para ello, cambie  `user1@contoso.com` y use su dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p127">Now set the To: line recipient of the email message. To do this, change  `user1@contoso.com` to use your SMTP address.</span></span> 
    
   ```cs
    email.ToRecipients.Add("user1@contoso.com");
   ```

3. <span data-ttu-id="a6d61-198">Establezca el asunto y el cuerpo del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a6d61-198">Set the subject and the body of the email message.</span></span>
    
   ```cs
    email.Subject = "HelloWorld";
    email.Body = new MessageBody("This is the first email I've sent by using the EWS Managed API.");
   ```

4. <span data-ttu-id="a6d61-199">Ya está listo para enviar su primer mensaje de correo electrónico mediante la API administrada EWS.</span><span class="sxs-lookup"><span data-stu-id="a6d61-199">You are now ready to send your first email message by using the EWS Managed API.</span></span> <span data-ttu-id="a6d61-200">El método **Send** llamará al servicio y enviará el mensaje de correo electrónico para su entrega.</span><span class="sxs-lookup"><span data-stu-id="a6d61-200">The **Send** method will call the service and submit the email message for delivery.</span></span> <span data-ttu-id="a6d61-201">Lea [comuníquese con EWS mediante el uso de la API administrada de EWS](how-to-communicate-with-ews-by-using-the-ews-managed-api.md) para obtener más información acerca de otros métodos que puede utilizar para comunicarse con Exchange.</span><span class="sxs-lookup"><span data-stu-id="a6d61-201">Read [Communicate with EWS by using the EWS Managed API](how-to-communicate-with-ews-by-using-the-ews-managed-api.md) to learn about other methods you can use to communicate with Exchange.</span></span> 
    
   ```cs
    email.Send();
   ```

5. <span data-ttu-id="a6d61-p129">Ya puede ejecutar la aplicación Hola a todos. En Visual Studio, seleccione **F5**. Se abrirá una ventana de consola en blanco. No verá nada en la ventana de consola mientras la aplicación se autentique, siga los redireccionamientos de Detección automática y realice su primera llamada para crear un mensaje de correo electrónico que usted se enviará a sí mismo. Si quiere ver las llamadas que se realizan, agregue las dos líneas de código siguientes antes de llamar al método **AutodiscoverUrl**. Después, presione F5. De este modo, se realizará un [seguimiento de las solicitudes y respuestas de EWS](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md) en la ventana de consola.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p129">You are ready to run your Hello World application. In Visual Studio, select **F5**. A blank console window will open. You will not see anything in the console window while your application authenticates, follows Autodiscover redirections, and then makes its first call to create an email message that you send to yourself. If you want to see the calls being made, add the following two lines of code before the **AutodiscoverUrl** method is called. Then press F5. This will [trace out the EWS requests and responses](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md) to the console window.</span></span> 
    
   ```cs
    service.TraceEnabled = true;
    service.TraceFlags = TraceFlags.All;
   ```

<span data-ttu-id="a6d61-p130">Ahora ya tiene una aplicación cliente activa de la API administrada EWS. Para su comodidad, en el ejemplo siguiente se muestra todo el código que agregó en Program.cs para crear la aplicación Hola a todos.</span><span class="sxs-lookup"><span data-stu-id="a6d61-p130">You now have a working EWS Managed API client application. For your convenience, the following example shows all the code that you added to Program.cs to create your Hello World application.</span></span>

```cs
using System;
using Microsoft.Exchange.WebServices.Data;
namespace HelloWorld
{
  class Program
  {
    static void Main(string[] args)
    {
      ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2007_SP1);
      service.Credentials = new WebCredentials("user1@contoso.com", "password");
      service.TraceEnabled = true;
      service.TraceFlags = TraceFlags.All;
      service.AutodiscoverUrl("user1@contoso.com", RedirectionUrlValidationCallback);
      EmailMessage email = new EmailMessage(service);
      email.ToRecipients.Add("user1@contoso.com");
      email.Subject = "HelloWorld";
      email.Body = new MessageBody("This is the first email I've sent by using the EWS Managed API");
      email.Send();
    }
    private static bool RedirectionUrlValidationCallback(string redirectionUrl)
    {
      // The default for the validation callback is to reject the URL.
      bool result = false;
      Uri redirectionUri = new Uri(redirectionUrl);
      // Validate the contents of the redirection URL. In this simple validation
      // callback, the redirection URL is considered valid if it is using HTTPS
      // to encrypt the authentication credentials. 
      if (redirectionUri.Scheme == "https")
      {
        result = true;
      }
      return result;
    }
  }
}
```

## <a name="next-steps"></a><span data-ttu-id="a6d61-211">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="a6d61-211">Next steps</span></span>
<span data-ttu-id="a6d61-212"><a name="Next"> </a></span><span class="sxs-lookup"><span data-stu-id="a6d61-212"></span></span>

<span data-ttu-id="a6d61-213">Si quiere ir más allá con su primera aplicación cliente de la API administrada EWS, explore los siguientes recursos:</span><span class="sxs-lookup"><span data-stu-id="a6d61-213">If you're ready to do more with your first EWS Managed API client application, explore the following resources:</span></span>
  
- [<span data-ttu-id="a6d61-214">Exchange 2013: 101 code samples (Exchange 2013: 101 ejemplos de código)</span><span class="sxs-lookup"><span data-stu-id="a6d61-214">Exchange 2013: 101 code samples</span></span>](http://code.msdn.microsoft.com/exchange/Exchange-2013-101-Code-3c38582c)
    
- [<span data-ttu-id="a6d61-215">Carpetas y elementos</span><span class="sxs-lookup"><span data-stu-id="a6d61-215">Folders and items</span></span>](folders-and-items-in-ews-in-exchange.md)
    
- [<span data-ttu-id="a6d61-216">EWSEditor</span><span class="sxs-lookup"><span data-stu-id="a6d61-216">EWSEditor</span></span>](http://ewseditor.codeplex.com/)
    
<span data-ttu-id="a6d61-217">Si surge algún problema con la aplicación [envíe una pregunta o un comentario al foro](http://social.technet.microsoft.com/Forums/exchange/en-US/home?forum=exchangesvrdevelopment) (y no olvide leer la publicación de más arriba).</span><span class="sxs-lookup"><span data-stu-id="a6d61-217">If you run into any issues with your application, [try posting a question or comment in the forum](http://social.technet.microsoft.com/Forums/exchange/en-US/home?forum=exchangesvrdevelopment) (and don't forget to read the top post).</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="a6d61-218">En esta sección</span><span class="sxs-lookup"><span data-stu-id="a6d61-218">In this section</span></span>
<span data-ttu-id="a6d61-219"><a name="Next"> </a></span><span class="sxs-lookup"><span data-stu-id="a6d61-219"></span></span>

- [<span data-ttu-id="a6d61-220">Hacer referencia al ensamblado de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="a6d61-220">Reference the EWS Managed API assembly</span></span>](how-to-reference-the-ews-managed-api-assembly.md)
    
- [<span data-ttu-id="a6d61-221">Establecer la dirección URL de servicio EWS mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="a6d61-221">Set the EWS service URL by using the EWS Managed API</span></span>](how-to-set-the-ews-service-url-by-using-the-ews-managed-api.md)
    
- [<span data-ttu-id="a6d61-222">Comunicarse con EWS mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="a6d61-222">Communicate with EWS by using the EWS Managed API</span></span>](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    
## <a name="see-also"></a><span data-ttu-id="a6d61-223">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6d61-223">See also</span></span>

- [<span data-ttu-id="a6d61-224">Empezar a utilizar servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="a6d61-224">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)    
- [<span data-ttu-id="a6d61-225">Introducción al diseño de EWS cliente de Exchange</span><span class="sxs-lookup"><span data-stu-id="a6d61-225">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)    
- [<span data-ttu-id="a6d61-226">Desarrollo de clientes de servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="a6d61-226">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)   
- [<span data-ttu-id="a6d61-227">Seguimiento de las solicitudes y respuestas para solucionar problemas de aplicaciones de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="a6d61-227">Trace requests and responses to troubleshoot EWS Managed API applications</span></span>](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
    

