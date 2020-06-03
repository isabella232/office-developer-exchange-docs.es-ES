---
title: Controlar el acceso de la aplicación cliente a EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 60ac3f7b-ba8a-4c93-99f7-c27002caff93
description: Obtenga información sobre las opciones para administrar el acceso de aplicaciones cliente a EWS.
localization_priority: Priority
ms.openlocfilehash: b887b8167e3d38946b1d6caffe12655ded89569f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528464"
---
# <a name="controlling-client-application-access-to-ews-in-exchange"></a>Controlar el acceso de la aplicación cliente a EWS en Exchange

Obtenga información sobre las opciones para administrar el acceso de aplicaciones cliente a EWS.
  
Todas las aplicaciones de cliente de EWS que cree deben tener acceso a Exchange Online, Exchange online como parte de Office 365 o a la versión de Exchange que comienza con Exchange 2013 antes de que pueda llamar a operaciones de EWS. Los administradores de servidores de prueba o de producción pueden usar el shell de administración de Exchange para limitar el acceso a EWS para todos los usuarios y aplicaciones, para los usuarios individuales o para las aplicaciones individuales. El control de acceso para EWS se basa en las cuentas de dominio. Cuando se realiza una conexión con credenciales que se autentican mediante la autoridad de seguridad local, el servidor devuelve un error que indica que solo se pueden conectar cuentas de dominio. 
  
## <a name="access-control-for-ews-clients-and-users"></a>Control de acceso para clientes y usuarios de EWS
<a name="bk_configure"> </a>

El administrador del servidor de prueba o de producción puede configurar el control de acceso para clientes que se conectan a EWS de las siguientes maneras: 
  
- Al impedir que se conecten todas las aplicaciones cliente.
    
- Al permitir que las aplicaciones cliente específicas solo se conecten.
    
- Al permitir que cualquier aplicación cliente se conecte excepto la que esté bloqueada específicamente.
    
- Al permitir que cualquier aplicación cliente se conecte.
    
Las aplicaciones se identifican por la cadena de agente de usuario que envían en la solicitud Web HTTP.
  
> [!IMPORTANT]
> El bloqueo en el nivel de aplicación no es una característica de seguridad. La cadena de agente de usuario se falsifica fácilmente. Si se permite el acceso de una aplicación a EWS, la aplicación debe seguir presentando credenciales que el servidor autentica antes de que la aplicación pueda conectarse a EWS. 
  
Los administradores también pueden configurar el control de acceso para los propietarios de buzones que se conectan a EWS de las maneras siguientes: 
  
- Al bloquear o permitir a toda la organización.
    
- Al bloquear o permitir a un grupo de usuarios identificado por un ámbito de autenticación basado en roles que incluya o excluya los propietarios de buzones que no tienen acceso a EWS.
    
- Bloqueando o permitiendo el propietario de un buzón de correo individual.
    
La configuración de control de acceso específica invalida la configuración de control de acceso general. Por ejemplo, si una organización deniega el acceso a EWS, pero el propietario de un buzón individual permite el acceso a la aplicación, prevalecerá la configuración individual y se permitirá el acceso. 
  
## <a name="delegation-and-ews-access-management"></a>Delegación y administración del acceso a EWS
<a name="bk_delegation"> </a>

Cuando los usuarios delegados que no tienen acceso a EWS usan la aplicación cliente, no podrán acceder al buzón de correo del usuario principal mediante EWS, incluso si el usuario principal tiene acceso a EWS. Si el usuario delegado tiene acceso a EWS, el delegado podrá usar la aplicación cliente de EWS para tener acceso al buzón de correo del usuario principal incluso si el usuario principal no tiene acceso a EWS. 
  
## <a name="impersonation-and-ews-access-management"></a>Suplantación y administración del acceso a EWS
<a name="bk_impersonation"> </a>

Es posible que las aplicaciones cliente que se conectan a EWS en nombre de propietarios de buzones de correo no puedan usar la configuración de EWS del propietario del buzón. Por ejemplo, una aplicación que archiva mensajes de correo electrónico para una compañía tiene que conectarse a EWS independientemente de la configuración de los usuarios del buzón. Otras aplicaciones, como los clientes de correo, tienen que usar la configuración de EWS del propietario del buzón. 
  
Los administradores deben crear una cuenta de suplantación para cada aplicación o clase de aplicación que usen en su servidor. Esto permitirá que el Administrador configure el ámbito de control de acceso basado en roles para todos los usuarios que no tengan permisos EWS. 
  
Para habilitar las cuentas de suplantación, el administrador del servidor de prueba o de producción debe realizar una de las siguientes acciones: 
  
- Agregue el grupo usuarios autenticados al grupo acceso compatible con versiones anteriores a Win2K. 
    
- Agregue el grupo servidores de Exchange al grupo de acceso de autorización de Windows. 
    
## <a name="exchange-management-shell-cmdlets-for-access-management"></a>Cmdlets del shell de administración de Exchange para la administración de acceso
<a name="bk_cmdlets"> </a>

Los administradores usan los siguientes cmdlets del shell de administración de Exchange para configurar los controles de acceso de EWS: 
  
- [Get-CASMailbox](https://technet.microsoft.com/library/bb124754.aspx)   
- [Set-CASMailbox](https://technet.microsoft.com/library/bb125264.aspx)   
- [Get-OrganizationConfig](https://technet.microsoft.com/library/aa997571.aspx)   
- [Set-OrganizationConfig](https://technet.microsoft.com/library/aa997443.aspx)
    
## <a name="see-also"></a>Vea también

- [Empezar a usar los servicios web de Exchange](start-using-web-services-in-exchange.md)  
- [Controlar el acceso a EWS en Exchange](how-to-control-access-to-ews-in-exchange.md)
- [PowerShell de Exchange Server (Shell de administración de Exchange)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)
- [Windows PowerShell](https://msdn.microsoft.com/library/dd835506%28v=vs.85%29.aspx)
    

