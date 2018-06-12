---
title: Controlar el acceso de la aplicación de cliente para EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60ac3f7b-ba8a-4c93-99f7-c27002caff93
description: Obtenga información sobre las opciones para administrar el acceso de la aplicación de cliente a EWS.
ms.openlocfilehash: 29a640178afc9814a0b2232225ae4307e49afed2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19762996"
---
# <a name="controlling-client-application-access-to-ews-in-exchange"></a>Controlar el acceso de la aplicación de cliente para EWS en Exchange

Obtenga información sobre las opciones para administrar el acceso de la aplicación de cliente a EWS.
  
Cualquier aplicación de cliente EWS que cree debe tener acceso a Exchange Online, Exchange Online como parte de Office 365, o una versión de Exchange comenzando con Exchange 2013 antes de que pueden llamar a las operaciones de EWS. Los administradores de servidores de prueba o de producción pueden usar el Shell de administración de Exchange para limitar el acceso a EWS para todos los usuarios y aplicaciones, para usuarios individuales o para aplicaciones individuales. Control de acceso para EWS se basa en las cuentas de dominio. Cuando se realiza una conexión con las credenciales que se autentican por la entidad de seguridad local, el servidor devuelve un error que indica que se pueden conectar sólo las cuentas de dominio. 
  
## <a name="access-control-for-ews-clients-and-users"></a>Control de acceso de los usuarios y los clientes EWS
<a name="bk_configure"> </a>

El administrador del servidor de prueba o de producción puede configurar el control de acceso para los clientes que se conectan a EWS de las siguientes maneras: 
  
- Mediante el bloqueo de todas las aplicaciones cliente de conexión.
    
- Al permitir que aplicaciones sólo para conectarse de cliente específico.
    
- Al permitir que cualquier aplicación de cliente para conectarse, excepto aquellos que estén bloqueados específicamente.
    
- Al permitir que cualquier aplicación de cliente para conectarse.
    
Las aplicaciones se identifican mediante la cadena de agente de usuario que se envían en la solicitud web HTTP.
  
> [! Nota de seguridad]-nivel de la aplicación no es una característica de seguridad bloqueo. La cadena de agente de usuario es suplantar fácilmente. Si se permite el acceso a EWS en una aplicación, la aplicación debe presentar las credenciales que se autentica el servidor antes de la aplicación puede conectarse a EWS. 
  
Los administradores también pueden configurar el control de acceso para los propietarios de buzón de correo que se conectan a EWS de las siguientes maneras: 
  
- Bloquear o permitir que toda la organización.
    
- Bloquear o permitir que un grupo de usuarios identificado por un ámbito de autenticación basado en roles que incluye o excluye los propietarios de los buzones de correo que no tienen acceso a EWS.
    
- Bloquear o permitir que a un propietario de buzón de correo individuales.
    
Configuración de control de acceso específico invalida la configuración de control de acceso general. Por ejemplo, si una organización deniega el acceso EWS pero un propietario del buzón de correo individuales se permitió el acceso de la aplicación, prevalecerá la opción individual y se permite el acceso. 
  
## <a name="delegation-and-ews-access-management"></a>Delegación y administración del acceso a EWS
<a name="bk_delegation"> </a>

Cuando los usuarios delegados que no tienen acceso a EWS use la aplicación de cliente, no podrán tener acceso a la entidad de seguridad del buzón del usuario mediante el uso de acceso EWS, incluso si el usuario de entidad de seguridad tiene EWS. Si el usuario delegado tiene acceso a EWS, el delegado podrá usar la aplicación de cliente EWS para obtener acceso a la entidad de seguridad del buzón del usuario, incluso si el usuario de entidad de seguridad no tiene EWS acceso. 
  
## <a name="impersonation-and-ews-access-management"></a>Suplantación y administración del acceso a EWS
<a name="bk_impersonation"> </a>

Es posible que las aplicaciones de cliente que se conectan a EWS en nombre de los propietarios de los buzones de correo no podrá usar la configuración de EWS del propietario del buzón. Por ejemplo, una aplicación que archiva los mensajes para una compañía tiene para conectarse a EWS independientemente de la configuración de qué el buzón de correo los usuarios son de correo electrónico. Otras aplicaciones, como los clientes de correo, es necesario usar la configuración de EWS del propietario del buzón. 
  
Los administradores deben crear una cuenta de suplantación para cada aplicación o una clase de aplicación que use en su servidor. Esto permitirá que el administrador configure el ámbito de control de acceso basado en roles para todos los usuarios que no tienen permisos de EWS. 
  
Para habilitar cuentas de suplantación, el administrador del servidor de prueba o de producción debe realizar una de las siguientes opciones: 
  
- Agregue el grupo Usuarios autenticados al grupo acceso Compatible Pre-Win2K. 
    
- Agregue el grupo de servidores de Exchange para el grupo de acceso de autorización de Windows. 
    
## <a name="exchange-management-shell-cmdlets-for-access-management"></a>Cmdlets del Shell de administración de Exchange para la administración de acceso
<a name="bk_cmdlets"> </a>

Los administradores usar los siguientes cmdlets del Shell de administración de Exchange para configurar el acceso a controles de EWS: 
  
- [Get-CASMailbox](http://technet.microsoft.com/en-us/library/bb124754.aspx)
    
- [Set-CASMailbox](http://technet.microsoft.com/en-us/library/bb125264.aspx)
    
- [Get-OrganizationConfig](http://technet.microsoft.com/en-us/library/aa997571.aspx)
    
- [Set-OrganizationConfig](http://technet.microsoft.com/en-us/library/aa997443.aspx)
    
## <a name="see-also"></a>Ver también

- [Empezar a utilizar servicios web de Exchange](start-using-web-services-in-exchange.md)  
- [Controlar el acceso a EWS en Exchange](how-to-control-access-to-ews-in-exchange.md)
- [Exchange Server PowerShell (Shell de administración de Exchange)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)
- [Windows PowerShell](http://msdn.microsoft.com/en-us/library/dd835506%28v=vs.85%29.aspx)
    

