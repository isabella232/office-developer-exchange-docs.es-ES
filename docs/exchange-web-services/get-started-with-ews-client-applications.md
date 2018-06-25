---
title: Empezar a trabajar con aplicaciones de cliente de EWS
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e6fd5c23-0ba5-4a7b-bdde-4a553447069f
description: Cree su primera aplicación utilizando Servicios Web Exchange (EWS) de Exchange.
ms.openlocfilehash: 911495c74f4c74114a86b1a3a98c9200db338b34
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763023"
---
# <a name="get-started-with-ews-client-applications"></a>Empezar a trabajar con aplicaciones de cliente de EWS

Este documento puede incluir contenido relacionado con funciones o productos preliminares que pueden cambiar mucho antes del lanzamiento comercial final. Este documento se proporciona "tal cual" solamente con fines informativos y Microsoft no realiza ninguna garantía, explícita ni implícita, en el documento. Cree su primera aplicación utilizando Servicios Web Exchange (EWS) de Exchange.
  
EWS es un servicio integral que las aplicaciones pueden usar para tener acceso a casi toda la información almacenada en un buzón de Exchange Online, Exchange Online como parte de Office 365 o Exchange local. EWS usa protocolos web estándar para proporcionar acceso a un servidor Exchange. Bibliotecas como la [API administrada de EWS](get-started-with-ews-managed-api-client-applications.md) ajustan las operaciones de EWS para proporcionar una interfaz orientada a objetos. Una vez que haya ejecutado los ejemplos de este artículo, tendrá un conocimiento básico de lo que puede hacer con EWS. 
  
Puede llamar a las operaciones de EWS desde cualquier sistema operativo o lenguaje, porque las solicitudes y respuestas de EWS usan el protocolo SOAP. Los ejemplos de este artículo se han escrito con C# y usan los objetos [HttpWebRequest](https://msdn.microsoft.com/library/System.Net.HttpWebRequest.aspx) y [HttpWebResponse](https://msdn.microsoft.com/library/System.Net.HttpWebResponse.aspx) .NET Framework. Sin embargo, la parte importante del código es el código XML que se usa para realizar la solicitud EWS y la respuesta XML devuelta desde el servidor. Los ejemplos de código hacen hincapié en las transacciones de XML y no en el procesamiento del código XML. 
  
## <a name="youll-need-an-exchange-server"></a>Necesitará un servidor de Exchange

Si ya tiene una cuenta de buzón de Exchange, puede omitir este paso. En caso contrario, dispone de las opciones siguientes para configurar un buzón de Exchange para su primera aplicación de EWS:
  
- [Obtener un sitio de Office 365 Developer](http://msdn.microsoft.com/en-us/library/office/fp179924.aspx)(recomendado). Esta es la forma más rápida de configurar un buzón de Exchange.
    
- Descargar [Exchange Server](http://office.microsoft.com/en-us/exchange/microsoft-exchange-try-or-buy-exchange-we-can-help-you-decide-FX103746846.aspx?WT%2Eintid1=ODC%5FENUS%5FFX103472230%5FXT103965589).
    
Después de haber comprobado que puede enviar y recibir correo electrónico desde el servidor Exchange, está listo para configurar el entorno de desarrollo. Puede usar Outlook Web App para comprobar que puede enviar correo electrónico.
  
También debe conocer la dirección URL del punto de conexión de EWS para su servidor. En una aplicación de producción, se usaría [Autodiscover](autodiscover-for-exchange.md) para determinar la dirección URL de EWS. Los ejemplos de este artículo usan la dirección URL del punto de conexión EWS de Office 365, https://outlook.office365.com/EWS/Exchange.asmx. La sección [Próximos pasos](#bk_next) contiene vínculos a más información sobre Autodiscover cuando esté listo. 
  
Si está probando la aplicación mediante un servidor Exchange que tiene el certificado autofirmado predeterminado, necesitará crear un [método de validación de certificados](how-to-validate-a-server-certificate-for-the-ews-managed-api.md) que cumpla los requisitos de seguridad de su organización. 
  
## <a name="set-up-your-development-environment"></a>Configurar el entorno de desarrollo

Las herramientas que usa para crear su primera aplicación de EWS dependen del sistema operativo y el idioma que use, y son principalmente una cuestión de gustos. Si quiere seguir los ejemplos de C# de este artículo, necesitará: 
  
- Cualquier versión de Visual Studio que admita la versión 4.0 de .NET Framework. 
    
- Una conexión a Internet que su equipo de desarrollo pueda usar para ponerse en contacto con el servidor Exchange. Si puede usar Outlook Web App con un nombre DNS en lugar de una dirección IP para conectarse al servidor Exchange, ya está preparado.
    
## <a name="create-your-first-ews-application"></a>Crear la primera aplicación de EWS

La aplicación de EWS que creará muestra dos escenarios típicos de uso de EWS:
  
1. Obtener información de un buzón de Exchange y mostrar esa información al usuario.
    
2. Realizar una acción, como enviar un correo electrónico, y comprobar la respuesta para ver si la acción se realizó correctamente.
    
Comencemos.
  
### <a name="set-up-the-solution"></a>Configurar la solución

En primer lugar, cree una nueva solución de aplicación de consola mediante Visual Studio. Cuando la solución esté lista, cree un nuevo objeto denominado Tracing.cs. Use este objeto para escribir información tanto en la consola como en un archivo de registro para que pueda revisar los resultados después de ejecutar el código. Pegue el siguiente código en el archivo Tracing.cs:
  
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

Luego abra el archivo Program.cs. Colocará el resto del código del ejemplo en este archivo.
  
En primer lugar, configure el shell del programa. El programa hará lo siguiente: 
  
1. Crear un archivo de registro para que la solicitud y la respuesta se puedan escribir en el disco para estudio posterior.
    
2. Obtener la dirección de correo electrónico y la contraseña de la cuenta a la que usted tendrá acceso.
    
3. Llamar a los métodos de ejemplo.
    
Reemplazar el método  `Main` en el archivo Program.cs por el código siguiente. 
  
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

Lo último que debe hacer es agregar el método estático  `GetPasswordFromConsole`. Este método devuelve un objeto [SecureString](https://msdn.microsoft.com/library/System.Security.SecureString.aspx) que contiene una contraseña escrita en la consola. 
  
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

### <a name="get-the-number-of-new-messages-in-an-inbox"></a>Obtener el número de nuevos mensajes en la Bandeja de entrada

Una operación común en una aplicación de EWS es obtener información sobre los mensajes de correo electrónico, las citas, las reuniones y las carpetas en donde se almacenan. En este ejemplo se obtiene el número de mensajes que hay en la Bandeja de entrada de una cuenta y se muestra el número total de mensajes y el número de mensajes no leídos. Esto demuestra las siguientes acciones comunes para aplicaciones de EWS:
  
- Realizar una solicitud EWS al servidor Exchange.
    
- Analizar la respuesta XML devuelta para obtener la información solicitada.
    
- Manejar los mensajes de error y las excepciones comunes.
    
Agregue el código siguiente al método  `ShowNumberOfMessagesInInbox` que era auxiliar después del método main. Cuando se ejecute la aplicación, se imprimirá el número de mensajes que hay en la Bandeja de entrada de la cuenta y el número de mensajes no leídos de la Bandeja de entrada. Después de ejecutar la aplicación, puede abrir el archivo GetStartedWithEWS.log para ver la solicitud XML que se envió al servidor Exchange y la respuesta que devolvió el servidor. 
  
```cs
      /// This is the XML request that is sent to the Exchange server.
      var getFolderSOAPRequest =
"<?xml version=\"1.0\" encoding=\"utf-8\"?>\n" +
"<soap:Envelope xmlns:soap=\"http://schemas.xmlsoap.org/soap/envelope/\"\n" +
"   xmlns:t=\"http://schemas.microsoft.com/exchange/services/2006/types\">\n" +
"<soap:Header>\n" +
"    <t:RequestServerVersion Version=\"Exchange2007_SP1\" />\n" +
"  </soap:Header>\n" +
"  <soap:Body>\n" +
"    <GetFolder xmlns=\"http://schemas.microsoft.com/exchange/services/2006/messages\"\n" +
"               xmlns:t=\"http://schemas.microsoft.com/exchange/services/2006/types\">\n" +
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
                                               ("{http://schemas.microsoft.com/exchange/services/2006/messages}ResponseCode")
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
                                              ("{http://schemas.microsoft.com/exchange/services/2006/messages}Folders")
                                            select folderElement;
            foreach (var folder in folders)
            {
              Tracing.Write("Folder name:     ");
              var folderName = from folderElement in
                                 folder.Descendants
                                 ("{http://schemas.microsoft.com/exchange/services/2006/types}DisplayName")
                               select folderElement.Value;
              Tracing.WriteLine(folderName.ElementAt(0));
              Tracing.Write("Total messages:  ");
              var totalCount = from folderElement in
                                 folder.Descendants
                                   ("{http://schemas.microsoft.com/exchange/services/2006/types}TotalCount")
                               select folderElement.Value;
              Tracing.WriteLine(totalCount.ElementAt(0));
              Tracing.Write("Unread messages: ");
              var unreadCount = from folderElement in
                                 folder.Descendants
                                   ("{http://schemas.microsoft.com/exchange/services/2006/types}UnreadCount")
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

### <a name="send-an-email-message"></a>Enviar un mensaje de correo electrónico

Otra operación común para una aplicación de EWS consiste en enviar mensajes de correo electrónico o convocatorias de reunión. En este ejemplo se crea y se envía un mensaje de correo electrónico usando las credenciales del usuario que se especificaron anteriormente. Aquí se ven estas tareas de aplicación comunes de EWS:
  
- Crear y enviar un correo electrónico.
    
- Analizar la respuesta XML devuelta para determinar si el correo electrónico se ha enviado correctamente.
    
- Manejar los mensajes de error y las excepciones comunes.
    
Agregue el código siguiente al método SendTestEmail que era auxiliar después del método main. Después de ejecutar la aplicación, puede abrir el archivo GetStartedWithEWS.log para ver la solicitud XML que se envió al servidor Exchange y la respuesta que devolvió el servidor.
  
```cs
var createItemSOAPRequest =
      "<?xml version=\"1.0\" encoding=\"utf-8\"?>\n" +
      "<soap:Envelope xmlns:xsi=\"http://www.w3.org/2001/XMLSchema-instance\" \n" +
      "               xmlns:m=\"http://schemas.microsoft.com/exchange/services/2006/messages\" \n" +
      "               xmlns:t=\"http://schemas.microsoft.com/exchange/services/2006/types\" \n" +
      "               xmlns:soap=\"http://schemas.xmlsoap.org/soap/envelope/\">\n" +
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
                                               ("{http://schemas.microsoft.com/exchange/services/2006/messages}ResponseCode")
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

## <a name="next-steps"></a>Pasos siguientes

Ahora que ya ha escrito su primera aplicación de EWS, está listo para descubrir otras formas de usar EWS. A continuación, le damos algunas ideas para empezar.
  
- Implemente [Autodiscover](autodiscover-for-exchange.md) en la aplicación para que se conecte al servidor Exchange correcto basándose en la dirección de correo electrónico del usuario. Vea también el ejemplo de [Exchange 2013: Obtener la configuración de usuario con Autodiscover](http://code.msdn.microsoft.com/Exchange-2013-Get-user-7e22c86e). 
    
- Mire la [Referencia de EWS](http://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx) para obtener más información sobre EWS. 
    
- Consulte las [Operaciones de EWS](http://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx) para obtener información sobre las operaciones que están disponibles. 
    
- Use el [Editor de EWS](http://ewseditor.codeplex.com/) para ver el tráfico SOAP enviado hacia y desde el servidor. 
    
Si surge algún problema con la aplicación [envíe una pregunta o un comentario al foro](http://social.technet.microsoft.com/Forums/exchange/en-US/home?forum=exchangesvrdevelopment) (y no olvide leer la primera publicación). 
  
## <a name="see-also"></a>Vea también

- [Empezar a utilizar servicios web de Exchange](start-using-web-services-in-exchange.md)   
- [Explore la API administrada de EWS, EWS y servicios web de Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) 
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)   
- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)  
- [Empezar a trabajar con aplicaciones de cliente de la API administrada de EWS](get-started-with-ews-managed-api-client-applications.md)
    

