---
title: Shell de administración de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cc0c4fa-9e13-45cb-88da-0486f2ac1bd0
description: Obtenga información sobre cómo usar el shell de administración de Exchange para desarrollar herramientas para la administración de Exchange Server.
ms.openlocfilehash: 38e75339a4ad97cf8ff99e1cbe9c01059e157941
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44435810"
---
# <a name="exchange-management-shell"></a>Shell de administración de Exchange

Obtenga información sobre cómo usar el shell de administración de Exchange para desarrollar herramientas para la administración de Exchange Server.
  
**Se aplica a:** Exchange Online | Exchange Server 2013 | Office 365
  
El shell de administración de Exchange proporciona un amplio conjunto de comandos, basados en la plataforma Windows PowerShell, para administrar Exchange Online, Exchange online como parte de Office 365 o una versión local de Exchange a partir de Exchange 2013. Puede usar el shell de administración de Exchange para crear dos tipos de herramientas: scripts de línea de comandos que funcionan en el entorno de Windows PowerShell y herramientas que usan los cmdlets del shell de administración de Exchange a través de una interfaz administrada. Puede usar aplicaciones administradas para crear una interfaz de usuario de Windows o basada en web estándar para administrar un servidor de Exchange. 
  
## <a name="what-you-need-to-know-about-the-exchange-management-shell"></a>Lo que debe saber sobre el shell de administración de Exchange

|Si está preguntando|Lea esto|
|:-----|:-----|
|Disponibilidad  <br/> |Los comandos del shell de administración de Exchange se instalan en todos los servidores que ejecutan versiones de Exchange a partir de Exchange 2007.<br/>Las aplicaciones cliente se pueden implementar en cualquier equipo que ejecute Windows PowerShell 2,0.<br/> Para obtener información sobre cómo obtener acceso al shell, vea [Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps).  <br/> |
|Lenguajes y herramientas  <br/> |Puede crear scripts del shell de administración de Exchange en cualquier editor de texto.<br/>Puede usar una de las muchas herramientas de terceros para crear scripts de Windows PowerShell que se pueden usar con el shell de administración de Exchange.  <br/> El [modelo de objetos del shell de administración de Exchange](exchange-management-shell-namespaces.md) se basa en .NET Framework.<br/>Puede usar cualquier lenguaje .NET para desarrollar aplicaciones de Shell de administración de Exchange.  <br/> |
|Las pruebas y las herramientas de depuración disponibles  <br/> |Puede usar una de las muchas aplicaciones de terceros para probar y depurar scripts del shell de administración de Exchange.  <br/> Puede usar Visual Studio y herramientas de terceros para probar y depurar aplicaciones de Shell de administración de Exchange administradas.  <br/> |
|Requisitos de plataforma del servidor  <br/> |Puede usar el shell de administración de Exchange en cualquier servidor de Exchange que tenga instalado Windows PowerShell 2,0.  <br/> |
|Requisitos de plataforma del cliente  <br/> |Las aplicaciones cliente de Shell de administración de Exchange requieren Windows PowerShell 2,0.  <br/> |
|Permisos  <br/> |Ejecutar una aplicación Shell de administración de Exchange requiere que el usuario tenga derechos de control de acceso basados en roles en los datos afectados del almacén de Exchange.<br/>Para obtener más información acerca del control de acceso basado en roles, consulte [Understanding role based access control](https://technet.microsoft.com/library/dd298183.aspx).  <br/> |
   
En los artículos de esta sección se describen las características de Shell de administración de Exchange que son importantes para crear herramientas de administración de Exchange. Para obtener información acerca de cómo planear, configurar o mantener Exchange, consulte el sitio de [Exchange](https://docs.microsoft.com/exchange/) .
  
## <a name="in-this-section"></a>En esta sección

- [Crear herramientas de Shell de administración de Exchange](create-exchange-management-shell-tools.md)
    
- [Espacios de nombres del shell de administración de Exchange](exchange-management-shell-namespaces.md)
    
## <a name="see-also"></a>Vea también
  
- [Documentación de Windows PowerShell](https://docs.microsoft.com/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-6)
- [Scripting de PowerShell](https://docs.microsoft.com/powershell/scripting/powershell-scripting?view=powershell-6)
    

