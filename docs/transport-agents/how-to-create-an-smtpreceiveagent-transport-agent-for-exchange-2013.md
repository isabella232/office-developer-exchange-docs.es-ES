---
title: Crear a un agente de transporte SmtpReceiveAgent para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cdc7c462-74a7-49d6-95b2-155d783840e9
description: Encuentre información acerca de cómo crear un agente de transporte SmtpReceiveAgent personalizado para usar con Exchange 2013.
ms.openlocfilehash: a74d5baae6334c5e17acb6335206964b48f320e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763473"
---
# <a name="create-an-smtpreceiveagent-transport-agent-for-exchange-2013"></a>Crear a un agente de transporte SmtpReceiveAgent para Exchange 2013

Encuentre información acerca de cómo crear un agente de transporte SmtpReceiveAgent personalizado para usar con Exchange 2013.
  
**Se aplica a:** Exchange Server 2013
  
Aplicaciones de ejemplo y fragmentos de código relacionados:

- [Exchange 2013: Crear a un agente de transporte de conversión de cuerpo](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0)
  
Las clases [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) y [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) permiten ampliar el comportamiento del servicio de transporte Front-End en un servidor de acceso de cliente o el servicio de transporte en un servidor de buzón de correo. Puede utilizar estas clases para implementar a los agentes de transporte que están diseñados para responder a los mensajes según entran en la organización. 
  
Las clases [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) y [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) incluyen los eventos que aparecen en la siguiente tabla. 
  
**La tabla 1. Eventos de clase SmtpReceiveAgent**

|**Evento**|**Descripción**|
|:-----|:-----|
|[OnAuthCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnAuthCommand.aspx) <br/> |Se usa cuando el agente requiere información que sólo se proporciona en el comando **AUTH** de SMTP, como un agente que acepta o rechaza intenta entregar un mensaje en función del tipo de método de autenticación usado.  <br/> |
|[OnConnect](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnConnect.aspx) <br/> |Se utiliza cuando el agente requiere información que se proporciona únicamente cuando se abre una conexión a través de SMTP para el servicio de transporte Front-End, como un agente que lleva a cabo una acción basada en la dirección o el dominio del servidor SMTP remoto.  <br/> |
|[OnDataCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDataCommand.aspx) <br/> |Utilice este evento cuando el agente requiere información que se proporciona en el comando SMTP **datos** .  <br/> |
|[OnDisconnect](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDisconnect.aspx) <br/> |Se utiliza cuando el agente requiere información que está disponible en el momento de desconexión, como la fecha y hora actuales, con el fin de realizar los cálculos de tiempo.  <br/> |
|[OnEhloCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEhloCommand.aspx) <br/> |Se usa cuando el agente requiere información que se proporciona en el comando SMTP **EHLO** ; Por ejemplo, si el agente acepta o rechaza mensajes en función de la identidad proporcionada en el comando **EHLO** .  <br/> |
|[OnEndOfAuthentication](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfAuthentication.aspx) <br/> |Se usa cuando el agente requiere información que está disponible después de que el servidor remoto finaliza el proceso de autenticación; Por ejemplo, un agente que realiza una acción en un mensaje en función de la información de autenticación proporcionada por el servidor SMTP remoto o el cliente.  <br/> |
|[OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) <br/> |Se utiliza cuando el agente debe llevar a cabo una acción basándose en los datos que está disponibles en el mensaje. Este evento no se desencadenará en el servicio de transporte Front-End. Si el agente de transporte tiene que usar este evento, se debe instalar en un servidor de buzón de correo.  <br/> |
|[OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) <br/> |Se utiliza cuando el agente debe llevar a cabo una acción según la información que está disponible en los encabezados del mensaje enviado.  <br/> |
   
## <a name="creating-a-custom-smtpreceiveagent-transport-agent"></a>Creación de un agente de transporte SmtpReceiveAgent personalizado

El siguiente procedimiento describe cómo crear a un agente de transporte SmtpReceiveAgent personalizado. 
  
### <a name="to-create-the-transport-agent"></a>Para crear al agente de transporte

1. Agregue referencias a los espacios de nombres.
    
   ```cs
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Smtp;
      using Microsoft.Exchange.Data.Transport.Email;
      using Microsoft.Exchange.Data.TextConverters;
  
   ```

   Puede encontrar estos espacios de nombres en el servidor de Exchange 2013. Cuando se agrega una referencia a estos espacios de nombres, tendrá acceso a los miembros de [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) así como otras clases que se usan en el [Exchange 2013: crear un agente de transporte de conversión de cuerpo](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) ejemplo. 
    
2. Implementar la clase derivada de la clase [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) . 
    
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

   Este código se cree una instancia de la clase derivada y reemplace el método **CreateAgent** para crear una instancia de su nuevo agente personalizado. 
    
3. Definir al agente.
    
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

   Después de definir la clase del agente, puede agregar la funcionalidad personalizada. En este ejemplo, el evento [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) se redirige a su controlador de eventos personalizado. 
    
## <a name="see-also"></a>Vea también

- [Conceptos de agente en Exchange 2013 de transporte](transport-agent-concepts-in-exchange-2013.md)    
- [Referencia de agente de transporte de Exchange 2013](transport-agent-reference-for-exchange-2013.md)    
- [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)    
- [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
    

