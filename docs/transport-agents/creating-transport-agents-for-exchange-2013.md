---
title: Crear agentes de transporte para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d291ab78-7cdd-4dbe-a5f4-9dc8e9650a33
description: Busque información sobre cómo crear agentes de transporte personalizados para Exchange 2013 y los requisitos del sistema para crear un agente personalizado.
ms.openlocfilehash: cb1cd180817524fe29a100a48d90444c75a77510
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462377"
---
# <a name="creating-transport-agents-for-exchange-2013"></a>Crear agentes de transporte para Exchange 2013

Busque información sobre cómo crear agentes de transporte personalizados para Exchange 2013 y los requisitos del sistema para crear un agente personalizado.
  
**Se aplica a:** Exchange Server 2013
  
Exchange Server 2013 incluye varios agentes de transporte que puede usar para procesar mensajes. Mediante el uso de los ensamblados que se incluyen con Exchange, puede crear sus propios agentes personalizados para realizar tareas específicas de acuerdo con las necesidades de su organización. Por ejemplo, puede usar un agente de transporte SmtpReceiveAgent para interceptar los mensajes recibidos a través del protocolo SMTP y procesar el mensaje para convertir el formato del cuerpo para que contenga texto con formato previo. Puede usar un agente de transporte RoutingAgent para registrar los mensajes que pasan a través del servidor en la ruta a otro servidor. También puede crear características más complejas que hagan uso de más de un tipo de agente. Por ejemplo, para crear un agente antivirus, puede implementar un SmtpReceiveAgent y un agente de RoutingAgent. Si tiene un componente en la red que no es compatible con el protocolo SMTP, puede usar un agente de transporte DeliveryAgent para controlar la comunicación entre el servidor Exchange y el componente externo. 
  
En este artículo se proporciona información acerca de los requisitos previos de y las tareas necesarias para crear su propio agente de transporte. Para obtener información acerca de la creación de agentes de transporte específicos, consulte [Create a RoutingAgent Transport Agent for exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md), [Create a SmtpReceiveAgent transport agent for Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md), and [Create a DeliveryAgent Transport Agent for Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md).
  
## <a name="prerequisites-for-creating-a-transport-agent"></a>Requisitos previos para crear un agente de transporte
<a name="bk_prerequisites"> </a>

Los siguientes son los requisitos previos que necesita para implementar un agente de transporte:
  
- Un equipo que ejecuta Exchange 2013 que ejecuta el servicio de transporte front-end en un servidor de transporte perimetral o de acceso de cliente, o el servicio de transporte en un servidor de buzones de correo. Para obtener información acerca de la arquitectura de los roles de servidor en Exchange 2013, consulte [conceptos de agentes de transporte en exchange 2013](transport-agent-concepts-in-exchange-2013.md).
    
- Los siguientes ensamblados para las clases de agente de transporte:
    
  - Microsoft. Exchange. Data. dll
    
  - Microsoft. Exchange. Data. Common. dll
    
  - Microsoft. Exchange. Transport. dll
    
- .NET Framework 4,5
    
También le recomendamos que instale Visual Studio 2012. Puede implementar agentes de transporte mediante Visual Basic .NET o C#.
  
## <a name="referencing-the-assemblies"></a>Referencia a los ensamblados
<a name="bk_ReferenceAssemblies"> </a>

Exchange 2013 proporciona una biblioteca de clases que admiten la extensión del comportamiento de transporte de Exchange. Estas clases requieren .NET Framework 4,5. Puede implementar agentes de transporte basados en estas clases con Visual Studio 2012.
  
El instalador de Exchange 2013 instala ensamblados que se usan para el desarrollo de agentes de transporte y los registra en la memoria caché global de ensamblados (GAC). Para empezar a implementar un agente de transporte, cree una referencia al ensamblado Microsoft. Exchange. Data. Transport en un proyecto de biblioteca de clases.
  
## <a name="implementing-a-transport-agent"></a>Implementación de un agente de transporte
<a name="bk_implementationExample"> </a>

En el ejemplo siguiente se muestra una implementación mínima de clases que derivan de las clases [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) y [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) . 
  
> [!CAUTION]
> Si hay varios agentes de transporte instalados y registrados para el mismo evento, se invocará a todos los agentes, incluso si un agente quita todos los destinatarios de un elemento de correo. > para evitar errores no controlados o un comportamiento impredecible, el agente de transporte debe controlar los casos en los que el recuento de destinatarios de un elemento de correo es igual a cero. 
  
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

## <a name="installing-and-enabling-an-agent"></a>Instalación y habilitación de un agente
<a name="bk_InstallEnable"> </a>

Después de compilar el agente en una DLL, debe instalar y habilitar el agente en su servidor de desarrollo de Exchange. En el shell de administración de Exchange, use el cmdlet [install-transportagent](https://technet.microsoft.com/library/aa997998.aspx) para instalar el agente y el cmdlet [enable-transportagent](https://technet.microsoft.com/library/bb124921.aspx) para habilitar el agente. Para obtener información acerca de cómo usar el shell de administración de Exchange, vea [Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps).
  
> [!CAUTION]
> Los agentes de transporte tienen acceso completo a todos los mensajes de correo electrónico que encuentran. Exchange 2013 no restringe el comportamiento de un agente de transporte. Los agentes de transporte que son inestables o que contienen errores de seguridad pueden afectar a la estabilidad y seguridad de Exchange 2013. Por lo tanto, solo debe instalar los agentes de transporte en los que confíe plenamente y que se hayan probado completamente. 
  
Cuando usa el cmdlet **install-TransportAgent** para instalar un agente, el shell de administración de Exchange mantiene un bloqueo en el ensamblado. Para liberar el bloqueo en el ensamblado, debe cerrar la instancia del shell de administración de Exchange que usó para instalar el agente. No podrá actualizar el ensamblado hasta que libere el bloqueo. 
  
En el ejemplo siguiente se muestra cómo usar el shell de administración de Exchange para instalar y habilitar un agente denominado mi agente mediante una clase derivada de [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) denominados alagents. MyAgentFactory. 
  
 `Install-TransportAgent -Name "MyCustomAgent" -TransportAgentFactory "MyAgents.MyAgentFactory" -AssemblyPath "C:\myagents\MyAgent.dll"`
  
En este ejemplo se asigna un nombre al agente MyCustomAgent en el servidor en el que está instalado el agente. En el siguiente ejemplo, se muestra cómo habilitar el agente denominado MyCustomAgent.
  
 `Enable-TransportAgent -Name "MyCustomAgent"`
  
Para administrar un agente de transporte en el servicio de transporte front-end en un servidor de acceso de cliente, agregue el siguiente valor al comando: `-TransportService FrontEnd` . Por ejemplo, para ver los agentes de transporte en el servicio de transporte front-end, ejecute el siguiente comando.
  
 `Get-TransportAgent -TransportService FrontEnd`
  
Para obtener más información acerca de la instalación, habilitación y administración del agente, consulte [Manage Transport Agents](https://technet.microsoft.com/library/bb125175%28v=exchg.150%29.aspx).
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_inthissection"> </a>

- [Crear un agente de transporte de RoutingAgent para Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)
    
- [Crear un agente de transporte de SmtpReceiveAgent para Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)
    
- [Crear un agente de transporte de DeliveryAgent para Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
    
## <a name="see-also"></a>Vea también

- [Conceptos del agente de transporte en Exchange 2013](transport-agent-concepts-in-exchange-2013.md)   
- [Referencia del agente de transporte para Exchange 2013](transport-agent-reference-for-exchange-2013.md)
    

