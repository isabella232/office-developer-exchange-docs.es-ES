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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763026"
---
# <a name="get-started-with-ews-managed-api-client-applications"></a>Empezar a trabajar con aplicaciones de cliente de la API administrada de EWS

Este documento puede incluir contenido relacionado con funciones o productos preliminares que pueden cambiar mucho antes del lanzamiento comercial final. Este documento se proporciona "tal cual" solamente con fines informativos y Microsoft no realiza ninguna garantía, explícita ni implícita, en el documento. Desarrolle una sencilla aplicación cliente de correo electrónico Hola a todos para Exchange mediante la API administrada EWS. 
  
La [API administrada EWS](http://aka.ms/ews-managed-api-readme) proporciona un modelo de objetos intuitivo y fácil de usar para enviar y recibir mensajes de servicios web desde aplicaciones cliente, aplicaciones de portal y aplicaciones de servicio. Puede tener acceso a casi toda la información almacenada en un buzón de correo de Exchange Online, Exchange Online como parte de Office 365 o Exchange Server mediante la API administrada EWS. Puede usar la información de este artículo como ayuda para desarrollar su primera aplicación cliente de la API administrada EWS. 
  
> [!NOTE]
> [!NOTA]  La API administrada EWS ya está disponible como un proyecto de código abierto en [GitHub](https://github.com/officedev/ews-managed-api). Puede usar la biblioteca de código abierto para: >  Contribuir con correcciones de errores y mejoras a la API. >  Obtener correcciones y mejoras antes de que estén disponibles en una versión oficial. >  Tener acceso a una implementación más completa y actualizada de la API, para usarla como referencia o para crear nuevas bibliotecas en nuevas plataformas. >  Le agradecemos las [aportaciones](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) que realice a través de GitHub. 
  
## <a name="youll-need-an-exchange-server"></a>Necesitará un servidor de Exchange
<a name="NeedExchange"> </a>

Si ya tiene una cuenta de buzón de Exchange, puede omitir esta sección. En caso contrario, dispone de las opciones siguientes para configurar un buzón de Exchange para su primera aplicación cliente EWS:
  
- Obtener un [sitio para desarrolladores de Office 365](http://msdn.microsoft.com/en-us/library/office/fp179924.aspx) (recomendado). Esta es la forma más rápida de configurar un buzón de Exchange. 
    
- Descargar [Exchange Server](http://office.microsoft.com/en-us/exchange/microsoft-exchange-try-or-buy-exchange-we-can-help-you-decide-FX103746846.aspx?WT%2Eintid1=ODC%5FENUS%5FFX103472230%5FXT103965589).
    
Una vez que haya comprobado que puede enviar y recibir correo electrónico desde Exchange, estará listo para configurar el entorno de desarrollo. Puede usar [Outlook Web App](http://technet.microsoft.com/en-us/library/jj657718%28v=exchg.150%29.aspx) del cliente web de Exchange para comprobar que puede enviar correo electrónico. 
  
## <a name="set-up-your-development-environment"></a>Configurar el entorno de desarrollo
<a name="Setup"> </a>

Asegúrese de que tiene acceso a los siguientes elementos:
  
- Cualquier versión de [Visual Studio](http://www.visualstudio.com/en-us/downloads/download-visual-studio-vs.aspx) que sea compatible con .NET Framework 4. Aunque técnicamente no se necesita Visual Studio porque se puede usar cualquier compilador de C#, recomendamos que lo use. 
    
- La [API administrada EWS](http://aka.ms/ews-managed-api-readme). Puede usar la versión de 64 o 32 bits, en función de su sistema. Use la ubicación de instalación predeterminada. 
    
## <a name="create-your-first-ews-managed-api-application"></a>Crear la primera aplicación de API administrada EWS
<a name="Create"> </a>

En estos pasos se da por supuesto que ha configurado un sitio para desarrolladores de Office 365. Si ha descargado e instalado Exchange, deberá [instalar un certificado válido](http://technet.microsoft.com/en-us/library/bb310769%28v=exchg.141%29.aspx) en el servidor de Exchange o [implementar una devolución de llamada de validación de certificado](how-to-validate-a-server-certificate-for-the-ews-managed-api.md) para un certificado autofirmado proporcionado de forma predeterminada. Tenga en cuenta también que estos pasos pueden variar ligeramente según la versión de Visual Studio que use. 
  
### <a name="step-1-create-a-project-in-visual-studio"></a>Paso 1: crear un proyecto en Visual Studio

1. En Visual Studio, en el menú **Archivo**, seleccione **Nuevo** y después elija **Proyecto**. Se abre el cuadro de diálogo **Nuevo proyecto**. 
    
2. Cree una **aplicación de consola de C#**. En el panel **Plantillas**, elija **Visual C#** y luego **Aplicación de consola**. 
    
3. Indique HelloWorld como nombre del proyecto y después elija **Aceptar**.
    
Visual Studio crea el proyecto y abre la ventana de documento de código Program.cs.

### <a name="step-2-add-a-reference-to-the-ews-managed-api"></a>Paso 2: agregar una referencia a la API administrada EWS

1. Si la ventana **Explorador de soluciones** ya está abierta, omita este paso y vaya al paso 2. Para abrir la ventana **Explorador de soluciones**, en el menú **Vista**, elija **Explorador de soluciones**. 
    
2. En el **Explorador de soluciones** y en el proyecto **HelloWorld**, abra el menú contextual (botón derecho) de **Referencias** y elija **Agregar referencia** en el menú contextual. Se abrirá un cuadro de diálogo para administrar las referencias del proyecto. 
    
3. Elija la opción **Examinar**. Vaya a la ubicación donde instaló el archivo DLL de la API administrada EWS. La ruta de acceso predeterminada que establece el programa de instalación es la siguiente: C:\Archivos de programa\Microsoft\Exchange\Web Services\<versión>\. La ruta de acceso puede variar en función de si descarga la versión de 32 o de 64 bits del archivo Microsoft.Exchange.WebServices.dll. Elija **Microsoft.Exchange.WebServices.dll** y seleccione **Aceptar** o **Agregar**. Esto agrega la referencia de la API administrada EWS a su proyecto. 
    
4. Si usa la API administrada 2.0 EWS, cambie el destino del proyecto HelloWorld a .NET Framework 4. Otras versiones de la API administrada EWS podrían usar una versión de destino diferente de .NET Framework.
    
5. Confirme que usa la versión de destino correcta de .NET Framework. Abra el menú contextual (botón derecho) del proyecto **HelloWorld** en el **Explorador de soluciones** y elija **Propiedades**. Compruebe que está seleccionado **.NET Framework 4** en el cuadro desplegable **Versión de .NET Framework de destino**. 
    
Ahora que ha configurado el proyecto y que ha creado una referencia a la API administrada EWS, está listo para crear su primera aplicación. Para simplificar las cosas, agregue el código al archivo Program.cs. Leer la [referencia del ensamblado de la API administrada de EWS](how-to-reference-the-ews-managed-api-assembly.md) para obtener más información acerca de cómo hacer referencia a la API administrada de EWS. En el paso siguiente, desarrollará el código básico para escribir la mayoría de las aplicaciones cliente de la API administrada EWS. 
### <a name="step-3-set-up-url-redirection-validation-for-autodiscover"></a>Paso 3: configurar la validación del redireccionamiento de la dirección URL para la Detección automática

- Agregue el siguiente método de devolución de llamada para la validación del redireccionamiento después del método **Main(string[] args)**. Esto valida si las direcciones URL redirigidas que devuelve la [Detección automática](autodiscover-for-exchange.md) representan un extremo HTTPS. 
    
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

Esta devolución de llamada de validación se pasará al objeto **ExchangeService** en el paso 4. Esto es necesario para que la aplicación confíe y siga los redireccionamientos de la Detección automática, ya que los resultados del redireccionamiento de la Detección automática proporcionan el extremo EWS para nuestra aplicación. 

### <a name="step-4-prepare-the-exchangeservice-object"></a>Paso 4: preparar el objeto ExchangeService

1. Agregue una referencia de directiva **using** a la API administrada EWS. Agregue el código siguiente después de la última directiva **using** en la parte superior de Program.cs. 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

2. En el método **Main**, cree una instancia del objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) con la versión del servicio que quiere tener como destino. En este ejemplo el destino es la versión más antigua del esquema EWS. 
    
   ```cs
    ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2007_SP1);
   ```

3. Si tiene como destino un servidor de Exchange local y el cliente está unido al dominio, vaya al paso 4. Si el cliente tiene como destino un buzón del sitio para desarrolladores de Exchange Online u Office 365, deberá pasar credenciales explícitas. Agregue el código siguiente después de crear instancias del objeto **ExchangeService** y establezca las credenciales de su cuenta de buzón. El nombre de usuario debe ser el nombre principal del usuario. Vaya al paso 5. 
    
   ```cs
    service.Credentials = new WebCredentials("user1@contoso.com", "password");
   ```

4. Los clientes unidos al dominio que tengan como destino un servidor de Exchange local pueden usar las credenciales predeterminadas del usuario que haya iniciado sesión, siempre y cuando dichas credenciales estén asociadas con un buzón. Agregue el código siguiente después de crear instancias del objeto **ExchangeService**. 
    
   ```cs
    service.UseDefaultCredentials = true;
   ```

   Si el cliente tiene como destino un buzón del sitio para desarrolladores de Exchange Online u Office 365, compruebe que [UseDefaultCredentials](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.usedefaultcredentials%28v=exchg.80%29.aspx) esté establecido en **false**, que es el valor predeterminado. El cliente está listo para realizar la primera llamada al servicio Detección automática para obtener la dirección URL del servicio para realizar llamadas al servicio EWS.
    
5. El método **AutodiscoverUrl** del objeto **ExchangeService** realiza una serie de llamadas al servicio Detección automática para obtener la dirección URL del servicio. Si esta llamada de método se realiza correctamente, la propiedad URL del objeto **ExchangeService** se establecerá con la dirección URL del servicio. Pase la dirección de correo electrónico del usuario y el objeto **RedirectionUrlValidationCallback** al método **AutodiscoverUrl**. Agregue el código siguiente después de especificar las credenciales en el paso 3 o 4. Cambie  `user1@contoso.com` a su dirección de correo electrónico de modo que el servicio Detección automática encuentre su extremo EWS. 
    
   ```cs
    service.AutodiscoverUrl("user1@contoso.com", RedirectionUrlValidationCallback);
   ```

En este momento, el cliente está configurado para hacer llamadas a EWS para tener acceso a los datos del buzón. Si ejecuta ahora el código, comprobará que la llamada de método **AutodiscoverUrl** funcionó si examina el contenido de la propiedad [ExchangeService.Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx). Si esta propiedad contiene una dirección URL, la llamada se ha realizado correctamente. Esto significa que la aplicación se autenticó correctamente con el servicio y que detectó el extremo EWS de su buzón. Ahora ya puede realizar las primeras llamadas a EWS. Para obtener más información acerca de cómo establecer la dirección URL de EWS, lea [establecer la dirección URL de servicio EWS mediante el uso de la API administrada de EWS](how-to-set-the-ews-service-url-by-using-the-ews-managed-api.md) . 

### <a name="step-6-create-your-first-hello-world-email-message"></a>Paso 6: crear el primer mensaje de correo electrónico de Hola a todos

1. Después de la llamada de método **AutodiscoverUrl**, cree una instancia de un nuevo objeto **EmailMessage** y pase el objeto de servicio que ha creado. 
    
   ```cs
    EmailMessage email = new EmailMessage(service);
   ```

   Ahora tiene un mensaje de correo electrónico en el que se ha establecido el enlace al servicio. Todas las llamadas iniciadas en el objeto **EmailMessage** tendrán el servicio como destino. 
    
2. Ahora establezca el destinatario de la línea Para: del mensaje de correo electrónico. Para ello, cambie  `user1@contoso.com` y use su dirección SMTP. 
    
   ```cs
    email.ToRecipients.Add("user1@contoso.com");
   ```

3. Establezca el asunto y el cuerpo del mensaje de correo electrónico.
    
   ```cs
    email.Subject = "HelloWorld";
    email.Body = new MessageBody("This is the first email I've sent by using the EWS Managed API.");
   ```

4. Ya está listo para enviar su primer mensaje de correo electrónico mediante la API administrada EWS. El método **Send** llamará al servicio y enviará el mensaje de correo electrónico para su entrega. Lea [comuníquese con EWS mediante el uso de la API administrada de EWS](how-to-communicate-with-ews-by-using-the-ews-managed-api.md) para obtener más información acerca de otros métodos que puede utilizar para comunicarse con Exchange. 
    
   ```cs
    email.Send();
   ```

5. Ya puede ejecutar la aplicación Hola a todos. En Visual Studio, seleccione **F5**. Se abrirá una ventana de consola en blanco. No verá nada en la ventana de consola mientras la aplicación se autentique, siga los redireccionamientos de Detección automática y realice su primera llamada para crear un mensaje de correo electrónico que usted se enviará a sí mismo. Si quiere ver las llamadas que se realizan, agregue las dos líneas de código siguientes antes de llamar al método **AutodiscoverUrl**. Después, presione F5. De este modo, se realizará un [seguimiento de las solicitudes y respuestas de EWS](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md) en la ventana de consola. 
    
   ```cs
    service.TraceEnabled = true;
    service.TraceFlags = TraceFlags.All;
   ```

Ahora ya tiene una aplicación cliente activa de la API administrada EWS. Para su comodidad, en el ejemplo siguiente se muestra todo el código que agregó en Program.cs para crear la aplicación Hola a todos.

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

## <a name="next-steps"></a>Pasos siguientes
<a name="Next"> </a>

Si quiere ir más allá con su primera aplicación cliente de la API administrada EWS, explore los siguientes recursos:
  
- [Exchange 2013: 101 code samples (Exchange 2013: 101 ejemplos de código)](http://code.msdn.microsoft.com/exchange/Exchange-2013-101-Code-3c38582c)
    
- [Carpetas y elementos](folders-and-items-in-ews-in-exchange.md)
    
- [EWSEditor](http://ewseditor.codeplex.com/)
    
Si surge algún problema con la aplicación [envíe una pregunta o un comentario al foro](http://social.technet.microsoft.com/Forums/exchange/en-US/home?forum=exchangesvrdevelopment) (y no olvide leer la publicación de más arriba). 
  
## <a name="in-this-section"></a>En esta sección
<a name="Next"> </a>

- [Hacer referencia al ensamblado de la API administrada de EWS](how-to-reference-the-ews-managed-api-assembly.md)
    
- [Establecer la dirección URL de servicio EWS mediante el uso de la API administrada de EWS](how-to-set-the-ews-service-url-by-using-the-ews-managed-api.md)
    
- [Comunicarse con EWS mediante el uso de la API administrada de EWS](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    
## <a name="see-also"></a>Ver también

- [Empezar a utilizar servicios web de Exchange](start-using-web-services-in-exchange.md)    
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)    
- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)   
- [Seguimiento de las solicitudes y respuestas para solucionar problemas de aplicaciones de la API administrada de EWS](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
    

