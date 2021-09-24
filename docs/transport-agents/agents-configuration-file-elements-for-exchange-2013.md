---
title: Elementos de archivo de configuración de agentes para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Agents
api_type:
- schema
ms.assetid: 3047653b-d712-46c1-ae0a-73f3975f5e9d
description: Busque información sobre los elementos XML en el archivo de configuración agents.config y fetagents.config en Exchange 2013.
ms.openlocfilehash: bdf394130f7818c5b956e8b15eed86a6318b9698
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510424"
---
# <a name="agents-configuration-file-elements-for-exchange-2013"></a>Elementos de archivo de configuración de agentes para Exchange 2013

Busque información sobre los elementos XML en el archivo de configuración agents.config y fetagents.config en Exchange 2013.
  
**Se aplica a:** Exchange Server 2013
  
Al instalar el rol de servidor Acceso de cliente o Buzón de correo en un servidor Exchange, el instalador crea un archivo XML que contiene información de configuración acerca de los agentes que están instalados en el servidor. No puede escribir directamente en este archivo. 
  
El servicio de transporte front-end se ejecuta en servidores de acceso de cliente y escribe en un archivo denominado fetagents.config. El servicio de transporte y el servicio de transporte de buzones de correo se ejecutan en servidores de buzones de correo y escriben en un archivo denominado agents.config. Un equipo que tenga el rol de servidor Acceso de cliente y el rol de servidor Buzón de correo tendrán un fetagents.config y un archivo agents.config cliente. 
  
La única forma admitida de escribir en estos archivos es mediante los cmdlets del agente de transporte en el Shell Exchange administración. Para obtener información acerca de los cmdlets del agente de transporte, [vea Mail Flow Cmdlets](https://technet.microsoft.com/library/aa998553%28v=exchg.150%29.aspx) on TechNet. 
  
> [!NOTE]
> Para distinguir entre los agentes que amplían el servicio de transporte front-end en el servidor de acceso de cliente y el servicio de transporte en el servidor de buzones de correo, los cmdlets de agente de transporte tienen un parámetro  _TransportService_ con un valor de "Concentrador" para el servicio de transporte y "FrontEnd" para el servicio de transporte front-end. 
  
Puede leer el archivo agents.config o fetagents.config para determinar la presencia y la información de configuración de uno o más agentes en el servidor. Esta documentación proporciona una referencia que puede usar para leer la información en el archivo agents.config o en el fetagents.config. El formato de ambos archivos es el mismo. Esta documentación no proporciona información sobre cómo escribir en los archivos.
  
> [!CAUTION]
> El uso de métodos no admitidos para escribir en el archivo agents.config o fetagents.config puede producir resultados inesperados, incluidos errores del servicio de transporte o agentes de transporte, o ambos. No escriba directamente en ninguno de estos archivos. El único método admitido para escribir en estos archivos es mediante el uso de los cmdlets de agente de transporte Exchange Shell de administración. 
  
## <a name="location-of-the-transport-agent-configuration-files"></a>Ubicación de los archivos de configuración del agente de transporte
<a name="bk_ConfigLoc"> </a>

Al instalar Exchange 2013, el instalador crea un archivo XML denominado agents.config.template o fetagents.config.template, según el rol de servidor instalado, en la carpeta \TransportRoles\Agents (donde está la carpeta en la que instaló \<ExchangeInstallFolder\> \<ExchangeInstallFolder\> Exchange 2013). Si instala el rol de servidor Acceso de cliente, Exchange 2013 copia el archivo fetagents.config.template en fetagents.config. Si instala el rol de servidor Buzón de correo, Exchange 2013 copia el archivo agents.config.template en agents.config. Exchange 2013 lee y escribe este archivo al cambiar la configuración de agentes de transporte en el servidor.
  
## <a name="verifying-a-transport-agent-installation"></a>Comprobación de una instalación de agente de transporte
<a name="bk_verifyinstall"> </a>

Puede usar las funcionalidades XML que el .NET Framework proporciona para leer y validar el archivo agents.config o el fetagents.config XML. Para comprobar la instalación y configuración de un agente de transporte, lea el XML en el archivo de configuración y busque el elemento [de](agent.md) agente que corresponde al agente de transporte. Si no **existe un** elemento de agente para el agente de transporte específico, no se instalará el agente de transporte. Si el agente de transporte está instalado, puede leer los atributos del **elemento agent** para determinar su configuración. 
  
## <a name="configuration-file-element-hierarchy"></a>Jerarquía de elementos de archivo de configuración
<a name="bk_elementref"> </a>

El código siguiente muestra la jerarquía de elementos en el archivo XML de configuración.
  
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
    
## <a name="see-also"></a>Ver también

- [Agentes de transporte en Exchange](transport-agents-in-exchange-2013.md)
- [Conceptos de agente de transporte Exchange 2013](transport-agent-concepts-in-exchange-2013.md)
- [Referencia de agente de transporte para Exchange 2013](transport-agent-reference-for-exchange-2013.md)
- [Espacios de nombres de agente de transporte Exchange 2013](transport-agent-namespaces-in-exchange-2013.md)
- [Cmdlets Flow correo](https://docs.microsoft.com/powershell/exchange/?view=exchange-ps)
    

