---
title: Configurar el entorno de desarrollo de aplicación de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 91b86e93-bdde-41c3-9680-45cf61420592
description: Obtenga información sobre cómo configurar el entorno de desarrollo para crear una aplicación de EWS que se comunica con Exchange.
ms.openlocfilehash: 0c7d4c6d37b28b6797bdb638930b8582f31ffc5e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763299"
---
# <a name="setting-up-your-exchange-application-development-environment"></a>Configurar el entorno de desarrollo de aplicación de Exchange

Obtenga información sobre cómo configurar el entorno de desarrollo para crear una aplicación de EWS que se comunica con Exchange.
  
Antes de comenzar a escribir la aplicación de servicios Web de Exchange (EWS), debe asegurarse de que el entorno de desarrollo cumple unos requisitos mínimos. Puede usar la API administrada de EWS, la API de acceso de cliente estándar para las aplicaciones de .NET Framework, para desarrollar la aplicación, o puede usar EWS en su propio, con nuestro sin un proxy generado automáticamente. En general, se recomienda que utilice la API administrada de EWS; Sin embargo, puede [Explorar la diferencia entre estas dos opciones](ews-client-design-overview-for-exchange.md) con más detalle para buscar out que uno es adecuada para usted. 
  
> [!NOTE]
>  [!NOTA]  La API administrada EWS ya está disponible como un proyecto de código abierto en [GitHub](https://github.com/officedev/ews-managed-api). Puede usar la biblioteca de código abierto para: >  Contribuir con correcciones de errores y mejoras a la API. >  Obtener correcciones y mejoras antes de que estén disponibles en una versión oficial. >  Tener acceso a una implementación más completa y actualizada de la API, para usarla como referencia o para crear nuevas bibliotecas en nuevas plataformas. >  Le agradecemos las [aportaciones](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) que realice a través de GitHub. 
  
## <a name="development-environment-for-the-ews-managed-api"></a>Entorno de desarrollo para la API administrada de EWS
<a name="bk_EWSMA"> </a>

Para crear una aplicación de API administrada de EWS, necesitará tener acceso a la siguiente:
  
- La [API administrada EWS](http://aka.ms/ews-managed-api-readme). 
    
    Puede almacenar los archivos de la API administrada de EWS en cualquier lugar en el equipo; de forma predeterminada, se instalan en los servicios de Files\Microsoft\Exchange\Web programa\\< número de versión\> carpeta.
    
- Un buzón de correo en un servidor de Exchange que ejecuta Exchange Online como parte de Office 365, Exchange Online o una versión de Exchange empezando con Exchange Server 2007. 
    
    Puede obtener un plan de Exchange Online para la empresa, incluida una versión de prueba gratuita desde el [sitio de Office 365](http://office.microsoft.com/en-us/business/compare-office-365-for-business-plans-FX102918419.aspx#fbid=1tsGNIE7e3a). Para conectar con el buzón de correo deben tener el nombre de usuario y las credenciales de la cuenta asociada con el buzón de correo.
    
- Una versión de Visual Studio desde Visual Studio 2005. Si actualmente no dispone de Visual Studio, puede descargar una versión gratuita de [Visual Studio 2010 Express](http://www.microsoft.com/visualstudio/eng/products/visual-studio-2010-express).
    
- Una versión de .NET Framework a partir con .NET Framework 3.5. .NET Framework 3.5 se puede descargar desde el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?LinkId=191777).
    
Además, es útil si tiene un poco familiarizado con C#. Aunque Visual Studio es compatible con otros idiomas además de C#, la mayoría del código de ejemplo disponible para la API administrada de EWS está escrito en C#.
  
## <a name="development-environment-for-ews"></a>Entorno de desarrollo para EWS
<a name="bk_EWS"> </a>

Puede usar EWS para desarrollar la aplicación en un par de maneras diferentes. Es la forma más sencilla de usar EWS crear archivos de texto que contienen las solicitudes XML y transmitirlos a Exchange. Para ello, aquí es lo que necesita: 
  
- Un simple editor de texto, como el Bloc de notas, para editar la solicitud XML. Va a hacer cualquier editor de texto, aunque es posible que desee que le ayudará a con la validación de la sintaxis XML como XMetal.
    
- Una herramienta o aplicación que puede enviar y recibir solicitudes SOAP XML y las respuestas, para que pueda comunicarse con Exchange.
    
Cuando se trabaja con XML sin formato, también resulta útil tener un conocimiento básico de formato XML.
  
La segunda forma de uso de EWS consiste en crear a un proxy generado automáticamente que le permite trabajar con las operaciones mediante el uso de un lenguaje de .NET como C#. Aquí es lo que necesita para que funcione con un proxy generado automáticamente:
  
- Una versión de Visual Studio 2005, para crear una referencia de proxy a partir de Visual Studio. Puede descargar una versión gratuita de [Visual Studio 2010 Express](http://www.microsoft.com/visualstudio/eng/products/visual-studio-2010-express).
    
- Una versión de .NET Framework a partir con .NET Framework 2.0. .NET Framework 3.5 se puede descargar desde el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?LinkId=191777).
    
Si utiliza a un proxy generado automáticamente, desea tener un poco familiarizado con la programación de C#.
  
> [!NOTE]
> Si es un programador de .NET Framework, le recomendamos que se va a usar la API administrada de EWS en lugar de servidores proxy generado automáticamente para el desarrollo en EWS. El modelo de objetos de la API administrada de EWS es más fácil de usar que los modelos de objetos de servidor proxy generado automáticamente. Además, la API administrada de EWS implementa la [detección automática](autodiscover-for-exchange.md) e incluye lógica del lado del cliente. 
  
## <a name="see-also"></a>Vea también


- [Configurar el entorno de desarrollo de aplicación de Exchange](setting-up-your-exchange-application-development-environment.md)
    
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
    
- [Controlar el acceso a EWS en Exchange](how-to-control-access-to-ews-in-exchange.md)
    
- [EWS genera modelos de objetos para Exchange](https://msdn.microsoft.com/en-us/library/jj190899)
    

