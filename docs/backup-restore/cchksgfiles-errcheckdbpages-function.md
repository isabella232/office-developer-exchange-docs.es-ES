---
title: CChkSGFiles.ErrCheckDbPages (función)
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
ms.openlocfilehash: f1588b1dbc4bd7e83683fa4432a175405ad17903
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19762977"
---
# <a name="cchksgfileserrcheckdbpages-function"></a>CChkSGFiles.ErrCheckDbPages (función)

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Valida un intervalo de páginas en una base de datos especificado. 
  
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

## <a name="parameters"></a>Sintaxis

### <a name="idb"></a>iDb
  
Parámetro de entrada. Un índice en la matriz de las bases de datos especificado en el parámetro **[] rgwszDb** a la función **ErrInit** . Se comprobará la base de datos indizada por este parámetro. 
    
### <a name="pvpagebuffer"></a>pvPageBuffer 
  
Parámetro de entrada. Un puntero a un búfer que contiene una o más páginas de base de datos que se va a comprobar. El tamaño del búfer debe ser un múltiplo del tamaño de página de base de datos, tal como lo devuelve en el parámetro **pcbDbPageSize** por la función **ErrCheckDbHeaders** . La aplicación de llamada debe llene el búfer con el contenido de página de la base de datos antes de llamar a **ErrCheckDbPages**.
    
### <a name="cbpagebuffer"></a>cbPageBuffer
  
Parámetro de entrada. El tamaño del parámetro **pvPageBuffer** , en bytes. Este valor debe ser un múltiplo del tamaño de página de base de datos, tal como lo devuelve en el parámetro **pcbDbPageSize** por la función **ErrCheckDbHeaders** . 
    
### <a name="rgpageinfo"></a>[] rgPageInfo 
  
Parámetro de entrada y salida. Una matriz de **página\_INFO** detallan de estructuras que **ErrCheckDbPages** se rellena con los resultados de cada página de la base de datos que está protegido. La matriz debe tener un elemento para cada página de base de datos que se pasa en el parámetro **pvPageBuffer** y el campo **ulPgno** de cada **página\_INFO** estructura debe establecerse en el número de página lógica que corresponde a la página de la base de datos. Para obtener más información, vea "Comentarios" más adelante en este tema. 
    
### <a name="cpageinfo"></a>cPageInfo
  
Parámetro de entrada. El número de entradas en la matriz **[] rgPageInfo** . Este valor debe ser igual que el número de páginas de base de datos que se pasa en el parámetro **pvPageBuffer** . 
    
### <a name="ulflags"></a>ulFlags 
  
Parámetro de entrada opcional. Este valor está reservado para uso futuro. El valor que se pasa en este parámetro debe ser 0 (cero).
    
## <a name="return-value"></a>Valor devuelto

Un código de error de la enumeración [ERR](cchksgfiles-err-enumeration.md) . 
  
## <a name="remarks"></a>Comentarios

Tenga en cuenta que tiene que ha especificado la base de datos en la matriz de las bases de datos que se pasan a la función **ErrInit** . Además, se debe llamar a **ErrCheckDbHeaders** antes de **ErrCheckDbPages**.
  
La aplicación de llamada debe asignar un búfer de memoria que es lo suficientemente grande como para contener las páginas de la base de datos que se va a comprobar. La aplicación es responsable de rellenar el búfer con el contenido de una o varias de estas páginas de base de datos. 
  
La aplicación de llamada debe llamar a **ErrCheckDbHeaders** antes de llamar a **ErrCheckDbPages**. Esta función se puede llamar tantas veces como sea necesario para cubrir todas las páginas de todos los archivos de base de datos que se va a revisar.
  
En el parámetro **[] rgPageInfo** , cada elemento devuelto contiene información acerca de la página de la base de datos en un **página\_INFO** estructura. Si la función **ErrCheckDbPages** devuelve un error, la aplicación debe comprobar cada uno de ellos **página\_INFO** estructura para determinar en qué página se ha encontrado el error. Por ejemplo, comparación de los valores **checksumActual** y **checksumExpected** indicará si se detectó un error de suma de comprobación en esa página de base de datos. 
  
Si **ErrCheckDbPages** detecta los errores en el contenido de la base de datos, creará una entrada de registro de eventos de Error de Windows. 
  
El objeto **CChkSGFiles** determina si todas las bases de datos registrados con la función **ErrInit** realmente se han activado. Específicamente, **CChkSGFiles** usa la función **ErrCheckDbPages** para determinar si realmente se ha comprobado el mismo número de páginas de base de datos indicada por **ErrCheckDbHeaders** . Si el número correcto de las páginas de cada base de datos no se protegieron correctamente, la función **ErrTerm** devuelve un error. 
  
Si está utilizando CHKSGFILES en una aplicación multiproceso, puede llamar a la función **ErrCheckDbPages** en la parte de la aplicación multiproceso. Tenga en cuenta que **ErrCheckDbPages** normalmente se llama varias veces para cada base de datos que está protegido. 
  
## <a name="requirements"></a>Requisitos

Exchange 2013 sólo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta que se ejecuta la aplicación debe tener permisos para los archivos de registro y base de datos que se va a revisar de lectura.
  

