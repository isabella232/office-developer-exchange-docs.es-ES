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
# <a name="reference-the-ews-managed-api-assembly"></a><span data-ttu-id="68ed8-103">Hacer referencia al ensamblado de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="68ed8-103">Reference the EWS Managed API assembly</span></span>

<span data-ttu-id="68ed8-104">Busque información sobre cómo hacer referencia al ensamblado de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="68ed8-104">Find information about how to reference the EWS Managed API assembly.</span></span>
  
<span data-ttu-id="68ed8-105">La API administrada de EWS proporciona una interfaz sencilla y completa para desarrollar y extender aplicaciones que usan servicios web Exchange (EWS).</span><span class="sxs-lookup"><span data-stu-id="68ed8-105">The EWS Managed API provides a simple and full-featured interface for developing and extending applications that use Exchange Web Services (EWS).</span></span> <span data-ttu-id="68ed8-106">Independientemente de si usa Visual Studio u otro editor de código para desarrollar la aplicación de la API administrada de EWS, necesitará hacer una referencia al ensamblado de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="68ed8-106">Whether you are using Visual Studio or another code editor to develop your EWS Managed API application, you will need to make a reference to the EWS Managed API assembly.</span></span> <span data-ttu-id="68ed8-107">Si todavía no ha instalado la API administrada EWS, asegúrese de [descargar la API](https://aka.ms/ews-managed-api-readme).</span><span class="sxs-lookup"><span data-stu-id="68ed8-107">If you haven't installed the EWS Managed API already, be sure to [download the API](https://aka.ms/ews-managed-api-readme).</span></span>
  
> [!NOTE]
> <span data-ttu-id="68ed8-108">La API administrada EWS ya está disponible como proyecto de código abierto en [GitHub](https://github.com/officedev/ews-managed-api).</span><span class="sxs-lookup"><span data-stu-id="68ed8-108">The EWS Managed API is now available as an open source project on [GitHub](https://github.com/officedev/ews-managed-api).</span></span> <span data-ttu-id="68ed8-109">Puede usar la biblioteca de código abierto para:</span><span class="sxs-lookup"><span data-stu-id="68ed8-109">You can use the open source library to:</span></span> 
> - <span data-ttu-id="68ed8-110">Contribuir con correcciones de errores y mejoras a la API.</span><span class="sxs-lookup"><span data-stu-id="68ed8-110">Contribute bug fixes and enhancements to the API.</span></span> 
> - <span data-ttu-id="68ed8-111">Obtener correcciones y mejoras antes de que estén disponibles en una versión oficial.</span><span class="sxs-lookup"><span data-stu-id="68ed8-111">Get fixes and enhancements before they are available in an official release.</span></span> 
> - <span data-ttu-id="68ed8-112">Tener acceso a una implementación más completa y actualizada de la API, para usarla como referencia o para crear nuevas bibliotecas en nuevas plataformas.</span><span class="sxs-lookup"><span data-stu-id="68ed8-112">Access the most comprehensive and up-to-date implementation of the API, to use as a reference or to create new libraries on new platforms.</span></span>
> 
>  <span data-ttu-id="68ed8-113">Le agradecemos las [aportaciones](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) que realice a través de GitHub.</span><span class="sxs-lookup"><span data-stu-id="68ed8-113">We welcome your [contributions](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) via GitHub.</span></span> 
  
## <a name="referencing-the-assembly"></a><span data-ttu-id="68ed8-114">Hacer referencia al ensamblado</span><span class="sxs-lookup"><span data-stu-id="68ed8-114">Referencing the assembly</span></span>

<span data-ttu-id="68ed8-115">La forma más común de agregar una referencia es usar Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="68ed8-115">The most common way to add a reference is to use Visual Studio.</span></span> <span data-ttu-id="68ed8-116">Sabemos que algunos desarrolladores nos gusta usar otros editores, por lo que se incluyen instrucciones para usar el compilador de línea de comandos, así como instrucciones para usar Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="68ed8-116">We know that some developers out there like to use other editors, so we are including instructions for using the command-line compiler as well as instructions for using Visual Studio.</span></span> <span data-ttu-id="68ed8-117">Es posible que observe que los ejemplos de código siguientes tienen las mismas instrucciones **using** .</span><span class="sxs-lookup"><span data-stu-id="68ed8-117">You might notice that the code examples that follow have the same **using** statements.</span></span> <span data-ttu-id="68ed8-118">La diferencia entre los dos métodos es que el compilador de línea de comandos necesita la ubicación del archivo de ensamblado.</span><span class="sxs-lookup"><span data-stu-id="68ed8-118">The difference between the two methods is that the command-line compiler needs the location of the assembly file.</span></span> <span data-ttu-id="68ed8-119">La referencia de Visual Studio administra esto por usted en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="68ed8-119">The Visual Studio reference handles this for you behind the scenes.</span></span> 
  
### <a name="to-add-a-reference-by-using-visual-studio"></a><span data-ttu-id="68ed8-120">Para agregar una referencia con Visual Studio</span><span class="sxs-lookup"><span data-stu-id="68ed8-120">To add a reference by using Visual Studio</span></span>

1. <span data-ttu-id="68ed8-121">Coloque el archivo Microsoft. Exchange. webservices. dll y el archivo Microsoft. Exchange. webservices. XML en una carpeta de su elección.</span><span class="sxs-lookup"><span data-stu-id="68ed8-121">Put the Microsoft.Exchange.WebServices.dll file and the Microsoft.Exchange.WebServices.xml file into a folder of your choice.</span></span> <span data-ttu-id="68ed8-122">De forma predeterminada, los archivos están instalados en `C:\Program Files\Microsoft\Exchange\Web Services\2.0\` , pero puede almacenar los archivos en cualquier lugar del equipo.</span><span class="sxs-lookup"><span data-stu-id="68ed8-122">By default, the files are installed in  `C:\Program Files\Microsoft\Exchange\Web Services\2.0\`, but you can store the files anywhere on your computer.</span></span>
    
2. <span data-ttu-id="68ed8-123">En el panel Explorador de soluciones en Visual Studio, seleccione **referencias**y, después, haga clic en **Agregar referencia**.</span><span class="sxs-lookup"><span data-stu-id="68ed8-123">In the Solution Explorer pane in Visual Studio, select **References**, and then choose **Add Reference**.</span></span> <span data-ttu-id="68ed8-124">Se abrirá la ventana Agregar referencia.</span><span class="sxs-lookup"><span data-stu-id="68ed8-124">This opens the Add Reference window.</span></span>
    
3. <span data-ttu-id="68ed8-125">En la ventana Agregar referencia, vaya a la pestaña **examinar** , busque la ubicación del archivo Microsoft. Exchange. webservices. dll, seleccione ese archivo y, después, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="68ed8-125">In the Add Reference window, navigate to the **Browse** tab, browse to the location of the Microsoft.Exchange.WebServices.dll file, select that file, and then select **OK**.</span></span> 
    
4. <span data-ttu-id="68ed8-126">Para usar la API administrada de EWS en su aplicación, agregue una instrucción **using** para el espacio de nombres **Microsoft. Exchange. webservices. Data** .</span><span class="sxs-lookup"><span data-stu-id="68ed8-126">To use the EWS Managed API in your application, add a **using** statement for the **Microsoft.Exchange.WebServices.Data** namespace.</span></span> 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

### <a name="to-add-a-reference-and-build-your-application-with-the-command-line-compiler"></a><span data-ttu-id="68ed8-127">Para agregar una referencia y compilar la aplicación con el compilador de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="68ed8-127">To add a reference and build your application with the command-line compiler</span></span>

1. <span data-ttu-id="68ed8-128">Coloque el archivo Microsoft. Exchange. webservices. dll en una carpeta de su elección.</span><span class="sxs-lookup"><span data-stu-id="68ed8-128">Put the Microsoft.Exchange.WebServices.dll file into a folder of your choice.</span></span> <span data-ttu-id="68ed8-129">Esta carpeta será la carpeta de salida del compilador.</span><span class="sxs-lookup"><span data-stu-id="68ed8-129">This folder will be the output folder for the compiler.</span></span>
    
2. <span data-ttu-id="68ed8-130">En el editor de código fuente, agregue una instrucción **using** al código fuente del espacio de nombres **Microsoft. Exchange. webservices. Data** .</span><span class="sxs-lookup"><span data-stu-id="68ed8-130">In your source code editor, add a **using** statement to the source code for the **Microsoft.Exchange.WebServices.Data** namespace.</span></span> 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

3. <span data-ttu-id="68ed8-131">Ejecute el compilador de línea de comandos para compilar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="68ed8-131">Run the command-line compiler to build the application.</span></span> <span data-ttu-id="68ed8-132">El siguiente comando usa el compilador de C# de .NET Framework para compilar la aplicación de Windows definida en el archivo de código fuente "program.cs".</span><span class="sxs-lookup"><span data-stu-id="68ed8-132">The following command uses the .NET Framework C# compiler to build the Windows application defined in the source code file "program.cs".</span></span> <span data-ttu-id="68ed8-133">Se supone que el compilador se encuentra en el directorio de instalación predeterminado y que el archivo Microsoft. Exchange. webservices. dll está en un subdirectorio del directorio actual denominado "Build".</span><span class="sxs-lookup"><span data-stu-id="68ed8-133">It assumes that the compiler is located in the default installation directory and that the Microsoft.Exchange.WebServices.dll file is in a subdirectory of the current directory named "build".</span></span>
    
   ```cs
    c:\Windows\Microsoft.NET\Framework\3.5\csc /target: winexe /out: build\testApplication /reference: build\Microsoft.Exchange.WebServices.dll program.cs
   ```

## <a name="see-also"></a><span data-ttu-id="68ed8-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="68ed8-134">See also</span></span>

- [<span data-ttu-id="68ed8-135">Empezar a trabajar con aplicaciones de cliente de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="68ed8-135">Get started with EWS Managed API client applications</span></span>](get-started-with-ews-managed-api-client-applications.md)    
- [<span data-ttu-id="68ed8-136">Configurar su entorno de desarrollo de aplicaciones de Exchange</span><span class="sxs-lookup"><span data-stu-id="68ed8-136">Setting up your Exchange application development environment</span></span>](setting-up-your-exchange-application-development-environment.md)   
- [<span data-ttu-id="68ed8-137">Comunicarse con EWS mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="68ed8-137">Communicate with EWS by using the EWS Managed API</span></span>](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    

