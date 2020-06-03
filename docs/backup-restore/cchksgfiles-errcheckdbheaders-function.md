---
title: Función función cchksgfiles. ErrCheckDbHeaders
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
ms.openlocfilehash: a62c5940322d3d7a71f2db93214f1e970fc6859b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455250"
---
# <a name="cchksgfileserrcheckdbheaders-function"></a>Función función cchksgfiles. ErrCheckDbHeaders

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013 
  
Valida los encabezados de los archivos de base de datos que especificó la función **ErrInit** . Esta función también devuelve el tamaño de página y el número de páginas de cada una de las bases de datos especificadas. 
  
```cs
Vitual ERRErrCheckDbHeaders  
(
        ULONG  * const pcbDbPageSize,
        ULONG  * const pcHeaderPagesPerDb,
        ULONG   const piDbErrorEncountered,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>Parámetros

### <a name="pcbdbpagesize"></a>pcbDbPageSize 
  
Parámetro de salida. El tamaño de página de cada una de las bases de datos especificadas, en bytes.
    
### <a name="pcheaderpagesperdb"></a>pcHeaderPagesPerDb 
  
Parámetro de salida. Número de páginas al principio de cada base de datos especificada que están reservadas por el motor de base de datos para uso interno. Tenga en cuenta que *no* debe pasar páginas de encabezado a la función **ErrCheckDbPages** para la validación. 
    
### <a name="pidberrorencountered"></a>piDbErrorEncountered
  
Parámetro de salida. Si el valor devuelto de la función indica un error, este parámetro será un índice en la matriz **rgwszDb []** pasada a la función **ErrInit** . El elemento de matriz indizada representa la base de datos en la que se encontró el error. Si la función no devuelve un valor de error, este valor de parámetro no es válido. 
    
### <a name="ulflags"></a>ulFlags 
  
Parámetro de entrada opcional. Este valor se reserva para uso futuro. El valor pasado debe ser 0 (cero).
    
## <a name="return-value"></a>Valor devuelto

Esta función devuelve un código de error de la [enumeración función cchksgfiles. err](cchksgfiles-err-enumeration.md).
  
## <a name="remarks"></a>Comentarios

**ErrCheckDbHeaders** comprueba que todas las bases de datos registradas con **ErrInit** tienen la misma firma de registro y tamaño de página de la base de datos. También puede usar el valor del parámetro **genMin** más bajo y el valor del parámetro más alto **genMax** para determinar el conjunto de archivos de registro que son necesarios para poner todas las bases de datos registradas en un estado de cierre limpio. 
  
El parámetro **piDbErrorEncountered** se establece únicamente cuando se detecta un error, tal como lo indica un valor devuelto distinto de cero **ErrCheckDbHeaders** . 
  
Cuando se produce un error en esta función, se agrega un evento de error al registro de eventos de error de Windows.
  
Puede llamar a **ErrCheckDbHeaders** solo después de llamar a **ErrInit**y debe llamarlo antes de llamar a **ErrCheckDbPages** y **ErrCheckLogs**.
  
Si está usando CHKSGFILES en una aplicación multiproceso, debe llamar a la función **ErrCheckDbHeaders** en la parte de subproceso único y puede llamarla solo una vez para cada objeto **CCheckSGFiles** . 
  
## <a name="requirements"></a>Requirements

Exchange 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de base de datos y de registro que se van a comprobar.
  

