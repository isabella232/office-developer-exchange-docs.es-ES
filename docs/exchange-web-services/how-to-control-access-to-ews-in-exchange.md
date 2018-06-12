---
title: Controlar el acceso a EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 61e29e54-e3e5-404a-84c0-93b61a25ca58
description: Encuentre información acerca de cómo controlar el acceso a EWS para los usuarios, aplicaciones o toda la organización.
ms.openlocfilehash: 956c28faba105ecf2a6b1452abe629ea2fc930e1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763044"
---
# <a name="control-access-to-ews-in-exchange"></a>Controlar el acceso a EWS en Exchange

Encuentre información acerca de cómo controlar el acceso a EWS para los usuarios, aplicaciones o toda la organización.
  
Si está utilizando la API administrada de EWS o EWS directamente, en la aplicación, puede controlar el acceso a servicios Web de Exchange (EWS). Si dispone de acceso de administrador al servidor de Exchange, puede administrar el acceso a EWS mediante el uso de la consola de administración de Exchange para controlar el acceso de forma global, para cada usuario y para cada aplicación.
  
## <a name="exchange-management-shell-cmdlets-for-configuring-access-control"></a>Cmdlets del Shell de administración de Exchange para configurar el control de acceso
<a name="bk_Cmdlets"> </a>

Puede usar los siguientes cmdlets del Shell de administración de Exchange para ver la configuración actual de acceso y configurar el acceso a controles de EWS:
  
- [Get-CASMailbox](http://technet.microsoft.com/en-us/library/bb124754.aspx) - muestra qué parámetros se establecen para un buzón determinado.   
- [Set-CASMailbox](http://technet.microsoft.com/en-us/library/bb125264.aspx) - parámetros de conjuntos de un buzón determinado.    
- [Get-OrganizationConfig](http://technet.microsoft.com/en-us/library/aa997571.aspx) - muestra los parámetros para toda la organización.    
- [Set-OrganizationConfig](http://technet.microsoft.com/en-us/library/aa997443.aspx) - establece los parámetros para toda la organización. 

<a name="bk_Examples"> </a>

## <a name="examples-controlling-access-to-ews"></a>Ejemplos: Controlar el acceso a EWS

Vamos a echar un vistazo a algunos escenarios que muestran cómo se puede controlar el acceso a la aplicación.
  
**La tabla 1. Comandos para controlar el acceso a EWS**

|Si desea |Use este comando|
|:-----|:-----|
|Bloquear todas las aplicaciones cliente de uso de EWS. | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceAllowList`<br/><br/>Esto permite que las aplicaciones que aparecen en la AllowList para conectarse. En este ejemplo, no hay aplicaciones se incluyen en el AllowList, por lo que no hay aplicaciones de pueden usar EWS. |
|Permitir que las aplicaciones usar EWS de una lista de cliente. | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceAllowList -EwsAllowList:"OWA/*"`<br/><br/>Esto permite aplicaciones específicas para el uso de EWS. En este ejemplo, cualquier aplicación que tenga un agente de usuario de la cadena que comienza por "OWA /" se permitió el acceso. |
|Permitir que todas las aplicaciones de cliente usar EWS excepto aquellos que estén bloqueados específicamente. | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceBlockList -EwsBlockList:"OWA/*"`<br/> <br/>En este ejemplo se bloquea sólo aplicaciones desde mediante EWS que tienen una cadena de agente de usuario que comienza por "OWA /". |
|Permitir que todas las aplicaciones de cliente usar EWS. | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceBlockList` <br/><br/> Debido a que no se ha especificado ninguna lista de bloqueo, todas las aplicaciones pueden usar EWS. |
|Bloquear toda la organización de uso de EWS. | `Set-OrganizationConfig -EwsEnabled:$false` |
|Permitir que toda la organización para uso de EWS. | `Set-OrganizationConfig -EwsEnabled:$true`|
|Bloquear un buzón individual de uso de EWS. | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$false`|
|Permitir que un buzón individual para uso de EWS. | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$true`|
   
## <a name="see-also"></a>Ver también

- [Configurar una aplicación de EWS](setting-up-your-ews-application.md)    
- [Controlar el acceso de la aplicación de cliente para EWS en Exchange](controlling-client-application-access-to-ews-in-exchange.md)   
- [Exchange Server PowerShell (Shell de administración de Exchange)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps) 
- [Windows PowerShell](http://msdn.microsoft.com/en-us/library/dd835506%28v=vs.85%29.aspx)
    

