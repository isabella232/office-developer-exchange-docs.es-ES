---
title: Opciones de configuración para EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6562639-9366-4a13-9fdb-2fa737833329
description: Busque información sobre las opciones de configuración que puede tener acceso su cliente EWS y las opciones configurables de Exchange que pueden afectar a su cliente EWS.
ms.openlocfilehash: d6c2866abf3dc16c77d84355afb9d86b0a9934c6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19762998"
---
# <a name="configuration-options-for-ews-in-exchange"></a>Opciones de configuración para EWS en Exchange

Busque información sobre las opciones de configuración que puede tener acceso su cliente EWS y las opciones configurables de Exchange que pueden afectar a su cliente EWS. 
  
Muchas opciones de configuración pueden afectar a lo que puede hacer la aplicación de cliente EWS. Estas opciones de configuración son: 
  
- Sólo lectura o lectura grabable desde el cliente.
    
- Tener acceso a en el servidor de Exchange que hospeda el servicio EWS.
    
Un cliente puede tener acceso a la configuración de un servidor de Exchange local, Exchange Online como parte de Office 365 y Exchange Online. Configuración del servidor de Exchange de todos los locales está disponible para los administradores de Exchange; Sin embargo, no todas estas opciones están disponibles para los administradores de inquilinos Exchange Online. En este artículo se describe qué clientes de opciones de configuración, los administradores de Exchange Server y Exchange Online inquilino pueden tener acceso los administradores.
  
## <a name="configuration-settings-that-clients-can-access"></a>Opciones de configuración que pueden tener acceso los clientes

La aplicación cliente puede obtener y establecer un número de opciones de configuración del servidor de Exchange. Opciones de configuración que necesitan todas las aplicaciones de EWS proporcionados por el servicio Detección automática. Otras opciones de configuración se utilizan para escenarios de aplicación específica. 
  
**La tabla 1. Características del servicio Web que proporcionan opciones de configuración para los clientes EWS**

|**Característica**|**Descripción**|
|:-----|:-----|
|Servicio de detección automática  <br/> |El [servicio Detección automática](autodiscover-for-exchange.md) proporciona aplicaciones con información de configuración de su cliente para que el cliente pueda configurar automáticamente propio para comunicarse con EWS.  <br/> |
|Información de configuración personalizada almacenada en un buzón de correo  <br/> |Puede usar una de varias opciones para [almacenar la información de configuración personalizada](persistent-application-settings-in-ews-in-exchange.md) en su buzón de correo: objetos de configuración de usuario, los elementos personalizados o las propiedades extendidas.  <br/> |
|Delegar la administración  <br/> | EWS proporciona operaciones CRUD para administrar el acceso de delegado a un buzón de correo. Los delegados son los usuarios que se ha concedido permiso de acceso a buzón de otro usuario.<br/><br/>  Puede usar las [operaciones de administración de delegado](http://msdn.microsoft.com/en-us/library/bb409286%28v=exchg.150%29.aspx#bk_delegate_management) para habilitar la delegación de la administración mediante el uso de EWS, o bien, si se usa la API administrada de EWS, puede usar los siguientes métodos:<br/><br/>- [ExchangeService.AddDelegates](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService.GetDelegates](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getdelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService.UpdateDelegates](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.updatedelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService.RemoveDelegates](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) <br/> |
|configuración de búsqueda de exhibición de documentos electrónicos  <br/> |las aplicaciones de cliente de exhibición de documentos electrónicos pueden obtener [información de configuración de búsqueda](http://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) que incluya una consulta de búsqueda de exhibición de documentos electrónicos, una lista de buzones de correo que admite búsquedas, y contiene el identificador del buzón de correo en contexto.  <br/> |
|Permisos de carpeta  <br/> |Permisos de carpeta limitan qué puede hacer un usuario en una carpeta pública y, en el caso de acceso delegado, lo que un delegado puede hacer en la carpeta de otro usuario. Puede usar el método [Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) o la [operación GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) para tener acceso al conjunto de permisos de todas las carpetas, incluidas las carpetas públicas, carpetas privadas compartidas o a la que los usuarios tienen acceso de delegado.  <br/> |
|Sugerencias de correo, la mensajería unificada o las reglas de protección  <br/> |La [operación de GetServiceConfiguration](http://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) proporciona [información de configuración de servicio](how-to-get-service-configuration-information-by-using-ews-in-exchange.md) de sólo lectura para las sugerencias de correo, la mensajería unificada y las reglas de protección.  <br/> |
   
## <a name="configuration-settings-that-administrators-can-access-on-the-exchange-server"></a>Opciones de configuración que pueden tener acceso los administradores en el servidor de Exchange

Mayoría de los escenarios de aplicación de cliente no requiere los cambios realizados en los valores de configuración del servidor; Sin embargo, algunos escenarios de hacen. Por ejemplo, para habilitar una aplicación de nivel intermedio para que actúe como un usuario, debe establecer la suplantación de Exchange en el servidor. Tenga en cuenta que sólo se pueden tener acceso a algunas opciones de configuración en los servidores de Exchange locales. Si se define en Exchange Online, la aplicación cliente que necesite trabajar con la configuración predeterminada.
  
**Tabla 2. Opciones de configuración de servidor de Exchange que afectan a los clientes EWS**

|**Característica**|**¿Accesible desde Exchange Online?**|**Para obtener más información, consulte...**|
|:-----|:-----|:-----|
|Configuración del directorio virtual (incluida la autenticación)  <br/> |No  <br/> |[Get-WebServicesVirtualDirectory](http://technet.microsoft.com/en-us/library/aa998810%28v=exchg.150%29.aspx) <br/> [Set-WebServicesVirtualDirectory](http://technet.microsoft.com/en-us/library/aa997233%28v=exchg.150%29.aspx) <br/> |
|Detección automática  <br/> |No  <br/> |[Get-AutodiscoverVirtualDirectory](http://technet.microsoft.com/en-us/library/aa996819%28v=exchg.150%29.aspx) <br/> [Set-AutodiscoverVirtualDirectory](http://technet.microsoft.com/en-us/library/aa998601%28v=exchg.150%29.aspx) <br/> |
|Cumplimiento de normas  <br/> |Sí  <br/> |[Archivado](http://technet.microsoft.com/en-us/library/dd979800%28v=exchg.150%29.aspx) <br/> [exhibición de documentos electrónicos](http://technet.microsoft.com/en-us/library/dd298021%28v=exchg.150%29.aspx) <br/> [Suspensión de retención](http://technet.microsoft.com/en-us/library/dd335168%28v=exchg.150%29.aspx) <br/> [Prevención de pérdida de datos](http://technet.microsoft.com/en-us/library/jj150527%28v=exchg.150%29.aspx) <br/> |
|Delegar la administración  <br/> |Sí  <br/> |[Administrar permisos para los destinatarios](http://technet.microsoft.com/en-us/library/jj919240%28v=exchg.150%29.aspx) <br/> |
|Suplantación de Exchange  <br/> |Sí  <br/> |[Configurar la suplantación de Exchange](http://msdn.microsoft.com/en-us/library/bb204095%28EXCHG.140%29.aspx) <br/> |
|Sugerencias de correo, la mensajería unificada o las reglas de protección  <br/> |Sí  <br/> |[Sugerencias de correo electrónico](http://technet.microsoft.com/en-us/library/jj649091%28v=exchg.150%29.aspx) <br/> [Mensajería unificada Cmdlets](http://technet.microsoft.com/en-us/library/aa997665%28v=exchg.150%29.aspx) <br/> [Reglas de protección de Outlook](http://technet.microsoft.com/en-us/library/dd638178%28v=exchg.150%29.aspx) <br/> |
|Limitación  <br/> |No  <br/> |[La configuración de limitación](ews-throttling-in-exchange.md) <br/> |
|Filtrado de agente de usuario  <br/> |Sí  <br/> |[Filtrado de agente de usuario](how-to-control-access-to-ews-in-exchange.md) <br/> |
   
## <a name="see-also"></a>Ver también

- [Obtener la información de configuración de servicio mediante el uso de EWS en Exchange](how-to-get-service-configuration-information-by-using-ews-in-exchange.md)
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)   
- [Empezar a utilizar servicios web de Exchange](start-using-web-services-in-exchange.md)   
- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    

