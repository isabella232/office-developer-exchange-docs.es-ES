---
title: Usar la respuesta Exchange cmdlet del Shell de administración
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: dac8e526-11c6-4c2e-b9a2-f016b1fc738a
description: Obtenga información sobre cómo usar la respuesta de un cmdlet Exchange Shell de administración en su Exchange aplicación administrada.
ms.openlocfilehash: be66be31e435be1553eba16d8f367a79317618f2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520971"
---
# <a name="use-the-exchange-management-shell-cmdlet-response"></a>Usar la respuesta Exchange cmdlet del Shell de administración

Obtenga información sobre cómo usar la respuesta de un cmdlet Exchange Shell de administración en su Exchange aplicación administrada.
  
**Se aplica a:** Exchange Online | Exchange Server 2013 | Office 365
  
Cada cmdlet Exchange Shell de administración devuelve una o más instancias de [PSObject](https://msdn.microsoft.com/library/system.management.automation.psobject%28VS.85%29.aspx) que proporcionan una vista coherente de cualquier objeto en el entorno Exchange Shell de administración. En este artículo se proporciona información sobre cómo usar las propiedades de una instancia **de PSObject** para devolver los valores de propiedad del objeto de api Exchange Server 2013. 
  
## <a name="prerequisites-for-using-cmdlet-responses"></a>Requisitos previos para usar respuestas de cmdlet
<a name="prerequisites_bk"> </a>

Para usar respuestas de cmdlet, necesita una referencia al espacio de **nombres System.Automation.Management.** 
  
> [!NOTE]
>  Cuando se usa Visual Studio para crear una aplicación, debe agregar una referencia al ensamblado System.Mangagement.Automation.dll al proyecto. Puede encontrar el ensamblado en una de las siguientes ubicaciones: 
> - En los sistemas operativos Windows XP y Windows Vista, el directorio de instalación de Windows PowerShell ($PSHOME). 
> - En los sistemas operativos Windows 7 y Windows 8, la siguiente carpeta: Windows\assembly\GAC_MSIL\System.Management.Automation. 
  
## <a name="windows-powershell-remote-runspace"></a>Windows PowerShell espacio de ejecución remoto
<a name="usingremoterunspace_bk"> </a>

El Shell Exchange de administración usa características de Windows PowerShell remotas para todos los comandos, incluso los comandos que se ejecutan en el servidor local. Como resultado, todas las respuestas de Exchange cmdlets del Shell de administración son XML serializados. Esto significa que, aunque el objeto de respuesta indica el tipo de objeto Exchange que se usó para generar la respuesta, el objeto de respuesta no se puede convertir al tipo de objeto Exchange respuesta; en su lugar, debe usar el paquete de propiedades expuesto por el objeto de respuesta para obtener los valores del tipo Exchange objeto.
  
El paquete de propiedades del objeto de respuesta contiene un par clave/valor para cada propiedad o método público del Exchange objeto. El objeto de respuesta contiene el nombre del tipo Exchange objeto subyacente; puede usar este nombre para determinar el tipo Exchange objeto que representa el objeto de respuesta para poder extraer la propiedad adecuada. Cada valor del paquete de propiedades también incluye información de tipo para que pueda convertir el valor de la propiedad en el tipo administrado adecuado.
  
## <a name="use-the-cmdlet-response"></a>Usar la respuesta cmdlet
<a name="usingPSObject_bk"> </a>

La [clase PSObject](https://msdn.microsoft.com/library/system.management.automation.psobject%28VS.85%29.aspx) expone las tres propiedades públicas siguientes que contienen los valores del objeto de API Exchange 2013: [Properties](https://msdn.microsoft.com/library/system.management.automation.psobject.properties%28VS.85%29.aspx), [Methods](https://msdn.microsoft.com/library/system.management.automation.psobject.methods%28VS.85%29.aspx)y [Members](https://msdn.microsoft.com/library/system.management.automation.psobject.members%28VS.85%29.aspx). Cada propiedad expuesta por el objeto api Exchange 2013 tiene un par clave/valor correspondiente en las **propiedades Properties** y **Members.** La aplicación puede indizar la **colección Properties** por el nombre de una propiedad para recuperar el valor de la propiedad. 
  
Puede usar la **propiedad TypeNames** de la instancia **de PSObject** para determinar el tipo del objeto Exchange subyacente encapsulado por la **instancia de PSObject.** La **propiedad TypeNames** es una colección de cadenas que contiene la jerarquía de objetos del tipo representado. Puede usar estos nombres para determinar el objeto representado por la instancia **de PSObject** para poder extraer la propiedad adecuada. 
  
En el siguiente ejemplo de código se usa la respuesta del cmdlet para imprimir el contenido de la colección **Properties** de una **instancia de PSObject** en la consola. El ejemplo de código requiere una referencia al espacio **de nombres System.Automation.Management.** 
  
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

## <a name="see-also"></a>Ver también

- [Crear herramientas de Shell de administración de Exchange](create-exchange-management-shell-tools.md)   
- [Obtener una lista de usuarios de correo mediante el Shell Exchange administración](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)
    

