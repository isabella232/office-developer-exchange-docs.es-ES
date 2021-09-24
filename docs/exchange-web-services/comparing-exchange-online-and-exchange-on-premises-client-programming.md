---
title: Comparación la programación de Exchange Online y el cliente de Exchange local
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 3c2eabe4-52bc-461e-a6dd-f65f22f16e50
description: Obtenga información sobre las consideraciones de diseño para crear una api administrada EWS o una aplicación cliente EWS que funcione con Exchange Online y Exchange local.
ms.openlocfilehash: 438965656e31eca586d06a5e0b6794c0eda87621
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512292"
---
# <a name="comparing-exchange-online-and-exchange-on-premises-client-programming"></a>Comparación la programación de Exchange Online y el cliente de Exchange local

Obtenga información sobre las consideraciones de diseño para crear una api administrada EWS o una aplicación cliente EWS que funcione con Exchange Online y Exchange local.
  
En la mayoría de los casos, los clientes y los servicios web de Exchange de destino funcionarán de la misma manera independientemente de si el destino es un Exchange Online, Exchange Online como parte de Office 365 o Exchange servidor local. Sin embargo, hay algunas excepciones y querrás asegurarte de que la aplicación pueda controlarlas. Use la información de este artículo para ayudarle a diseñar el cliente para que se Exchange Online y Exchange local.

<a name="autodiscover"> </a>

## <a name="autodiscover-client-programming-considerations"></a>Consideraciones de programación de cliente de detección automática

[Detección automática](autodiscover-for-exchange.md) proporciona información de configuración para Exchange clientes. Una aplicación cliente puede detectar su información de configuración de una de tres maneras, en función de si el cliente está destinado Exchange Online o Exchange local. 
  
**Tabla 1. Tipos de servicio de detección automática y Exchange aplicabilidad**

|**Tipo de servicio de detección automática**|**Se aplica a**|
|:-----|:-----|
|[Detección automática de SOAP](autodiscover-for-exchange.md#bk_Options) <br/> |Exchange Online versiones de Exchange locales a partir de Exchange 2010  <br/> |
|[Detección automática de POX ](autodiscover-for-exchange.md#bk_Options) <br/> |Exchange Online versiones de Exchange locales a partir de Exchange 2007  <br/> |
|[Búsqueda de punto de conexión de servicio (SCP)](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md) <br/> |Versiones de Exchange locales a partir de Exchange 2007  <br/> |
   
Además de la información de configuración del cliente, esa detección automática SOAP y POX también devuelve la versión de servicio Exchange e indica si el servicio está hospedado por Exchange Online. Esta información se devuelve en diferentes elementos, según el tipo de detección automática que use.
  
**Tabla 2. Elementos de detección automática que devuelven la versión del servicio Exchange Online información de hospedaje**

|**Tipo de servicio de detección automática**|**Elemento XML que contiene la versión de servicio**|**Elemento XML que indica si el usuario tiene una Exchange Online cuenta**|
|:-----|:-----|:-----|
|Detección automática de SOAP  <br/> |[Elemento Setting (SOAP)](https://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) con el valor de texto **CasVersion.**  <br/> |[Elemento Setting (SOAP)](https://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) con el valor de texto **UserMSOnline.**  <br/> |
|Detección automática de POX   <br/> |[ServerVersion (POX)](https://msdn.microsoft.com/library/2c0bc41c-2452-4fc8-a19c-0e85f9fdbc4a%28Office.15%29.aspx) <br/> |**MicrosoftOnline** <br/> |
   
Asegúrese de que el cliente captura esta [](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md) información para que pueda dirigirse al conjunto de características que está disponible en el Exchange servidor. Esto puede ser útil para determinar si el cliente puede esperar un comportamiento diferente en función de si el buzón del usuario se encuentra en una organización Exchange Online o Exchange local. 

<a name="testing"> </a>

## <a name="testing-and-log-files-in-applications-that-target-exchange-online"></a>Prueba y registro de archivos en aplicaciones destinadas a Exchange Online

Exchange Online proporciona acceso a los archivos de registro del protocolo EWS, los contadores de rendimiento ews y los eventos de servicio relacionados con EWS que están disponibles en servidores Exchange local. Sin embargo, el acceso a estos es útil para descubrir cómo funciona la aplicación cuando interactúa con EWS. Asegúrese de probar la aplicación en un servidor Exchange local para que pueda optimizar su rendimiento. Si es posible, puede cambiar la configuración de limitación en el servidor de prueba para que coincida con la configuración de limitación de Exchange Online, de modo que pueda evaluar cómo se comportará la aplicación cuando se conecte a Exchange Online. [](https://technet.microsoft.com/library/bb232205%28v=exchg.150%29.aspx#Policies) 
  
> [!TIP]
> Puede usar la herramienta [EWSRelentless para](https://ewsrelentless.codeplex.com/) realizar una prueba de carga de EWS. Puede usar esta herramienta con un servidor de prueba, los registros de protocolo EWS, los contadores de rendimiento de EWS, los eventos de servicio y la configuración de limitación de EWS para comprender mejor el rendimiento de EWS bajo carga. 

<a name="throttling"> </a>

## <a name="throttling-settings-and-exchange-online"></a>Configuración de limitación y Exchange Online

Los valores predeterminados de la configuración de limitación de [EWS](ews-throttling-in-exchange.md) son diferentes para Exchange Online que para Exchange locales. Además, no puede cambiar la Exchange Online de limitación. Puede usar los cmdlets Exchange Shell de administración para detectar la configuración de limitación de Exchange local; sin embargo, estos cmdlets no están habilitados para Exchange Online. 

<a name="ems"> </a>

## <a name="exchange-management-shell-cmdlets-and-configuration-settings"></a>Exchange Cmdlets y opciones de configuración del Shell de administración

Varios cmdlets pueden afectar directa o indirectamente a las API de servicio web en Exchange Online y Exchange local. Los cmdlets no están disponibles para lo siguiente en Exchange Online:
  
- Configuración de limitación 
    
- Configuración del directorio virtual 
    
- Configuración de autenticación
    
Para obtener más información acerca de los cmdlets que están disponibles para Exchange Online, vea [Cmdlets de PowerShell en Exchange Online](http://help.outlook.com/140/dd575549.aspx). Para obtener más información acerca de los cmdlets que están disponibles Exchange locales, vea [Exchange cmdlets de 2013](https://technet.microsoft.com/library/bb124413%28v=exchg.150%29.aspx).
  
## <a name="client-affinity-and-network-load-balancers"></a>Equilibradores de carga de red y afinidad de cliente
<a name="affinity"> </a>

La mayoría de las comunicaciones EWS no requieren que el cliente participe en el mantenimiento de la afinidad con Exchange. Las suscripciones a eventos de buzón requieren que el cliente proporcione cookies y otra información para mantener la afinidad con el servidor de Exchange que mantiene la cola de eventos de buzón de un usuario. Exchange Server 2010 usa exchangecookie para mantener la afinidad de cliente en los equilibradores de carga de red. Exchange Online y las versiones de Exchange locales a partir de Exchange 2013 usan el encabezado [X-AnchorMailbox, el encabezado X-PreferServerAffinity y la cookie X-BackEndOverrideCookie](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_howmaintained) para mantener la afinidad de las notificaciones de buzones. 
  
## <a name="authentication"></a>Autenticación
<a name="auth"> </a>

Los clientes pueden autenticarse Exchange Online mediante Basic o OAuth. Las versiones Exchange locales a partir de Exchange 2013 usan NTLM de forma predeterminada; sin embargo, es posible configurar Exchange local para usar la autenticación básica también. 
  
## <a name="client-latency-diagnostics"></a>Diagnósticos de latencia de cliente
<a name="diag"> </a>

Exchange Online recopila diagnósticos de latencia de cliente si se notifican. Esto ayuda a Microsoft a solucionar problemas de conectividad con Exchange Online. Exchange local no recopila diagnósticos de latencia de cliente. Si el cliente está Exchange local, el cliente no puede notificar diagnósticos de latencia al servidor.
  
## <a name="functionality-in-the-ews-managed-api"></a>Funcionalidad en la API administrada de EWS
<a name="ewsma"> </a>

La API administrada ews expone algunas funciones específicas de Exchange locales, como la búsqueda de conexiones de punto de servicio y algunas funciones específicas de Exchange Online, como los informes de latencia de cliente. Tenga en cuenta que es posible que algunas funciones se implementen en Exchange Online antes de que se implemente en la API administrada ews. 
  
La siguiente funcionalidad de LA API administrada ews solo se aplica a Exchange Online:
  
- Informes de latencia de cliente
    
- Autenticación previa básica
    
- La capacidad de solicitar que el RequestId se devuelva en respuestas
    
## <a name="api-features-in-exchange-online-plans-and-exchange-server-editions"></a>Características de API en Exchange Online planes y Exchange Server ediciones
<a name="exo"> </a>

Los distintos conjuntos de características pueden estar disponibles en Office 365 y Exchange Online planes, o en las versiones estándar y empresarial de Exchange Server. Tenga en cuenta que es posible que algunas funciones de api no estén disponibles para la aplicación cliente en función del plan Exchange Online o la edición Exchange Server que hospeda el buzón de un usuario. 
   
Dado que la disponibilidad de características puede cambiar, se recomienda comprobar los planes de Exchange Online y las ediciones Exchange Server para evaluar cómo la disponibilidad de características puede afectar al cliente. También puede diseñar el cliente para comprobar la disponibilidad de características mediante la operación [GetServiceConfiguration](how-to-get-service-configuration-information-by-using-ews-in-exchange.md) o enviando solicitudes de prueba para las operaciones que implementan las características. Si la característica no está disponible, la respuesta del servidor lo indicará como tal. 
  
## <a name="other-considerations"></a>Otras consideraciones
<a name="other"> </a>

Puede hacer lo siguiente al dirigirse a Exchange local, pero no Exchange Online:
  
- Cree un cliente que esté instalado en el Exchange servidor. 
    
- Instale [agentes de transporte personalizados](../transport-agents/transport-agents-in-exchange-2013.md) que puedan afectar a la entrega y al contenido de los mensajes que cree y envíe con EWS y otros clientes. 
    
## <a name="see-also"></a>Ver también

- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
- [Comparación Exchange Online y Exchange Server 2013](https://blogs.technet.com/b/exchange/archive/2012/09/19/comparing-exchange-online-and-exchange-server-2013.aspx)  
- [Comparar todos los Office 365 planes para empresas](https://office.microsoft.com/business/compare-all-office-365-for-business-plans-FX104051403.aspx)
- [EwsRelentless: herramienta de generación de carga ews](https://ewsrelentless.codeplex.com/)
- [Disponibilidad de características de API de servicio web en Exchange y la API administrada ews](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md)
- [Limitación de EWS en Exchange](ews-throttling-in-exchange.md)
    

