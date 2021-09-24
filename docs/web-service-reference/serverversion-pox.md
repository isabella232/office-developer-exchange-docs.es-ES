---
title: ServerVersion (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 2c0bc41c-2452-4fc8-a19c-0e85f9fdbc4a
description: El elemento ServerVersion representa el número de versión del equipo que se ejecuta Microsoft Exchange Server.
ms.openlocfilehash: bc7f9daa62e628e41f7541a609550e90af211928
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59527380"
---
# <a name="serverversion-pox"></a>ServerVersion (POX)

El **elemento ServerVersion** representa el número de versión del equipo que se ejecuta Microsoft Exchange Server. 
  
- [AutoDiscover (POX)](autodiscover-pox.md) 
- [Response (POX)](response-pox.md)
- [Account (POX)](account-pox.md)
- [Protocol (POX)](protocol-pox.md)
- [ServerVersion (POX)](serverversion-pox.md)
  
```xml
<ServerVersion/>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Protocol (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange que tiene instalado el rol de servidor Acceso de cliente.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el número Exchange versión del servidor.
  
## <a name="remarks"></a>Comentarios

El **valor de ServerVersion** solo es válido si el elemento [Type (POX)](type-pox.md) es igual a EXCH o EXPR. El **valor ServerVersion** es un número hexadecimal que contiene los valores MajorVersion, MinorVersion y MajorBuildNumber del servidor. 
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se encubre un valor **ServerVersion** que se devuelve en una respuesta de detección automática para obtener y mostrar MajorVersion, MinorVersion y MajorBuildNumber. Este ejemplo permite escribir un valor hexadecimal para el **valor ServerVersion.** Si no se introduce ningún valor de **ServerVersion,** se usa un valor **predeterminado de ServerVersion** de 738180DA. 
  
```csharp
static void Main(string[] args)
{
    // Convert a ServerVersion value that is returned from an Autodiscover request.
    // The value is a hex value and can be converted to the MajorVersion, MinorVersion,
    // and MajorBuildNumber.
    Console.WriteLine("Enter ServerVersion returned from the Autodiscover (eg. 738180DA) and Enter.");
    Console.WriteLine("To use the default ServerVersion of 738180DA, just hit Enter.");
    // Get the hexadecimal ServerVersion value.
    string serverversionhex = Console.ReadLine();
    // If nothing is entered, use the default server version of "738180DA"
    if (serverversionhex == "")
    {
        serverversionhex = "738180DA";
    }
    Console.WriteLine("ServerVersion (Hex) = " + serverversionhex);
    string serverversionbinary = Convert.ToString(Convert.ToInt32(serverversionhex, 16), 2);
    // The ServerVersion (binary) should be 32 bits in length. If the 
    // server version in binary is a length of 31 characters, the leading
    // zero has been removed in the conversion process. Put the missing zero back.
    if (serverversionbinary.Length == 31)
    {
        serverversionbinary = String.Concat("0", serverversionbinary);
    }
    Console.WriteLine("ServerVersion (bin) = " + serverversionbinary);
    // The first 4 bits represent a number used for comparison against  
    // older version number structures. You can ignore this.
    // The next 6 bits represent the major version number.
    int majorversion = Convert.ToInt32(serverversionbinary.Substring(4, 6), 2);
    Console.WriteLine("MajorVersion: " + majorversion);
    // The next 6 bits represent the minor version number.
    int minorversion = Convert.ToInt32(serverversionbinary.Substring(10, 6), 2);
    Console.WriteLine("MinorVersion: " + minorversion);
    
    // The next bit represent a flag - you can ignore this.
    // The next 15 bits represent the major build number.
    int majorbuild = Convert.ToInt32(serverversionbinary.Substring(17, 15), 2);
    Console.WriteLine("MajorBuildVersion: " + majorbuild);
    Console.WriteLine("\n\nPress any key to continue");
    Console.ReadKey();
}
```

## <a name="see-also"></a>Ver también

- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

