---
title: Crear un agente de transporte de SmtpReceiveAgent para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cdc7c462-74a7-49d6-95b2-155d783840e9
description: Descubra cómo crear un agente de transporte de SmtpReceiveAgent personalizado para usarlo con Exchange 2013.
ms.openlocfilehash: 5ba021d02849ffc7e125029f0fd18ebf14c3f8da
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459142"
---
# <a name="create-an-smtpreceiveagent-transport-agent-for-exchange-2013"></a>Crear un agente de transporte de SmtpReceiveAgent para Exchange 2013

Descubra cómo crear un agente de transporte de SmtpReceiveAgent personalizado para usarlo con Exchange 2013.
  
**Se aplica a:** Exchange Server 2013
  
Fragmentos de código y aplicaciones de ejemplo relacionados:

- [Exchange 2013: crear un agente de transporte de conversión de cuerpo](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0)
  
Las clases [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) y [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) permiten ampliar el comportamiento del servicio de transporte front-end en un servidor de acceso de cliente o el servicio de transporte en un servidor de buzones de correo. Puede usar estas clases para implementar agentes de transporte diseñados para responder a los mensajes a medida que entran en la organización. 
  
Las clases [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) y [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) incluyen los eventos que se enumeran en la tabla siguiente. 
  
**Tabla 1. Eventos de la clase SmtpReceiveAgent**

|**Event**|**Descripción**|
|:-----|:-----|
|[OnAuthCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnAuthCommand.aspx) <br/> |Se usa cuando el agente requiere información que se proporciona únicamente en el comando **auth** de SMTP, como un agente que acepta o rechaza los intentos de entregar un mensaje en función del tipo de método de autenticación usado.  <br/> |
|[OnConnect](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnConnect.aspx) <br/> |Se usa cuando el agente requiere información que se proporciona únicamente cuando se abre una conexión a través de SMTP para el servicio de transporte front-end, como un agente que realiza una acción basada en la dirección o el dominio del servidor SMTP remoto.  <br/> |
|[OnDataCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDataCommand.aspx) <br/> |Use este evento cuando su agente requiera la información que se proporciona en el comando de **datos** SMTP.  <br/> |
|[OnDisconnect](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDisconnect.aspx) <br/> |Se usa cuando el agente requiere información que está disponible en el momento de la desconexión, como la fecha y la hora actuales, a fin de realizar cálculos de tiempo.  <br/> |
|[OnEhloCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEhloCommand.aspx) <br/> |Se usa cuando el agente requiere información que se proporciona en el comando SMTP **EHLO** ; por ejemplo, si el agente acepta o rechaza mensajes en función de la identidad proporcionada en el comando **EHLO** .  <br/> |
|[OnEndOfAuthentication](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfAuthentication.aspx) <br/> |Se usa cuando el agente requiere información que está disponible después de que el servidor remoto complete el proceso de autenticación; por ejemplo, para un agente que realiza una acción en un mensaje en función de la información de autenticación proporcionada por el servidor SMTP remoto o el cliente.  <br/> |
|[OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) <br/> |Se usa cuando el agente debe realizar una acción basándose en los datos que están disponibles en el mensaje. Este evento no se desencadenará en el servicio de transporte de front-end. Si el agente de transporte tiene que usar este evento, deberá instalarlo en un servidor de buzones de correo.  <br/> |
|[OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) <br/> |Se usa cuando el agente debe realizar una acción basándose en la información que está disponible en los encabezados del mensaje enviado.  <br/> |
   
## <a name="creating-a-custom-smtpreceiveagent-transport-agent"></a>Creación de un agente de transporte de SmtpReceiveAgent personalizado

El siguiente procedimiento describe cómo crear un agente de transporte de SmtpReceiveAgent personalizado. 
  
### <a name="to-create-the-transport-agent"></a>Para crear el agente de transporte

1. Agregue referencias a los espacios de nombres.
    
   ```cs
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Smtp;
      using Microsoft.Exchange.Data.Transport.Email;
      using Microsoft.Exchange.Data.TextConverters;
  
   ```

   Puede encontrar estos espacios de nombres en su servidor Exchange 2013. Al agregar una referencia a estos espacios de nombres, tendrá acceso a los miembros de [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) , así como a otras clases usadas en la muestra de [Exchange 2013: Build a Body Conversion Transport Agent](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) . 
    
2. Implemente la clase derivada para la clase [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) . 
    
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

   Este código creará una instancia de la clase derivada y reemplazará el método **CreateAgent** para crear una instancia del nuevo agente personalizado. 
    
3. Definir el agente.
    
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

   Después de definir la clase del agente, puede agregar su funcionalidad personalizada. En este ejemplo, el evento [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) se redirige a su controlador de eventos personalizado. 
    
## <a name="see-also"></a>Vea también

- [Conceptos del agente de transporte en Exchange 2013](transport-agent-concepts-in-exchange-2013.md)    
- [Referencia del agente de transporte para Exchange 2013](transport-agent-reference-for-exchange-2013.md)    
- [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)    
- [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
    

