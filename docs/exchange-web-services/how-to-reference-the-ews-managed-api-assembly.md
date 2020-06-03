---
title: Hacer referencia al ensamblado de la API administrada de EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 130990db-6297-42dc-9f5d-f68a2400872a
description: Busque información sobre cómo hacer referencia al ensamblado de la API administrada de EWS.
localization_priority: Priority
ms.openlocfilehash: d49091781da279d87a1eab35608f19ece43a0333
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527764"
---
# <a name="reference-the-ews-managed-api-assembly"></a>Hacer referencia al ensamblado de la API administrada de EWS

Busque información sobre cómo hacer referencia al ensamblado de la API administrada de EWS.
  
La API administrada de EWS proporciona una interfaz sencilla y completa para desarrollar y extender aplicaciones que usan servicios web Exchange (EWS). Independientemente de si usa Visual Studio u otro editor de código para desarrollar la aplicación de la API administrada de EWS, necesitará hacer una referencia al ensamblado de la API administrada de EWS. Si todavía no ha instalado la API administrada EWS, asegúrese de [descargar la API](https://aka.ms/ews-managed-api-readme).
  
> [!NOTE]
> La API administrada EWS ya está disponible como proyecto de código abierto en [GitHub](https://github.com/officedev/ews-managed-api). Puede usar la biblioteca de código abierto para: 
> - Contribuir con correcciones de errores y mejoras a la API. 
> - Obtener correcciones y mejoras antes de que estén disponibles en una versión oficial. 
> - Tener acceso a una implementación más completa y actualizada de la API, para usarla como referencia o para crear nuevas bibliotecas en nuevas plataformas.
> 
>  Le agradecemos las [aportaciones](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) que realice a través de GitHub. 
  
## <a name="referencing-the-assembly"></a>Hacer referencia al ensamblado

La forma más común de agregar una referencia es usar Visual Studio. Sabemos que algunos desarrolladores nos gusta usar otros editores, por lo que se incluyen instrucciones para usar el compilador de línea de comandos, así como instrucciones para usar Visual Studio. Es posible que observe que los ejemplos de código siguientes tienen las mismas instrucciones **using** . La diferencia entre los dos métodos es que el compilador de línea de comandos necesita la ubicación del archivo de ensamblado. La referencia de Visual Studio administra esto por usted en segundo plano. 
  
### <a name="to-add-a-reference-by-using-visual-studio"></a>Para agregar una referencia con Visual Studio

1. Coloque el archivo Microsoft. Exchange. webservices. dll y el archivo Microsoft. Exchange. webservices. XML en una carpeta de su elección. De forma predeterminada, los archivos están instalados en `C:\Program Files\Microsoft\Exchange\Web Services\2.0\` , pero puede almacenar los archivos en cualquier lugar del equipo.
    
2. En el panel Explorador de soluciones en Visual Studio, seleccione **referencias**y, después, haga clic en **Agregar referencia**. Se abrirá la ventana Agregar referencia.
    
3. En la ventana Agregar referencia, vaya a la pestaña **examinar** , busque la ubicación del archivo Microsoft. Exchange. webservices. dll, seleccione ese archivo y, después, seleccione **Aceptar**. 
    
4. Para usar la API administrada de EWS en su aplicación, agregue una instrucción **using** para el espacio de nombres **Microsoft. Exchange. webservices. Data** . 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

### <a name="to-add-a-reference-and-build-your-application-with-the-command-line-compiler"></a>Para agregar una referencia y compilar la aplicación con el compilador de línea de comandos

1. Coloque el archivo Microsoft. Exchange. webservices. dll en una carpeta de su elección. Esta carpeta será la carpeta de salida del compilador.
    
2. En el editor de código fuente, agregue una instrucción **using** al código fuente del espacio de nombres **Microsoft. Exchange. webservices. Data** . 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

3. Ejecute el compilador de línea de comandos para compilar la aplicación. El siguiente comando usa el compilador de C# de .NET Framework para compilar la aplicación de Windows definida en el archivo de código fuente "program.cs". Se supone que el compilador se encuentra en el directorio de instalación predeterminado y que el archivo Microsoft. Exchange. webservices. dll está en un subdirectorio del directorio actual denominado "Build".
    
   ```cs
    c:\Windows\Microsoft.NET\Framework\3.5\csc /target: winexe /out: build\testApplication /reference: build\Microsoft.Exchange.WebServices.dll program.cs
   ```

## <a name="see-also"></a>Vea también

- [Empezar a trabajar con aplicaciones de cliente de la API administrada de EWS](get-started-with-ews-managed-api-client-applications.md)    
- [Configurar su entorno de desarrollo de aplicaciones de Exchange](setting-up-your-exchange-application-development-environment.md)   
- [Comunicarse con EWS mediante la API administrada de EWS](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    

