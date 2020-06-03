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
# <a name="use-the-exchange-management-shell-cmdlet-response"></a>Usar la respuesta del cmdlet de Shell de administración de Exchange

Obtenga información sobre cómo usar la respuesta de un cmdlet del shell de administración de Exchange en su aplicación administrada de Exchange.
  
**Se aplica a:** Exchange Online | Exchange Server 2013 | Office 365
  
Cada cmdlet del shell de administración de Exchange devuelve una o más instancias de [PSObject](https://msdn.microsoft.com/library/system.management.automation.psobject%28VS.85%29.aspx) que proporcionan una vista coherente de cualquier objeto en el entorno de Shell de administración de Exchange. En este artículo se proporciona información acerca de cómo usar las propiedades de una instancia de **PSObject** para devolver los valores de propiedad del objeto subyacente de la API de Exchange Server 2013. 
  
## <a name="prerequisites-for-using-cmdlet-responses"></a>Requisitos previos para usar respuestas de cmdlet
<a name="prerequisites_bk"> </a>

Para usar las respuestas de cmdlet, necesita una referencia al espacio de nombres **System. Automation. Management** . 
  
> [!NOTE]
>  Cuando use Visual Studio para crear una aplicación, debe agregar una referencia al ensamblado System. Mangagement. Automation. dll en el proyecto. Puede encontrar el ensamblado en una de las siguientes ubicaciones: 
> - En los sistemas operativos Windows XP y Windows Vista, el directorio de instalación de Windows PowerShell ($PSHOME). 
> - En los sistemas operativos Windows 7 y Windows 8, la siguiente carpeta: Windows\assembly\GAC_MSIL\System.Management.Automation. 
  
## <a name="windows-powershell-remote-runspace"></a>Espacio de ejecución remoto de Windows PowerShell
<a name="usingremoterunspace_bk"> </a>

El shell de administración de Exchange usa características de Windows PowerShell remotas para todos los comandos, incluso los que se ejecutan en el servidor local. Como resultado, todas las respuestas de los cmdlets del shell de administración de Exchange son XML serializado. Esto significa que, aunque el objeto Response indica el tipo de objeto de Exchange que se usó para generar la respuesta, el objeto Response no puede convertirse en el tipo de objeto de Exchange; en su lugar, debe usar el contenedor de propiedades que expone el objeto Response para obtener los valores del tipo de objeto de Exchange.
  
El contenedor de propiedades en el objeto Response contiene un par clave-valor para cada propiedad o método públicos en el tipo de objeto de Exchange. El objeto Response contiene el nombre del tipo de objeto de Exchange subyacente; puede usar este nombre para determinar el tipo de objeto de Exchange representado por el objeto Response para que pueda extraer la propiedad adecuada. Cada valor del contenedor de propiedades también incluye información de tipos, por lo que puede convertir el valor de la propiedad en el tipo administrado adecuado.
  
## <a name="use-the-cmdlet-response"></a>Usar la respuesta del cmdlet
<a name="usingPSObject_bk"> </a>

La clase [PSObject](https://msdn.microsoft.com/library/system.management.automation.psobject%28VS.85%29.aspx) expone las siguientes tres propiedades públicas que contienen los valores del objeto subyacente de la API de Exchange 2013: [propiedades](https://msdn.microsoft.com/library/system.management.automation.psobject.properties%28VS.85%29.aspx), [métodos](https://msdn.microsoft.com/library/system.management.automation.psobject.methods%28VS.85%29.aspx)y [miembros](https://msdn.microsoft.com/library/system.management.automation.psobject.members%28VS.85%29.aspx). Cada propiedad expuesta por el objeto de la API de Exchange 2013 tiene un par clave-valor correspondiente en las propiedades **Properties** y **Members** . La aplicación puede indizar la colección **Properties** por el nombre de una propiedad para recuperar el valor de la propiedad. 
  
Puede usar la propiedad **TypeNames** de la instancia de **psobject** para determinar el tipo del objeto de Exchange subyacente que está encapsulado por la instancia de **psobject** . La propiedad **TypeNames** es una colección de cadenas que contiene la jerarquía de objetos del tipo representado. Puede usar estos nombres para determinar el objeto representado por la instancia de **PSObject** de modo que pueda extraer la propiedad adecuada. 
  
En el ejemplo de código siguiente se usa la respuesta de cmdlet para imprimir el contenido de la colección **Properties** de una instancia de **PSObject** en la consola. El ejemplo de código requiere una referencia al espacio de nombres **System. Automation. Management** . 
  
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

## <a name="see-also"></a>Vea también

- [Crear herramientas de Shell de administración de Exchange](create-exchange-management-shell-tools.md)   
- [Obtener una lista de usuarios de correo mediante el shell de administración de Exchange](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)
    

