---
title: Hacer referencia al ensamblado de la API administrada de EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 130990db-6297-42dc-9f5d-f68a2400872a
description: Obtenga información acerca de cómo hacer referencia al ensamblado de la API administrada de EWS.
ms.openlocfilehash: af7b1ec449c24e7fa4db89abb30e5ebc9f8d329e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763161"
---
# <a name="reference-the-ews-managed-api-assembly"></a>Hacer referencia al ensamblado de la API administrada de EWS

Obtenga información acerca de cómo hacer referencia al ensamblado de la API administrada de EWS.
  
La API administrada de EWS proporciona una interfaz simple y completas para desarrollar y ampliación de las aplicaciones que usan servicios Web de Exchange (EWS). Si usa Visual Studio u otro editor de código para desarrollar la aplicación de la API administrada de EWS, debe hacer referencia al ensamblado de la API administrada de EWS. Si no ha instalado la API administrada de EWS ya, asegúrese de [Descargar la API](http://aka.ms/ews-managed-api-readme).
  
> [!NOTE]
>  [!NOTA]  La API administrada EWS ya está disponible como un proyecto de código abierto en [GitHub](https://github.com/officedev/ews-managed-api). Puede usar la biblioteca de código abierto para: >  Contribuir con correcciones de errores y mejoras a la API. >  Obtener correcciones y mejoras antes de que estén disponibles en una versión oficial. >  Tener acceso a una implementación más completa y actualizada de la API, para usarla como referencia o para crear nuevas bibliotecas en nuevas plataformas. >  Le agradecemos las [aportaciones](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) que realice a través de GitHub. 
  
## <a name="referencing-the-assembly"></a>Hacer referencia al ensamblado

Es la manera más común para agregar una referencia a usar Visual Studio. Se sabe que algunos desarrolladores lo gustaría usan otros editores, por lo que vamos a incluir instrucciones sobre cómo usar el compilador de línea de comandos, así como instrucciones para el uso de Visual Studio. Es posible que tenga en cuenta que los ejemplos de código siguientes tienen las mismas instrucciones de **uso** . La diferencia entre los dos métodos es que el compilador de línea de comandos necesita la ubicación del archivo de ensamblado. La referencia de Visual Studio encarga de segundo plano. 
  
### <a name="to-add-a-reference-by-using-visual-studio"></a>Para agregar una referencia mediante el uso de Visual Studio

1. Coloque el archivo Microsoft.Exchange.WebServices.dll y el archivo Microsoft.Exchange.WebServices.xml en una carpeta de su elección. De forma predeterminada, los archivos se instalan en `C:\Program Files\Microsoft\Exchange\Web Services\2.0\`, pero puede almacenar los archivos en cualquier lugar en el equipo.
    
2. En el panel Explorador de soluciones en Visual Studio, seleccione **referencias**y, a continuación, seleccione **Agregar referencia**. Se abrirá la ventana Agregar referencia.
    
3. En la ventana Agregar referencia, vaya a la ficha **Examinar** , vaya a la ubicación del archivo Microsoft.Exchange.WebServices.dll, seleccione el archivo y, a continuación, seleccione **Aceptar**. 
    
4. Para usar la API administrada de EWS en la aplicación, agregue una instrucción **using** para el espacio de nombres **Microsoft.Exchange.WebServices.Data** . 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

### <a name="to-add-a-reference-and-build-your-application-with-the-command-line-compiler"></a>Para agregar una referencia y crear la aplicación con el compilador de línea de comandos

1. Coloque el archivo Microsoft.Exchange.WebServices.dll en una carpeta de su elección. Esta carpeta será la carpeta de salida para el compilador.
    
2. En el editor de código fuente, agregue una instrucción **using** para el código de origen para el espacio de nombres **Microsoft.Exchange.WebServices.Data** . 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

3. Ejecutar el compilador de línea de comandos para generar la aplicación. El comando siguiente utiliza el compilador de .NET Framework C# para generar la aplicación de Windows definida en el archivo de código fuente "program.cs". Se supone que el compilador se encuentra en el directorio de instalación predeterminado y que el archivo Microsoft.Exchange.WebServices.dll está en un subdirectorio del directorio actual denominado "build".
    
   ```cs
    c:\Windows\Microsoft.NET\Framework\3.5\csc /target: winexe /out: build\testApplication /reference: build\Microsoft.Exchange.WebServices.dll program.cs
   ```

## <a name="see-also"></a>Vea también

- [Empezar a trabajar con aplicaciones de cliente de la API administrada de EWS](get-started-with-ews-managed-api-client-applications.md)    
- [Configurar el entorno de desarrollo de aplicación de Exchange](setting-up-your-exchange-application-development-environment.md)   
- [Comunicarse con EWS mediante el uso de la API administrada de EWS](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    

