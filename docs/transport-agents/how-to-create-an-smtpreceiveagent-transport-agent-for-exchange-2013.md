---
title: Crear un agente de transporte SmtpReceiveAgent para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: cdc7c462-74a7-49d6-95b2-155d783840e9
description: Descubra cómo crear un agente de transporte SmtpReceiveAgent personalizado para usarlo con Exchange 2013.
ms.openlocfilehash: a441f93113798c10421e9073e266c28fd87bca8d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513034"
---
# <a name="create-an-smtpreceiveagent-transport-agent-for-exchange-2013"></a>Crear un agente de transporte SmtpReceiveAgent para Exchange 2013

Descubra cómo crear un agente de transporte SmtpReceiveAgent personalizado para usarlo con Exchange 2013.
  
**Se aplica a:** Exchange Server 2013
  
Fragmentos de código relacionados y aplicaciones de ejemplo:

- [Exchange 2013: crear un agente de transporte de conversión de cuerpo](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0)
  
Las [clases SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) y [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) permiten ampliar el comportamiento del servicio de transporte front-end en un servidor de acceso de cliente o el servicio de transporte en un servidor de buzones de correo. Puede usar estas clases para implementar agentes de transporte diseñados para responder a los mensajes a medida que llegan a la organización. 
  
Las [clases SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) y [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) incluyen los eventos enumerados en la tabla siguiente. 
  
**Tabla 1. Eventos de clase SmtpReceiveAgent**

|**Event**|**Descripción**|
|:-----|:-----|
|[OnAuthCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnAuthCommand.aspx) <br/> |Se usa cuando el agente requiere información que solo se proporciona en el comando **SMTP AUTH,** como un agente que acepta o rechaza los intentos de entregar un mensaje en función del tipo de método de autenticación usado.  <br/> |
|[OnConnect](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnConnect.aspx) <br/> |Se usa cuando el agente requiere información que solo se proporciona cuando se abre una conexión mediante SMTP al servicio de transporte front-end, como un agente que realiza una acción basada en la dirección o el dominio del servidor SMTP remoto.  <br/> |
|[OnDataCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDataCommand.aspx) <br/> |Use este evento cuando el agente requiera información que se proporciona en el comando SMTP **DATA.**  <br/> |
|[OnDisconnect](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDisconnect.aspx) <br/> |Se usa cuando el agente requiere información disponible en el momento de la desconexión, como la fecha y hora actuales, para realizar cálculos de hora.  <br/> |
|[OnEhloCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEhloCommand.aspx) <br/> |Úsalo cuando el agente requiera información que se proporciona en el comando **SMTP EHLO;** por ejemplo, si el agente acepta o rechaza mensajes en función de la identidad proporcionada en el **comando EHLO.**  <br/> |
|[OnEndOfAuthentication](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfAuthentication.aspx) <br/> |Úse cuando el agente requiera información que esté disponible después de que el servidor remoto complete el proceso de autenticación; por ejemplo, para un agente que realiza una acción en un mensaje basándose en la información de autenticación proporcionada por el cliente o servidor SMTP remoto.  <br/> |
|[OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) <br/> |Se usa cuando el agente debe realizar una acción basada en los datos disponibles en el mensaje. Este evento no se disparará en el servicio de transporte front-end. Si el agente de transporte tiene que usar este evento, debe instalarlo en un servidor de buzones de correo.  <br/> |
|[OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) <br/> |Se usa cuando el agente debe realizar una acción en función de la información disponible en los encabezados del mensaje enviado.  <br/> |
   
## <a name="creating-a-custom-smtpreceiveagent-transport-agent"></a>Creación de un agente de transporte SmtpReceiveAgent personalizado

En el siguiente procedimiento se describe cómo crear un agente de transporte SmtpReceiveAgent personalizado. 
  
### <a name="to-create-the-transport-agent"></a>Para crear el agente de transporte

1. Agregue referencias a los espacios de nombres.
    
   ```cs
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Smtp;
      using Microsoft.Exchange.Data.Transport.Email;
      using Microsoft.Exchange.Data.TextConverters;
  
   ```

   Puede encontrar estos espacios de nombres en el servidor Exchange 2013. Al agregar una referencia a estos espacios de nombres, tendrá acceso a los miembros [smtpreceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) así como a otras clases usadas en el ejemplo de agente de transporte de conversión de cuerpo [de Exchange 2013:](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) Crear un agente de transporte de conversión de cuerpo. 
    
2. Implemente la clase derivada para la [clase SmtpReceiveAgentFactory.](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) 
    
   ```cs
      public class BodyConversionFactory : SmtpReceiveAgentFactory
      {
          /// <summary>
          /// Create a new BodyConversion
          /// </summary>
          /// <param name="server">Exchange server</param>
          /// <returns>A new BodyConversion</returns>
          public override SmtpReceiveAgent CreateAgent(SmtpServer server)
          {
              return new BodyConversion();
          }
      }
  
   ```

   Este código creará una instancia de la clase derivada e invalidará el **método CreateAgent** para crear una instancia del nuevo agente personalizado. 
    
3. Defina el agente.
    
   ```cs
     public class BodyConversion : SmtpReceiveAgent
      {
          // Your custom code goes here
          /// <summary>
          /// The constructor registers an end of data event handler.
          /// </summary>
          public BodyConversion()
          {
              Debug.WriteLine("[BodyConversion] Agent constructor");
              this.OnEndOfData += new EndOfDataEventHandler(this.OnEndOfDataHandler);
          }
      }
  
   ```

   Después de definir la clase de agente, puede agregar la funcionalidad personalizada. En este ejemplo, el [evento OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) se redirige al controlador de eventos personalizado. 
    
## <a name="see-also"></a>Ver también

- [Conceptos de agente de transporte Exchange 2013](transport-agent-concepts-in-exchange-2013.md)    
- [Referencia de agente de transporte para Exchange 2013](transport-agent-reference-for-exchange-2013.md)    
- [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)    
- [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
    

