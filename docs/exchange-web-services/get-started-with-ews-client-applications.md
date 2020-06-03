---
title: Empezar a trabajar con aplicaciones de cliente de EWS
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.assetid: e6fd5c23-0ba5-4a7b-bdde-4a553447069f
description: Cree su primera aplicación utilizando Servicios Web Exchange (EWS) de Exchange.
localization_priority: Priority
ms.openlocfilehash: fd02c46777dabd04b492ba3c4420a0737640c5eb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528401"
---
# <a name="get-started-with-ews-client-applications"></a><span data-ttu-id="286bd-103">Empezar a trabajar con aplicaciones de cliente de EWS</span><span class="sxs-lookup"><span data-stu-id="286bd-103">Get started with EWS client applications</span></span>

<span data-ttu-id="286bd-104">Cree su primera aplicación utilizando Servicios Web Exchange (EWS) de Exchange.</span><span class="sxs-lookup"><span data-stu-id="286bd-104">Create your first application by using Exchange Web Services (EWS) in Exchange.</span></span>
  
<span data-ttu-id="286bd-p101">EWS es un servicio integral que las aplicaciones pueden usar para tener acceso a casi toda la información almacenada en un buzón de Exchange Online, Exchange Online como parte de Office 365 o Exchange local. EWS usa protocolos web estándar para proporcionar acceso a un servidor Exchange. Bibliotecas como la [API administrada de EWS](get-started-with-ews-managed-api-client-applications.md) ajustan las operaciones de EWS para proporcionar una interfaz orientada a objetos. Una vez que haya ejecutado los ejemplos de este artículo, tendrá un conocimiento básico de lo que puede hacer con EWS.</span><span class="sxs-lookup"><span data-stu-id="286bd-p101">EWS is a comprehensive service that your applications can use to access almost all the information stored in an Exchange Online, Exchange Online as part of Office 365, or Exchange on-premises mailbox. EWS uses standard web protocols to provide access to an Exchange server; libraries like the [EWS Managed API](get-started-with-ews-managed-api-client-applications.md) wrap the EWS operations to provide an object-oriented interface. After you've run the examples in this article, you will have a basic understanding of what you can do with EWS.</span></span> 
  
<span data-ttu-id="286bd-p102">Puede llamar a las operaciones de EWS desde cualquier sistema operativo o lenguaje, porque las solicitudes y respuestas de EWS usan el protocolo SOAP. Los ejemplos de este artículo se han escrito con C# y usan los objetos [HttpWebRequest](https://msdn.microsoft.com/library/System.Net.HttpWebRequest.aspx) y [HttpWebResponse](https://msdn.microsoft.com/library/System.Net.HttpWebResponse.aspx) .NET Framework. Sin embargo, la parte importante del código es el código XML que se usa para realizar la solicitud EWS y la respuesta XML devuelta desde el servidor. Los ejemplos de código hacen hincapié en las transacciones de XML y no en el procesamiento del código XML.</span><span class="sxs-lookup"><span data-stu-id="286bd-p102">You can call EWS operations from any operating system or language, because the EWS requests and responses use the SOAP protocol. The examples in this article are written using C# and make use of the .NET Framework [HttpWebRequest](https://msdn.microsoft.com/library/System.Net.HttpWebRequest.aspx) and [HttpWebResponse](https://msdn.microsoft.com/library/System.Net.HttpWebResponse.aspx) objects; however, the important part of the code is the XML used to make the EWS request and the XML response returned from the server. The code examples emphasize the XML transactions and not processing the XML.</span></span> 
  
## <a name="youll-need-an-exchange-server"></a><span data-ttu-id="286bd-111">Necesitará un servidor de Exchange</span><span class="sxs-lookup"><span data-stu-id="286bd-111">You'll need an Exchange server</span></span>

<span data-ttu-id="286bd-p103">Si ya tiene una cuenta de buzón de Exchange, puede omitir este paso. En caso contrario, dispone de las opciones siguientes para configurar un buzón de Exchange para su primera aplicación de EWS:</span><span class="sxs-lookup"><span data-stu-id="286bd-p103">If you already have an Exchange mailbox account, you can skip this step. Otherwise, you have the following options for setting up an Exchange mailbox for your first EWS application:</span></span>
  
- <span data-ttu-id="286bd-p104">[Obtener un sitio de Office 365 Developer](https://msdn.microsoft.com/library/office/fp179924.aspx)(recomendado). Esta es la forma más rápida de configurar un buzón de Exchange.</span><span class="sxs-lookup"><span data-stu-id="286bd-p104">[Get an Office 365 Developer Site ](https://msdn.microsoft.com/library/office/fp179924.aspx)(recommended). This is the quickest way for you to get an Exchange mailbox.</span></span>
    
- <span data-ttu-id="286bd-116">Descargar [Exchange Server](https://office.microsoft.com/exchange/microsoft-exchange-try-or-buy-exchange-we-can-help-you-decide-FX103746846.aspx?WT%2Eintid1=ODC%5FENUS%5FFX103472230%5FXT103965589).</span><span class="sxs-lookup"><span data-stu-id="286bd-116">Download [Exchange Server](https://office.microsoft.com/exchange/microsoft-exchange-try-or-buy-exchange-we-can-help-you-decide-FX103746846.aspx?WT%2Eintid1=ODC%5FENUS%5FFX103472230%5FXT103965589).</span></span>

    
<span data-ttu-id="286bd-p105">Después de haber comprobado que puede enviar y recibir correo electrónico desde el servidor Exchange, está listo para configurar el entorno de desarrollo. Puede usar Outlook Web App para comprobar que puede enviar correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="286bd-p105">After you've verified that you can send and receive email from your Exchange server you are ready to set up your development environment. You can use Outlook Web App to verify that you can send email.</span></span>
  
<span data-ttu-id="286bd-p106">También debe conocer la dirección URL del punto de conexión de EWS para su servidor. En una aplicación de producción, se usaría [Autodiscover](autodiscover-for-exchange.md) para determinar la dirección URL de EWS. Los ejemplos de este artículo usan la dirección URL del punto de conexión EWS de Office 365, `https://outlook.office365.com/EWS/Exchange.asmx`. La sección [Próximos pasos](#bk_next) contiene vínculos a más información sobre Autodiscover cuando esté listo.</span><span class="sxs-lookup"><span data-stu-id="286bd-p106">You'll also need to know the URL of the EWS endpoint for your server. In a production application, you'd use [Autodiscover](autodiscover-for-exchange.md) to determine the EWS URL. The examples in this article use the Office 365 EWS endpoint URL, `https://outlook.office365.com/EWS/Exchange.asmx`. The [Next steps](#bk_next) section has links to more information about Autodiscover when you're ready.</span></span> 
  
<span data-ttu-id="286bd-123">Si está probando la aplicación mediante un servidor Exchange que tiene el certificado autofirmado predeterminado, necesitará crear un [método de validación de certificados](how-to-validate-a-server-certificate-for-the-ews-managed-api.md) que cumpla los requisitos de seguridad de su organización.</span><span class="sxs-lookup"><span data-stu-id="286bd-123">If you are testing your application using an Exchange server that has the default self-signed certificate, you'll need to create a [certificate validation method](how-to-validate-a-server-certificate-for-the-ews-managed-api.md) that meets the security requirements of your organization.</span></span> 
  
## <a name="set-up-your-development-environment"></a><span data-ttu-id="286bd-124">Configurar el entorno de desarrollo</span><span class="sxs-lookup"><span data-stu-id="286bd-124">Set up your development environment</span></span>

<span data-ttu-id="286bd-p107">Las herramientas que usa para crear su primera aplicación de EWS dependen del sistema operativo y el idioma que use, y son principalmente una cuestión de gustos. Si quiere seguir los ejemplos de C# de este artículo, necesitará:</span><span class="sxs-lookup"><span data-stu-id="286bd-p107">The tools that you use to create your first EWS application depend on the operating system and language that you use, and are mostly a matter of taste. If you want to follow along with the C# examples in this article, you'll need:</span></span> 
  
- <span data-ttu-id="286bd-127">Cualquier versión de Visual Studio que admita la versión 4.0 de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="286bd-127">Any version of Visual Studio that supports the .NET Framework 4.0.</span></span> 
    
- <span data-ttu-id="286bd-p108">Una conexión a Internet que su equipo de desarrollo pueda usar para ponerse en contacto con el servidor Exchange. Si puede usar Outlook Web App con un nombre DNS en lugar de una dirección IP para conectarse al servidor Exchange, ya está preparado.</span><span class="sxs-lookup"><span data-stu-id="286bd-p108">An Internet connection that your development machine can use to contact your Exchange server. If you can use Outlook Web App with a DNS name rather than an IP address to connect to your Exchange server, you are set up.</span></span>
    
## <a name="create-your-first-ews-application"></a><span data-ttu-id="286bd-130">Crear la primera aplicación de EWS</span><span class="sxs-lookup"><span data-stu-id="286bd-130">Create your first EWS application</span></span>

<span data-ttu-id="286bd-131">La aplicación de EWS que creará muestra dos escenarios típicos de uso de EWS:</span><span class="sxs-lookup"><span data-stu-id="286bd-131">The EWS application that you will create shows two typical scenarios for using EWS:</span></span>
  
1. <span data-ttu-id="286bd-132">Obtener información de un buzón de Exchange y mostrar esa información al usuario.</span><span class="sxs-lookup"><span data-stu-id="286bd-132">Get information from an Exchange mailbox and display that information to the user.</span></span>
    
2. <span data-ttu-id="286bd-133">Realizar una acción, como enviar un correo electrónico, y comprobar la respuesta para ver si la acción se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="286bd-133">Perform an action, such as sending an email, and check the response to see if the action succeeded.</span></span>
    
<span data-ttu-id="286bd-134">Comencemos.</span><span class="sxs-lookup"><span data-stu-id="286bd-134">Let's get started.</span></span>
  
### <a name="set-up-the-solution"></a><span data-ttu-id="286bd-135">Configurar la solución</span><span class="sxs-lookup"><span data-stu-id="286bd-135">Set up the solution</span></span>

<span data-ttu-id="286bd-p109">En primer lugar, cree una nueva solución de aplicación de consola mediante Visual Studio. Cuando la solución esté lista, cree un nuevo objeto denominado Tracing.cs. Use este objeto para escribir información tanto en la consola como en un archivo de registro para que pueda revisar los resultados después de ejecutar el código. Pegue el siguiente código en el archivo Tracing.cs:</span><span class="sxs-lookup"><span data-stu-id="286bd-p109">First, create a new console application solution using Visual Studio. When the solution is ready, create a new object called Tracing.cs. Use this object to write information to both the console and a log file so that you can review the results after you run your code. Paste the following code into the Tracing.cs file.</span></span>
  
```cs
using System;
using System.IO;
namespace Microsoft.Exchange.Samples.EWS
{
  class Tracing
  {
    private static TextWriter logFileWriter = null;
    public static void OpenLog(string fileName)
    {
      logFileWriter = new StreamWriter(fileName);
    }
    public static void Write(string format, params object[] args)
    {
      Console.Write(format, args);
      if (logFileWriter != null)
      {
        logFileWriter.Write(format, args);
      }
    }
    public static void WriteLine(string format, params object[] args)
    {
      Console.WriteLine(format, args);
      if (logFileWriter != null)
      {
        logFileWriter.WriteLine(format, args);
      }
    }
    public static void CloseLog()
    {
      logFileWriter.Flush();
      logFileWriter.Close();
    }
  }
}
```

<span data-ttu-id="286bd-p110">Luego abra el archivo Program.cs. Colocará el resto del código del ejemplo en este archivo.</span><span class="sxs-lookup"><span data-stu-id="286bd-p110">Next, open the Program.cs file. You will put the rest of the code for the example in this file.</span></span>
  
<span data-ttu-id="286bd-p111">En primer lugar, configure el shell del programa. El programa hará lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="286bd-p111">First, set up the shell of the program. The program will:</span></span> 
  
1. <span data-ttu-id="286bd-144">Crear un archivo de registro para que la solicitud y la respuesta se puedan escribir en el disco para estudio posterior.</span><span class="sxs-lookup"><span data-stu-id="286bd-144">Create a log file so that the request and response can be written to disk for later study.</span></span>
    
2. <span data-ttu-id="286bd-145">Obtener la dirección de correo electrónico y la contraseña de la cuenta a la que usted tendrá acceso.</span><span class="sxs-lookup"><span data-stu-id="286bd-145">Get the email address and password of the account that you'll access.</span></span>
    
3. <span data-ttu-id="286bd-146">Llamar a los métodos de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="286bd-146">Call the sample methods.</span></span>
    
<span data-ttu-id="286bd-147">Reemplazar el método  `Main` en el archivo Program.cs por el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="286bd-147">Replace the  `Main` method in the Program.cs with the following code.</span></span> 
  
```cs
    static void Main(string[] args)
    {
      // Start tracing to console and a log file.
      Tracing.OpenLog("./GetStartedWithEWS.log");
      Tracing.WriteLine("EWS sample application started.");
      var isValidEmailAddress = false;
      Console.Write("Enter an email address: ");
      var emailAddress = Console.ReadLine();
      
        isValidEmailAddress = (emailAddress.Contains("@") &amp;&amp; emailAddress.Contains("."));
      if (!isValidEmailAddress)
      {
        Tracing.WriteLine("Email address " + emailAddress + " is not a valid SMTP address. Closing program.");
        return;
      }
      SecureString password = GetPasswordFromConsole();
      if (password.Length == 0)
      {
        Tracing.WriteLine("Password empty, closing program.");
      }
      NetworkCredential userCredentials = new NetworkCredential(emailAddress, password);
      // These are the sample methods that demonstrate using EWS.
      // ShowNumberOfMessagesInInbox(userCredentials);
      // SendTestEmail(userCredentials);
     
      Tracing.WriteLine("EWS sample application ends.");
      Tracing.CloseLog();
      Console.WriteLine("Press enter to exit: ");
      Console.ReadLine();
    }
    // These method stubs will be filled in later.
    private static void ShowNumberOfMessagesInInbox(NetworkCredential userCredentials)
    {
    }
    private static void SendTestEmail(NetworkCredential userCredentials)
    {
    }
```

<span data-ttu-id="286bd-p112">Lo último que debe hacer es agregar el método estático  `GetPasswordFromConsole`. Este método devuelve un objeto [SecureString](https://msdn.microsoft.com/library/System.Security.SecureString.aspx) que contiene una contraseña escrita en la consola.</span><span class="sxs-lookup"><span data-stu-id="286bd-p112">The last thing that you need to do is add the  `GetPasswordFromConsole` static method. This method returns a [SecureString](https://msdn.microsoft.com/library/System.Security.SecureString.aspx) object that contains a password typed at the console.</span></span> 
  
```cs
    private static SecureString GetPasswordFromConsole()
    {
      SecureString password = new SecureString();
      bool readingPassword = true;
      Console.Write("Enter password: ");
      while (readingPassword)
      {
        ConsoleKeyInfo userInput = Console.ReadKey(true);
        switch (userInput.Key)
        {
          case (ConsoleKey.Enter):
            readingPassword = false;
            break;
          case (ConsoleKey.Escape):
            password.Clear();
            readingPassword = false;
            break;
          case (ConsoleKey.Backspace):
            if (password.Length > 0)
            {
              password.RemoveAt(password.Length - 1);
              Console.SetCursorPosition(Console.CursorLeft - 1, Console.CursorTop);
              Console.Write(" ");
              Console.SetCursorPosition(Console.CursorLeft - 1, Console.CursorTop);
            }
            break;
          default:
            if (userInput.KeyChar != 0)
            {
              password.AppendChar(userInput.KeyChar);
              Console.Write("*");
            }
            break;
        }
      }
      Console.WriteLine();
      password.MakeReadOnly();
      return password;
    }
```

### <a name="get-the-number-of-new-messages-in-an-inbox"></a><span data-ttu-id="286bd-150">Obtener el número de nuevos mensajes en la Bandeja de entrada</span><span class="sxs-lookup"><span data-stu-id="286bd-150">Get the number of new messages in an Inbox</span></span>

<span data-ttu-id="286bd-p113">Una operación común en una aplicación de EWS es obtener información sobre los mensajes de correo electrónico, las citas, las reuniones y las carpetas en donde se almacenan. En este ejemplo se obtiene el número de mensajes que hay en la Bandeja de entrada de una cuenta y se muestra el número total de mensajes y el número de mensajes no leídos. Esto demuestra las siguientes acciones comunes para aplicaciones de EWS:</span><span class="sxs-lookup"><span data-stu-id="286bd-p113">A common operation in an EWS application is to get information about email messages, appointments, meetings, and the folders that store them. This example gets the number of messages in an account's Inbox and displays the total number of messages and the number of unread messages. It demonstrates the following common actions for EWS applications:</span></span>
  
- <span data-ttu-id="286bd-154">Realizar una solicitud EWS al servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="286bd-154">Making an EWS request to the Exchange server.</span></span>
    
- <span data-ttu-id="286bd-155">Analizar la respuesta XML devuelta para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="286bd-155">Parsing the returned XML response for the requested information.</span></span>
    
- <span data-ttu-id="286bd-156">Manejar los mensajes de error y las excepciones comunes.</span><span class="sxs-lookup"><span data-stu-id="286bd-156">Handling common exceptions and error messages.</span></span>
    
<span data-ttu-id="286bd-p114">Agregue el código siguiente al método  `ShowNumberOfMessagesInInbox` que era auxiliar después del método main. Cuando se ejecute la aplicación, se imprimirá el número de mensajes que hay en la Bandeja de entrada de la cuenta y el número de mensajes no leídos de la Bandeja de entrada. Después de ejecutar la aplicación, puede abrir el archivo GetStartedWithEWS.log para ver la solicitud XML que se envió al servidor Exchange y la respuesta que devolvió el servidor.</span><span class="sxs-lookup"><span data-stu-id="286bd-p114">Add the following code to the  `ShowNumberOfMessagesInInbox` method that was stubbed out after the main method. When you run the application, it will print the number of messages in the account's Inbox and the number of unread messages in the Inbox. After you run the application, you can open the GetStartedWithEWS.log file to see the XML request that was sent to the Exchange server and the response that the server returned.</span></span> 
  
```cs
      /// This is the XML request that is sent to the Exchange server.
      var getFolderSOAPRequest =
"<?xml version=\"1.0\" encoding=\"utf-8\"?>\n" +
"<soap:Envelope xmlns:soap=\"https://schemas.xmlsoap.org/soap/envelope/\"\n" +
"   xmlns:t=\"https://schemas.microsoft.com/exchange/services/2006/types\">\n" +
"<soap:Header>\n" +
"    <t:RequestServerVersion Version=\"Exchange2007_SP1\" />\n" +
"  </soap:Header>\n" +
"  <soap:Body>\n" +
"    <GetFolder xmlns=\"https://schemas.microsoft.com/exchange/services/2006/messages\"\n" +
"               xmlns:t=\"https://schemas.microsoft.com/exchange/services/2006/types\">\n" +
"      <FolderShape>\n" +
"        <t:BaseShape>Default</t:BaseShape>\n" +
"      </FolderShape>\n" +
"      <FolderIds>\n" +
"        <t:DistinguishedFolderId Id=\"inbox\"/>\n" +
"      </FolderIds>\n" +
"    </GetFolder>\n" +
"  </soap:Body>\n" +
"</soap:Envelope>\n";
      // Write the get folder operation request to the console and log file.
      Tracing.WriteLine("Get folder operation request:");
      Tracing.WriteLine(getFolderSOAPRequest);
      var getFolderRequest = WebRequest.CreateHttp(Office365WebServicesURL);
      getFolderRequest.AllowAutoRedirect = false;
      getFolderRequest.Credentials = userCredentials;
      getFolderRequest.Method = "POST";
      getFolderRequest.ContentType = "text/xml";
      var requestWriter = new StreamWriter(getFolderRequest.GetRequestStream());
      requestWriter.Write(getFolderSOAPRequest);
      requestWriter.Close();
      try
      {
        var getFolderResponse = (HttpWebResponse)(getFolderRequest.GetResponse());
        if (getFolderResponse.StatusCode == HttpStatusCode.OK)
        {
          var responseStream = getFolderResponse.GetResponseStream();
          XElement responseEnvelope = XElement.Load(responseStream);
          if (responseEnvelope != null)
          {
            // Write the response to the console and log file.
            Tracing.WriteLine("Response:");
            StringBuilder stringBuilder = new StringBuilder();
            XmlWriterSettings settings = new XmlWriterSettings();
            settings.Indent = true;
            XmlWriter writer = XmlWriter.Create(stringBuilder, settings);
            responseEnvelope.Save(writer);
            writer.Close();
            Tracing.WriteLine(stringBuilder.ToString());
            // Check the response for error codes. If there is an error, throw an application exception.
            IEnumerable<XElement> errorCodes = from errorCode in responseEnvelope.Descendants
                                               ("{https://schemas.microsoft.com/exchange/services/2006/messages}ResponseCode")
                                               select errorCode;
            foreach (var errorCode in errorCodes)
            {
              if (errorCode.Value != "NoError")
              {
                switch (errorCode.Parent.Name.LocalName.ToString())
                {
                  case "Response":
                    string responseError = "Response-level error getting inbox information:\n" + errorCode.Value;
                    throw new ApplicationException(responseError);
                  case "UserResponse":
                    string userError = "User-level error getting inbox information:\n" + errorCode.Value;
                    throw new ApplicationException(userError);
                }
              }
            }
            // Process the response.
            IEnumerable<XElement> folders = from folderElement in
                                              responseEnvelope.Descendants
                                              ("{https://schemas.microsoft.com/exchange/services/2006/messages}Folders")
                                            select folderElement;
            foreach (var folder in folders)
            {
              Tracing.Write("Folder name:     ");
              var folderName = from folderElement in
                                 folder.Descendants
                                 ("{https://schemas.microsoft.com/exchange/services/2006/types}DisplayName")
                               select folderElement.Value;
              Tracing.WriteLine(folderName.ElementAt(0));
              Tracing.Write("Total messages:  ");
              var totalCount = from folderElement in
                                 folder.Descendants
                                   ("{https://schemas.microsoft.com/exchange/services/2006/types}TotalCount")
                               select folderElement.Value;
              Tracing.WriteLine(totalCount.ElementAt(0));
              Tracing.Write("Unread messages: ");
              var unreadCount = from folderElement in
                                 folder.Descendants
                                   ("{https://schemas.microsoft.com/exchange/services/2006/types}UnreadCount")
                               select folderElement.Value;
              Tracing.WriteLine(unreadCount.ElementAt(0));
            }
          }
        }
      }
      catch (WebException ex)
      {
        Tracing.WriteLine("Caught Web exception:");
        Tracing.WriteLine(ex.Message);
      }
      catch (ApplicationException ex)
      {
        Tracing.WriteLine("Caught application exception:");
        Tracing.WriteLine(ex.Message);
      }

```

### <a name="send-an-email-message"></a><span data-ttu-id="286bd-160">Enviar un mensaje de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="286bd-160">Send an email message</span></span>

<span data-ttu-id="286bd-p115">Otra operación común para una aplicación de EWS consiste en enviar mensajes de correo electrónico o convocatorias de reunión. En este ejemplo se crea y se envía un mensaje de correo electrónico usando las credenciales del usuario que se especificaron anteriormente. Aquí se ven estas tareas de aplicación comunes de EWS:</span><span class="sxs-lookup"><span data-stu-id="286bd-p115">Another common operation for an EWS application is to send email messages or meeting requests. This example creates and sends an email message using the user credentials that were entered earlier. It demonstrates these common EWS application tasks:</span></span>
  
- <span data-ttu-id="286bd-164">Crear y enviar un correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="286bd-164">Creating and sending an email.</span></span>
    
- <span data-ttu-id="286bd-165">Analizar la respuesta XML devuelta para determinar si el correo electrónico se ha enviado correctamente.</span><span class="sxs-lookup"><span data-stu-id="286bd-165">Parsing the returned XML response to determine if the email was correctly sent.</span></span>
    
- <span data-ttu-id="286bd-166">Manejar los mensajes de error y las excepciones comunes.</span><span class="sxs-lookup"><span data-stu-id="286bd-166">Handling common exceptions and error messages.</span></span>
    
<span data-ttu-id="286bd-p116">Agregue el código siguiente al método SendTestEmail que era auxiliar después del método main. Después de ejecutar la aplicación, puede abrir el archivo GetStartedWithEWS.log para ver la solicitud XML que se envió al servidor Exchange y la respuesta que devolvió el servidor.</span><span class="sxs-lookup"><span data-stu-id="286bd-p116">Add the following code to the SendTestEmail method that was stubbed out after the main method. After you run the application, you can open the GetStartedWithEWS.log file to see the XML request that was sent to the Exchange server and the response that the server returned.</span></span>
  
```cs
var createItemSOAPRequest =
      "<?xml version=\"1.0\" encoding=\"utf-8\"?>\n" +
      "<soap:Envelope xmlns:xsi=\"http://www.w3.org/2001/XMLSchema-instance\" \n" +
      "               xmlns:m=\"https://schemas.microsoft.com/exchange/services/2006/messages\" \n" +
      "               xmlns:t=\"https://schemas.microsoft.com/exchange/services/2006/types\" \n" +
      "               xmlns:soap=\"https://schemas.xmlsoap.org/soap/envelope/\">\n" +
      "  <soap:Header>\n" +
      "    <t:RequestServerVersion Version=\"Exchange2007_SP1\" />\n" +
      "  </soap:Header>\n" +
      "  <soap:Body>\n" +
      "    <m:CreateItem MessageDisposition=\"SendAndSaveCopy\">\n" +
      "      <m:SavedItemFolderId>\n" +
      "        <t:DistinguishedFolderId Id=\"sentitems\" />\n" +
      "      </m:SavedItemFolderId>\n" +
      "      <m:Items>\n" +
      "        <t:Message>\n" +
      "          <t:Subject>Company Soccer Team</t:Subject>\n" +
      "          <t:Body BodyType=\"HTML\">Are you interested in joining?</t:Body>\n" +
      "          <t:ToRecipients>\n" +
      "            <t:Mailbox>\n" +
      "              <t:EmailAddress>sadie@contoso.com</t:EmailAddress>\n" +
      "              </t:Mailbox>\n" +
      "          </t:ToRecipients>\n" +
      "        </t:Message>\n" +
      "      </m:Items>\n" +
      "    </m:CreateItem>\n" +
      "  </soap:Body>\n" +
      "</soap:Envelope>\n";
      // Write the create item operation request to the console and log file.
      Tracing.WriteLine("Get folder operation request:");
      Tracing.WriteLine(createItemSOAPRequest);
      var getFolderRequest = WebRequest.CreateHttp(Office365WebServicesURL);
      getFolderRequest.AllowAutoRedirect = false;
      getFolderRequest.Credentials = userCredentials;
      getFolderRequest.Method = "POST";
      getFolderRequest.ContentType = "text/xml";
      var requestWriter = new StreamWriter(getFolderRequest.GetRequestStream());
      requestWriter.Write(createItemSOAPRequest);
      requestWriter.Close();
      try
      {
        var getFolderResponse = (HttpWebResponse)(getFolderRequest.GetResponse());
        if (getFolderResponse.StatusCode == HttpStatusCode.OK)
        {
          var responseStream = getFolderResponse.GetResponseStream();
          XElement responseEnvelope = XElement.Load(responseStream);
          if (responseEnvelope != null)
          {
            // Write the response to the console and log file.
            Tracing.WriteLine("Response:");
            StringBuilder stringBuilder = new StringBuilder();
            XmlWriterSettings settings = new XmlWriterSettings();
            settings.Indent = true;
            XmlWriter writer = XmlWriter.Create(stringBuilder, settings);
            responseEnvelope.Save(writer);
            writer.Close();
            Tracing.WriteLine(stringBuilder.ToString());
            // Check the response for error codes. If there is an error, throw an application exception.
            IEnumerable<XElement> errorCodes = from errorCode in responseEnvelope.Descendants
                                               ("{https://schemas.microsoft.com/exchange/services/2006/messages}ResponseCode")
                                               select errorCode;
            foreach (var errorCode in errorCodes)
            {
              if (errorCode.Value != "NoError")
              {
                switch (errorCode.Parent.Name.LocalName.ToString())
                {
                  case "Response":
                    string responseError = "Response-level error getting inbox information:\n" + errorCode.Value;
                    throw new ApplicationException(responseError);
                  case "UserResponse":
                    string userError = "User-level error getting inbox information:\n" + errorCode.Value;
                    throw new ApplicationException(userError);
                }
              }
            }
            Tracing.WriteLine("Message sent successfully.");
          }
        }
      }
      catch (WebException ex)
      {
        Tracing.WriteLine("Caught Web exception:");
        Tracing.WriteLine(ex.Message);
      }
      catch (ApplicationException ex)
      {
        Tracing.WriteLine("Caught application exception:");
        Tracing.WriteLine(ex.Message);
      }
```

<a name="bk_next"></a>

## <a name="next-steps"></a><span data-ttu-id="286bd-169">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="286bd-169">Next steps</span></span>

<span data-ttu-id="286bd-p117">Ahora que ya ha escrito su primera aplicación de EWS, está listo para descubrir otras formas de usar EWS. A continuación, le damos algunas ideas para empezar.</span><span class="sxs-lookup"><span data-stu-id="286bd-p117">Now that you've written your first EWS application, you're ready to discover other ways to use EWS. Here are some ideas to get you started:</span></span>
  
- <span data-ttu-id="286bd-p118">Implemente [Autodiscover](autodiscover-for-exchange.md) en la aplicación para que se conecte al servidor Exchange correcto basándose en la dirección de correo electrónico del usuario. Vea también el ejemplo de [Exchange 2013: Obtener la configuración de usuario con Autodiscover](https://code.msdn.microsoft.com/Exchange-2013-Get-user-7e22c86e).</span><span class="sxs-lookup"><span data-stu-id="286bd-p118">Implement [Autodiscover](autodiscover-for-exchange.md) in your application so that your application will connect to the correct Exchange server based on the user's email address. See also the [Exchange 2013: Get user settings with Autodiscover](https://code.msdn.microsoft.com/Exchange-2013-Get-user-7e22c86e) sample.</span></span> 
    
- <span data-ttu-id="286bd-174">Mire la [Referencia de EWS](https://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx) para obtener más información sobre EWS.</span><span class="sxs-lookup"><span data-stu-id="286bd-174">Look at the [EWS reference](https://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx) for more information about EWS.</span></span> 
    
- <span data-ttu-id="286bd-175">Consulte las [Operaciones de EWS](https://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx) para obtener información sobre las operaciones que están disponibles.</span><span class="sxs-lookup"><span data-stu-id="286bd-175">See the [EWS operations](https://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx) for information about the operations that are available.</span></span> 
    
- <span data-ttu-id="286bd-176">Use el [Editor de EWS](http://ewseditor.codeplex.com/) para ver el tráfico SOAP enviado hacia y desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="286bd-176">Use [EWS Editor](http://ewseditor.codeplex.com/) to see the SOAP traffic sent to and from the server.</span></span> 
    
<span data-ttu-id="286bd-177">Si surge algún problema con la aplicación [envíe una pregunta o un comentario al foro](https://social.technet.microsoft.com/Forums/exchange/home?forum=exchangesvrdevelopment) (y no olvide leer la primera publicación).</span><span class="sxs-lookup"><span data-stu-id="286bd-177">If you run into any issues with your application, [try posting a question or comment in the forum](https://social.technet.microsoft.com/Forums/exchange/home?forum=exchangesvrdevelopment) (and don't forget to read the first post).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="286bd-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="286bd-178">See also</span></span>

- [<span data-ttu-id="286bd-179">Empezar a usar los servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="286bd-179">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)   
- [<span data-ttu-id="286bd-180">Explore la API administrada de EWS, EWS y servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="286bd-180">Explore the EWS Managed API, EWS, and web services in Exchange</span></span>](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) 
- [<span data-ttu-id="286bd-181">Introducción al diseño de EWS cliente de Exchange</span><span class="sxs-lookup"><span data-stu-id="286bd-181">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)   
- [<span data-ttu-id="286bd-182">Desarrollo de clientes de servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="286bd-182">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)  
- [<span data-ttu-id="286bd-183">Empezar a trabajar con aplicaciones de cliente de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="286bd-183">Get started with EWS Managed API client applications</span></span>](get-started-with-ews-managed-api-client-applications.md)
    