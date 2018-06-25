---
title: Usar la respuesta de cmdlet del Shell de administración de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dac8e526-11c6-4c2e-b9a2-f016b1fc738a
description: Obtenga información sobre cómo usar la respuesta de un cmdlet del Shell de administración de Exchange en su aplicación Exchange administrado.
ms.openlocfilehash: 5edf75afd556f67e815bc519c87586f2f62f057b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763310"
---
# <a name="use-the-exchange-management-shell-cmdlet-response"></a>Usar la respuesta de cmdlet del Shell de administración de Exchange

Obtenga información sobre cómo usar la respuesta de un cmdlet del Shell de administración de Exchange en su aplicación Exchange administrado.
  
**Se aplica a:** Exchange Online | Exchange Server 2013 | Office 365
  
Cada cmdlet del Shell de administración de Exchange devuelve una o más instancias de [PSObject](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject%28VS.85%29.aspx) que proporcionan una vista coherente de cualquier objeto en el entorno de Shell de administración de Exchange. En este artículo se proporciona información acerca de cómo usar las propiedades de una instancia de **PSObject** para devolver los valores de propiedad del objeto de Exchange Server 2013 API subyacente. 
  
## <a name="prerequisites-for-using-cmdlet-responses"></a>Requisitos previos para usar las respuestas de cmdlet
<a name="prerequisites_bk"> </a>

Para usar las respuestas de cmdlet, se necesita una referencia al espacio de nombres **System.Automation.Management** . 
  
> [!NOTE]
>  Cuando se utiliza Visual Studio para crear una aplicación, debe agregar una referencia al ensamblado System.Mangagement.Automation.dll al proyecto. Puede encontrar el ensamblado en una de las siguientes ubicaciones: 
> - En los sistemas operativos Windows XP y Windows Vista, el directorio de instalación de Windows PowerShell ($PSHOME). 
> - En los sistemas operativos Windows 7 y Windows 8, la siguiente carpeta: Windows\assembly\GAC_MSIL\System.Management.Automation. 
  
## <a name="windows-powershell-remote-runspace"></a>Espacio de ejecución remota de Windows PowerShell
<a name="usingremoterunspace_bk"> </a>

El Shell de administración de Exchange usa las características de Windows PowerShell remotas para todos los comandos, incluso los comandos que se ejecutan en el servidor local. Como resultado, todas las respuestas desde el Shell de administración de Exchange cmdlets están serializan XML. Esto significa que aunque el objeto de respuesta indica el tipo de objeto de Exchange que se usó para generar la respuesta, el objeto de respuesta no se puede convertir al tipo de objeto de Exchange; en su lugar, debe usar el contenedor de propiedades expuestos por el objeto de respuesta para obtener los valores desde el tipo de objeto de Exchange.
  
El contenedor de propiedades en el objeto de respuesta contiene un par de clave y valor para cada propiedad pública o un método en el tipo de objeto de Exchange. El objeto response contiene el nombre del tipo de objeto de Exchange subyacente; Puede usar este nombre para determinar el tipo de objeto de Exchange que está representado por el objeto response de modo que puede extraer la propiedad correspondiente. Cada valor en el contenedor de propiedades también incluye información de tipo de modo que pueda convertir el valor de la propiedad para el tipo administrado adecuado.
  
## <a name="use-the-cmdlet-response"></a>Usar la respuesta de cmdlet
<a name="usingPSObject_bk"> </a>

La clase [PSObject](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject%28VS.85%29.aspx) expone las siguientes tres propiedades públicas que contienen los valores del objeto de Exchange 2013 API subyacente: [Propiedades](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject.properties%28VS.85%29.aspx), [métodos](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject.methods%28VS.85%29.aspx)y [miembros](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject.members%28VS.85%29.aspx). Cada propiedad expuestos por el objeto de la API de Exchange 2013 tiene un par de clave y valor correspondiente en las propiedades de **las propiedades** y **los miembros** . La aplicación puede indizar la colección de **Propiedades** por el nombre de una propiedad que se va a recuperar el valor de la propiedad. 
  
Puede usar la propiedad **TypeNames** de la instancia de **PSObject** para determinar el tipo del objeto subyacente Exchange encapsulado por la instancia **PSObject** . La propiedad **TypeNames** es una colección de cadenas que contiene la jerarquía de objetos del tipo representado. Puede usar estos nombres para determinar el objeto que está representado por la instancia **PSObject** por lo que puede extraer la propiedad correspondiente. 
  
En el ejemplo de código siguiente se usa la respuesta de cmdlet para imprimir el contenido de la colección de **Propiedades** de una instancia de **PSObject** en la consola. El ejemplo de código requiere una referencia al espacio de nombres **System.Automation.Management** . 
  
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

- [Creación de herramientas de Shell de administración de Exchange](create-exchange-management-shell-tools.md)   
- [Obtener una lista de usuarios de correo mediante el Shell de administración de Exchange](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)
    

