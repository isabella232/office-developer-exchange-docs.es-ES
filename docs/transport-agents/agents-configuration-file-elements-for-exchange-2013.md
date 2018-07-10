---
title: Elementos del archivo de configuración de los agentes para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Agents
api_type:
- schema
ms.assetid: 3047653b-d712-46c1-ae0a-73f3975f5e9d
description: Busque información sobre los elementos XML en el archivo de configuración agents.config y fetagents.config en Exchange 2013.
ms.openlocfilehash: dd58c4bc21a968db2ca5b13e0c53f7058b29f233
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763352"
---
# <a name="agents-configuration-file-elements-for-exchange-2013"></a><span data-ttu-id="5e5a5-103">Elementos del archivo de configuración de los agentes para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="5e5a5-103">Agents configuration file elements for Exchange 2013</span></span>

<span data-ttu-id="5e5a5-104">Busque información sobre los elementos XML en el archivo de configuración agents.config y fetagents.config en Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="5e5a5-104">Find information about the XML elements in the agents.config and fetagents.config configuration file in Exchange 2013.</span></span>
  
<span data-ttu-id="5e5a5-105">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="5e5a5-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="5e5a5-106">Cuando se instala el acceso de cliente o el rol de servidor de buzón de correo en un servidor de Exchange, el programa de instalación crea un archivo XML que contiene información de configuración acerca de los agentes que están instalados en el servidor.</span><span class="sxs-lookup"><span data-stu-id="5e5a5-106">When you install the Client Access or the Mailbox server role on an Exchange server, the installer creates an XML file that contains configuration information about agents that are installed on the server.</span></span> <span data-ttu-id="5e5a5-107">No se puede escribir directamente a este archivo.</span><span class="sxs-lookup"><span data-stu-id="5e5a5-107">You cannot write directly to this file.</span></span> 
  
<span data-ttu-id="5e5a5-108">El servicio de transporte Front-End se ejecuta en servidores de acceso de cliente y se escribe en un archivo denominado fetagents.config. El servicio de transporte y el servicio de transporte de buzón de correo ejecutan en servidores de buzones y escriben en un archivo denominado agents.config. Un equipo que tiene el rol de servidor de acceso de cliente y el rol de servidor de buzón de correo tendrán un fetagents.config y un archivo agents.config.</span><span class="sxs-lookup"><span data-stu-id="5e5a5-108">The Front End Transport service runs on Client Access servers and writes to a file named fetagents.config. The Transport service and the Mailbox Transport service run on Mailbox servers, and write to a file named agents.config. A computer that has both the Client Access server role and the Mailbox server role will have both a fetagents.config and an agents.config file.</span></span> 
  
<span data-ttu-id="5e5a5-109">Es la única forma admitida para escribir en estos archivos mediante el uso de los cmdlets de agente de transporte en el Shell de administración de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5e5a5-109">The only supported way to write to these files is by using the transport agent cmdlets in the Exchange Management Shell.</span></span> <span data-ttu-id="5e5a5-110">Para obtener información acerca de los cmdlets de agente de transporte, consulte [Cmdlets de flujo de correo](http://technet.microsoft.com/es-es/library/aa998553%28v=exchg.150%29.aspx) en TechNet.</span><span class="sxs-lookup"><span data-stu-id="5e5a5-110">For information about the transport agent cmdlets, see [Mail Flow Cmdlets](http://technet.microsoft.com/es-es/library/aa998553%28v=exchg.150%29.aspx) on TechNet.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5e5a5-111">Para distinguir entre los agentes que amplían el servicio de transporte Front-End en el servidor de acceso de cliente y el servicio de transporte en el servidor de buzón de correo, los cmdlets de agente de transporte tiene un parámetro de _TransportService_ con un valor de "Concentrador" para el transporte servicio y "FrontEnd" para el servicio de transporte Front-End.</span><span class="sxs-lookup"><span data-stu-id="5e5a5-111">To distinguish between agents that extend the Front End Transport service on the Client Access server and the Transport service on the Mailbox server, transport agent cmdlets have a  _TransportService_ parameter with a value of "Hub" for the Transport service and "FrontEnd" for the Front End Transport service.</span></span> 
  
<span data-ttu-id="5e5a5-112">Puede leer el agents.config o el archivo fetagents.config para determinar la presencia de y la información de configuración para uno o varios agentes en el servidor.</span><span class="sxs-lookup"><span data-stu-id="5e5a5-112">You can read the agents.config or fetagents.config file to determine the presence of and configuration information for one or more agents on the server.</span></span> <span data-ttu-id="5e5a5-113">Esta documentación proporciona una referencia que puede usar para leer la información en el archivo agents.config o la fetagents.config. El formato de ambos de estos archivos es el mismo.</span><span class="sxs-lookup"><span data-stu-id="5e5a5-113">This documentation provides a reference that you can use to read the information in either the agents.config file or the fetagents.config. The format for both of these files is the same.</span></span> <span data-ttu-id="5e5a5-114">Esta documentación no proporciona información acerca de cómo escribir en los archivos.</span><span class="sxs-lookup"><span data-stu-id="5e5a5-114">This documentation does not provide information about how to write to the files.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="5e5a5-115">Uso de métodos no admitidos para escribir en el archivo agents.config o fetagents.config puede producir resultados inesperados, incluido el error del servicio de transporte o los agentes de transporte o ambos.</span><span class="sxs-lookup"><span data-stu-id="5e5a5-115">Using unsupported methods to write to the agents.config file or fetagents.config can produce unexpected results, including failure of the transport service or transport agents, or both.</span></span> <span data-ttu-id="5e5a5-116">No se escriben directamente a cualquiera de estos archivos.</span><span class="sxs-lookup"><span data-stu-id="5e5a5-116">Do not write directly to either of these files.</span></span> <span data-ttu-id="5e5a5-117">Es el único método admitido para escribir en estos archivos mediante el uso de los cmdlets de agente de transporte de Exchange Management Shell.</span><span class="sxs-lookup"><span data-stu-id="5e5a5-117">The only supported method for writing to these files is by using the Exchange Management Shell transport agent cmdlets.</span></span> 
  
## <a name="location-of-the-transport-agent-configuration-files"></a><span data-ttu-id="5e5a5-118">Ubicación de los archivos de configuración del agente de transporte</span><span class="sxs-lookup"><span data-stu-id="5e5a5-118">Location of the transport agent configuration files</span></span>
<span data-ttu-id="5e5a5-119"><a name="bk_ConfigLoc"> </a></span><span class="sxs-lookup"><span data-stu-id="5e5a5-119"></span></span>

<span data-ttu-id="5e5a5-120">Al instalar Exchange 2013, el programa de instalación crea un archivo XML que se denomina agents.config.template o fetagents.config.template, según el rol de servidor instalado, en la \<ExchangeInstallFolder\>\TransportRoles\Agents carpeta (donde \<ExchangeInstallFolder\> es la carpeta en la que ha instalado Exchange 2013).</span><span class="sxs-lookup"><span data-stu-id="5e5a5-120">When you install Exchange 2013, the installer creates an XML file that is named either agents.config.template or fetagents.config.template, depending on the server role installed, in the \<ExchangeInstallFolder\>\TransportRoles\Agents folder (where \<ExchangeInstallFolder\> is the folder in which you installed Exchange 2013).</span></span> <span data-ttu-id="5e5a5-121">Si instala el rol de servidor de acceso de cliente, Exchange 2013 copia el archivo fetagents.config.template a fetagents.config. Si instala el rol de servidor de buzón de correo, Exchange 2013 copia el archivo agents.config.template en agents.config. Exchange 2013 lee y escribe en este archivo cuando se cambia la configuración de los agentes de transporte en el servidor.</span><span class="sxs-lookup"><span data-stu-id="5e5a5-121">If you install the Client Access server role, Exchange 2013 copies the fetagents.config.template file to fetagents.config. If you install the Mailbox server role, Exchange 2013 copies the agents.config.template file to agents.config. Exchange 2013 reads and writes this file when you change the transport agents configuration on the server.</span></span>
  
## <a name="verifying-a-transport-agent-installation"></a><span data-ttu-id="5e5a5-122">Comprobar una instalación de agente de transporte</span><span class="sxs-lookup"><span data-stu-id="5e5a5-122">Verifying a transport agent installation</span></span>
<span data-ttu-id="5e5a5-123"><a name="bk_verifyinstall"> </a></span><span class="sxs-lookup"><span data-stu-id="5e5a5-123"></span></span>

<span data-ttu-id="5e5a5-124">Puede usar las capacidades XML que proporciona .NET Framework para leer y validar el agents.config o el archivo XML de fetagents.config.</span><span class="sxs-lookup"><span data-stu-id="5e5a5-124">You can use the XML capabilities that the .NET Framework provides to read and validate the agents.config or the fetagents.config XML file.</span></span> <span data-ttu-id="5e5a5-125">Para comprobar la instalación y configuración de un agente de transporte, leer el archivo XML en el archivo de configuración y busque el elemento de [agente](agent.md) que se corresponde con el agente de transporte.</span><span class="sxs-lookup"><span data-stu-id="5e5a5-125">To verify the installation and configuration of a transport agent, read the XML in the configuration file and find the [agent](agent.md) element that corresponds to the transport agent.</span></span> <span data-ttu-id="5e5a5-126">Si no existe un elemento de **agente** para el agente de transporte específica, no está instalado el agente de transporte.</span><span class="sxs-lookup"><span data-stu-id="5e5a5-126">If an **agent** element for the specific transport agent does not exist, the transport agent is not installed.</span></span> <span data-ttu-id="5e5a5-127">Si está instalado el agente de transporte, puede leer los atributos del elemento de **agente** para determinar su configuración.</span><span class="sxs-lookup"><span data-stu-id="5e5a5-127">If the transport agent is installed, you can read the attributes of the **agent** element to determine its configuration.</span></span> 
  
## <a name="configuration-file-element-hierarchy"></a><span data-ttu-id="5e5a5-128">Jerarquía de elementos del archivo de configuración</span><span class="sxs-lookup"><span data-stu-id="5e5a5-128">Configuration file element hierarchy</span></span>
<span data-ttu-id="5e5a5-129"><a name="bk_elementref"> </a></span><span class="sxs-lookup"><span data-stu-id="5e5a5-129"></span></span>

<span data-ttu-id="5e5a5-130">El código siguiente muestra la jerarquía de elementos del archivo de configuración XML.</span><span class="sxs-lookup"><span data-stu-id="5e5a5-130">The following code shows the element hierarchy in the configuration XML file.</span></span>
  
```XML
<configuration>
    <mexRuntime>
        <monitoring>
            <agentExecution/>
            <messageSnapshot/>
        </monitoring>
        <agentList>
            <agent/>
            <agent/>
            <agent />
        </agentList>
    </mexRuntim>
</configuration>
```

## <a name="in-this-section"></a><span data-ttu-id="5e5a5-131">En esta sección</span><span class="sxs-lookup"><span data-stu-id="5e5a5-131">In this section</span></span>
<span data-ttu-id="5e5a5-132"><a name="bk_elementreflist"> </a></span><span class="sxs-lookup"><span data-stu-id="5e5a5-132"></span></span>

- [<span data-ttu-id="5e5a5-133">agente</span><span class="sxs-lookup"><span data-stu-id="5e5a5-133">agent</span></span>](agent.md)
    
- [<span data-ttu-id="5e5a5-134">agentExecution</span><span class="sxs-lookup"><span data-stu-id="5e5a5-134">agentExecution</span></span>](agentexecution.md)
    
- [<span data-ttu-id="5e5a5-135">agentList</span><span class="sxs-lookup"><span data-stu-id="5e5a5-135">agentList</span></span>](agentlist.md)
    
- [<span data-ttu-id="5e5a5-136">configuración</span><span class="sxs-lookup"><span data-stu-id="5e5a5-136">configuration</span></span>](configuration.md)
    
- [<span data-ttu-id="5e5a5-137">messageSnapshot</span><span class="sxs-lookup"><span data-stu-id="5e5a5-137">messageSnapshot</span></span>](messagesnapshot.md)
    
- [<span data-ttu-id="5e5a5-138">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="5e5a5-138">mexRuntime</span></span>](mexruntime.md)
    
- [<span data-ttu-id="5e5a5-139">supervisión</span><span class="sxs-lookup"><span data-stu-id="5e5a5-139">monitoring</span></span>](monitoring.md)
    
## <a name="see-also"></a><span data-ttu-id="5e5a5-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e5a5-140">See also</span></span>

- [<span data-ttu-id="5e5a5-141">Los agentes de transporte en Exchange</span><span class="sxs-lookup"><span data-stu-id="5e5a5-141">Transport agents in Exchange</span></span>](transport-agents-in-exchange-2013.md)
- [<span data-ttu-id="5e5a5-142">Conceptos de agente en Exchange 2013 de transporte</span><span class="sxs-lookup"><span data-stu-id="5e5a5-142">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)
- [<span data-ttu-id="5e5a5-143">Referencia de agente de transporte de Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="5e5a5-143">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)
- [<span data-ttu-id="5e5a5-144">Espacios de nombres de agente en Exchange 2013 de transporte</span><span class="sxs-lookup"><span data-stu-id="5e5a5-144">Transport agent namespaces in Exchange 2013</span></span>](transport-agent-namespaces-in-exchange-2013.md)
- [<span data-ttu-id="5e5a5-145">Cmdlets de flujo de correo</span><span class="sxs-lookup"><span data-stu-id="5e5a5-145">Mail Flow Cmdlets</span></span>](https://docs.microsoft.com/es-es/powershell/exchange/?view=exchange-ps)
    

