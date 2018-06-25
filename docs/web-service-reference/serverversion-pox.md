---
title: ServerVersion (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2c0bc41c-2452-4fc8-a19c-0e85f9fdbc4a
description: El elemento ServerVersion representa el número de versión del equipo que ejecuta Microsoft Exchange Server.
ms.openlocfilehash: ef0562e166094d75d0dd92f5f48bb558e11a2cad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837391"
---
# <a name="serverversion-pox"></a><span data-ttu-id="5f77a-103">ServerVersion (POX)</span><span class="sxs-lookup"><span data-stu-id="5f77a-103">ServerVersion (POX)</span></span>

<span data-ttu-id="5f77a-104">El elemento **ServerVersion** representa el número de versión del equipo que ejecuta Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5f77a-104">The **ServerVersion** element represents the version number of the computer that is running Microsoft Exchange Server.</span></span> 
  
- [<span data-ttu-id="5f77a-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="5f77a-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md) 
- [<span data-ttu-id="5f77a-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="5f77a-106">Response (POX)</span></span>](response-pox.md)
- [<span data-ttu-id="5f77a-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="5f77a-107">Account (POX)</span></span>](account-pox.md)
- [<span data-ttu-id="5f77a-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="5f77a-108">Protocol (POX)</span></span>](protocol-pox.md)
- [<span data-ttu-id="5f77a-109">ServerVersion (POX)</span><span class="sxs-lookup"><span data-stu-id="5f77a-109">ServerVersion (POX)</span></span>](serverversion-pox.md)
  
```xml
<ServerVersion/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="5f77a-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5f77a-110">Attributes and elements</span></span>

<span data-ttu-id="5f77a-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5f77a-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5f77a-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="5f77a-112">Attributes</span></span>

<span data-ttu-id="5f77a-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5f77a-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5f77a-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5f77a-114">Child elements</span></span>

<span data-ttu-id="5f77a-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5f77a-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5f77a-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5f77a-116">Parent elements</span></span>

|<span data-ttu-id="5f77a-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="5f77a-117">**Element**</span></span>|<span data-ttu-id="5f77a-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5f77a-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f77a-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="5f77a-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="5f77a-120">Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="5f77a-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5f77a-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5f77a-121">Text value</span></span>

<span data-ttu-id="5f77a-122">El valor de texto representa el número de versión de Exchange server.</span><span class="sxs-lookup"><span data-stu-id="5f77a-122">The text value represents the Exchange server version number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5f77a-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5f77a-123">Remarks</span></span>

<span data-ttu-id="5f77a-124">El valor de **ServerVersion** sólo es válido si el elemento de [Tipo (POX)](type-pox.md) es igual a EXCH o EXPR.</span><span class="sxs-lookup"><span data-stu-id="5f77a-124">The **ServerVersion** value is only valid if the [Type (POX)](type-pox.md) element is equal to EXCH or EXPR.</span></span> <span data-ttu-id="5f77a-125">El valor de **ServerVersion** es un número hexadecimal que contiene el MajorVersion, MinorVersion, MajorBuildNumber del servidor.</span><span class="sxs-lookup"><span data-stu-id="5f77a-125">The **ServerVersion** value is a hexadecimal number that contains the MajorVersion, MinorVersion, and MajorBuildNumber of the server.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5f77a-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5f77a-126">Example</span></span>

<span data-ttu-id="5f77a-127">El siguiente convierte de ejemplo un **ServerVersion** valor que es devuelto en una respuesta de detección automática para obtener y mostrar el MajorVersion, MinorVersion y MajorBuildNumber.</span><span class="sxs-lookup"><span data-stu-id="5f77a-127">The following example coverts a **ServerVersion** value that is returned in an Autodiscover response to obtain and display the MajorVersion, MinorVersion, and MajorBuildNumber.</span></span> <span data-ttu-id="5f77a-128">En este ejemplo se permite escribir un valor hexadecimal para el valor **ServerVersion** .</span><span class="sxs-lookup"><span data-stu-id="5f77a-128">This example enables you to enter a hexadecimal value for the **ServerVersion** value.</span></span> <span data-ttu-id="5f77a-129">Si no se especifica ningún valor **ServerVersion** , se usa un valor de **ServerVersion** predeterminado de 738180DA.</span><span class="sxs-lookup"><span data-stu-id="5f77a-129">If no **ServerVersion** value is entered, a default **ServerVersion** value of 738180DA is used.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="5f77a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f77a-130">See also</span></span>

- [<span data-ttu-id="5f77a-131">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="5f77a-131">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

