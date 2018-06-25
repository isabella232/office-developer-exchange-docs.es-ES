---
title: CChkSGFiles.ErrCheckDbHeaders (función)
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrCheckDbHeaders
api_type:
- dllExport
ms.assetid: 75289cd2-35b1-4f75-a651-dce01f1ddda1
description: 'Última modificación: 22 de febrero de 2013'
ms.openlocfilehash: a407019063b34970e883a00ca4f4d730935d7cba
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19762984"
---
# <a name="cchksgfileserrcheckdbheaders-function"></a>CChkSGFiles.ErrCheckDbHeaders (función)

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013 
  
Valida los encabezados de los archivos de base de datos que se han especificado por la función **ErrInit** . Esta función devuelve también el tamaño de página y el número de páginas en cada una de las bases de datos especificados. 
  
```cs
Vitual ERRErrCheckDbHeaders  
(
        ULONG  * const pcbDbPageSize,
        ULONG  * const pcHeaderPagesPerDb,
        ULONG   const piDbErrorEncountered,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>Sintaxis

### <a name="pcbdbpagesize"></a>pcbDbPageSize 
  
Parámetro de salida. El tamaño de página de cada una de las bases de datos especificados, en bytes.
    
### <a name="pcheaderpagesperdb"></a>pcHeaderPagesPerDb 
  
Parámetro de salida. El número de páginas al principio de cada uno especifica la base de datos que están reservados por el motor de base de datos para uso interno. Tenga en cuenta que debe *pasar páginas del encabezado a la función **ErrCheckDbPages** para la validación* . 
    
### <a name="pidberrorencountered"></a>piDbErrorEncountered
  
Parámetro de salida. Si el valor devuelto de la función indica un error, este parámetro será un índice en la matriz **[] rgwszDb** que se pasan a la función **ErrInit** . Elemento de la matriz indizada representa la base de datos en el que se encontró el error. Si la función no devuelve un valor de error, este valor de parámetro no es válido. 
    
### <a name="ulflags"></a>ulFlags 
  
Parámetro de entrada opcional. Este valor está reservado para uso futuro. El valor pasado debe ser 0 (cero).
    
## <a name="return-value"></a>Valor devuelto

Esta función devuelve un código de error de la [enumeración CChkSGFiles.ERR](cchksgfiles-err-enumeration.md).
  
## <a name="remarks"></a>Comentarios

**ErrCheckDbHeaders** comprueba que todas las bases de datos registrados con **ErrInit** tienen el mismo registro firma y base de datos de tamaño de página. También puede usar el valor del parámetro **genMin** más bajo y el valor del parámetro **genMax** más alto para determinar el conjunto de archivos de registro que son necesarios para poner todos los de las bases de datos registrados en un estado de cierre limpio. 
  
El parámetro **piDbErrorEncountered** sólo se establece cuando se detecta un error, indicada por un valor distinto de cero **ErrCheckDbHeaders** valor devuelto. 
  
Cuando se produce un error en esta función, se agregará un evento de error al registro de eventos de Error de Windows.
  
Se puede llamar a **ErrCheckDbHeaders** sólo después de llamar a **ErrInit**, y debe llamar antes de llamar a **ErrCheckDbPages** y **ErrCheckLogs**.
  
Si utiliza en una aplicación multiproceso CHKSGFILES, debe llamar a la función **ErrCheckDbHeaders** en la parte de un único subproceso y se le puede llamar sólo una vez para cada objeto **CCheckSGFiles** . 
  
## <a name="requirements"></a>Requisitos

Exchange 2013 sólo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de registro y base de datos que se va a revisar.
  

