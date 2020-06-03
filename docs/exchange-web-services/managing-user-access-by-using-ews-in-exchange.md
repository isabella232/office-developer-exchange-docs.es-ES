---
title: Administración del acceso de usuarios mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 48f0170c-8786-405f-86cb-568b7314a425
description: Descubra Cuáles son sus opciones para administrar el acceso de las cuentas de usuario a su servidor de Exchange.
ms.openlocfilehash: 476292d4db206f22cd84134ce2b46957e9fe85fc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456248"
---
# <a name="managing-user-access-by-using-ews-in-exchange"></a>Administración del acceso de usuarios mediante EWS en Exchange

Descubra Cuáles son sus opciones para administrar el acceso de las cuentas de usuario a su servidor de Exchange.
  
Los servicios web Exchange (EWS) y la API administrada de EWS proporcionan un número limitado de operaciones que puede usar para administrar cuentas en Exchange Online, Exchange online como parte de Office 365 o una versión de Exchange que empiece por Exchange 2013. Puede usar las operaciones que se muestran en la figura siguiente para administrar los delegados y establecer los permisos de acceso a la carpeta para otras cuentas. 
  
**Operaciones de EWS para acceso delegado y de carpeta**

![Opciones de administración de usuarios de EWS.](media/Exchange_ManagingUserAccess_1.png)
  
Si la aplicación necesita un control adicional sobre las cuentas en un servidor de Exchange, puede usar los cmdlets del shell de administración de Exchange para administrar las cuentas. Puede llamar a los cmdlets del shell de administración de Exchange mediante uno de los siguientes procedimientos:
  
- Escribir una aplicación con C# o Visual Basic que llame a los cmdlets del shell de administración de Exchange. Puede consultar el código de ejemplo de la documentación de la [API del shell de administración de Exchange](../management/exchange-management-shell.md) para obtener información sobre cómo llamar a un cmdlet. 
    
- Uso de Windows PowerShell y scripts de Windows PowerShell para llamar a los cmdlets del shell de administración de Exchange. Puede encontrar una lista completa de [Exchange Server PowerShell (Shell de administración de Exchange)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps), junto con ejemplos que muestran cómo usarlas. 
    
## <a name="see-also"></a>Vea también

- [Configurar la aplicación EWS](setting-up-your-ews-application.md)   
- [Cmdlets de Exchange 2013](https://docs.microsoft.com/powershell/exchange/?view=exchange-ps)  
    

