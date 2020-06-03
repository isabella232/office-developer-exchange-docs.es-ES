---
title: Controlar el acceso a EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 61e29e54-e3e5-404a-84c0-93b61a25ca58
description: Descubra cómo controlar el acceso a EWS para usuarios, aplicaciones o toda la organización.
localization_priority: Priority
ms.openlocfilehash: bd65b099ab15c1514945d8a1cfa4e9b1428a4755
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456881"
---
# <a name="control-access-to-ews-in-exchange"></a>Controlar el acceso a EWS en Exchange

Descubra cómo controlar el acceso a EWS para usuarios, aplicaciones o toda la organización.
  
Independientemente de si usa la API administrada de EWS, o EWS directamente, en su aplicación, puede controlar el acceso a los servicios web Exchange (EWS). Si tiene acceso de administrador a su servidor de Exchange, puede administrar el acceso a EWS mediante el shell de administración de Exchange para controlar el acceso globalmente, para cada usuario y para cada aplicación.
  
## <a name="exchange-management-shell-cmdlets-for-configuring-access-control"></a>Cmdlets del shell de administración de Exchange para configurar el control de acceso
<a name="bk_Cmdlets"> </a>

Puede usar los siguientes cmdlets del shell de administración de Exchange para ver la configuración de acceso actual y establecer los controles de acceso EWS:
  
- [Get-CASMailbox](https://technet.microsoft.com/library/bb124754.aspx) : muestra qué parámetros se establecen para un buzón en particular.   
- [Set-CASMailbox](https://technet.microsoft.com/library/bb125264.aspx) : establece parámetros para un buzón en particular.    
- [Get-OrganizationConfig](https://technet.microsoft.com/library/aa997571.aspx) : muestra los parámetros para toda la organización.    
- [Set-OrganizationConfig](https://technet.microsoft.com/library/aa997443.aspx) : establece los parámetros para toda la organización. 

<a name="bk_Examples"> </a>

## <a name="examples-controlling-access-to-ews"></a>Ejemplos: controlar el acceso a EWS

Echemos un vistazo a algunos escenarios que muestran cómo se puede controlar el acceso a la aplicación.
  
**Tabla 1. Comandos para controlar el acceso a EWS**

|Si desea |Use este comando|
|:-----|:-----|
|Bloquear todas las aplicaciones cliente para que no usen EWS. | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceAllowList`<br/><br/>Esto permite que las aplicaciones enumeradas en AllowList se conecten. En este ejemplo, no se incluye ninguna aplicación en la AllowList, por lo que ninguna aplicación puede usar EWS. |
|Permitir una lista de aplicaciones cliente para usar EWS. | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceAllowList -EwsAllowList:"OWA/*"`<br/><br/>Esto permite que aplicaciones específicas usen EWS. En este ejemplo, se permite el acceso a cualquier aplicación que tenga una cadena de agente de usuario que comience por "OWA/". |
|Permitir que todas las aplicaciones cliente usen EWS, excepto aquellas que se bloquean específicamente. | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceBlockList -EwsBlockList:"OWA/*"`<br/> <br/>En este ejemplo solo se impide que las aplicaciones usen EWS que tienen una cadena de agente de usuario que comienza con "OWA/". |
|Permitir que todas las aplicaciones cliente usen EWS. | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceBlockList` <br/><br/> Como no se especifica ninguna lista de bloqueo, todas las aplicaciones pueden usar EWS. |
|Impedir que toda la organización use EWS. | `Set-OrganizationConfig -EwsEnabled:$false` |
|Permitir a toda la organización usar EWS. | `Set-OrganizationConfig -EwsEnabled:$true`|
|Impedir que un buzón individual use EWS. | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$false`|
|Permitir a un buzón individual usar EWS. | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$true`|
   
## <a name="see-also"></a>Vea también

- [Configurar la aplicación EWS](setting-up-your-ews-application.md)    
- [Controlar el acceso de la aplicación cliente a EWS en Exchange](controlling-client-application-access-to-ews-in-exchange.md)   
- [PowerShell de Exchange Server (Shell de administración de Exchange)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps) 
- [Windows PowerShell](https://msdn.microsoft.com/library/dd835506%28v=vs.85%29.aspx)
    

