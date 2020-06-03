---
title: Opciones de configuración de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6562639-9366-4a13-9fdb-2fa737833329
description: Busque información sobre las opciones de configuración a las que puede tener acceso el cliente de EWS y la configuración de Exchange configurable que puede afectar a su cliente de EWS.
ms.openlocfilehash: 55f927b7b301bdfaa298bcd254b18a00cf1692d9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456160"
---
# <a name="configuration-options-for-ews-in-exchange"></a>Opciones de configuración de EWS en Exchange

Busque información sobre las opciones de configuración a las que puede tener acceso el cliente de EWS y la configuración de Exchange configurable que puede afectar a su cliente de EWS. 
  
Muchas opciones de configuración pueden afectar a lo que puede hacer la aplicación cliente de EWS. Estas opciones de configuración pueden ser: 
  
- De solo lectura o de lectura y escritura desde el cliente.
    
- Se obtiene acceso al servidor Exchange que hospeda el servicio EWS.
    
Un cliente puede obtener acceso a la configuración de Exchange Online, Exchange online como parte de Office 365 y un servidor de Exchange local. Todas las opciones de configuración locales de Exchange Server están disponibles para los administradores de Exchange; sin embargo, no todas estas opciones de configuración están disponibles para los administradores de espacios empresariales de Exchange Online. En este artículo se describe qué opciones de configuración tienen los clientes, los administradores de Exchange Server y los administradores de inquilinos de Exchange Online.
  
## <a name="configuration-settings-that-clients-can-access"></a>Opciones de configuración a las que pueden tener acceso los clientes

La aplicación cliente puede obtener y establecer un número de opciones de configuración desde el servidor de Exchange. El servicio de detección automática proporciona las opciones de configuración que todas las aplicaciones de EWS necesitan. Otras opciones de configuración se usan para escenarios de aplicación específicos. 
  
**Tabla 1. Características del servicio Web que proporcionan opciones de configuración para los clientes de EWS**

|**Característica**|**Descripción**|
|:-----|:-----|
|Servicio Detección automática  <br/> |El [servicio de detección](autodiscover-for-exchange.md) automática proporciona a las aplicaciones cliente información de configuración para que el cliente pueda configurarse automáticamente para comunicarse con EWS.  <br/> |
|Información de configuración personalizada almacenada en un buzón  <br/> |Puede usar una de varias opciones para [almacenar información de configuración personalizada](persistent-application-settings-in-ews-in-exchange.md) en su buzón: objetos de configuración de usuario, elementos personalizados o propiedades extendidas.  <br/> |
|Delegación de la administración  <br/> | EWS proporciona operaciones CRUD para administrar el acceso delegado a un buzón de correo. Los delegados son usuarios a los que se les ha concedido permiso para tener acceso al buzón de otro usuario.<br/><br/>  Puede usar las [operaciones de administración de delegación](https://msdn.microsoft.com/library/bb409286%28v=exchg.150%29.aspx#bk_delegate_management) para habilitar la administración de delegación mediante EWS o, si está usando la API administrada de EWS, puede usar los métodos siguientes:<br/><br/>- [ExchangeService. AddDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService. GetDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getdelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService. UpdateDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.updatedelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService. RemoveDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) <br/> |
|configuración de búsqueda de exhibición de documentos electrónicos  <br/> |las aplicaciones cliente de eDiscovery pueden obtener [información de configuración de búsqueda](https://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) que incluya una consulta de búsqueda de exhibición de documentos electrónicos, una lista de buzones de correo que se pueden buscar y el identificador de suspensiones de buzones de correo locales.  <br/> |
|Permisos de carpeta  <br/> |Los permisos de carpeta limitan lo que un usuario puede hacer en una carpeta pública y, en el caso de acceso delegado, lo que puede hacer un delegado en la carpeta de otro usuario. Puede usar el método [Folder. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) o la [operación GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) para tener acceso al conjunto de permisos de cada carpeta, incluidas las carpetas públicas, las carpetas privadas compartidas o las carpetas a las que los usuarios tienen acceso delegado.  <br/> |
|Sugerencias de correo, mensajería unificada o reglas de protección  <br/> |La [operación GetServiceConfiguration](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) proporciona [información de configuración del servicio](how-to-get-service-configuration-information-by-using-ews-in-exchange.md) de solo lectura para sugerencias de correo, mensajería unificada y reglas de protección.  <br/> |
   
## <a name="configuration-settings-that-administrators-can-access-on-the-exchange-server"></a>Opciones de configuración a las que pueden tener acceso los administradores en el servidor Exchange

La mayoría de los escenarios de aplicación cliente no requieren cambios en la configuración del servidor; sin embargo, en algunos escenarios sí. Por ejemplo, para habilitar una aplicación de nivel intermedio para que actúe como usuario, debe configurar la suplantación de Exchange en el servidor. Tenga en cuenta que solo se puede tener acceso a algunas configuraciones en servidores locales de Exchange. Si está destinado a Exchange Online, es posible que la aplicación cliente necesite trabajar con la configuración predeterminada.
  
**Tabla 2. Opciones de configuración de Exchange Server que afectan a los clientes de EWS**

|**Característica**|**¿Accesible desde Exchange Online?**|**Para obtener más información, consulte...**|
|:-----|:-----|:-----|
|Configuración del directorio virtual (incluida la autenticación)  <br/> |No  <br/> |[Get-WebServicesVirtualDirectory](https://technet.microsoft.com/library/aa998810%28v=exchg.150%29.aspx) <br/> [Set-WebServicesVirtualDirectory](https://technet.microsoft.com/library/aa997233%28v=exchg.150%29.aspx) <br/> |
|Detección automática  <br/> |No  <br/> |[Get-AutodiscoverVirtualDirectory](https://technet.microsoft.com/library/aa996819%28v=exchg.150%29.aspx) <br/> [Set-AutodiscoverVirtualDirectory](https://technet.microsoft.com/library/aa998601%28v=exchg.150%29.aspx) <br/> |
|Cumplimiento  <br/> |Sí  <br/> |[Archivado](https://technet.microsoft.com/library/dd979800%28v=exchg.150%29.aspx) <br/> [Exhibición de documentos electrónicos (eDiscovery)](https://technet.microsoft.com/library/dd298021%28v=exchg.150%29.aspx) <br/> [Suspensión de la retención](https://technet.microsoft.com/library/dd335168%28v=exchg.150%29.aspx) <br/> [Prevención de pérdida de datos](https://technet.microsoft.com/library/jj150527%28v=exchg.150%29.aspx) <br/> |
|Delegación de la administración  <br/> |Sí  <br/> |[Manage Permissions for Recipients](https://technet.microsoft.com/library/jj919240%28v=exchg.150%29.aspx) <br/> |
|Suplantación de Exchange  <br/> |Sí  <br/> |[Configurar la suplantación de Exchange](https://msdn.microsoft.com/library/bb204095%28EXCHG.140%29.aspx) <br/> |
|Sugerencias de correo, mensajería unificada o reglas de protección  <br/> |Sí  <br/> |[Sugerencias de correo electrónico](https://technet.microsoft.com/library/jj649091%28v=exchg.150%29.aspx) <br/> [Cmdlets de mensajería unificada](https://technet.microsoft.com/library/aa997665%28v=exchg.150%29.aspx) <br/> [Reglas de protección de Outlook](https://technet.microsoft.com/library/dd638178%28v=exchg.150%29.aspx) <br/> |
|Limitación  <br/> |No  <br/> |[Configuración de limitación](ews-throttling-in-exchange.md) <br/> |
|Filtrado de agente de usuario  <br/> |Sí  <br/> |[Filtrado de agente de usuario](how-to-control-access-to-ews-in-exchange.md) <br/> |
   
## <a name="see-also"></a>Vea también

- [Obtener información de configuración de servicio mediante EWS en Exchange](how-to-get-service-configuration-information-by-using-ews-in-exchange.md)
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)   
- [Empezar a usar los servicios web de Exchange](start-using-web-services-in-exchange.md)   
- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    

