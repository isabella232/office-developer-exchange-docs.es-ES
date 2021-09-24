---
title: Shell de administración de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8cc0c4fa-9e13-45cb-88da-0486f2ac1bd0
description: Encuentre información sobre cómo usar el Shell de administración Exchange para desarrollar herramientas para la administración Exchange servidor.
ms.openlocfilehash: ee1cbcb174c7153ca6cd9bb089580b372bf9029b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516156"
---
# <a name="exchange-management-shell"></a>Shell de administración de Exchange

Encuentre información sobre cómo usar el Shell de administración Exchange para desarrollar herramientas para la administración Exchange servidor.
  
**Se aplica a:** Exchange Online | Exchange Server 2013 | Office 365
  
El Shell de administración de Exchange proporciona un amplio conjunto de comandos, basados en la plataforma Windows PowerShell, para administrar Exchange Online, Exchange Online como parte de Office 365 o una versión local de Exchange empezando por Exchange 2013. Puede usar el Shell de administración de Exchange para crear dos tipos de herramientas: scripts de línea de comandos que funcionan en el entorno de Windows PowerShell y herramientas que usan los cmdlets del Shell de administración de Exchange a través de una interfaz administrada. Puede usar aplicaciones administradas para crear una interfaz de usuario Windows o basada en web para administrar un servidor Exchange web. 
  
## <a name="what-you-need-to-know-about-the-exchange-management-shell"></a>Lo que necesita saber sobre el Shell Exchange administración

|Si te estás preguntando acerca de|Lea esto|
|:-----|:-----|
|Disponibilidad  <br/> |Exchange Los comandos del Shell de administración se instalan en todos los servidores que ejecutan versiones de Exchange a partir Exchange 2007.<br/>Las aplicaciones cliente se pueden implementar en cualquier equipo que ejecute Windows PowerShell 2.0.<br/> Para obtener información acerca del acceso al shell, [vea Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps).  <br/> |
|Lenguajes y herramientas  <br/> |Puede crear scripts Exchange Shell de administración en cualquier editor de texto.<br/>Puede usar una de las muchas herramientas de terceros para crear Windows PowerShell scripts que se pueden usar con el Shell Exchange administración.  <br/> El [Exchange de objetos del Shell de administración](exchange-management-shell-namespaces.md) se basa en el .NET Framework.<br/>Puede usar cualquier lenguaje .NET para desarrollar aplicaciones Exchange Shell de administración.  <br/> |
|Las pruebas y las herramientas de depuración disponibles  <br/> |Puede usar una de muchas aplicaciones de terceros para probar y depurar Exchange scripts del Shell de administración.  <br/> Puede usar herramientas Visual Studio y de terceros para probar y depurar aplicaciones administradas Exchange Shell de administración.  <br/> |
|Requisitos de plataforma del servidor  <br/> |Puede usar el Shell Exchange administración en cualquier servidor Exchange que tenga Windows PowerShell 2.0 instalado.  <br/> |
|Requisitos de plataforma del cliente  <br/> |Exchange Las aplicaciones cliente del Shell de administración Windows PowerShell 2.0.  <br/> |
|Permisos  <br/> |La ejecución de Exchange shell de administración requiere que el usuario tenga derechos de control de acceso basados en roles en los datos afectados en el Exchange almacén.<br/>Para obtener más información sobre el control de acceso basado en roles, vea [Understanding Role Based Access Control](https://technet.microsoft.com/library/dd298183.aspx).  <br/> |
   
En los artículos de esta sección se describen Exchange del Shell de administración que son importantes para crear Exchange de administración. Para obtener información acerca de la planeación, configuración o mantenimiento de Exchange, consulte [el Exchange](https://docs.microsoft.com/exchange/) sitio.
  
## <a name="in-this-section"></a>En esta sección

- [Crear herramientas de Shell de administración de Exchange](create-exchange-management-shell-tools.md)
    
- [Espacios de nombres del Shell de administración de Exchange](exchange-management-shell-namespaces.md)
    
## <a name="see-also"></a>Ver también
  
- [Windows PowerShell documentación](https://docs.microsoft.com/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-6)
- [Scripting de PowerShell](https://docs.microsoft.com/powershell/scripting/powershell-scripting?view=powershell-6)
    

