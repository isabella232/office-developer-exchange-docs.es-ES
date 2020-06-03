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
# <a name="creating-transport-agents-for-exchange-2013"></a><span data-ttu-id="0d1f9-103">Crear agentes de transporte para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="0d1f9-103">Creating transport agents for Exchange 2013</span></span>

<span data-ttu-id="0d1f9-104">Busque información sobre cómo crear agentes de transporte personalizados para Exchange 2013 y los requisitos del sistema para crear un agente personalizado.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-104">Find information about how to create custom transport agents for Exchange 2013, and the system requirements for creating a custom agent.</span></span>
  
<span data-ttu-id="0d1f9-105">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="0d1f9-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="0d1f9-106">Exchange Server 2013 incluye varios agentes de transporte que puede usar para procesar mensajes.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-106">Exchange Server 2013 includes several transport agents that you can use to process messages.</span></span> <span data-ttu-id="0d1f9-107">Mediante el uso de los ensamblados que se incluyen con Exchange, puede crear sus propios agentes personalizados para realizar tareas específicas de acuerdo con las necesidades de su organización.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-107">By using the assemblies that come with Exchange, you can create your own custom agents to perform specific tasks according to the needs of your organization.</span></span> <span data-ttu-id="0d1f9-108">Por ejemplo, puede usar un agente de transporte SmtpReceiveAgent para interceptar los mensajes recibidos a través del protocolo SMTP y procesar el mensaje para convertir el formato del cuerpo para que contenga texto con formato previo.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-108">For example, you can use an SmtpReceiveAgent transport agent to intercept messages that are received via the SMTP protocol and process the message to convert the format of the body to contain preformatted text.</span></span> <span data-ttu-id="0d1f9-109">Puede usar un agente de transporte RoutingAgent para registrar los mensajes que pasan a través del servidor en la ruta a otro servidor.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-109">You can use a RoutingAgent transport agent to log the messages that pass through the server on route to another server.</span></span> <span data-ttu-id="0d1f9-110">También puede crear características más complejas que hagan uso de más de un tipo de agente.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-110">You can also create more complex features that make use of more than one type of agent.</span></span> <span data-ttu-id="0d1f9-111">Por ejemplo, para crear un agente antivirus, puede implementar un SmtpReceiveAgent y un agente de RoutingAgent.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-111">For example, to create an antivirus agent, you can implement an SmtpReceiveAgent and a RoutingAgent agent.</span></span> <span data-ttu-id="0d1f9-112">Si tiene un componente en la red que no es compatible con el protocolo SMTP, puede usar un agente de transporte DeliveryAgent para controlar la comunicación entre el servidor Exchange y el componente externo.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-112">If you have a component on your network that does not support the SMTP protocol, you can use a DeliveryAgent transport agent to handle the communication between your Exchange server and your external component.</span></span> 
  
<span data-ttu-id="0d1f9-113">En este artículo se proporciona información acerca de los requisitos previos de y las tareas necesarias para crear su propio agente de transporte.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-113">This article provides information about the prerequisites for and tasks involved in creating your own transport agent.</span></span> <span data-ttu-id="0d1f9-114">Para obtener información acerca de la creación de agentes de transporte específicos, consulte [Create a RoutingAgent Transport Agent for exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md), [Create a SmtpReceiveAgent transport agent for Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md), and [Create a DeliveryAgent Transport Agent for Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md).</span><span class="sxs-lookup"><span data-stu-id="0d1f9-114">For information about creating specific transport agents, see [Create a RoutingAgent transport agent for Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md), [Create an SmtpReceiveAgent transport agent for Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md), and [Create a DeliveryAgent transport agent for Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md).</span></span>
  
## <a name="prerequisites-for-creating-a-transport-agent"></a><span data-ttu-id="0d1f9-115">Requisitos previos para crear un agente de transporte</span><span class="sxs-lookup"><span data-stu-id="0d1f9-115">Prerequisites for creating a transport agent</span></span>
<span data-ttu-id="0d1f9-116"><a name="bk_prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="0d1f9-116"><a name="bk_prerequisites"> </a></span></span>

<span data-ttu-id="0d1f9-117">Los siguientes son los requisitos previos que necesita para implementar un agente de transporte:</span><span class="sxs-lookup"><span data-stu-id="0d1f9-117">The following are the prerequisites that you need in order to implement a transport agent:</span></span>
  
- <span data-ttu-id="0d1f9-118">Un equipo que ejecuta Exchange 2013 que ejecuta el servicio de transporte front-end en un servidor de transporte perimetral o de acceso de cliente, o el servicio de transporte en un servidor de buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-118">A computer running Exchange 2013 that is running the Front End Transport service on a Client Access or Edge Transport server, or the Transport service on a Mailbox server.</span></span> <span data-ttu-id="0d1f9-119">Para obtener información acerca de la arquitectura de los roles de servidor en Exchange 2013, consulte [conceptos de agentes de transporte en exchange 2013](transport-agent-concepts-in-exchange-2013.md).</span><span class="sxs-lookup"><span data-stu-id="0d1f9-119">For information about the server role architecture in Exchange 2013, see [Transport agent concepts in Exchange 2013](transport-agent-concepts-in-exchange-2013.md).</span></span>
    
- <span data-ttu-id="0d1f9-120">Los siguientes ensamblados para las clases de agente de transporte:</span><span class="sxs-lookup"><span data-stu-id="0d1f9-120">The following assemblies for the transport agent classes:</span></span>
    
  - <span data-ttu-id="0d1f9-121">Microsoft. Exchange. Data. dll</span><span class="sxs-lookup"><span data-stu-id="0d1f9-121">Microsoft.Exchange.Data.dll</span></span>
    
  - <span data-ttu-id="0d1f9-122">Microsoft. Exchange. Data. Common. dll</span><span class="sxs-lookup"><span data-stu-id="0d1f9-122">Microsoft.Exchange.Data.Common.dll</span></span>
    
  - <span data-ttu-id="0d1f9-123">Microsoft. Exchange. Transport. dll</span><span class="sxs-lookup"><span data-stu-id="0d1f9-123">Microsoft.Exchange.Transport.dll</span></span>
    
- <span data-ttu-id="0d1f9-124">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="0d1f9-124">The .NET Framework 4.5</span></span>
    
<span data-ttu-id="0d1f9-125">También le recomendamos que instale Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-125">We also recommend that you install Visual Studio 2012.</span></span> <span data-ttu-id="0d1f9-126">Puede implementar agentes de transporte mediante Visual Basic .NET o C#.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-126">You can implement transport agents by using either Visual Basic .NET or C#.</span></span>
  
## <a name="referencing-the-assemblies"></a><span data-ttu-id="0d1f9-127">Referencia a los ensamblados</span><span class="sxs-lookup"><span data-stu-id="0d1f9-127">Referencing the assemblies</span></span>
<span data-ttu-id="0d1f9-128"><a name="bk_ReferenceAssemblies"> </a></span><span class="sxs-lookup"><span data-stu-id="0d1f9-128"><a name="bk_ReferenceAssemblies"> </a></span></span>

<span data-ttu-id="0d1f9-129">Exchange 2013 proporciona una biblioteca de clases que admiten la extensión del comportamiento de transporte de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-129">Exchange 2013 provides a library of classes that support the extension of Exchange transport behavior.</span></span> <span data-ttu-id="0d1f9-130">Estas clases requieren .NET Framework 4,5.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-130">These classes require the .NET Framework 4.5.</span></span> <span data-ttu-id="0d1f9-131">Puede implementar agentes de transporte basados en estas clases con Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-131">You can implement transport agents based on these classes by using Visual Studio 2012.</span></span>
  
<span data-ttu-id="0d1f9-132">El instalador de Exchange 2013 instala ensamblados que se usan para el desarrollo de agentes de transporte y los registra en la memoria caché global de ensamblados (GAC).</span><span class="sxs-lookup"><span data-stu-id="0d1f9-132">The Exchange 2013 installer installs assemblies that are used for transport agent development and registers them in the global assembly cache (GAC).</span></span> <span data-ttu-id="0d1f9-133">Para empezar a implementar un agente de transporte, cree una referencia al ensamblado Microsoft. Exchange. Data. Transport en un proyecto de biblioteca de clases.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-133">To begin implementing a transport agent, create a reference to the Microsoft.Exchange.Data.Transport assembly in a class library project.</span></span>
  
## <a name="implementing-a-transport-agent"></a><span data-ttu-id="0d1f9-134">Implementación de un agente de transporte</span><span class="sxs-lookup"><span data-stu-id="0d1f9-134">Implementing a transport agent</span></span>
<span data-ttu-id="0d1f9-135"><a name="bk_implementationExample"> </a></span><span class="sxs-lookup"><span data-stu-id="0d1f9-135"><a name="bk_implementationExample"> </a></span></span>

<span data-ttu-id="0d1f9-136">En el ejemplo siguiente se muestra una implementación mínima de clases que derivan de las clases [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) y [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0d1f9-136">The following example shows a minimal implementation of classes that derive from the [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) and [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) classes.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="0d1f9-137">Si hay varios agentes de transporte instalados y registrados para el mismo evento, se invocará a todos los agentes, incluso si un agente quita todos los destinatarios de un elemento de correo.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-137">If multiple transport agents are installed and registered for the same event, all agents will be invoked, even if one agent removes all the recipients from a mail item.</span></span> <span data-ttu-id="0d1f9-138">> para evitar errores no controlados o un comportamiento impredecible, el agente de transporte debe controlar los casos en los que el recuento de destinatarios de un elemento de correo es igual a cero.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-138">> To avoid unhandled errors or unpredictable behavior, your transport agent should handle cases in which the recipient count on a mail item is equal to zero.</span></span> 
  
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

## <a name="installing-and-enabling-an-agent"></a><span data-ttu-id="0d1f9-139">Instalación y habilitación de un agente</span><span class="sxs-lookup"><span data-stu-id="0d1f9-139">Installing and enabling an agent</span></span>
<span data-ttu-id="0d1f9-140"><a name="bk_InstallEnable"> </a></span><span class="sxs-lookup"><span data-stu-id="0d1f9-140"><a name="bk_InstallEnable"> </a></span></span>

<span data-ttu-id="0d1f9-141">Después de compilar el agente en una DLL, debe instalar y habilitar el agente en su servidor de desarrollo de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-141">After you compile your agent to a DLL, you must install and enable the agent on your development Exchange server.</span></span> <span data-ttu-id="0d1f9-142">En el shell de administración de Exchange, use el cmdlet [install-transportagent](https://technet.microsoft.com/library/aa997998.aspx) para instalar el agente y el cmdlet [enable-transportagent](https://technet.microsoft.com/library/bb124921.aspx) para habilitar el agente.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-142">In the Exchange Management Shell, use the [Install-TransportAgent](https://technet.microsoft.com/library/aa997998.aspx) cmdlet to install your agent, and the [Enable-TransportAgent](https://technet.microsoft.com/library/bb124921.aspx) cmdlet to enable your agent.</span></span> <span data-ttu-id="0d1f9-143">Para obtener información acerca de cómo usar el shell de administración de Exchange, vea [Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="0d1f9-143">For information about how to use the Exchange Management Shell, see [Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps).</span></span>
  
> [!CAUTION]
> <span data-ttu-id="0d1f9-144">Los agentes de transporte tienen acceso completo a todos los mensajes de correo electrónico que encuentran.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-144">Transport agents have full access to all email messages that they encounter.</span></span> <span data-ttu-id="0d1f9-145">Exchange 2013 no restringe el comportamiento de un agente de transporte.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-145">Exchange 2013 does not restrict the behavior of a transport agent.</span></span> <span data-ttu-id="0d1f9-146">Los agentes de transporte que son inestables o que contienen errores de seguridad pueden afectar a la estabilidad y seguridad de Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-146">Transport agents that are unstable or that contain security flaws might affect the stability and security of Exchange 2013.</span></span> <span data-ttu-id="0d1f9-147">Por lo tanto, solo debe instalar los agentes de transporte en los que confíe plenamente y que se hayan probado completamente.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-147">Therefore, you should only install transport agents that you fully trust and that have been fully tested.</span></span> 
  
<span data-ttu-id="0d1f9-148">Cuando usa el cmdlet **install-TransportAgent** para instalar un agente, el shell de administración de Exchange mantiene un bloqueo en el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-148">When you use the **Install-TransportAgent** cmdlet to install an agent, the Exchange Management Shell keeps a lock on the assembly.</span></span> <span data-ttu-id="0d1f9-149">Para liberar el bloqueo en el ensamblado, debe cerrar la instancia del shell de administración de Exchange que usó para instalar el agente.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-149">To release the lock on the assembly, you must close the instance of the Exchange Management Shell that you used to install the agent.</span></span> <span data-ttu-id="0d1f9-150">No podrá actualizar el ensamblado hasta que libere el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-150">You will be unable to update the assembly until you release the lock.</span></span> 
  
<span data-ttu-id="0d1f9-151">En el ejemplo siguiente se muestra cómo usar el shell de administración de Exchange para instalar y habilitar un agente denominado mi agente mediante una clase derivada de [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) denominados alagents. MyAgentFactory.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-151">The following example shows how to use the Exchange Management Shell to install and enable an agent named MyAgent by using a class derived from [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) named MyAgents.MyAgentFactory.</span></span> 
  
 `Install-TransportAgent -Name "MyCustomAgent" -TransportAgentFactory "MyAgents.MyAgentFactory" -AssemblyPath "C:\myagents\MyAgent.dll"`
  
<span data-ttu-id="0d1f9-152">En este ejemplo se asigna un nombre al agente MyCustomAgent en el servidor en el que está instalado el agente.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-152">This example names the agent MyCustomAgent on the server on which the agent is installed.</span></span> <span data-ttu-id="0d1f9-153">En el siguiente ejemplo, se muestra cómo habilitar el agente denominado MyCustomAgent.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-153">The following example shows how to enable the agent named MyCustomAgent.</span></span>
  
 `Enable-TransportAgent -Name "MyCustomAgent"`
  
<span data-ttu-id="0d1f9-154">Para administrar un agente de transporte en el servicio de transporte front-end en un servidor de acceso de cliente, agregue el siguiente valor al comando: `-TransportService FrontEnd` .</span><span class="sxs-lookup"><span data-stu-id="0d1f9-154">To manage a transport agent in the Front End Transport service on a Client Access server, add the following value to the command:  `-TransportService FrontEnd`.</span></span> <span data-ttu-id="0d1f9-155">Por ejemplo, para ver los agentes de transporte en el servicio de transporte front-end, ejecute el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="0d1f9-155">For example, to view the transport agents in the Front End Transport service, run the following command.</span></span>
  
 `Get-TransportAgent -TransportService FrontEnd`
  
<span data-ttu-id="0d1f9-156">Para obtener más información acerca de la instalación, habilitación y administración del agente, consulte [Manage Transport Agents](https://technet.microsoft.com/library/bb125175%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0d1f9-156">For more information about installing, enabling, and managing your agent, see [Manage Transport Agents](https://technet.microsoft.com/library/bb125175%28v=exchg.150%29.aspx).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="0d1f9-157">En esta sección</span><span class="sxs-lookup"><span data-stu-id="0d1f9-157">In this section</span></span>
<span data-ttu-id="0d1f9-158"><a name="bk_inthissection"> </a></span><span class="sxs-lookup"><span data-stu-id="0d1f9-158"><a name="bk_inthissection"> </a></span></span>

- [<span data-ttu-id="0d1f9-159">Crear un agente de transporte de RoutingAgent para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="0d1f9-159">Create a RoutingAgent transport agent for Exchange 2013</span></span>](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)
    
- [<span data-ttu-id="0d1f9-160">Crear un agente de transporte de SmtpReceiveAgent para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="0d1f9-160">Create an SmtpReceiveAgent transport agent for Exchange 2013</span></span>](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)
    
- [<span data-ttu-id="0d1f9-161">Crear un agente de transporte de DeliveryAgent para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="0d1f9-161">Create a DeliveryAgent transport agent for Exchange 2013</span></span>](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
    
## <a name="see-also"></a><span data-ttu-id="0d1f9-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d1f9-162">See also</span></span>

- [<span data-ttu-id="0d1f9-163">Conceptos del agente de transporte en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="0d1f9-163">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)   
- [<span data-ttu-id="0d1f9-164">Referencia del agente de transporte para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="0d1f9-164">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)
    

