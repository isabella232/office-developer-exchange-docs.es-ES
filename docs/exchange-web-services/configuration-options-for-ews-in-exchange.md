---
title: Opciones de configuración para EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: f6562639-9366-4a13-9fdb-2fa737833329
description: Busque información sobre las opciones de configuración a las que puede tener acceso el cliente EWS y la configuración Exchange configuración que puede afectar al cliente EWS.
ms.openlocfilehash: ed7667086b36897fd07031526e5a4657a120d505
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522288"
---
# <a name="configuration-options-for-ews-in-exchange"></a>Opciones de configuración para EWS en Exchange

Busque información sobre las opciones de configuración a las que puede tener acceso el cliente EWS y la configuración Exchange configuración que puede afectar al cliente EWS. 
  
Muchas opciones de configuración pueden afectar a lo que puede hacer la aplicación cliente EWS. Estas opciones de configuración son: 
  
- Solo lectura o lectura-escritura desde el cliente.
    
- Se tiene acceso en el servidor Exchange que hospeda el servicio EWS.
    
Un cliente puede tener acceso a la configuración Exchange Online, Exchange Online como parte de Office 365 y un servidor Exchange local. Todos los servidores locales Exchange configuración del servidor están disponibles para Exchange administradores; sin embargo, no todas estas opciones están disponibles para Exchange Online administradores de inquilinos. En este artículo se describen los clientes de configuración, Exchange Server administradores y Exchange Online a los administradores de inquilinos.
  
## <a name="configuration-settings-that-clients-can-access"></a>Opciones de configuración a las que pueden acceder los clientes

La aplicación cliente puede obtener y establecer varias opciones de configuración desde el Exchange cliente. El servicio de detección automática proporciona las opciones de configuración que necesitan todas las aplicaciones EWS. Otras opciones de configuración se usan para escenarios de aplicación específicos. 
  
**Tabla 1. Características del servicio web que proporcionan opciones de configuración para clientes EWS**

|**Característica**|**Descripción**|
|:-----|:-----|
|Servicio Detección automática  <br/> |El [servicio de detección automática](autodiscover-for-exchange.md) proporciona a las aplicaciones cliente información de configuración para que el cliente pueda configurarse automáticamente para comunicarse con EWS.  <br/> |
|Información de configuración personalizada almacenada en un buzón  <br/> |Puede usar una de [](persistent-application-settings-in-ews-in-exchange.md) varias opciones para almacenar información de configuración personalizada en el buzón: objetos de configuración de usuario, elementos personalizados o propiedades extendidas.  <br/> |
|Administración de delegados  <br/> | EWS proporciona operaciones CRUD para administrar el acceso delegado a un buzón. Los delegados son usuarios a los que se les ha concedido permiso para acceder al buzón de otro usuario.<br/><br/>  Puede usar las [operaciones](https://msdn.microsoft.com/library/bb409286%28v=exchg.150%29.aspx#bk_delegate_management) de administración de delegados para habilitar la administración de delegados mediante EWS o, si usa la API administrada ews, puede usar los métodos siguientes:<br/><br/>- [ExchangeService.AddDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService.GetDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getdelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService.UpdateDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.updatedelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService.RemoveDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) <br/> |
|Configuración de búsqueda de exhibición de documentos electrónicos  <br/> |Las aplicaciones cliente de [](https://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) exhibición de documentos electrónicos pueden obtener información de configuración de búsqueda que incluye una consulta de búsqueda de exhibición de documentos electrónicos, una lista de buzones que se pueden buscar y el identificador de las retenciones de buzones locales.  <br/> |
|Permisos de carpeta  <br/> |Los permisos de carpeta limitan lo que un usuario puede hacer en una carpeta pública y, en el caso del acceso delegado, lo que un delegado puede hacer en la carpeta de otro usuario. Puede usar el método [Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) o la operación [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) para obtener acceso al conjunto de permisos de cada carpeta, incluidas las carpetas públicas, las carpetas privadas compartidas o las carpetas a las que los usuarios tienen acceso delegado.  <br/> |
|Sugerencias de correo, mensajería unificada o reglas de protección  <br/> |La [operación GetServiceConfiguration](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) proporciona información de configuración de servicio [de](how-to-get-service-configuration-information-by-using-ews-in-exchange.md) solo lectura para sugerencias de correo, mensajería unificada y reglas de protección.  <br/> |
   
## <a name="configuration-settings-that-administrators-can-access-on-the-exchange-server"></a>Opciones de configuración a las que los administradores pueden tener acceso en el Exchange servidor

La mayoría de los escenarios de aplicación cliente no requieren cambios en las opciones de configuración del servidor; sin embargo, algunos escenarios sí. Por ejemplo, para permitir que una aplicación de nivel intermedio actúe como usuario, debe establecer Exchange suplantación en el servidor. Tenga en cuenta que solo se puede acceder a algunas opciones de configuración en servidores Exchange local. Si está destinado a Exchange Online, es posible que la aplicación cliente tenga que trabajar con la configuración predeterminada.
  
**Tabla 2. Exchange opciones de configuración de servidor que afectan a clientes EWS**

|**Característica**|**Accesible desde Exchange Online?**|**Para obtener más información, vea...**|
|:-----|:-----|:-----|
|Configuración del directorio virtual (incluida la autenticación)  <br/> |No  <br/> |[Get-WebServicesVirtualDirectory](https://technet.microsoft.com/library/aa998810%28v=exchg.150%29.aspx) <br/> [Set-WebServicesVirtualDirectory](https://technet.microsoft.com/library/aa997233%28v=exchg.150%29.aspx) <br/> |
|Detección automática  <br/> |No  <br/> |[Get-AutodiscoverVirtualDirectory](https://technet.microsoft.com/library/aa996819%28v=exchg.150%29.aspx) <br/> [Set-AutodiscoverVirtualDirectory](https://technet.microsoft.com/library/aa998601%28v=exchg.150%29.aspx) <br/> |
|Cumplimiento  <br/> |Sí  <br/> |[Archivado](https://technet.microsoft.com/library/dd979800%28v=exchg.150%29.aspx) <br/> [eDiscovery](https://technet.microsoft.com/library/dd298021%28v=exchg.150%29.aspx) <br/> [Suspensión de la retención](https://technet.microsoft.com/library/dd335168%28v=exchg.150%29.aspx) <br/> [Prevención de pérdida de datos](https://technet.microsoft.com/library/jj150527%28v=exchg.150%29.aspx) <br/> |
|Administración de delegados  <br/> |Sí  <br/> |[Manage Permissions for Recipients](https://technet.microsoft.com/library/jj919240%28v=exchg.150%29.aspx) <br/> |
|Exchange Suplantación  <br/> |Sí  <br/> |[Configurar Exchange suplantación de identidad](https://msdn.microsoft.com/library/bb204095%28EXCHG.140%29.aspx) <br/> |
|Sugerencias de correo, mensajería unificada o reglas de protección  <br/> |Sí  <br/> |[Sugerencias de correo electrónico](https://technet.microsoft.com/library/jj649091%28v=exchg.150%29.aspx) <br/> [Cmdlets de mensajería unificada](https://technet.microsoft.com/library/aa997665%28v=exchg.150%29.aspx) <br/> [Reglas de protección de Outlook](https://technet.microsoft.com/library/dd638178%28v=exchg.150%29.aspx) <br/> |
|Limitación  <br/> |No  <br/> |[Configuración de limitación](ews-throttling-in-exchange.md) <br/> |
|Filtrado de agentes de usuario  <br/> |Sí  <br/> |[Filtrado de agentes de usuario](how-to-control-access-to-ews-in-exchange.md) <br/> |
   
## <a name="see-also"></a>Ver también

- [Obtener información de configuración de servicio mediante EWS en Exchange](how-to-get-service-configuration-information-by-using-ews-in-exchange.md)
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)   
- [Empezar a usar los servicios web de Exchange](start-using-web-services-in-exchange.md)   
- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    

