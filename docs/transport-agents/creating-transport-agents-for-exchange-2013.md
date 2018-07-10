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
# <a name="creating-transport-agents-for-exchange-2013"></a><span data-ttu-id="171e2-103">Creación de los agentes de transporte de Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="171e2-103">Creating transport agents for Exchange 2013</span></span>

<span data-ttu-id="171e2-104">Obtenga información sobre cómo crear agentes de transporte personalizados para Exchange 2013 y los requisitos del sistema para la creación de un agente personalizado.</span><span class="sxs-lookup"><span data-stu-id="171e2-104">Find information about how to create custom transport agents for Exchange 2013, and the system requirements for creating a custom agent.</span></span>
  
<span data-ttu-id="171e2-105">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="171e2-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="171e2-106">Exchange Server 2013 incluye a varios agentes de transporte que pueden utilizar para procesar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="171e2-106">Exchange Server 2013 includes several transport agents that you can use to process messages.</span></span> <span data-ttu-id="171e2-107">Mediante el uso de los ensamblados que se incluyen con Exchange, puede crear sus propios agentes personalizados para realizar tareas específicas de acuerdo con las necesidades de su organización.</span><span class="sxs-lookup"><span data-stu-id="171e2-107">By using the assemblies that come with Exchange, you can create your own custom agents to perform specific tasks according to the needs of your organization.</span></span> <span data-ttu-id="171e2-108">Por ejemplo, puede usar a un agente de transporte SmtpReceiveAgent para interceptar los mensajes que se reciben mediante el protocolo SMTP y procesar el mensaje para convertir el formato del cuerpo para contener texto con formato previo.</span><span class="sxs-lookup"><span data-stu-id="171e2-108">For example, you can use an SmtpReceiveAgent transport agent to intercept messages that are received via the SMTP protocol and process the message to convert the format of the body to contain preformatted text.</span></span> <span data-ttu-id="171e2-109">Puede usar a un agente de transporte RoutingAgent para registrar los mensajes que pasan a través del servidor en la ruta a otro servidor.</span><span class="sxs-lookup"><span data-stu-id="171e2-109">You can use a RoutingAgent transport agent to log the messages that pass through the server on route to another server.</span></span> <span data-ttu-id="171e2-110">También puede crear más complejas características que hacen uso de más de un tipo de agente.</span><span class="sxs-lookup"><span data-stu-id="171e2-110">You can also create more complex features that make use of more than one type of agent.</span></span> <span data-ttu-id="171e2-111">Por ejemplo, para crear a un agente antivirus, puede implementar un SmtpReceiveAgent y un agente de RoutingAgent.</span><span class="sxs-lookup"><span data-stu-id="171e2-111">For example, to create an antivirus agent, you can implement an SmtpReceiveAgent and a RoutingAgent agent.</span></span> <span data-ttu-id="171e2-112">Si tiene un componente de la red que no es compatible con el protocolo SMTP, puede usar a un agente de transporte DeliveryAgent para controlar la comunicación entre el servidor de Exchange y su componente externo.</span><span class="sxs-lookup"><span data-stu-id="171e2-112">If you have a component on your network that does not support the SMTP protocol, you can use a DeliveryAgent transport agent to handle the communication between your Exchange server and your external component.</span></span> 
  
<span data-ttu-id="171e2-113">En este artículo se proporciona información acerca de los requisitos previos para y las tareas que intervienen en la creación de su propio agente de transporte.</span><span class="sxs-lookup"><span data-stu-id="171e2-113">This article provides information about the prerequisites for and tasks involved in creating your own transport agent.</span></span> <span data-ttu-id="171e2-114">Para obtener información acerca de cómo crear agentes de transporte específica, vea [crear un agente de transporte RoutingAgent para Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md), [crear un agente de transporte SmtpReceiveAgent para Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)y [crear un agente de transporte DeliveryAgent para Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md).</span><span class="sxs-lookup"><span data-stu-id="171e2-114">For information about creating specific transport agents, see [Create a RoutingAgent transport agent for Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md), [Create an SmtpReceiveAgent transport agent for Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md), and [Create a DeliveryAgent transport agent for Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md).</span></span>
  
## <a name="prerequisites-for-creating-a-transport-agent"></a><span data-ttu-id="171e2-115">Requisitos previos para crear a un agente de transporte</span><span class="sxs-lookup"><span data-stu-id="171e2-115">Prerequisites for creating a transport agent</span></span>
<span data-ttu-id="171e2-116"><a name="bk_prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="171e2-116"></span></span>

<span data-ttu-id="171e2-117">Los siguientes son los requisitos previos que necesita para implementar a un agente de transporte:</span><span class="sxs-lookup"><span data-stu-id="171e2-117">The following are the prerequisites that you need in order to implement a transport agent:</span></span>
  
- <span data-ttu-id="171e2-118">Un equipo que ejecuta Exchange 2013 que se ejecuta el servicio de transporte Front-End en un servidor acceso de cliente o de transporte perimetral, o el servicio de transporte en un servidor de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="171e2-118">A computer running Exchange 2013 that is running the Front End Transport service on a Client Access or Edge Transport server, or the Transport service on a Mailbox server.</span></span> <span data-ttu-id="171e2-119">Para obtener información acerca de la arquitectura de rol de servidor en Exchange 2013, vea [de transporte conceptos de agente de Exchange 2013](transport-agent-concepts-in-exchange-2013.md).</span><span class="sxs-lookup"><span data-stu-id="171e2-119">For information about the server role architecture in Exchange 2013, see [Transport agent concepts in Exchange 2013](transport-agent-concepts-in-exchange-2013.md).</span></span>
    
- <span data-ttu-id="171e2-120">Los siguientes ensamblados para las clases de agente de transporte:</span><span class="sxs-lookup"><span data-stu-id="171e2-120">The following assemblies for the transport agent classes:</span></span>
    
  - <span data-ttu-id="171e2-121">Microsoft.Exchange.Data.dll</span><span class="sxs-lookup"><span data-stu-id="171e2-121">Microsoft.Exchange.Data.dll</span></span>
    
  - <span data-ttu-id="171e2-122">Microsoft.Exchange.Data.Common.dll</span><span class="sxs-lookup"><span data-stu-id="171e2-122">Microsoft.Exchange.Data.Common.dll</span></span>
    
  - <span data-ttu-id="171e2-123">Microsoft.Exchange.Transport.dll</span><span class="sxs-lookup"><span data-stu-id="171e2-123">Microsoft.Exchange.Transport.dll</span></span>
    
- <span data-ttu-id="171e2-124">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="171e2-124">The .NET Framework 4.5</span></span>
    
<span data-ttu-id="171e2-125">También se recomienda que instale Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="171e2-125">We also recommend that you install Visual Studio 2012.</span></span> <span data-ttu-id="171e2-126">Agentes de transporte se pueden implementar mediante el uso de Visual Basic .NET o C#.</span><span class="sxs-lookup"><span data-stu-id="171e2-126">You can implement transport agents by using either Visual Basic .NET or C#.</span></span>
  
## <a name="referencing-the-assemblies"></a><span data-ttu-id="171e2-127">Hacer referencia a los ensamblados</span><span class="sxs-lookup"><span data-stu-id="171e2-127">Referencing the assemblies</span></span>
<span data-ttu-id="171e2-128"><a name="bk_ReferenceAssemblies"> </a></span><span class="sxs-lookup"><span data-stu-id="171e2-128"></span></span>

<span data-ttu-id="171e2-129">Exchange 2013 proporciona una biblioteca de clases que admiten la extensión de comportamiento de transporte de Exchange.</span><span class="sxs-lookup"><span data-stu-id="171e2-129">Exchange 2013 provides a library of classes that support the extension of Exchange transport behavior.</span></span> <span data-ttu-id="171e2-130">Estas clases requieren .NET Framework 4.5.</span><span class="sxs-lookup"><span data-stu-id="171e2-130">These classes require the .NET Framework 4.5.</span></span> <span data-ttu-id="171e2-131">Puede implementar a los agentes de transporte en función de estas clases mediante el uso de Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="171e2-131">You can implement transport agents based on these classes by using Visual Studio 2012.</span></span>
  
<span data-ttu-id="171e2-132">El programa de instalación de Exchange 2013 instala los ensamblados que se usan para el desarrollo de agente de transporte y los registra en la memoria caché de ensamblados global (GAC).</span><span class="sxs-lookup"><span data-stu-id="171e2-132">The Exchange 2013 installer installs assemblies that are used for transport agent development and registers them in the global assembly cache (GAC).</span></span> <span data-ttu-id="171e2-133">Para empezar a implementar a un agente de transporte, cree una referencia al ensamblado Microsoft.Exchange.Data.Transport en un proyecto de biblioteca de clases.</span><span class="sxs-lookup"><span data-stu-id="171e2-133">To begin implementing a transport agent, create a reference to the Microsoft.Exchange.Data.Transport assembly in a class library project.</span></span>
  
## <a name="implementing-a-transport-agent"></a><span data-ttu-id="171e2-134">Implementación de un agente de transporte</span><span class="sxs-lookup"><span data-stu-id="171e2-134">Implementing a transport agent</span></span>
<span data-ttu-id="171e2-135"><a name="bk_implementationExample"> </a></span><span class="sxs-lookup"><span data-stu-id="171e2-135"></span></span>

<span data-ttu-id="171e2-136">En el ejemplo siguiente se muestra una implementación mínima de clases que se derivan de las clases [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) y [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) .</span><span class="sxs-lookup"><span data-stu-id="171e2-136">The following example shows a minimal implementation of classes that derive from the [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) and [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) classes.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="171e2-137">Si varios agentes de transporte se ha instalado y registrados para el mismo evento, todos los agentes se invocará, incluso si un agente quita a todos los destinatarios de un elemento de correo.</span><span class="sxs-lookup"><span data-stu-id="171e2-137">If multiple transport agents are installed and registered for the same event, all agents will be invoked, even if one agent removes all the recipients from a mail item.</span></span> <span data-ttu-id="171e2-138">> Para evitar errores no controlados o un comportamiento inesperado, el agente de transporte debe administrar los casos en que el recuento de destinatarios en un elemento de correo es igual a cero.</span><span class="sxs-lookup"><span data-stu-id="171e2-138">> To avoid unhandled errors or unpredictable behavior, your transport agent should handle cases in which the recipient count on a mail item is equal to zero.</span></span> 
  
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

## <a name="installing-and-enabling-an-agent"></a><span data-ttu-id="171e2-139">Instalar y habilitar un agente</span><span class="sxs-lookup"><span data-stu-id="171e2-139">Installing and enabling an agent</span></span>
<span data-ttu-id="171e2-140"><a name="bk_InstallEnable"> </a></span><span class="sxs-lookup"><span data-stu-id="171e2-140"></span></span>

<span data-ttu-id="171e2-141">Después de compilar al agente a un archivo DLL, debe instalar y habilitar al agente de en el servidor de desarrollo de Exchange.</span><span class="sxs-lookup"><span data-stu-id="171e2-141">After you compile your agent to a DLL, you must install and enable the agent on your development Exchange server.</span></span> <span data-ttu-id="171e2-142">En el Shell de administración de Exchange, use el cmdlet [Install-TransportAgent](http://technet.microsoft.com/es-es/library/aa997998.aspx) para instalar al agente y el cmdlet [Enable-TransportAgent](http://technet.microsoft.com/es-es/library/bb124921.aspx) para habilitar al agente.</span><span class="sxs-lookup"><span data-stu-id="171e2-142">In the Exchange Management Shell, use the [Install-TransportAgent](http://technet.microsoft.com/es-es/library/aa997998.aspx) cmdlet to install your agent, and the [Enable-TransportAgent](http://technet.microsoft.com/es-es/library/bb124921.aspx) cmdlet to enable your agent.</span></span> <span data-ttu-id="171e2-143">Para obtener información acerca de cómo usar el Shell de administración de Exchange, consulte [Exchange Server PowerShell (Shell de administración de Exchange)](https://docs.microsoft.com/es-es/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="171e2-143">For information about how to use the Exchange Management Shell, see [Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/es-es/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps).</span></span>
  
> [!CAUTION]
> <span data-ttu-id="171e2-144">Los agentes de transporte tienen acceso total a todos los mensajes de correo electrónico que se encuentren.</span><span class="sxs-lookup"><span data-stu-id="171e2-144">Transport agents have full access to all email messages that they encounter.</span></span> <span data-ttu-id="171e2-145">Exchange 2013 no restringir el comportamiento de un agente de transporte.</span><span class="sxs-lookup"><span data-stu-id="171e2-145">Exchange 2013 does not restrict the behavior of a transport agent.</span></span> <span data-ttu-id="171e2-146">Los agentes de transporte que se inestable o que contienen errores de seguridad pueden afectar a la estabilidad y la seguridad de Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="171e2-146">Transport agents that are unstable or that contain security flaws might affect the stability and security of Exchange 2013.</span></span> <span data-ttu-id="171e2-147">Por lo tanto, sólo debe instalar a los agentes de transporte que plena confianza y que se han probado completamente.</span><span class="sxs-lookup"><span data-stu-id="171e2-147">Therefore, you should only install transport agents that you fully trust and that have been fully tested.</span></span> 
  
<span data-ttu-id="171e2-148">Cuando use el cmdlet **Install-TransportAgent** para instalar a un agente, el Shell de administración de Exchange mantiene un bloqueo en el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="171e2-148">When you use the **Install-TransportAgent** cmdlet to install an agent, the Exchange Management Shell keeps a lock on the assembly.</span></span> <span data-ttu-id="171e2-149">Para liberar el bloqueo en el ensamblado, debe cerrar la sesión de la consola de administración de Exchange que usó para instalar al agente.</span><span class="sxs-lookup"><span data-stu-id="171e2-149">To release the lock on the assembly, you must close the instance of the Exchange Management Shell that you used to install the agent.</span></span> <span data-ttu-id="171e2-150">Podrá actualizar el ensamblado hasta que se libere el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="171e2-150">You will be unable to update the assembly until you release the lock.</span></span> 
  
<span data-ttu-id="171e2-151">En el ejemplo siguiente se muestra cómo usar el Shell de administración de Exchange para instalar y habilitar a un agente denominado MyAgent mediante el uso de una clase derivada de [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) denominado MyAgents.MyAgentFactory.</span><span class="sxs-lookup"><span data-stu-id="171e2-151">The following example shows how to use the Exchange Management Shell to install and enable an agent named MyAgent by using a class derived from [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) named MyAgents.MyAgentFactory.</span></span> 
  
 `Install-TransportAgent -Name "MyCustomAgent" -TransportAgentFactory "MyAgents.MyAgentFactory" -AssemblyPath "C:\myagents\MyAgent.dll"`
  
<span data-ttu-id="171e2-152">En este ejemplo se da nombre al agente MyCustomAgent en el servidor en el que está instalado el agente.</span><span class="sxs-lookup"><span data-stu-id="171e2-152">This example names the agent MyCustomAgent on the server on which the agent is installed.</span></span> <span data-ttu-id="171e2-153">En el ejemplo siguiente se muestra cómo habilitar al agente denominado MyCustomAgent.</span><span class="sxs-lookup"><span data-stu-id="171e2-153">The following example shows how to enable the agent named MyCustomAgent.</span></span>
  
 `Enable-TransportAgent -Name "MyCustomAgent"`
  
<span data-ttu-id="171e2-154">Para administrar un agente de transporte en el servicio de transporte Front-End en un servidor de acceso de cliente, agregue el siguiente valor para el comando: `-TransportService FrontEnd`.</span><span class="sxs-lookup"><span data-stu-id="171e2-154">To manage a transport agent in the Front End Transport service on a Client Access server, add the following value to the command:  `-TransportService FrontEnd`.</span></span> <span data-ttu-id="171e2-155">Por ejemplo, para ver a los agentes de transporte en el servicio de transporte Front-End, ejecute el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="171e2-155">For example, to view the transport agents in the Front End Transport service, run the following command.</span></span>
  
 `Get-TransportAgent -TransportService FrontEnd`
  
<span data-ttu-id="171e2-156">Para obtener más información acerca de cómo instalar, habilitar y administrar a su agente, vea [Administrar agentes de transporte](http://technet.microsoft.com/es-es/library/bb125175%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="171e2-156">For more information about installing, enabling, and managing your agent, see [Manage Transport Agents](http://technet.microsoft.com/es-es/library/bb125175%28v=exchg.150%29.aspx).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="171e2-157">En esta sección</span><span class="sxs-lookup"><span data-stu-id="171e2-157">In this section</span></span>
<span data-ttu-id="171e2-158"><a name="bk_inthissection"> </a></span><span class="sxs-lookup"><span data-stu-id="171e2-158"></span></span>

- [<span data-ttu-id="171e2-159">Crear a un agente de transporte RoutingAgent para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="171e2-159">Create a RoutingAgent transport agent for Exchange 2013</span></span>](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)
    
- [<span data-ttu-id="171e2-160">Crear a un agente de transporte SmtpReceiveAgent para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="171e2-160">Create an SmtpReceiveAgent transport agent for Exchange 2013</span></span>](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)
    
- [<span data-ttu-id="171e2-161">Crear a un agente de transporte DeliveryAgent para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="171e2-161">Create a DeliveryAgent transport agent for Exchange 2013</span></span>](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
    
## <a name="see-also"></a><span data-ttu-id="171e2-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="171e2-162">See also</span></span>

- [<span data-ttu-id="171e2-163">Conceptos de agente en Exchange 2013 de transporte</span><span class="sxs-lookup"><span data-stu-id="171e2-163">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)   
- [<span data-ttu-id="171e2-164">Referencia de agente de transporte de Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="171e2-164">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)
    

