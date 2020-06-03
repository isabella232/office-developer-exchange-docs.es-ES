---
title: Usar la respuesta del cmdlet de Shell de administración de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dac8e526-11c6-4c2e-b9a2-f016b1fc738a
description: Obtenga información sobre cómo usar la respuesta de un cmdlet del shell de administración de Exchange en su aplicación administrada de Exchange.
ms.openlocfilehash: c1b81356ab5dc288ab08287d47581871c36beb05
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44435705"
---
# <a name="use-the-exchange-management-shell-cmdlet-response"></a><span data-ttu-id="d6610-103">Usar la respuesta del cmdlet de Shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="d6610-103">Use the Exchange Management Shell cmdlet response</span></span>

<span data-ttu-id="d6610-104">Obtenga información sobre cómo usar la respuesta de un cmdlet del shell de administración de Exchange en su aplicación administrada de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d6610-104">Learn how to use the response from an Exchange Management Shell cmdlet in your Exchange managed application.</span></span>
  
<span data-ttu-id="d6610-105">**Se aplica a:** Exchange Online | Exchange Server 2013 | Office 365</span><span class="sxs-lookup"><span data-stu-id="d6610-105">**Applies to:** Exchange Online | Exchange Server 2013 | Office 365</span></span>
  
<span data-ttu-id="d6610-106">Cada cmdlet del shell de administración de Exchange devuelve una o más instancias de [PSObject](https://msdn.microsoft.com/library/system.management.automation.psobject%28VS.85%29.aspx) que proporcionan una vista coherente de cualquier objeto en el entorno de Shell de administración de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d6610-106">Each Exchange Management Shell cmdlet returns one or more [PSObject](https://msdn.microsoft.com/library/system.management.automation.psobject%28VS.85%29.aspx) instances that provide a consistent view of any object in the Exchange Management Shell environment.</span></span> <span data-ttu-id="d6610-107">En este artículo se proporciona información acerca de cómo usar las propiedades de una instancia de **PSObject** para devolver los valores de propiedad del objeto subyacente de la API de Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d6610-107">This article provides information about how to use the properties of a **PSObject** instance to return the property values of the underlying Exchange Server 2013 API object.</span></span> 
  
## <a name="prerequisites-for-using-cmdlet-responses"></a><span data-ttu-id="d6610-108">Requisitos previos para usar respuestas de cmdlet</span><span class="sxs-lookup"><span data-stu-id="d6610-108">Prerequisites for using cmdlet responses</span></span>
<span data-ttu-id="d6610-109"><a name="prerequisites_bk"> </a></span><span class="sxs-lookup"><span data-stu-id="d6610-109"><a name="prerequisites_bk"> </a></span></span>

<span data-ttu-id="d6610-110">Para usar las respuestas de cmdlet, necesita una referencia al espacio de nombres **System. Automation. Management** .</span><span class="sxs-lookup"><span data-stu-id="d6610-110">To use cmdlet responses, you need a reference to the **System.Automation.Management** namespace.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="d6610-111">Cuando use Visual Studio para crear una aplicación, debe agregar una referencia al ensamblado System. Mangagement. Automation. dll en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="d6610-111">When you are using Visual Studio to create an application, you must add a reference to the System.Mangagement.Automation.dll assembly to the project.</span></span> <span data-ttu-id="d6610-112">Puede encontrar el ensamblado en una de las siguientes ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="d6610-112">You can find the assembly in one of the following locations:</span></span> 
> - <span data-ttu-id="d6610-113">En los sistemas operativos Windows XP y Windows Vista, el directorio de instalación de Windows PowerShell ($PSHOME).</span><span class="sxs-lookup"><span data-stu-id="d6610-113">For Windows XP and Windows Vista operating systems, the Windows PowerShell installation directory ($PSHOME).</span></span> 
> - <span data-ttu-id="d6610-114">En los sistemas operativos Windows 7 y Windows 8, la siguiente carpeta: Windows\assembly\GAC_MSIL\System.Management.Automation.</span><span class="sxs-lookup"><span data-stu-id="d6610-114">For the Windows 7 and Windows 8 operating systems, the following folder: Windows\assembly\GAC_MSIL\System.Management.Automation.</span></span> 
  
## <a name="windows-powershell-remote-runspace"></a><span data-ttu-id="d6610-115">Espacio de ejecución remoto de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d6610-115">Windows PowerShell remote runspace</span></span>
<span data-ttu-id="d6610-116"><a name="usingremoterunspace_bk"> </a></span><span class="sxs-lookup"><span data-stu-id="d6610-116"><a name="usingremoterunspace_bk"> </a></span></span>

<span data-ttu-id="d6610-117">El shell de administración de Exchange usa características de Windows PowerShell remotas para todos los comandos, incluso los que se ejecutan en el servidor local.</span><span class="sxs-lookup"><span data-stu-id="d6610-117">The Exchange Management Shell uses remote Windows PowerShell features for all commands, even commands that are run on the local server.</span></span> <span data-ttu-id="d6610-118">Como resultado, todas las respuestas de los cmdlets del shell de administración de Exchange son XML serializado.</span><span class="sxs-lookup"><span data-stu-id="d6610-118">As a result, all responses from Exchange Management Shell cmdlets are serialized XML.</span></span> <span data-ttu-id="d6610-119">Esto significa que, aunque el objeto Response indica el tipo de objeto de Exchange que se usó para generar la respuesta, el objeto Response no puede convertirse en el tipo de objeto de Exchange; en su lugar, debe usar el contenedor de propiedades que expone el objeto Response para obtener los valores del tipo de objeto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d6610-119">This means that although the response object indicates the Exchange object type that was used to generate the response, the response object cannot be cast to the Exchange object type; instead, you must use the property bag that is exposed by the response object to obtain the values from the Exchange object type.</span></span>
  
<span data-ttu-id="d6610-120">El contenedor de propiedades en el objeto Response contiene un par clave-valor para cada propiedad o método públicos en el tipo de objeto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d6610-120">The property bag in the response object contains a key/value pair for each public property or method in the Exchange object type.</span></span> <span data-ttu-id="d6610-121">El objeto Response contiene el nombre del tipo de objeto de Exchange subyacente; puede usar este nombre para determinar el tipo de objeto de Exchange representado por el objeto Response para que pueda extraer la propiedad adecuada.</span><span class="sxs-lookup"><span data-stu-id="d6610-121">The response object contains the name of the underlying Exchange object type; you can use this name to determine the Exchange object type that is represented by the response object so that you can extract the appropriate property.</span></span> <span data-ttu-id="d6610-122">Cada valor del contenedor de propiedades también incluye información de tipos, por lo que puede convertir el valor de la propiedad en el tipo administrado adecuado.</span><span class="sxs-lookup"><span data-stu-id="d6610-122">Each value in the property bag also includes type information so that you can cast the property value to the appropriate managed type.</span></span>
  
## <a name="use-the-cmdlet-response"></a><span data-ttu-id="d6610-123">Usar la respuesta del cmdlet</span><span class="sxs-lookup"><span data-stu-id="d6610-123">Use the cmdlet response</span></span>
<span data-ttu-id="d6610-124"><a name="usingPSObject_bk"> </a></span><span class="sxs-lookup"><span data-stu-id="d6610-124"><a name="usingPSObject_bk"> </a></span></span>

<span data-ttu-id="d6610-125">La clase [PSObject](https://msdn.microsoft.com/library/system.management.automation.psobject%28VS.85%29.aspx) expone las siguientes tres propiedades públicas que contienen los valores del objeto subyacente de la API de Exchange 2013: [propiedades](https://msdn.microsoft.com/library/system.management.automation.psobject.properties%28VS.85%29.aspx), [métodos](https://msdn.microsoft.com/library/system.management.automation.psobject.methods%28VS.85%29.aspx)y [miembros](https://msdn.microsoft.com/library/system.management.automation.psobject.members%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d6610-125">The [PSObject](https://msdn.microsoft.com/library/system.management.automation.psobject%28VS.85%29.aspx) class exposes the following three public properties that contain the values of the underlying Exchange 2013 API object: [Properties](https://msdn.microsoft.com/library/system.management.automation.psobject.properties%28VS.85%29.aspx), [Methods](https://msdn.microsoft.com/library/system.management.automation.psobject.methods%28VS.85%29.aspx), and [Members](https://msdn.microsoft.com/library/system.management.automation.psobject.members%28VS.85%29.aspx).</span></span> <span data-ttu-id="d6610-126">Cada propiedad expuesta por el objeto de la API de Exchange 2013 tiene un par clave-valor correspondiente en las propiedades **Properties** y **Members** .</span><span class="sxs-lookup"><span data-stu-id="d6610-126">Each property that is exposed by the Exchange 2013 API object has a corresponding key/value pair in the **Properties** and **Members** properties.</span></span> <span data-ttu-id="d6610-127">La aplicación puede indizar la colección **Properties** por el nombre de una propiedad para recuperar el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d6610-127">Your application can index the **Properties** collection by the name of a property to retrieve the value of the property.</span></span> 
  
<span data-ttu-id="d6610-128">Puede usar la propiedad **TypeNames** de la instancia de **psobject** para determinar el tipo del objeto de Exchange subyacente que está encapsulado por la instancia de **psobject** .</span><span class="sxs-lookup"><span data-stu-id="d6610-128">You can use the **TypeNames** property of the **PSObject** instance to determine the type of the underlying Exchange object that is encapsulated by the **PSObject** instance.</span></span> <span data-ttu-id="d6610-129">La propiedad **TypeNames** es una colección de cadenas que contiene la jerarquía de objetos del tipo representado.</span><span class="sxs-lookup"><span data-stu-id="d6610-129">The **TypeNames** property is a collection of strings that contains the object hierarchy of the represented type.</span></span> <span data-ttu-id="d6610-130">Puede usar estos nombres para determinar el objeto representado por la instancia de **PSObject** de modo que pueda extraer la propiedad adecuada.</span><span class="sxs-lookup"><span data-stu-id="d6610-130">You can use these names to determine the object that is represented by the **PSObject** instance so that you can extract the appropriate property.</span></span> 
  
<span data-ttu-id="d6610-131">En el ejemplo de código siguiente se usa la respuesta de cmdlet para imprimir el contenido de la colección **Properties** de una instancia de **PSObject** en la consola.</span><span class="sxs-lookup"><span data-stu-id="d6610-131">The following code example uses the cmdlet response to print the contents of the **Properties** collection of a **PSObject** instance on the console.</span></span> <span data-ttu-id="d6610-132">El ejemplo de código requiere una referencia al espacio de nombres **System. Automation. Management** .</span><span class="sxs-lookup"><span data-stu-id="d6610-132">The code example requires a reference to the **System.Automation.Management** namespace.</span></span> 
  
```cs
foreach (PSPropertyInfo propertyInfo in psObject.Properties)
{
    Console.WriteLine(string.Format("{0}: {1}",
        propertyInfo.Name, propertyInfo.Value);
}
```

<br/>

```vb
For Each PropertyInfo As PSProperty In ObjectInfo.Properties
    Console.WriteLine(String.Format("{0}: {1}", PropertyInfo.Name, PropertyInfo.Value))
Next

```

## <a name="see-also"></a><span data-ttu-id="d6610-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6610-133">See also</span></span>

- [<span data-ttu-id="d6610-134">Crear herramientas de Shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="d6610-134">Create Exchange Management Shell tools</span></span>](create-exchange-management-shell-tools.md)   
- [<span data-ttu-id="d6610-135">Obtener una lista de usuarios de correo mediante el shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="d6610-135">Get a list of mail users by using the Exchange Management Shell</span></span>](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)
    

