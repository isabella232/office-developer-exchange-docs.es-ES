---
title: Creación de los agentes de transporte de Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d291ab78-7cdd-4dbe-a5f4-9dc8e9650a33
description: Obtenga información sobre cómo crear agentes de transporte personalizados para Exchange 2013 y los requisitos del sistema para la creación de un agente personalizado.
ms.openlocfilehash: 6146e37c44441bed1d30d08f71ede255dba26440
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763351"
---
# <a name="creating-transport-agents-for-exchange-2013"></a>Creación de los agentes de transporte de Exchange 2013

Obtenga información sobre cómo crear agentes de transporte personalizados para Exchange 2013 y los requisitos del sistema para la creación de un agente personalizado.
  
**Se aplica a:** Exchange Server 2013
  
Exchange Server 2013 incluye a varios agentes de transporte que pueden utilizar para procesar los mensajes. Mediante el uso de los ensamblados que se incluyen con Exchange, puede crear sus propios agentes personalizados para realizar tareas específicas de acuerdo con las necesidades de su organización. Por ejemplo, puede usar a un agente de transporte SmtpReceiveAgent para interceptar los mensajes que se reciben mediante el protocolo SMTP y procesar el mensaje para convertir el formato del cuerpo para contener texto con formato previo. Puede usar a un agente de transporte RoutingAgent para registrar los mensajes que pasan a través del servidor en la ruta a otro servidor. También puede crear más complejas características que hacen uso de más de un tipo de agente. Por ejemplo, para crear a un agente antivirus, puede implementar un SmtpReceiveAgent y un agente de RoutingAgent. Si tiene un componente de la red que no es compatible con el protocolo SMTP, puede usar a un agente de transporte DeliveryAgent para controlar la comunicación entre el servidor de Exchange y su componente externo. 
  
En este artículo se proporciona información acerca de los requisitos previos para y las tareas que intervienen en la creación de su propio agente de transporte. Para obtener información acerca de cómo crear agentes de transporte específica, vea [crear un agente de transporte RoutingAgent para Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md), [crear un agente de transporte SmtpReceiveAgent para Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)y [crear un agente de transporte DeliveryAgent para Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md).
  
## <a name="prerequisites-for-creating-a-transport-agent"></a>Requisitos previos para crear a un agente de transporte
<a name="bk_prerequisites"> </a>

Los siguientes son los requisitos previos que necesita para implementar a un agente de transporte:
  
- Un equipo que ejecuta Exchange 2013 que se ejecuta el servicio de transporte Front-End en un servidor acceso de cliente o de transporte perimetral, o el servicio de transporte en un servidor de buzón de correo. Para obtener información acerca de la arquitectura de rol de servidor en Exchange 2013, vea [de transporte conceptos de agente de Exchange 2013](transport-agent-concepts-in-exchange-2013.md).
    
- Los siguientes ensamblados para las clases de agente de transporte:
    
  - Microsoft.Exchange.Data.dll
    
  - Microsoft.Exchange.Data.Common.dll
    
  - Microsoft.Exchange.Transport.dll
    
- .NET Framework 4.5
    
También se recomienda que instale Visual Studio 2012. Agentes de transporte se pueden implementar mediante el uso de Visual Basic .NET o C#.
  
## <a name="referencing-the-assemblies"></a>Hacer referencia a los ensamblados
<a name="bk_ReferenceAssemblies"> </a>

Exchange 2013 proporciona una biblioteca de clases que admiten la extensión de comportamiento de transporte de Exchange. Estas clases requieren .NET Framework 4.5. Puede implementar a los agentes de transporte en función de estas clases mediante el uso de Visual Studio 2012.
  
El programa de instalación de Exchange 2013 instala los ensamblados que se usan para el desarrollo de agente de transporte y los registra en la memoria caché de ensamblados global (GAC). Para empezar a implementar a un agente de transporte, cree una referencia al ensamblado Microsoft.Exchange.Data.Transport en un proyecto de biblioteca de clases.
  
## <a name="implementing-a-transport-agent"></a>Implementación de un agente de transporte
<a name="bk_implementationExample"> </a>

En el ejemplo siguiente se muestra una implementación mínima de clases que se derivan de las clases [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) y [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) . 
  
> [!CAUTION]
> Si varios agentes de transporte se ha instalado y registrados para el mismo evento, todos los agentes se invocará, incluso si un agente quita a todos los destinatarios de un elemento de correo. > Para evitar errores no controlados o un comportamiento inesperado, el agente de transporte debe administrar los casos en que el recuento de destinatarios en un elemento de correo es igual a cero. 
  
```cs
using System;
using System.Collections.Generic;
using System.Text;
using Microsoft.Exchange.Data.Transport;
using Microsoft.Exchange.Data.Transport.Smtp;
namespace MyAgents
{
    public sealed class MyAgentFactory : SmtpReceiveAgentFactory
    {
        public override SmtpReceiveAgent CreateAgent(SmtpServer server)
        {
            return new MyAgent();
        }
    }
    public class MyAgent : SmtpReceiveAgent
    {
        public MyAgent()
        {
            this.OnEndOfData += new EndOfDataEventHandler(MyEndOfDataHandler);
        }
        private void MyEndOfDataHandler (ReceiveMessageEventSource source, EndOfDataEventArgs e)
        {
            // The following line appends text to the subject of the message that caused the event.
            e.MailItem.Message.Subject += " - this text appended by MyAgent";
        }
    }
}
```

```vb
Imports System
Imports System.Collections.Generic
Imports System.Text
Imports Microsoft.Exchange.Data.Transport
Imports Microsoft.Exchange.Data.Transport.Smtp
Namespace MyAgents
    NotInheritable Class MyAgentFactory
        Inherits SmtpReceiveAgentFactory
        Public Overrides Function CreateAgent(ByVal server as SmtpServer) As SmtpReceiveAgent
            Return New MyAgent
        End Function
    End Class
    Public Class MyAgent
        Inherits SmtpReceiveAgent
        Private Sub MyEndOfDataHandler(ByVal source As ReceiveMessageEventSource, ByVal e As EndOfDataEventArgs) Handles Me.OnEndOfData
            ' The following line appends text to the subject of the message that caused the event.
            e.MailItem.Message.Subject &amp;= e.MailItem.Message.Subject + " - this text appended by MyAgent"
        End Sub
    End Class
End Namespace
```

## <a name="installing-and-enabling-an-agent"></a>Instalar y habilitar un agente
<a name="bk_InstallEnable"> </a>

Después de compilar al agente a un archivo DLL, debe instalar y habilitar al agente de en el servidor de desarrollo de Exchange. En el Shell de administración de Exchange, use el cmdlet [Install-TransportAgent](http://technet.microsoft.com/en-us/library/aa997998.aspx) para instalar al agente y el cmdlet [Enable-TransportAgent](http://technet.microsoft.com/en-us/library/bb124921.aspx) para habilitar al agente. Para obtener información acerca de cómo usar el Shell de administración de Exchange, consulte [Exchange Server PowerShell (Shell de administración de Exchange)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps).
  
> [!CAUTION]
> Los agentes de transporte tienen acceso total a todos los mensajes de correo electrónico que se encuentren. Exchange 2013 no restringir el comportamiento de un agente de transporte. Los agentes de transporte que se inestable o que contienen errores de seguridad pueden afectar a la estabilidad y la seguridad de Exchange 2013. Por lo tanto, sólo debe instalar a los agentes de transporte que plena confianza y que se han probado completamente. 
  
Cuando use el cmdlet **Install-TransportAgent** para instalar a un agente, el Shell de administración de Exchange mantiene un bloqueo en el ensamblado. Para liberar el bloqueo en el ensamblado, debe cerrar la sesión de la consola de administración de Exchange que usó para instalar al agente. Podrá actualizar el ensamblado hasta que se libere el bloqueo. 
  
En el ejemplo siguiente se muestra cómo usar el Shell de administración de Exchange para instalar y habilitar a un agente denominado MyAgent mediante el uso de una clase derivada de [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) denominado MyAgents.MyAgentFactory. 
  
 `Install-TransportAgent -Name "MyCustomAgent" -TransportAgentFactory "MyAgents.MyAgentFactory" -AssemblyPath "C:\myagents\MyAgent.dll"`
  
En este ejemplo se da nombre al agente MyCustomAgent en el servidor en el que está instalado el agente. En el ejemplo siguiente se muestra cómo habilitar al agente denominado MyCustomAgent.
  
 `Enable-TransportAgent -Name "MyCustomAgent"`
  
Para administrar un agente de transporte en el servicio de transporte Front-End en un servidor de acceso de cliente, agregue el siguiente valor para el comando: `-TransportService FrontEnd`. Por ejemplo, para ver a los agentes de transporte en el servicio de transporte Front-End, ejecute el siguiente comando.
  
 `Get-TransportAgent -TransportService FrontEnd`
  
Para obtener más información acerca de cómo instalar, habilitar y administrar a su agente, vea [Administrar agentes de transporte](http://technet.microsoft.com/en-us/library/bb125175%28v=exchg.150%29.aspx).
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_inthissection"> </a>

- [Crear a un agente de transporte RoutingAgent para Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)
    
- [Crear a un agente de transporte SmtpReceiveAgent para Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)
    
- [Crear a un agente de transporte DeliveryAgent para Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
    
## <a name="see-also"></a>Vea también

- [Conceptos de agente en Exchange 2013 de transporte](transport-agent-concepts-in-exchange-2013.md)   
- [Referencia de agente de transporte de Exchange 2013](transport-agent-reference-for-exchange-2013.md)
    

