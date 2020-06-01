---
title: Elementos del archivo de configuración de agentes para Exchange 2013
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
description: Busque información sobre los elementos XML en el archivo Agents. config y el archivo de configuración fetagents. config en Exchange 2013.
ms.openlocfilehash: f19fe8316a78cef668db881e630562d3be8be64a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461572"
---
# <a name="agents-configuration-file-elements-for-exchange-2013"></a><span data-ttu-id="0622b-103">Elementos del archivo de configuración de agentes para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="0622b-103">Agents configuration file elements for Exchange 2013</span></span>

<span data-ttu-id="0622b-104">Busque información sobre los elementos XML en el archivo Agents. config y el archivo de configuración fetagents. config en Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="0622b-104">Find information about the XML elements in the agents.config and fetagents.config configuration file in Exchange 2013.</span></span>
  
<span data-ttu-id="0622b-105">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="0622b-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="0622b-106">Al instalar el rol de servidor de acceso de cliente o buzón de correo en un servidor de Exchange, el instalador crea un archivo XML que contiene información de configuración sobre los agentes que están instalados en el servidor.</span><span class="sxs-lookup"><span data-stu-id="0622b-106">When you install the Client Access or the Mailbox server role on an Exchange server, the installer creates an XML file that contains configuration information about agents that are installed on the server.</span></span> <span data-ttu-id="0622b-107">No puede escribir directamente en este archivo.</span><span class="sxs-lookup"><span data-stu-id="0622b-107">You cannot write directly to this file.</span></span> 
  
<span data-ttu-id="0622b-108">El servicio de transporte de front-end se ejecuta en los servidores de acceso de cliente y escribe en un archivo denominado fetagents. config. El servicio de transporte y el servicio de transporte de buzones de correo se ejecutan en servidores de buzones de correo y escriben en un archivo denominado Agents. config. Un equipo que tenga el rol de servidor acceso de clientes y el rol de servidor buzón de correo tendrá un archivo fetagents. config y un archivo Agents. config.</span><span class="sxs-lookup"><span data-stu-id="0622b-108">The Front End Transport service runs on Client Access servers and writes to a file named fetagents.config. The Transport service and the Mailbox Transport service run on Mailbox servers, and write to a file named agents.config. A computer that has both the Client Access server role and the Mailbox server role will have both a fetagents.config and an agents.config file.</span></span> 
  
<span data-ttu-id="0622b-109">La única forma admitida de escribir en estos archivos es mediante el uso de cmdlets de agente de transporte en el shell de administración de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0622b-109">The only supported way to write to these files is by using the transport agent cmdlets in the Exchange Management Shell.</span></span> <span data-ttu-id="0622b-110">Para obtener información acerca de los cmdlets del agente de transporte, consulte [mail Flow cmdlets](https://technet.microsoft.com/library/aa998553%28v=exchg.150%29.aspx) en TechNet.</span><span class="sxs-lookup"><span data-stu-id="0622b-110">For information about the transport agent cmdlets, see [Mail Flow Cmdlets](https://technet.microsoft.com/library/aa998553%28v=exchg.150%29.aspx) on TechNet.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0622b-111">Para distinguir entre agentes que amplían el servicio de transporte front-end en el servidor de acceso de cliente y el servicio de transporte en el servidor de buzones de correo, los cmdlets de agente de transporte tienen un parámetro _TransportService_ con un valor de "Hub" para el servicio de transporte y "frontend" para el servicio de transporte front-end.</span><span class="sxs-lookup"><span data-stu-id="0622b-111">To distinguish between agents that extend the Front End Transport service on the Client Access server and the Transport service on the Mailbox server, transport agent cmdlets have a  _TransportService_ parameter with a value of "Hub" for the Transport service and "FrontEnd" for the Front End Transport service.</span></span> 
  
<span data-ttu-id="0622b-112">Puede leer el archivo Agents. config o fetagents. config para determinar la presencia y la información de configuración de uno o más agentes en el servidor.</span><span class="sxs-lookup"><span data-stu-id="0622b-112">You can read the agents.config or fetagents.config file to determine the presence of and configuration information for one or more agents on the server.</span></span> <span data-ttu-id="0622b-113">Esta documentación proporciona una referencia que puede usar para leer la información en el archivo Agents. config o en fetagents. config. El formato de ambos archivos es el mismo.</span><span class="sxs-lookup"><span data-stu-id="0622b-113">This documentation provides a reference that you can use to read the information in either the agents.config file or the fetagents.config. The format for both of these files is the same.</span></span> <span data-ttu-id="0622b-114">En esta documentación no se proporciona información sobre cómo escribir en los archivos.</span><span class="sxs-lookup"><span data-stu-id="0622b-114">This documentation does not provide information about how to write to the files.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="0622b-115">El uso de métodos no admitidos para escribir en el archivo Agents. config o fetagents. config puede producir resultados inesperados, incluido el error del servicio de transporte o los agentes de transporte, o ambos.</span><span class="sxs-lookup"><span data-stu-id="0622b-115">Using unsupported methods to write to the agents.config file or fetagents.config can produce unexpected results, including failure of the transport service or transport agents, or both.</span></span> <span data-ttu-id="0622b-116">No escriba directamente en ninguno de estos archivos.</span><span class="sxs-lookup"><span data-stu-id="0622b-116">Do not write directly to either of these files.</span></span> <span data-ttu-id="0622b-117">El único método admitido para escribir en estos archivos es mediante los cmdlets del agente de transporte del shell de administración de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0622b-117">The only supported method for writing to these files is by using the Exchange Management Shell transport agent cmdlets.</span></span> 
  
## <a name="location-of-the-transport-agent-configuration-files"></a><span data-ttu-id="0622b-118">Ubicación de los archivos de configuración del agente de transporte</span><span class="sxs-lookup"><span data-stu-id="0622b-118">Location of the transport agent configuration files</span></span>
<span data-ttu-id="0622b-119"><a name="bk_ConfigLoc"> </a></span><span class="sxs-lookup"><span data-stu-id="0622b-119"><a name="bk_ConfigLoc"> </a></span></span>

<span data-ttu-id="0622b-120">Al instalar Exchange 2013, el instalador crea un archivo XML que se denomina Agents. config. template o fetagents. config. template, en función de la función de servidor instalada, en la \<ExchangeInstallFolder\> carpeta \TransportRoles\Agents (donde \<ExchangeInstallFolder\> es la carpeta en la que instaló Exchange 2013).</span><span class="sxs-lookup"><span data-stu-id="0622b-120">When you install Exchange 2013, the installer creates an XML file that is named either agents.config.template or fetagents.config.template, depending on the server role installed, in the \<ExchangeInstallFolder\>\TransportRoles\Agents folder (where \<ExchangeInstallFolder\> is the folder in which you installed Exchange 2013).</span></span> <span data-ttu-id="0622b-121">Si instala la función de servidor de acceso de cliente, Exchange 2013 copia el archivo fetagents. config. template en fetagents. config. Si instala el rol de servidor buzón de correo, Exchange 2013 copia el archivo Agents. config. template en Agents. config. Exchange 2013 Lee y escribe este archivo cuando cambia la configuración de los agentes de transporte en el servidor.</span><span class="sxs-lookup"><span data-stu-id="0622b-121">If you install the Client Access server role, Exchange 2013 copies the fetagents.config.template file to fetagents.config. If you install the Mailbox server role, Exchange 2013 copies the agents.config.template file to agents.config. Exchange 2013 reads and writes this file when you change the transport agents configuration on the server.</span></span>
  
## <a name="verifying-a-transport-agent-installation"></a><span data-ttu-id="0622b-122">Comprobación de la instalación de un agente de transporte</span><span class="sxs-lookup"><span data-stu-id="0622b-122">Verifying a transport agent installation</span></span>
<span data-ttu-id="0622b-123"><a name="bk_verifyinstall"> </a></span><span class="sxs-lookup"><span data-stu-id="0622b-123"><a name="bk_verifyinstall"> </a></span></span>

<span data-ttu-id="0622b-124">Puede usar las funciones XML que proporciona .NET Framework para leer y validar los agentes. config o el archivo XML fetagents. config.</span><span class="sxs-lookup"><span data-stu-id="0622b-124">You can use the XML capabilities that the .NET Framework provides to read and validate the agents.config or the fetagents.config XML file.</span></span> <span data-ttu-id="0622b-125">Para comprobar la instalación y la configuración de un agente de transporte, lea el XML en el archivo de configuración y busque el elemento [agente](agent.md) que corresponde al agente de transporte.</span><span class="sxs-lookup"><span data-stu-id="0622b-125">To verify the installation and configuration of a transport agent, read the XML in the configuration file and find the [agent](agent.md) element that corresponds to the transport agent.</span></span> <span data-ttu-id="0622b-126">Si no existe un elemento **agente** para el agente de transporte específico, el agente de transporte no está instalado.</span><span class="sxs-lookup"><span data-stu-id="0622b-126">If an **agent** element for the specific transport agent does not exist, the transport agent is not installed.</span></span> <span data-ttu-id="0622b-127">Si el agente de transporte está instalado, puede leer los atributos del elemento **Agent** para determinar su configuración.</span><span class="sxs-lookup"><span data-stu-id="0622b-127">If the transport agent is installed, you can read the attributes of the **agent** element to determine its configuration.</span></span> 
  
## <a name="configuration-file-element-hierarchy"></a><span data-ttu-id="0622b-128">Jerarquía de elementos del archivo de configuración</span><span class="sxs-lookup"><span data-stu-id="0622b-128">Configuration file element hierarchy</span></span>
<span data-ttu-id="0622b-129"><a name="bk_elementref"> </a></span><span class="sxs-lookup"><span data-stu-id="0622b-129"><a name="bk_elementref"> </a></span></span>

<span data-ttu-id="0622b-130">El siguiente código muestra la jerarquía de elementos en el archivo XML de configuración.</span><span class="sxs-lookup"><span data-stu-id="0622b-130">The following code shows the element hierarchy in the configuration XML file.</span></span>
  
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

## <a name="in-this-section"></a><span data-ttu-id="0622b-131">En esta sección</span><span class="sxs-lookup"><span data-stu-id="0622b-131">In this section</span></span>
<span data-ttu-id="0622b-132"><a name="bk_elementreflist"> </a></span><span class="sxs-lookup"><span data-stu-id="0622b-132"><a name="bk_elementreflist"> </a></span></span>

- [<span data-ttu-id="0622b-133">Representante</span><span class="sxs-lookup"><span data-stu-id="0622b-133">agent</span></span>](agent.md)
    
- [<span data-ttu-id="0622b-134">agentExecution</span><span class="sxs-lookup"><span data-stu-id="0622b-134">agentExecution</span></span>](agentexecution.md)
    
- [<span data-ttu-id="0622b-135">agentList</span><span class="sxs-lookup"><span data-stu-id="0622b-135">agentList</span></span>](agentlist.md)
    
- [<span data-ttu-id="0622b-136">configuración</span><span class="sxs-lookup"><span data-stu-id="0622b-136">configuration</span></span>](configuration.md)
    
- [<span data-ttu-id="0622b-137">messageSnapshot</span><span class="sxs-lookup"><span data-stu-id="0622b-137">messageSnapshot</span></span>](messagesnapshot.md)
    
- [<span data-ttu-id="0622b-138">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="0622b-138">mexRuntime</span></span>](mexruntime.md)
    
- [<span data-ttu-id="0622b-139">monitor</span><span class="sxs-lookup"><span data-stu-id="0622b-139">monitoring</span></span>](monitoring.md)
    
## <a name="see-also"></a><span data-ttu-id="0622b-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="0622b-140">See also</span></span>

- [<span data-ttu-id="0622b-141">Agentes de transporte en Exchange</span><span class="sxs-lookup"><span data-stu-id="0622b-141">Transport agents in Exchange</span></span>](transport-agents-in-exchange-2013.md)
- [<span data-ttu-id="0622b-142">Conceptos del agente de transporte en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="0622b-142">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)
- [<span data-ttu-id="0622b-143">Referencia del agente de transporte para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="0622b-143">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)
- [<span data-ttu-id="0622b-144">Espacios de nombres de agente de transporte en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="0622b-144">Transport agent namespaces in Exchange 2013</span></span>](transport-agent-namespaces-in-exchange-2013.md)
- [<span data-ttu-id="0622b-145">Cmdlets de flujo de correo</span><span class="sxs-lookup"><span data-stu-id="0622b-145">Mail Flow Cmdlets</span></span>](https://docs.microsoft.com/powershell/exchange/?view=exchange-ps)
    

