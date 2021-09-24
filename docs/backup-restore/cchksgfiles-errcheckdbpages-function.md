---
title: Función CChkSGFiles.ErrCheckDbPages
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ErrCheckDbPages
api_type:
- dllExport
ms.assetid: 5e981a7c-28cd-470c-b7eb-606463e9dd05
description: 'Last modified: February 22, 2013'
ms.openlocfilehash: e458e4ad552abfebb7611822a6e756bdd2ac6350
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510410"
---
# <a name="cchksgfileserrcheckdbpages-function"></a>Función CChkSGFiles.ErrCheckDbPages

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Valida un rango de páginas en una base de datos especificada. 
  
```cs
Vitual ERRErrCheckDbPages  
(
    Const ULONGiDb,
    Const VOID  * const pvPageBuffer,
    Const ULONGcbPageBuffer,
    PAGE_INFOrgPageInfo[],
    Const ULONGcPageInfo,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>Parámetros

### <a name="idb"></a>iDb
  
Parámetro Input. Un índice en la matriz de bases de datos especificada en el **parámetro rgwszDb[]** para la **función ErrInit.** Se comprobará la base de datos indizada por este parámetro. 
    
### <a name="pvpagebuffer"></a>pvPageBuffer 
  
Parámetro Input. Puntero a un búfer que contiene una o varias páginas de base de datos que se deben comprobar. El tamaño del búfer debe ser un múltiplo del tamaño de página de la base de datos, como se devuelve en el **parámetro pcbDbPageSize** mediante la **función ErrCheckDbHeaders.** La aplicación que llama debe rellenar el búfer con el contenido de la página de base de datos antes de llamar a **ErrCheckDbPages**.
    
### <a name="cbpagebuffer"></a>cbPageBuffer
  
Parámetro Input. El tamaño del parámetro **pvPageBuffer,** en bytes. Este valor debe ser un múltiplo del tamaño de página de la base de datos, tal como se devuelve en el **parámetro pcbDbPageSize** mediante la **función ErrCheckDbHeaders.** 
    
### <a name="rgpageinfo"></a>rgPageInfo[] 
  
Parámetro input/output. Una matriz **de estructuras PAGE \_ INFO** que **ErrCheckDbPages** rellena con resultados detallados de cada página de base de datos que se comprueba. La matriz debe tener un elemento para cada página de base de datos pasada en el parámetro **pvPageBuffer** y el campo **ulPgno** de cada estructura **PAGE \_ INFO** debe establecerse en el número de página lógica que corresponde a la página de la base de datos. Para obtener más información, vea "Comentarios" más adelante en este tema. 
    
### <a name="cpageinfo"></a>cPageInfo
  
Parámetro Input. El número de entradas de la **matriz rgPageInfo[].** Este valor debe ser igual al número de páginas de base de datos pasadas en el **parámetro pvPageBuffer.** 
    
### <a name="ulflags"></a>ulFlags 
  
Parámetro de entrada opcional. Este valor está reservado para uso futuro. El valor pasado en este parámetro debe ser 0 (cero).
    
## <a name="return-value"></a>Valor devuelto

Código de error de la [enumeración ERR.](cchksgfiles-err-enumeration.md) 
  
## <a name="remarks"></a>Comentarios

Tenga en cuenta que debe haber especificado la base de datos en la matriz de bases de datos pasadas a la **función ErrInit.** Además, se debe llamar a **ErrCheckDbHeaders** antes **de ErrCheckDbPages**.
  
La aplicación que llama debe asignar un búfer de memoria lo suficientemente grande como para contener las páginas de base de datos que se deben comprobar. La aplicación es responsable de rellenar el búfer con el contenido de una o varias de estas páginas de base de datos. 
  
La aplicación que llama debe llamar **a ErrCheckDbHeaders** antes de llamar a **ErrCheckDbPages**. Se puede llamar a esta función tantas veces como sea necesario para cubrir todas las páginas de todos los archivos de base de datos que se van a comprobar.
  
En el **parámetro rgPageInfo[],** cada elemento devuelto contiene información sobre la página de base de datos en una **estructura DE INFORMACIÓN \_ DE** PÁGINA. Si la **función ErrCheckDbPages** devuelve un error, la aplicación debe comprobar cada estructura **PAGE \_ INFO** para determinar en qué página se encontró el error. Por ejemplo, la comparación de los **valores checksumActual** y **checksumExpected** indicará si se detectó un error de suma de comprobación en esa página de base de datos. 
  
Si **ErrCheckDbPages** detecta algún error en el contenido de la base de datos, creará una Windows registro de eventos Error. 
  
El **objeto CChkSGFiles** determina si todas las bases de datos registradas con la **función ErrInit** se comprobaron realmente. En concreto, **CChkSGFiles** usa la función **ErrCheckDbPages** para determinar si realmente se ha comprobado el mismo número de páginas de base de datos indicadas por **ErrCheckDbHeaders.** Si el número correcto de páginas de cada base de datos no se ha comprobado correctamente, la **función ErrTerm** devuelve un error. 
  
Si usa CHKSGFILES en una aplicación multiproceso, puede llamar a la **función ErrCheckDbPages** en la parte multiproceso de la aplicación. Tenga en cuenta **que ErrCheckDbPages** suele llamarse varias veces para cada base de datos que se comprueba. 
  
## <a name="requirements"></a>Requisitos

Exchange 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta en la que se ejecuta la aplicación debe tener permisos de lectura para la base de datos y los archivos de registro que se van a comprobar.
  

