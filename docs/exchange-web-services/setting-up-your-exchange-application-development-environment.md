---
title: Configurar su entorno de desarrollo de aplicaciones de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 91b86e93-bdde-41c3-9680-45cf61420592
description: Obtenga información sobre cómo configurar el entorno de desarrollo para crear una aplicación de EWS que se comunique con Exchange.
localization_priority: Priority
ms.openlocfilehash: 01a106817f29bd696991b8a0c5d7d9b7dd420b94
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463765"
---
# <a name="setting-up-your-exchange-application-development-environment"></a>Configurar su entorno de desarrollo de aplicaciones de Exchange

Obtenga información sobre cómo configurar el entorno de desarrollo para crear una aplicación de EWS que se comunique con Exchange.
  
Antes de empezar a escribir la aplicación de servicios Web de Exchange (EWS), deberá asegurarse de que el entorno de desarrollo cumple unos requisitos mínimos. Puede usar la API administrada de EWS, la API de acceso de cliente estándar para las aplicaciones de .NET Framework, para desarrollar la aplicación o puede usar EWS por su cuenta, con nuestro sin un proxy generado automáticamente. En general, se recomienda usar la API administrada de EWS; sin embargo, puede [explorar la diferencia entre estas dos opciones](ews-client-design-overview-for-exchange.md) con más detalle para averiguar cuál es la más adecuada para usted. 
  
> [!NOTE]
> La API administrada EWS ya está disponible como proyecto de código abierto en [GitHub](https://github.com/officedev/ews-managed-api). Puede usar la biblioteca de código abierto para: 
> - Contribuir con correcciones de errores y mejoras a la API. 
> - Obtener correcciones y mejoras antes de que estén disponibles en una versión oficial. 
> - Tener acceso a una implementación más completa y actualizada de la API, para usarla como referencia o para crear nuevas bibliotecas en nuevas plataformas.
> 
>  Le agradecemos las [aportaciones](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) que realice a través de GitHub. 
  
## <a name="development-environment-for-the-ews-managed-api"></a>Entorno de desarrollo para la API administrada de EWS
<a name="bk_EWSMA"> </a>

Para crear una aplicación de la API administrada de EWS, necesitará tener acceso a lo siguiente:
  
- La [API administrada EWS](https://aka.ms/ews-managed-api-readme). 
    
    Puede almacenar los archivos de la API administrada de EWS en cualquier lugar del equipo; de forma predeterminada, se instalan en la Files\Microsoft\Exchange\Web de la carpeta de número de versión del programa \\<Services \> .
    
- Un buzón de correo en un servidor de Exchange que ejecuta Exchange Online, Exchange online como parte de Office 365 o una versión de Exchange que empieza con Exchange Server 2007. 
    
    Puede obtener un plan de Exchange Online para empresas, incluida una prueba gratuita, desde el [sitio de Office 365](https://office.microsoft.com/business/compare-office-365-for-business-plans-FX102918419.aspx#fbid=1tsGNIE7e3a). Para conectarse al buzón de correo, debe tener el nombre de usuario y las credenciales de la cuenta asociada con el buzón.

    
- Una versión de Visual Studio a partir de Visual Studio 2005. Si actualmente no tiene Visual Studio, puede descargar una [versión gratuita](https://visualstudio.microsoft.com/).
    
- Una versión de .NET Framework a partir de .NET Framework 3,5. Puede descargar .NET Framework 3,5 desde el centro de [descarga de Microsoft](https://go.microsoft.com/fwlink/?LinkId=191777).
    
Además, es útil si está familiarizado con C#. Aunque Visual Studio admite otros lenguajes además de C#, la mayor parte del código de ejemplo disponible para la API administrada de EWS está escrito en C#.
  
## <a name="development-environment-for-ews"></a>Entorno de desarrollo para EWS
<a name="bk_EWS"> </a>

Puede usar EWS para desarrollar la aplicación de dos maneras diferentes. La forma más sencilla de usar EWS es crear archivos de texto que contengan las solicitudes XML y transmitirlos a Exchange. Para ello, puede ver lo que necesita: 
  
- Un editor de texto simple, como el Bloc de notas, para editar la solicitud XML. Cualquier editor de texto lo hará, aunque es posible que le interese usar una validación de sintaxis XML como XMetal.
    
- Una herramienta o aplicación que puede enviar y recibir respuestas y solicitudes XML de SOAP, para poder comunicarse con Exchange.
    
Cuando se trabaja con XML sin formato, también es útil tener conocimientos básicos sobre el formato XML.
  
La segunda forma de usar EWS es crear un proxy generado automáticamente que le permita trabajar con las operaciones mediante un lenguaje .NET como C#. Esto es lo que necesita para trabajar con un proxy generado automáticamente:
  
- Una versión de Visual Studio a partir de Visual Studio 2005, para crear una referencia de proxy. Puede descargar una [versión gratuita](https://visualstudio.microsoft.com/).
    
- Una versión de .NET Framework a partir de .NET Framework 2,0. Puede descargar .NET Framework 3,5 desde el centro de [descarga de Microsoft](https://go.microsoft.com/fwlink/?LinkId=191777).
    
Si usa un proxy generado automáticamente, le interesará estar familiarizado con la programación en C#.
  
> [!NOTE]
> Si es desarrollador de .NET Framework, le animamos a usar la API administrada de EWS en lugar de los proxy generados automáticamente para desarrollar con EWS. El modelo de objetos de la API administrada de EWS es más fácil de usar que los modelos de objetos de proxy generados automáticamente. Además, la API administrada de EWS implementa [detección automática](autodiscover-for-exchange.md) e incluye lógica del lado cliente. 
  
## <a name="see-also"></a>Vea también

- [Configurar su entorno de desarrollo de aplicaciones de Exchange](setting-up-your-exchange-application-development-environment.md)   
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)  
- [Controlar el acceso a EWS en Exchange](how-to-control-access-to-ews-in-exchange.md)  
- [Modelos de objeto generados por EWS para Exchange](https://msdn.microsoft.com/library/jj190899)
    