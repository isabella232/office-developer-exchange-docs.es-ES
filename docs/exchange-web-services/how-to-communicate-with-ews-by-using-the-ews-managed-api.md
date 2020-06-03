---
title: Comunicarse con EWS mediante la API administrada de EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: d1b78293-da02-413a-875c-681e99146af3
description: Obtenga información sobre cómo usar la API administrada de EWS para comunicarse con EWS en Exchange.
localization_priority: Priority
ms.openlocfilehash: be807f2d936bf79d181476ec8eb12f20fca7950f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528247"
---
# <a name="communicate-with-ews-by-using-the-ews-managed-api"></a>Comunicarse con EWS mediante la API administrada de EWS

Obtenga información sobre cómo usar la API administrada de EWS para comunicarse con EWS en Exchange.
  
La clase [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) de la API administrada de EWS contiene los métodos y las propiedades que se usan para establecer las credenciales de usuario, identificar el extremo de EWS, enviar y recibir mensajes SOAP y configurar el enlace para comunicarse con EWS. Antes de poder usar la API administrada de EWS para realizar cualquier tarea, tiene que crear una instancia de la clase **ExchangeService** y enlazarla a EWS. 
  
Después de configurar un objeto [ExchangeService](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.aspx) con credenciales de usuario y el punto de conexión de EWS, cualquier objeto de buzón de correo que haga referencia al objeto [ExchangeService](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.aspx) puede usar los siguientes tipos de método para comunicarse con EWS: 
  
- Métodos del objeto ExchangeService: todos los métodos del objeto **ExchangeService** que no se heredan del tipo de **objeto** base realizan llamadas a EWS. 
    
- Los métodos de tipo de carpeta y elemento de buzón de Exchange.
    
**Tabla 1. Métodos de tipo de carpeta y elemento de buzón de correo que se comunican con EWS**

|Method|Lo que hace|Operaciones a las que llama|
|:-----|:-----|:-----|
|[Load](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.load%28v=exchg.80%29.aspx) <br/> |Obtiene las propiedades de un elemento, datos adjuntos o un objeto de configuración de usuario.  <br/> |[Operación GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/><br/> [Operación GetAttachment](https://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx) <br/><br/> [Operación GetUserConfiguration](https://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) <br/> |
|[BIND](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> |Rellena un nuevo elemento en el cliente con información de un elemento existente en el servidor.  <br/> |[Operación GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |
|[Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) <br/> |Guarda la copia del elemento de cliente en el servidor.  <br/> |[Operación UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/><br/> [Operación UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/><br/>[Operación CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/><br/>[Operación CreateFolder](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
|[Actualización](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> |Actualiza el servidor con los cambios realizados en el cliente.<br/><br/>Para elementos y carpetas, el método **Update** usa la [operación UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) y la [operación UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx).  <br/> |[Operación UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/><br/>[Operación UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|[Eliminar](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> |Elimina un elemento en el servidor.<br/><br/>Para elementos y carpetas, el método **Delete** usa la y la [operación DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx).  <br/> |[Operación DeleteItem](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/><br/> [Operación DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |
|[Copy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> |Crea una copia del elemento o carpetas en el servidor.  <br/> |[Operación CopyItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/><br/> [Operación CopyFolder](https://msdn.microsoft.com/library/c7ea0d68-9793-4144-b378-d99536776db9%28Office.15%29.aspx) <br/> |
|[Move](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> |Mueve elementos o carpetas en el servidor.  <br/> |[Operación MoveItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/><br/> [Operación MoveFolder](https://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <br/> |
   
## <a name="to-use-the-ews-managed-api-to-communicate-with-ews"></a>Para usar la API administrada de EWS para comunicarse con EWS

1. Cree una instancia de la clase **ExchangeService** . 
    
   ```csharp
    ExchangeService service = new ExchangeService();
   ```

   > [!NOTE]
   > Si se crea una instancia de **ExchangeService** con un constructor vacío, se creará una instancia enlazada a la versión más reciente conocida de Exchange. Como alternativa, puede dirigirse a una versión específica de Exchange especificando version como parámetro. `ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2007_SP1);`
  
2. Establezca las credenciales del usuario que envía solicitudes al servidor de Exchange. Si desea conectarse a EWS desde un equipo que ha iniciado sesión en el dominio, con las credenciales del usuario autenticado, establezca la propiedad **UseDefaultCredentials** del objeto **ExchangeService** en **true**.
    
   ```cs
    // Connect by using the default credentials of the authenticated user.
    service.UseDefaultCredentials = true;
   ```

   Si no desea conectarse con las credenciales de usuario predeterminadas, establezca la propiedad **Credentials** en el objeto **ExchangeService** para especificar explícitamente las credenciales de un usuario diferente. Si usa Exchange online o Exchange online como parte de Office 365, usará la autenticación básica, con solo un nombre de usuario y una contraseña. Se requiere un nombre de dominio para la autenticación NTLM. 
    
   ```cs
    // Connect by using the credentials of user1 at contoso.com.
    service.Credentials = new WebCredentials("user1@contoso.com", "password");
   ```

   También puede especificar las credenciales del usuario con el nombre de dominio y la contraseña del usuario.
    
   ```cs
    // Connect by using the credentials of contoso/user1.
    service.Credentials = new WebCredentials("user1", "password", "contoso");
   ```

   > [!NOTE]
   > Si la propiedad **UseDefaultCredentials** está establecida en **true**, se omite el valor de la propiedad **Credentials** . 
  
3. Establezca la dirección URL del extremo de EWS. Esta dirección URL busca el archivo. asmx de Exchange en el servidor de acceso de cliente.
    
   ```cs
    // Use Autodiscover to set the URL endpoint.
    service.AutodiscoverUrl("user1@contoso.com");
   ```

   > [!NOTE]
   >  Aunque se puede establecer explícitamente la propiedad **URL** de **ExchangeService** en un valor codificado, se recomienda usar el servicio de detección automática por los motivos siguientes: > detección automática determina el mejor punto de conexión para un usuario determinado (el extremo más cercano al servidor de buzones del usuario). > la dirección URL de EWS puede cambiar si se implementan nuevos servidores de acceso de cliente. En este escenario, el uso de la [detección automática](autodiscover-for-exchange.md) significa que no es necesario realizar cambios en el código. > debe establecer la dirección URL explícitamente o llamar a **AutodiscoverUrl**, pero no debe hacer ambas cosas. 
  
## <a name="see-also"></a>Vea también

- [Empezar a trabajar con aplicaciones de cliente de la API administrada de EWS](get-started-with-ews-managed-api-client-applications.md) 
- [Usar autodetección para buscar puntos de conexión](how-to-use-autodiscover-to-find-connection-points.md)   
- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    

