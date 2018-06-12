---
title: Comunicarse con EWS mediante el uso de la API administrada de EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d1b78293-da02-413a-875c-681e99146af3
description: Obtenga información acerca de cómo usar la API administrada de EWS para comunicarse con EWS en Exchange.
ms.openlocfilehash: 773fcc3f7e95d25effb5a686d4b79ec22610df8c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763053"
---
# <a name="communicate-with-ews-by-using-the-ews-managed-api"></a>Comunicarse con EWS mediante el uso de la API administrada de EWS

Obtenga información acerca de cómo usar la API administrada de EWS para comunicarse con EWS en Exchange.
  
La clase [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) en la API administrada de EWS contiene los métodos y propiedades que usan para establecer las credenciales de usuario, identifique el extremo EWS, enviar y recibir mensajes SOAP y configurar el enlace para comunicarse con EWS. Antes de que puede usar la API administrada de EWS para llevar a cabo cualquier tarea, se debe crear una instancia de la clase **ExchangeService** y enlazarla a EWS. 
  
Después de configurar un objeto [ExchangeService](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.aspx) con las credenciales de usuario y el extremo EWS, cualquier objeto de buzón de correo que hace referencia al objeto [ExchangeService](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.aspx) puede usar los siguientes tipos de método para comunicarse con EWS: 
  
- Métodos del objeto ExchangeService: todos los métodos en el objeto **ExchangeService** que no se heredan del tipo de **objeto** base realizan llamadas a EWS. 
    
- Elemento de buzón de correo de Exchange y carpeta escriba métodos.
    
**La tabla 1. Métodos que se comunican con EWS de tipo de elemento de buzón de correo y de carpeta**

|Método|Para qué sirve|Operaciones que se llama|
|:-----|:-----|:-----|
|[Load](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.load%28v=exchg.80%29.aspx) <br/> |Obtiene las propiedades en un objeto de configuración de usuario, datos adjuntos o elemento.  <br/> |[Operación GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/><br/> [Operación GetAttachment](http://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx) <br/><br/> [Operación GetUserConfiguration](http://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) <br/> |
|[Enlazar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> |Rellena un nuevo elemento en el cliente con información de un elemento existente en el servidor.  <br/> |[Operación GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |
|[Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) <br/> |Guarda la copia del elemento de cliente en el servidor.  <br/> |[Operación UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/><br/> [Operación UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/><br/>[Operación CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/><br/>[Operación CreateFolder](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
|[Actualizar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> |Actualiza el servidor con los cambios realizados en el cliente.<br/><br/>Para los elementos y carpetas, el método **Update** usa la [operación UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) y la [operación UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx).  <br/> |[Operación UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/><br/>[Operación UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|[Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> |Elimina un elemento en el servidor.<br/><br/>Para los elementos y carpetas, el método **Delete** usa la y la [operación DeleteFolder](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx).  <br/> |[Operación DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/><br/> [Operación DeleteFolder](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |
|[Copy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> |Crea una copia del elemento o las carpetas en el servidor.  <br/> |[Operación CopyItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/><br/> [Operación CopyFolder](http://msdn.microsoft.com/library/c7ea0d68-9793-4144-b378-d99536776db9%28Office.15%29.aspx) <br/> |
|[Mover](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> |Mueve elementos o carpetas en el servidor.  <br/> |[Operación MoveItem](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/><br/> [Operación MoveFolder](http://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <br/> |
   
## <a name="to-use-the-ews-managed-api-to-communicate-with-ews"></a>Para usar la API administrada de EWS para comunicarse con EWS

1. Crear una instancia de la clase **ExchangeService** . 
    
   ```csharp
    ExchangeService service = new ExchangeService();
   ```

   > [!NOTE]
   > Creación de instancias de **ExchangeService** con un constructor vacío, se creará una instancia que está enlazada a la última versión conocida de Exchange. Como alternativa, puede dirigir una versión específica de Exchange mediante la especificación de versión como un parámetro. `ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2007_SP1);`
  
2. Establecer las credenciales del usuario que envía las solicitudes al servidor de Exchange. Si desea conectarse a EWS desde un equipo que ha iniciado sesión en el dominio, con las credenciales del usuario autenticado, establezca la propiedad **UseDefaultCredentials** en el objeto **ExchangeService** en **true**.
    
   ```cs
    // Connect by using the default credentials of the authenticated user.
    service.UseDefaultCredentials = true;
   ```

   Si no desea conectarse mediante el uso de las credenciales del usuario de forma predeterminada, establezca la propiedad de **credenciales** en el objeto **ExchangeService** para especificar explícitamente las credenciales de un usuario diferente. Si usa Exchange Online o Exchange Online como parte de Office 365, que usará la autenticación básica, con sólo un nombre de usuario y una contraseña. Un nombre de dominio se requiere para la autenticación NTLM. 
    
   ```cs
    // Connect by using the credentials of user1 at contoso.com.
    service.Credentials = new WebCredentials("user1@contoso.com", "password");
   ```

   También puede especificar las credenciales del usuario mediante el uso de nombre de dominio del usuario y la contraseña.
    
   ```cs
    // Connect by using the credentials of contoso/user1.
    service.Credentials = new WebCredentials("user1", "password", "contoso");
   ```

   > [!NOTE]
   > Si se establece la propiedad **UseDefaultCredentials** en **true**, se omite el valor de la propiedad de **credenciales** . 
  
3. Establecer la dirección URL del extremo de EWS. Esta dirección URL localiza el archivo exchange.asmx en el servidor de acceso de cliente.
    
   ```cs
    // Use Autodiscover to set the URL endpoint.
    service.AutodiscoverUrl("user1@contoso.com");
   ```

   > [!NOTE]
   >  Aunque puede establecer explícitamente la propiedad **dirección Url** de la **ExchangeService** en un valor codificados de forma rígida, se recomienda usar el servicio Detección automática en su lugar, por los motivos siguientes: > detección automática determina el extremo de procedimientos para un usuario determinado (el extremo que más se aproxime al servidor de buzón de correo del usuario). > La dirección URL de EWS podría cambiar si se implementan nuevos servidores de acceso de cliente. En este escenario, el uso de [detección automática](autodiscover-for-exchange.md) significa que no hay ningún cambio de código es necesario. > Debe establecer explícitamente la dirección URL o llamar a **AutodiscoverUrl**, pero no debe hacer ambos. 
  
## <a name="see-also"></a>Ver también

- [Empezar a trabajar con aplicaciones de cliente de la API administrada de EWS](get-started-with-ews-managed-api-client-applications.md) 
- [Usar detección automática para buscar puntos de conexión](how-to-use-autodiscover-to-find-connection-points.md)   
- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    

