---
title: Comparación de la programación de clientes de Exchange Online y Exchange local
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3c2eabe4-52bc-461e-a6dd-f65f22f16e50
description: Obtenga información sobre las consideraciones de diseño para crear una API administrada de EWS o una aplicación cliente de EWS que funcione con Exchange Online y Exchange local.
ms.openlocfilehash: 8b4dbae5cadfed377aa3a7179144a7cea68bc35c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456167"
---
# <a name="comparing-exchange-online-and-exchange-on-premises-client-programming"></a>Comparación de la programación de clientes de Exchange Online y Exchange local

Obtenga información sobre las consideraciones de diseño para crear una API administrada de EWS o una aplicación cliente de EWS que funcione con Exchange Online y Exchange local.
  
En la mayoría de los casos, los clientes y los servicios Web de Exchange de destino funcionarán de la misma forma independientemente de si el destino es un Exchange Online, Exchange online como parte de Office 365 o un servidor local de Exchange. Sin embargo, hay algunas excepciones y querrá asegurarse de que la aplicación puede administrarlas. Use la información de este artículo como ayuda para diseñar el cliente de como destino Exchange Online y Exchange local.

<a name="autodiscover"> </a>

## <a name="autodiscover-client-programming-considerations"></a>Consideraciones sobre la programación de clientes de detección automática

[Detección automática](autodiscover-for-exchange.md) proporciona información de configuración para los clientes de Exchange. Una aplicación cliente puede detectar su información de configuración de una de estas tres maneras, en función de si el cliente está destinado a Exchange online o Exchange local. 
  
**Tabla 1. Tipos de servicio de detección automática y aplicabilidad de Exchange**

|**Tipo de servicio Detección automática**|**Se aplica a**|
|:-----|:-----|
|[Detección automática de SOAP](autodiscover-for-exchange.md#bk_Options) <br/> |Exchange Online y versiones de Exchange locales a partir de Exchange 2010  <br/> |
|[Detección automática de POX ](autodiscover-for-exchange.md#bk_Options) <br/> |Exchange Online y versiones de Exchange locales a partir de Exchange 2007  <br/> |
|[Búsqueda de punto de conexión de servicio (SCP)](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md) <br/> |Versiones de Exchange local a partir de Exchange 2007  <br/> |
   
Además de la información de configuración del cliente, la detección automática SOAP y POX también devuelve la versión del servicio de Exchange e indica si Exchange Online hospeda el servicio. Esta información se devuelve en elementos diferentes, según el tipo de detección automática que se use.
  
**Tabla 2. Elementos de detección automática que devuelven la versión del servicio y la información de hospedaje de Exchange Online**

|**Tipo de servicio Detección automática**|**Elemento XML que contiene la versión de servicio**|**Elemento XML que indica si el usuario tiene una cuenta de Exchange Online**|
|:-----|:-----|:-----|
|Detección automática de SOAP  <br/> |Elemento de [configuración (SOAP)](https://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) con el valor de texto **CasVersion** .  <br/> |Elemento de [configuración (SOAP)](https://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) con el valor de texto **UserMSOnline** .  <br/> |
|Detección automática de POX   <br/> |[ServerVersion (POX)](https://msdn.microsoft.com/library/2c0bc41c-2452-4fc8-a19c-0e85f9fdbc4a%28Office.15%29.aspx) <br/> |**MicrosoftOnline** <br/> |
   
Asegúrese de que el cliente captura esta información para que pueda dirigirse al [conjunto de características](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md) que está disponible en el servidor de Exchange. Esto puede ser útil para determinar si el cliente puede esperar un comportamiento diferente en función de si el buzón de correo del usuario se encuentra en una organización de Exchange online o de Exchange local. 

<a name="testing"> </a>

## <a name="testing-and-log-files-in-applications-that-target-exchange-online"></a>Pruebas y archivos de registro en aplicaciones destinadas a Exchange Online

Exchange online no proporciona acceso a los archivos de registro de protocolo EWS, los contadores de rendimiento EWS y los eventos de servicio relacionados con EWS que están disponibles en los servidores de Exchange locales. Sin embargo, el acceso a ellos es útil para descubrir cómo realiza la aplicación cuando interactúa con EWS. Asegúrese de probar la aplicación con un servidor local de Exchange de prueba para poder optimizar su rendimiento. Si es posible, puede [cambiar la configuración de limitación](https://technet.microsoft.com/library/bb232205%28v=exchg.150%29.aspx#Policies) en el servidor de prueba para que se ajuste a la configuración de limitación de Exchange Online, de modo que pueda evaluar cómo se comportará la aplicación cuando se conecte a Exchange Online. 
  
> [!TIP]
> Puede usar la herramienta [EWSRelentless](https://ewsrelentless.codeplex.com/) para realizar una prueba de carga de EWS. Puede usar esta herramienta con un servidor de prueba, los registros de protocolo EWS, los contadores de rendimiento de EWS, los eventos de servicio y la configuración de limitación de EWS para comprender mejor cómo funciona EWS con Load. 

<a name="throttling"> </a>

## <a name="throttling-settings-and-exchange-online"></a>Configuración de limitación y Exchange Online

Los valores predeterminados para la [configuración de limitación de EWS](ews-throttling-in-exchange.md) son distintos para Exchange online que para Exchange local. Además, no puede cambiar la configuración de limitación de Exchange Online. Puede usar los cmdlets del shell de administración de Exchange para descubrir la configuración de limitación de Exchange local; sin embargo, estos cmdlets no están habilitados para Exchange Online. 

<a name="ems"> </a>

## <a name="exchange-management-shell-cmdlets-and-configuration-settings"></a>Opciones de configuración y cmdlets del shell de administración de Exchange

Varios cmdlets pueden afectar directa o indirectamente a las API de servicio Web en Exchange Online y Exchange local. Los cmdlets no están disponibles para los siguientes en Exchange Online:
  
- Configuración de limitación 
    
- Configuración del directorio virtual 
    
- Configuración de autenticación
    
Para más información sobre los cmdlets que están disponibles para Exchange Online, consulte [cmdlets de PowerShell en Exchange Online](http://help.outlook.com/140/dd575549.aspx). Para obtener más información acerca de los cmdlets que están disponibles para Exchange local, consulte [cmdlets de exchange 2013](https://technet.microsoft.com/library/bb124413%28v=exchg.150%29.aspx).
  
## <a name="client-affinity-and-network-load-balancers"></a>Afinidad de cliente y equilibradores de carga de red
<a name="affinity"> </a>

La mayoría de las comunicaciones de EWS no requieren que el cliente participe en el mantenimiento de la afinidad con Exchange. Las suscripciones a eventos de buzón de correo requieren que el cliente proporcione cookies y otra información para mantener la afinidad con el servidor de Exchange que mantiene la cola de eventos de buzón de un usuario. Exchange Server 2010 usa exchangecookie para mantener la afinidad de cliente en los equilibradores de carga de red. Exchange Online y las versiones de Exchange local que comienzan con Exchange 2013 usan el [encabezado x-AnchorMailbox, el encabezado x-PreferServerAffinity y la cookie x-BackEndOverrideCookie](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_howmaintained) para mantener la afinidad de las notificaciones de buzón de correo. 
  
## <a name="authentication"></a>Autenticación
<a name="auth"> </a>

Los clientes pueden autenticarse con Exchange online mediante Basic o OAuth. Las versiones de Exchange local que comienzan con Exchange 2013 usan NTLM de forma predeterminada; sin embargo, es posible configurar Exchange local para que también use la autenticación básica. 
  
## <a name="client-latency-diagnostics"></a>Diagnósticos de latencia de cliente
<a name="diag"> </a>

Exchange Online recopila el diagnóstico de latencia de cliente si se informa de ellos. Esto ayuda a Microsoft a solucionar problemas de conectividad con Exchange Online. Exchange local no recopila diagnósticos de latencia de cliente. Si el cliente tiene como destino Exchange en el entorno local, el cliente no puede informar del diagnóstico de latencia al servidor.
  
## <a name="functionality-in-the-ews-managed-api"></a>Funcionalidad en la API administrada de EWS
<a name="ewsma"> </a>

La API administrada de EWS expone algunas funciones específicas de Exchange local, como la búsqueda de conexiones de punto de servicio y algunas funciones específicas de Exchange Online, como los informes de latencia de cliente. Tenga en cuenta que es posible implementar algunas funcionalidades en Exchange Online antes de implementarlas en la API administrada de EWS. 
  
La siguiente funcionalidad de la API administrada de EWS solo se aplica a Exchange Online:
  
- Informes de latencia de cliente
    
- Autenticación previa básica
    
- La capacidad de solicitar que se devuelva RequestId en respuestas
    
## <a name="api-features-in-exchange-online-plans-and-exchange-server-editions"></a>Características de la API en los planes de Exchange Online y las ediciones de Exchange Server
<a name="exo"> </a>

Los distintos conjuntos de características pueden estar disponibles en distintos planes de Office 365 y Exchange Online, o en las versiones Standard y Enterprise de Exchange Server. Tenga en cuenta que algunas funciones de API podrían no estar disponibles para la aplicación cliente según el plan de Exchange online o la edición de Exchange Server que hospeda el buzón de un usuario. 
  
**Tabla 3. Variaciones de características de la API en planes y ediciones**

|**Característica de la API**|**Consideraciones de planeación o edición**|
|:-----|:-----|

| Acceso de EWS a cuentas, excepto mediante la suplantación de Exchange  <br/> | No se permite en los [planes de Office 365 para empresas: quiosco](https://office.microsoft.com/business/compare-office-365-kiosk-plans-FX103178917.aspx).  <br/> |


| Mensajería unificada (UM)  <br/> | Solo disponible con Office 365 Enterprise (E3) Plan, Exchange Online plan 2 y Exchange Server 2013 Enterprise Edition.  <br/> | | Integración de servicios de dominio de Active Directory (AD DS)  <br/> | No disponible en el plan Office 365 Small Business and Office 365 Small Business Premium.  <br/> | | Information Rights Management, archiving y retenciones legales  <br/> | Solo disponible con los planes de Office 365 Enterprise (E3 y E4).  <br/> | | Protección contra la pérdida de datos  <br/> | Solo disponible con los planes de Office 365 Enterprise, Exchange Online plan 2 y Exchange Server 2013 Enterprise Edition.  <br/> |
   
Como la disponibilidad de las características puede cambiar, le recomendamos que revise los planes de Exchange Online y las ediciones de Exchange Server para evaluar cómo puede afectar la disponibilidad de las características a su cliente. También puede diseñar el cliente para comprobar la disponibilidad de la característica mediante el uso de la [operación GetServiceConfiguration](how-to-get-service-configuration-information-by-using-ews-in-exchange.md) o mediante el envío de solicitudes de prueba para las operaciones que implementan las características. Si la característica no está disponible, la respuesta del servidor le indicará como tal. 
  
## <a name="other-considerations"></a>Otras consideraciones
<a name="other"> </a>

Puede hacer lo siguiente al dirigirse a Exchange local, pero no a Exchange Online:
  
- Cree un cliente que esté instalado en el servidor de Exchange. 
    
- Instale [agentes de transporte personalizados](../transport-agents/transport-agents-in-exchange-2013.md) que puedan afectar la entrega y el contenido de los mensajes que cree y envíe con EWS y otros clientes. 
    
## <a name="see-also"></a>Vea también

- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
- [Comparación de Exchange Online y Exchange Server 2013](https://blogs.technet.com/b/exchange/archive/2012/09/19/comparing-exchange-online-and-exchange-server-2013.aspx)  
- [Comparar todos los planes de Office 365 para empresas](https://office.microsoft.com/business/compare-all-office-365-for-business-plans-FX104051403.aspx)
- [EwsRelentless: herramienta de generación de carga EWS](https://ewsrelentless.codeplex.com/)
- [Disponibilidad de características de API de servicio Web en Exchange y la API administrada de EWS](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md)
- [Limitación de EWS en Exchange](ews-throttling-in-exchange.md)
    

