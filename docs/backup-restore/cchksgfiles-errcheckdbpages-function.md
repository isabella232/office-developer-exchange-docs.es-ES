---
title: Función función cchksgfiles. ErrCheckDbPages
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrCheckDbPages
api_type:
- dllExport
ms.assetid: 5e981a7c-28cd-470c-b7eb-606463e9dd05
description: 'Última modificación: 22 de febrero de 2013'
ms.openlocfilehash: 78d2dbee6253096d597b4ec2de3878f40ee1b6d7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526728"
---
# <a name="cchksgfileserrcheckdbpages-function"></a>Función función cchksgfiles. ErrCheckDbPages

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Valida un intervalo de páginas de una base de datos especificada. 
  
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
  
Parámetro de entrada. Un índice en la matriz de bases de datos especificado en el parámetro **rgwszDb []** para la función **ErrInit** . Se comprobará la base de datos indizada por este parámetro. 
    
### <a name="pvpagebuffer"></a>pvPageBuffer 
  
Parámetro de entrada. Un puntero a un búfer que contiene una o más páginas de base de datos que se van a comprobar. El tamaño del búfer debe ser un múltiplo del tamaño de página de la base de datos, tal como lo devuelve la función **ErrCheckDbHeaders** en el parámetro **pcbDbPageSize** . La aplicación de llamada debe rellenar el búfer con el contenido de la página de base de datos antes de llamar a **ErrCheckDbPages**.
    
### <a name="cbpagebuffer"></a>cbPageBuffer
  
Parámetro de entrada. El tamaño del parámetro **pvPageBuffer** , en bytes. Este valor debe ser un múltiplo del tamaño de página de la base de datos, tal como lo devuelve la función **ErrCheckDbHeaders** en el parámetro **pcbDbPageSize** . 
    
### <a name="rgpageinfo"></a>rgPageInfo[] 
  
Parámetro de entrada/salida. Matriz de estructuras **de \_ información de página** que **ErrCheckDbPages** rellena con los resultados detallados de cada página de base de datos que se comprueba. La matriz debe tener un elemento por cada página de base de datos pasada en el parámetro **pvPageBuffer** , y el campo **ulPgno** de cada estructura de ** \_ información de página** debe establecerse en el número de página lógica que corresponde a la página de la base de datos. Para obtener más información, vea la sección "Comentarios" más adelante en este tema. 
    
### <a name="cpageinfo"></a>cPageInfo
  
Parámetro de entrada. Número de entradas de la matriz **rgPageInfo []** . Este valor debe ser igual al número de páginas de base de datos pasadas en el parámetro **pvPageBuffer** . 
    
### <a name="ulflags"></a>ulFlags 
  
Parámetro de entrada opcional. Este valor se reserva para uso futuro. El valor que se pasa en este parámetro debe ser 0 (cero).
    
## <a name="return-value"></a>Valor devuelto

Un código de error de la enumeración [Err](cchksgfiles-err-enumeration.md) . 
  
## <a name="remarks"></a>Comentarios

Tenga en cuenta que debe especificar la base de datos en la matriz de bases de datos que se ha pasado a la función **ErrInit** . Además, se debe llamar a **ErrCheckDbHeaders** antes de **ErrCheckDbPages**.
  
La aplicación de llamada debe asignar un búfer de memoria lo suficientemente grande como para que las páginas de base de datos se comprueben. La aplicación es responsable de rellenar el búfer con el contenido de una o varias páginas de la base de datos. 
  
La aplicación de llamada debe llamar a **ErrCheckDbHeaders** antes de llamar a **ErrCheckDbPages**. Se puede llamar a esta función tantas veces como sea necesario para cubrir todas las páginas de todos los archivos de base de datos que se van a comprobar.
  
En el parámetro **rgPageInfo []** , cada elemento devuelto contiene información sobre la página de la base de datos en una estructura de ** \_ información de página** . Si la función **ErrCheckDbPages** devuelve un error, la aplicación debe comprobar cada estructura de ** \_ información de página** para determinar en qué página se encontró el error. Por ejemplo, si se comparan los valores **checksumActual** y **checksumExpected** , se indicará si se ha detectado un error de suma de comprobación en esa página de base de datos. 
  
Si **ErrCheckDbPages** detecta algún error en el contenido de la base de datos, creará una entrada de registro de eventos de error de Windows. 
  
El objeto **función cchksgfiles** determina si se han comprobado realmente todas las bases de datos registradas con la función **ErrInit** . Concretamente, **función cchksgfiles** usa la función **ErrCheckDbPages** para determinar si se ha comprobado realmente el mismo número de páginas de base de datos que indica **ErrCheckDbHeaders** . Si no se comprobó correctamente el número correcto de páginas en cada base de datos, la función **ErrTerm** devuelve un error. 
  
Si está usando CHKSGFILES en una aplicación multiproceso, puede llamar a la función **ErrCheckDbPages** en la parte multiproceso de la aplicación. Tenga en cuenta que se suele llamar a **ErrCheckDbPages** varias veces para cada base de datos que se comprueba. 
  
## <a name="requirements"></a>Requirements

Exchange 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta con la que se ejecuta la aplicación debe tener permisos de lectura para los archivos de base de datos y de registro que se van a comprobar.
  

