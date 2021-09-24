---
title: Administración del acceso de usuarios mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 48f0170c-8786-405f-86cb-568b7314a425
description: Descubra cuáles son sus opciones para administrar el acceso de cuentas de usuario a su Exchange usuario.
ms.openlocfilehash: 431f61a0cbdfcc522eb1481399ffab1f31df9e62
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520979"
---
# <a name="managing-user-access-by-using-ews-in-exchange"></a>Administración del acceso de usuarios mediante EWS en Exchange

Descubra cuáles son sus opciones para administrar el acceso de cuentas de usuario a su Exchange usuario.
  
Exchange Los servicios web (EWS) y la API administrada ews proporcionan un número limitado de operaciones que puede usar para administrar cuentas en Exchange Online, Exchange Online como parte de Office 365 o una versión de Exchange a partir de Exchange 2013. Puede usar las operaciones que se muestran en la siguiente figura para administrar delegados y establecer permisos de acceso a carpetas para otras cuentas. 
  
**Operaciones EWS para el acceso delegado y de carpetas**

![Opciones de administración de usuarios de EWS.](media/Exchange_ManagingUserAccess_1.png)
  
Si la aplicación necesita un control adicional sobre las cuentas en un servidor Exchange, puede usar los cmdlets del Shell de administración Exchange administrar las cuentas. Puede llamar a los cmdlets Exchange Shell de administración mediante uno de los siguientes procedimientos:
  
- Escribir una aplicación mediante C# o Visual Basic que llama a los cmdlets Exchange Shell de administración. Puede ver el código de ejemplo en la documentación Exchange API del [Shell](../management/exchange-management-shell.md) de administración para obtener información sobre cómo llamar a un cmdlet. 
    
- Usar Windows PowerShell y Windows PowerShell scripts para llamar a Exchange cmdlets del Shell de administración. Puede encontrar una lista completa de la Exchange Server [PowerShell (Exchange Shell](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)de administración) , junto con ejemplos que muestran cómo usarlos. 
    
## <a name="see-also"></a>Vea también

- [Configurar la aplicación EWS](setting-up-your-ews-application.md)   
- [Exchange cmdlets de 2013](https://docs.microsoft.com/powershell/exchange/?view=exchange-ps)  
    

