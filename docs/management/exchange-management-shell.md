---
title: Shell de administración de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cc0c4fa-9e13-45cb-88da-0486f2ac1bd0
description: Obtenga información acerca de cómo usar el Shell de administración de Exchange para desarrollar herramientas de administración de Exchange server.
ms.openlocfilehash: 1cb0328bdb0eebda0ce4eda929e1bfb21be451f4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763312"
---
# <a name="exchange-management-shell"></a>Shell de administración de Exchange

Obtenga información acerca de cómo usar el Shell de administración de Exchange para desarrollar herramientas de administración de Exchange server.
  
**Se aplica a:** Exchange Online | Exchange Server 2013 | Office 365
  
El Shell de administración de Exchange proporciona un amplio conjunto de comandos, en función de la plataforma de Windows PowerShell para la administración de Exchange Online, Exchange Online como parte de Office 365 o una versión local de Exchange comenzando con Exchange 2013. Puede usar el Shell de administración de Exchange para crear dos tipos de herramientas: secuencias de comandos de línea de comandos que funcionan dentro del entorno de Windows PowerShell y herramientas que use los cmdlets del Shell de administración de Exchange a través de una interfaz administrada. Puede usar aplicaciones administradas para crear un estándar de Windows o la interfaz de usuario basada en web para administrar un servidor de Exchange. 
  
## <a name="what-you-need-to-know-about-the-exchange-management-shell"></a>¿Qué necesita saber sobre el Shell de administración de Exchange

|Si se pregunta acerca de|Lea esto|
|:-----|:-----|
|Disponibilidad  <br/> |Comandos de Shell de administración de Exchange se instalan en todos los servidores que ejecutan versiones de Exchange a partir de Exchange 2007.<br/>Las aplicaciones cliente se pueden implementar en cualquier equipo que ejecute Windows PowerShell 2.0.<br/> Para obtener información acerca del acceso a la consola, consulte [Exchange Server PowerShell (Shell de administración de Exchange)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps).  <br/> |
|Lenguajes y herramientas  <br/> |Puede crear secuencias de comandos de Shell de administración de Exchange en cualquier editor de texto.<br/>Puede usar una de las muchas herramientas de terceros para la creación de scripts de Windows PowerShell que se pueden usar con el Shell de administración de Exchange.  <br/> El [modelo de objetos de Shell de administración de Exchange](exchange-management-shell-namespaces.md) se basa en .NET Framework.<br/>Puede utilizar cualquier lenguaje de .NET para desarrollar aplicaciones de Shell de administración de Exchange.  <br/> |
|Las pruebas y las herramientas de depuración disponibles  <br/> |Puede usar una de las muchas aplicaciones de terceros para probar y depurar las secuencias de comandos de Shell de administración de Exchange.  <br/> Puede usar Visual Studio y herramientas de terceros para probar y depurar las aplicaciones de consola de administración de Exchange administradas.  <br/> |
|Requisitos de plataforma del servidor  <br/> |Puede usar el Shell de administración de Exchange en cualquier servidor de Exchange que tiene instalado Windows PowerShell 2.0.  <br/> |
|Requisitos de plataforma del cliente  <br/> |Las aplicaciones de cliente de Shell de administración de Exchange requieren Windows PowerShell 2.0.  <br/> |
|Permisos  <br/> |Ejecuta un Shell de administración de Exchange aplicación requiere que el usuario tiene derechos de control de acceso basado en roles a los datos afectados en el almacén de Exchange.<br/>Para obtener más información acerca de control de acceso basado en roles, consulte [Understanding Role Based Access Control](http://technet.microsoft.com/en-us/library/dd298183.aspx).  <br/> |
   
Los artículos de esta sección describen las características de Shell de administración de Exchange que son importantes para la creación de herramientas de administración de Exchange. Para obtener información acerca de la planeación, la configuración y el mantenimiento de Exchange, consulte el sitio de [Exchange](https://docs.microsoft.com/en-us/exchange/) .
  
## <a name="in-this-section"></a>En esta sección

- [Creación de herramientas de Shell de administración de Exchange](create-exchange-management-shell-tools.md)
    
- [Espacios de nombres de Shell de administración de Exchange](exchange-management-shell-namespaces.md)
    
## <a name="see-also"></a>Vea también
  
- [Documentación de Windows PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-6)
- [Secuencias de comandos de PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/powershell-scripting?view=powershell-6)
    

