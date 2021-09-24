---
title: Función CChkSGFiles.ErrCheckDbHeaders
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ErrCheckDbHeaders
api_type:
- dllExport
ms.assetid: 75289cd2-35b1-4f75-a651-dce01f1ddda1
description: 'Last modified: February 22, 2013'
ms.openlocfilehash: 215a0d1126fce48b7e3800016619b0c52915312b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510473"
---
# <a name="cchksgfileserrcheckdbheaders-function"></a>Función CChkSGFiles.ErrCheckDbHeaders

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013 
  
Valida los encabezados de los archivos de base de datos especificados por la **función ErrInit.** Esta función también devuelve el tamaño de página y el número de páginas en cada una de las bases de datos especificadas. 
  
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
  
Parámetro de salida. Tamaño de página de cada una de las bases de datos especificadas, en bytes.
    
### <a name="pcheaderpagesperdb"></a>pcHeaderPagesPerDb 
  
Parámetro de salida. Número de páginas al principio de cada base de datos especificada reservadas por el motor de base de datos para uso interno. Tenga en cuenta que no *debe pasar* páginas de encabezado a la **función ErrCheckDbPages** para la validación. 
    
### <a name="pidberrorencountered"></a>piDbErrorEncountered
  
Parámetro de salida. Si el valor devuelto de la función indica un error, este parámetro será un índice en la matriz **rgwszDb[]** pasada a la **función ErrInit.** El elemento de matriz indizada representa la base de datos en la que se encontró el error. Si la función no devuelve un valor de error, este valor de parámetro no es válido. 
    
### <a name="ulflags"></a>ulFlags 
  
Parámetro de entrada opcional. Este valor está reservado para uso futuro. El valor pasado debe ser 0 (cero).
    
## <a name="return-value"></a>Valor devuelto

Esta función devuelve un código de error de la [enumeración CChkSGFiles.ERR](cchksgfiles-err-enumeration.md).
  
## <a name="remarks"></a>Comentarios

**ErrCheckDbHeaders** comprueba que todas las bases de datos registradas con **ErrInit** tienen el mismo tamaño de página de base de datos y firma de registro. También puede usar el valor de parámetro **genMin** más bajo y el valor de parámetro **genMax** más alto para determinar el conjunto de archivos de registro necesarios para llevar todas las bases de datos registradas a un estado de apagado limpio. 
  
El **parámetro piDbErrorEncountered** solo se establece cuando se detecta un error, como indica un valor devuelto **errCheckDbHeaders** distinto de cero. 
  
Cuando se produce un error en esta función, se agregará un evento de error al registro de eventos error Windows error.
  
Puede llamar a **ErrCheckDbHeaders** solo después de llamar a **ErrInit** y debe llamarlo antes de llamar a **ErrCheckDbPages** y **ErrCheckLogs**.
  
Si usa CHKSGFILES en una aplicación multiproceso, debe llamar a la **función ErrCheckDbHeaders** en la parte de subproceso único y puede llamarla solo una vez para cada objeto **CCheckSGFiles.** 
  
## <a name="requirements"></a>Requisitos

Exchange 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a la base de datos y a los archivos de registro que se van a comprobar.
  

