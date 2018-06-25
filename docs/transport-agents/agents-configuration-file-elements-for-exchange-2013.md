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
# <a name="agents-configuration-file-elements-for-exchange-2013"></a>Elementos del archivo de configuración de los agentes para Exchange 2013

Busque información sobre los elementos XML en el archivo de configuración agents.config y fetagents.config en Exchange 2013.
  
**Se aplica a:** Exchange Server 2013
  
Cuando se instala el acceso de cliente o el rol de servidor de buzón de correo en un servidor de Exchange, el programa de instalación crea un archivo XML que contiene información de configuración acerca de los agentes que están instalados en el servidor. No se puede escribir directamente a este archivo. 
  
El servicio de transporte Front-End se ejecuta en servidores de acceso de cliente y se escribe en un archivo denominado fetagents.config. El servicio de transporte y el servicio de transporte de buzón de correo ejecutan en servidores de buzones y escriben en un archivo denominado agents.config. Un equipo que tiene el rol de servidor de acceso de cliente y el rol de servidor de buzón de correo tendrán un fetagents.config y un archivo agents.config. 
  
Es la única forma admitida para escribir en estos archivos mediante el uso de los cmdlets de agente de transporte en el Shell de administración de Exchange. Para obtener información acerca de los cmdlets de agente de transporte, consulte [Cmdlets de flujo de correo](http://technet.microsoft.com/en-us/library/aa998553%28v=exchg.150%29.aspx) en TechNet. 
  
> [!NOTE]
> Para distinguir entre los agentes que amplían el servicio de transporte Front-End en el servidor de acceso de cliente y el servicio de transporte en el servidor de buzón de correo, los cmdlets de agente de transporte tiene un parámetro de _TransportService_ con un valor de "Concentrador" para el transporte servicio y "FrontEnd" para el servicio de transporte Front-End. 
  
Puede leer el agents.config o el archivo fetagents.config para determinar la presencia de y la información de configuración para uno o varios agentes en el servidor. Esta documentación proporciona una referencia que puede usar para leer la información en el archivo agents.config o la fetagents.config. El formato de ambos de estos archivos es el mismo. Esta documentación no proporciona información acerca de cómo escribir en los archivos.
  
> [!CAUTION]
> Uso de métodos no admitidos para escribir en el archivo agents.config o fetagents.config puede producir resultados inesperados, incluido el error del servicio de transporte o los agentes de transporte o ambos. No se escriben directamente a cualquiera de estos archivos. Es el único método admitido para escribir en estos archivos mediante el uso de los cmdlets de agente de transporte de Exchange Management Shell. 
  
## <a name="location-of-the-transport-agent-configuration-files"></a>Ubicación de los archivos de configuración del agente de transporte
<a name="bk_ConfigLoc"> </a>

Al instalar Exchange 2013, el programa de instalación crea un archivo XML que se denomina agents.config.template o fetagents.config.template, según el rol de servidor instalado, en la \<ExchangeInstallFolder\>\TransportRoles\Agents carpeta (donde \<ExchangeInstallFolder\> es la carpeta en la que ha instalado Exchange 2013). Si instala el rol de servidor de acceso de cliente, Exchange 2013 copia el archivo fetagents.config.template a fetagents.config. Si instala el rol de servidor de buzón de correo, Exchange 2013 copia el archivo agents.config.template en agents.config. Exchange 2013 lee y escribe en este archivo cuando se cambia la configuración de los agentes de transporte en el servidor.
  
## <a name="verifying-a-transport-agent-installation"></a>Comprobar una instalación de agente de transporte
<a name="bk_verifyinstall"> </a>

Puede usar las capacidades XML que proporciona .NET Framework para leer y validar el agents.config o el archivo XML de fetagents.config. Para comprobar la instalación y configuración de un agente de transporte, leer el archivo XML en el archivo de configuración y busque el elemento de [agente](agent.md) que se corresponde con el agente de transporte. Si no existe un elemento de **agente** para el agente de transporte específica, no está instalado el agente de transporte. Si está instalado el agente de transporte, puede leer los atributos del elemento de **agente** para determinar su configuración. 
  
## <a name="configuration-file-element-hierarchy"></a>Jerarquía de elementos del archivo de configuración
<a name="bk_elementref"> </a>

El código siguiente muestra la jerarquía de elementos del archivo de configuración XML.
  
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

- [agente](agent.md)
    
- [agentExecution](agentexecution.md)
    
- [agentList](agentlist.md)
    
- [configuración](configuration.md)
    
- [messageSnapshot](messagesnapshot.md)
    
- [mexRuntime](mexruntime.md)
    
- [supervisión](monitoring.md)
    
## <a name="see-also"></a>Vea también

- [Los agentes de transporte en Exchange](transport-agents-in-exchange-2013.md)
- [Conceptos de agente en Exchange 2013 de transporte](transport-agent-concepts-in-exchange-2013.md)
- [Referencia de agente de transporte de Exchange 2013](transport-agent-reference-for-exchange-2013.md)
- [Espacios de nombres de agente en Exchange 2013 de transporte](transport-agent-namespaces-in-exchange-2013.md)
- [Cmdlets de flujo de correo](https://docs.microsoft.com/en-us/powershell/exchange/?view=exchange-ps)
    

