---
title: Comparación de Exchange Online y la programación de cliente de Exchange local
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3c2eabe4-52bc-461e-a6dd-f65f22f16e50
description: Obtenga información sobre las consideraciones de diseño para la creación de una aplicación de cliente EWS que funcione con Exchange Online y Exchange local o la API administrada de EWS.
ms.openlocfilehash: 87c6ee476e06b50c339901bf61020b0fc98f8486
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763021"
---
# <a name="comparing-exchange-online-and-exchange-on-premises-client-programming"></a>Comparación de Exchange Online y la programación de cliente de Exchange local

Obtenga información sobre las consideraciones de diseño para la creación de una aplicación de cliente EWS que funcione con Exchange Online y Exchange local o la API administrada de EWS.
  
Para la mayor parte, los clientes y la web de servicios de Exchange tienen como objetivo funcionará del mismo modo, independientemente de si el destino es un Exchange Online, Exchange Online como parte de Office 365, Exchange local o en servidor. Sin embargo, hay algunas excepciones, y desea asegurarse de que su aplicación puede tratar a ellos. Use la información de este artículo para ayudarle a diseñar el cliente para dirigir ambos Exchange Online y Exchange local.

<a name="autodiscover"> </a>

## <a name="autodiscover-client-programming-considerations"></a>Consideraciones de programación de cliente de detección automática

[Detección automática](autodiscover-for-exchange.md) proporciona información de configuración para los clientes de Exchange. Una aplicación cliente puede detectar su información de configuración en uno de tres maneras, dependiendo de si el cliente es dirigir contenido Exchange Online o Exchange local. 
  
**La tabla 1. Tipos de servicio de detección automática y la capacidad de aplicación de Exchange**

|**Tipo de servicio de detección automática**|**Se aplica a**|
|:-----|:-----|
|[Detección automática de SOAP](autodiscover-for-exchange.md#bk_Options) <br/> |Exchange Online y versiones de Exchange local iniciando con Exchange 2010  <br/> |
|[Detección automática de POX ](autodiscover-for-exchange.md#bk_Options) <br/> |Exchange Online y versiones de Exchange local iniciando con Exchange 2007  <br/> |
|[Búsqueda de servicio (SCP) de punto de conexión](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md) <br/> |Versiones de Exchange local iniciando con Exchange 2007  <br/> |
   
Además de la información de configuración cliente, que SOAP y detección automática de POX también devuelven la versión de servicio de Exchange e indican si el servicio está hospedado por Exchange Online. Esta información se devuelve en elementos diferentes, según el tipo de detección automática que use.
  
**Tabla 2. Elementos de detección automática que devuelven la versión del service y Exchange Online información de hospedaje**

|**Tipo de servicio de detección automática**|**Elemento XML que contiene la versión de servicio**|**Elemento XML que indica si el usuario tiene una cuenta de Exchange Online**|
|:-----|:-----|:-----|
|Detección automática de SOAP  <br/> |Elemento de [Configuración (SOAP)](http://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) con el valor de texto **CasVersion** .  <br/> |Elemento de [Configuración (SOAP)](http://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) con el valor de texto **UserMSOnline** .  <br/> |
|Detección automática de POX   <br/> |[ServerVersion (POX)](http://msdn.microsoft.com/library/2c0bc41c-2452-4fc8-a19c-0e85f9fdbc4a%28Office.15%29.aspx) <br/> |**MicrosoftOnline** <br/> |
   
Asegúrese de que el cliente de captura esta información, por lo que se puede orientar el [conjunto de características](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md) que está disponible en el servidor de Exchange. Esto puede resultar útil para determinar si su cliente puede esperar un comportamiento diferente en función de si el buzón del usuario se encuentra en un Exchange Online o Exchange organización local. 

<a name="testing"> </a>

## <a name="testing-and-log-files-in-applications-that-target-exchange-online"></a>Archivos de registro y las pruebas en las aplicaciones que estén destinados a Exchange Online

Exchange Online no proporciona acceso a los archivos de registro del protocolo EWS, contadores de rendimiento de EWS y eventos de servicio relacionadas con EWS que están disponibles en los servidores de Exchange locales. Acceso a estas es útil, sin embargo, para descubrir cómo se realiza la aplicación cuando interactúa con EWS. Asegúrese de probar la aplicación en un servidor de Exchange local de prueba para que puede optimizar su rendimiento. Si es posible, se puede [cambiar la configuración de limitación](http://technet.microsoft.com/en-us/library/bb232205%28v=exchg.150%29.aspx#Policies) en el servidor de prueba para que coincida con la configuración de limitación para Exchange Online, por lo que puede evaluar el comportamiento de la aplicación cuando se conecta a Exchange Online. 
  
> [!TIP]
> Puede usar la herramienta [EWSRelentless](https://ewsrelentless.codeplex.com/) para llevar a cabo una prueba de carga EWS. Puede usar esta herramienta con un servidor de prueba, los registros de protocolo EWS, contadores de rendimiento de EWS, eventos de servicio y la configuración de la limitación de EWS para comprender mejor cómo realiza EWS bajo carga. 

<a name="throttling"> </a>

## <a name="throttling-settings-and-exchange-online"></a>La configuración de limitación y Exchange Online

Los valores predeterminados para la [configuración de la limitación EWS](ews-throttling-in-exchange.md) son diferentes para Exchange Online para Exchange local. Además, no puede cambiar la configuración de limitación Exchange Online. Puede usar los cmdlets del Shell de administración de Exchange para detectar la configuración de limitación para Exchange local; Sin embargo, los cmdlets no están habilitados para Exchange Online. 

<a name="ems"> </a>

## <a name="exchange-management-shell-cmdlets-and-configuration-settings"></a>Configuración de los cmdlets y la configuración del Shell de administración de Exchange

Un número de cmdlets puede directa o indirectamente afectan a las API del servicio web de Exchange en línea y local de Exchange. Cmdlets de no están disponibles para los siguientes procedimientos en Exchange Online:
  
- La configuración de limitación 
    
- Configuración del directorio virtual 
    
- Configuración de autenticación
    
Para obtener información detallada acerca de los cmdlets que están disponibles para Exchange Online, consulte [cmdlets de PowerShell en Exchange Online](http://help.outlook.com/en-us/140/dd575549.aspx). Para obtener más información acerca de los cmdlets que están disponibles para Exchange local, consulte [Exchange 2013 cmdlets](http://technet.microsoft.com/en-us/library/bb124413%28v=exchg.150%29.aspx).
  
## <a name="client-affinity-and-network-load-balancers"></a>Equilibradores de carga de red y la afinidad del cliente
<a name="affinity"> </a>

La mayoría de EWS de comunicación no requiere que el cliente de participar en el mantenimiento de afinidad con Exchange. Las suscripciones a eventos de buzón de correo requieren que el cliente de proporcionar las cookies y otra información para mantener la afinidad con el servidor de Exchange que mantiene la cola de eventos de buzón de correo para un usuario. Exchange Server 2010 usa el exchangecookie para mantener la afinidad del cliente a través de los equilibradores de carga de red. Exchange Online y versiones de Exchange local iniciando con Exchange 2013 usan [encabezado X-AnchorMailbox, encabezado X-PreferServerAffinity y X-BackEndOverrideCookie cookie](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_howmaintained) para mantener la afinidad para las notificaciones de buzón de correo. 
  
## <a name="authentication"></a>Autenticación
<a name="auth"> </a>

Los clientes pueden autenticarse con Exchange Online mediante el uso de Basic o OAuth. Las versiones de Exchange local iniciando con Exchange 2013 usar NTLM de forma predeterminada; Sin embargo, es posible configurar Exchange local para usar la autenticación básica. 
  
## <a name="client-latency-diagnostics"></a>Diagnósticos de latencia de cliente
<a name="diag"> </a>

Exchange Online recopila diagnósticos de latencia de cliente si se informan de. Esto ayuda a soporte técnico de Microsoft a solucionar problemas de conectividad con Exchange Online. Exchange local no recopilar diagnósticos de latencia de cliente. Si dirige a su cliente de Exchange local, el cliente no puede notificar diagnósticos de latencia en el servidor.
  
## <a name="functionality-in-the-ews-managed-api"></a>API administrada de funcionalidad en la dirección URL de EWS
<a name="ewsma"> </a>

La API administrada de EWS expone la funcionalidad de algunos que es específico de Exchange local, como la búsqueda del servicio de punto de conexión y parte de la funcionalidad que es específica de Exchange Online, como informes de latencia de cliente. Tenga en cuenta que es posible que algunas funcionalidades que implementarse en Exchange Online antes de que se implementa en la API administrada de EWS. 
  
Las siguientes funciones de la API administrada de EWS sólo es aplicable a Exchange Online:
  
- Informes de latencia de cliente
    
- Autenticación básica previa
    
- La capacidad para solicitar que se devuelva el ID en las respuestas
    
## <a name="api-features-in-exchange-online-plans-and-exchange-server-editions"></a>Características de la API en las ediciones de Exchange Server y los planes de Exchange Online
<a name="exo"> </a>

Conjuntos de características diferentes pueden estar disponibles en diferentes planes de Office 365 y Exchange Online, o en las versiones standard y enterprise de Exchange Server. Tenga en cuenta que es podrían que algunas funcionalidades de API no estén disponibles para la aplicación de cliente según el plan de Exchange Online o edition de Exchange Server que hospeda el buzón de un usuario. 
  
**Tabla 3. Variantes de la característica de API a través de los planes y las ediciones**

|**Característica de API**|**Consideraciones de planeación o edition**|
|:-----|:-----|
|EWS tener acceso a las cuentas, excepto a través de la suplantación de Exchange  <br/> |No se permite en el [Office 365 para la empresa: planes de quiosco](http://office.microsoft.com/en-us/business/compare-office-365-kiosk-plans-FX103178917.aspx).  <br/> |
|Mensajería unificada (UM)  <br/> |Sólo está disponible con las ediciones de Exchange Server 2013 Enterprise, Exchange Online Plan 2 y plan de Office 365 Enterprise (E3).  <br/> |
|La integración de servicios de dominio de Active Directory (AD DS)  <br/> |No está disponible con el plan de Office 365 pequeña empresa y Office 365 Small Business Premium.  <br/> |
|Las suspensiones de Information Rights Management, archivado y legales  <br/> |Sólo está disponible con los planes de Office 365 Enterprise (E3 y E4).  <br/> |
|Protección ante la pérdida de datos  <br/> |Sólo está disponible con los planes de empresa de Office 365, Exchange Online Plan 2 y las ediciones empresariales de Exchange Server 2013.  <br/> |
   
Debido a que puede cambiar la disponibilidad de la característica, se recomienda que compruebe las ediciones de Exchange Server y los planes de Exchange Online para evaluar cómo disponibilidad de características puede afectar a su cliente. También puede diseñar su cliente para comprobar la disponibilidad de la característica mediante el uso de la [operación de GetServiceConfiguration](how-to-get-service-configuration-information-by-using-ews-in-exchange.md) o mediante el envío de solicitudes de pruebas para las operaciones que implementan las características. Si la característica no está disponible, la respuesta del servidor indicará como tales. 
  
## <a name="other-considerations"></a>Otras consideraciones
<a name="other"> </a>

Puede hacer lo siguiente cuando los destinatarios de Exchange local, pero no Exchange Online:
  
- Crear a un cliente que está instalado en el servidor de Exchange. 
    
- Instalar [los agentes de transporte personalizados](../transport-agents/transport-agents-in-exchange-2013.md) que pueden afectar a la entrega y el contenido de los mensajes que cree y envíe con EWS y otros clientes. 
    
## <a name="see-also"></a>Vea también

- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
- [Comparación de Exchange Online y Exchange Server 2013](http://blogs.technet.com/b/exchange/archive/2012/09/19/comparing-exchange-online-and-exchange-server-2013.aspx)  
- [Comparar todos los Office 365 para planes de negocio](http://office.microsoft.com/en-us/business/compare-all-office-365-for-business-plans-FX104051403.aspx)
- [EwsRelentless - herramienta de generación de carga de EWS](https://ewsrelentless.codeplex.com/)
- [Disponibilidad de característica del servicio Web de API de Exchange y la API administrada de EWS](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md)
- [EWS limitación en Exchange](ews-throttling-in-exchange.md)
    

