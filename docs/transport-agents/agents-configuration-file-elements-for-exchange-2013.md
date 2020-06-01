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
# <a name="agents-configuration-file-elements-for-exchange-2013"></a>Elementos del archivo de configuración de agentes para Exchange 2013

Busque información sobre los elementos XML en el archivo Agents. config y el archivo de configuración fetagents. config en Exchange 2013.
  
**Se aplica a:** Exchange Server 2013
  
Al instalar el rol de servidor de acceso de cliente o buzón de correo en un servidor de Exchange, el instalador crea un archivo XML que contiene información de configuración sobre los agentes que están instalados en el servidor. No puede escribir directamente en este archivo. 
  
El servicio de transporte de front-end se ejecuta en los servidores de acceso de cliente y escribe en un archivo denominado fetagents. config. El servicio de transporte y el servicio de transporte de buzones de correo se ejecutan en servidores de buzones de correo y escriben en un archivo denominado Agents. config. Un equipo que tenga el rol de servidor acceso de clientes y el rol de servidor buzón de correo tendrá un archivo fetagents. config y un archivo Agents. config. 
  
La única forma admitida de escribir en estos archivos es mediante el uso de cmdlets de agente de transporte en el shell de administración de Exchange. Para obtener información acerca de los cmdlets del agente de transporte, consulte [mail Flow cmdlets](https://technet.microsoft.com/library/aa998553%28v=exchg.150%29.aspx) en TechNet. 
  
> [!NOTE]
> Para distinguir entre agentes que amplían el servicio de transporte front-end en el servidor de acceso de cliente y el servicio de transporte en el servidor de buzones de correo, los cmdlets de agente de transporte tienen un parámetro _TransportService_ con un valor de "Hub" para el servicio de transporte y "frontend" para el servicio de transporte front-end. 
  
Puede leer el archivo Agents. config o fetagents. config para determinar la presencia y la información de configuración de uno o más agentes en el servidor. Esta documentación proporciona una referencia que puede usar para leer la información en el archivo Agents. config o en fetagents. config. El formato de ambos archivos es el mismo. En esta documentación no se proporciona información sobre cómo escribir en los archivos.
  
> [!CAUTION]
> El uso de métodos no admitidos para escribir en el archivo Agents. config o fetagents. config puede producir resultados inesperados, incluido el error del servicio de transporte o los agentes de transporte, o ambos. No escriba directamente en ninguno de estos archivos. El único método admitido para escribir en estos archivos es mediante los cmdlets del agente de transporte del shell de administración de Exchange. 
  
## <a name="location-of-the-transport-agent-configuration-files"></a>Ubicación de los archivos de configuración del agente de transporte
<a name="bk_ConfigLoc"> </a>

Al instalar Exchange 2013, el instalador crea un archivo XML que se denomina Agents. config. template o fetagents. config. template, en función de la función de servidor instalada, en la \<ExchangeInstallFolder\> carpeta \TransportRoles\Agents (donde \<ExchangeInstallFolder\> es la carpeta en la que instaló Exchange 2013). Si instala la función de servidor de acceso de cliente, Exchange 2013 copia el archivo fetagents. config. template en fetagents. config. Si instala el rol de servidor buzón de correo, Exchange 2013 copia el archivo Agents. config. template en Agents. config. Exchange 2013 Lee y escribe este archivo cuando cambia la configuración de los agentes de transporte en el servidor.
  
## <a name="verifying-a-transport-agent-installation"></a>Comprobación de la instalación de un agente de transporte
<a name="bk_verifyinstall"> </a>

Puede usar las funciones XML que proporciona .NET Framework para leer y validar los agentes. config o el archivo XML fetagents. config. Para comprobar la instalación y la configuración de un agente de transporte, lea el XML en el archivo de configuración y busque el elemento [agente](agent.md) que corresponde al agente de transporte. Si no existe un elemento **agente** para el agente de transporte específico, el agente de transporte no está instalado. Si el agente de transporte está instalado, puede leer los atributos del elemento **Agent** para determinar su configuración. 
  
## <a name="configuration-file-element-hierarchy"></a>Jerarquía de elementos del archivo de configuración
<a name="bk_elementref"> </a>

El siguiente código muestra la jerarquía de elementos en el archivo XML de configuración.
  
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

## <a name="in-this-section"></a>En esta sección
<a name="bk_elementreflist"> </a>

- [Representante](agent.md)
    
- [agentExecution](agentexecution.md)
    
- [agentList](agentlist.md)
    
- [configuración](configuration.md)
    
- [messageSnapshot](messagesnapshot.md)
    
- [mexRuntime](mexruntime.md)
    
- [monitor](monitoring.md)
    
## <a name="see-also"></a>Vea también

- [Agentes de transporte en Exchange](transport-agents-in-exchange-2013.md)
- [Conceptos del agente de transporte en Exchange 2013](transport-agent-concepts-in-exchange-2013.md)
- [Referencia del agente de transporte para Exchange 2013](transport-agent-reference-for-exchange-2013.md)
- [Espacios de nombres de agente de transporte en Exchange 2013](transport-agent-namespaces-in-exchange-2013.md)
- [Cmdlets de flujo de correo](https://docs.microsoft.com/powershell/exchange/?view=exchange-ps)
    

