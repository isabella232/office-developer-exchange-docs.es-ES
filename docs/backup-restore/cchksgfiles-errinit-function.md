---
title: Función función cchksgfiles. ErrInit
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrInit
api_type:
- dllExport
ms.assetid: 61bb3af1-8b51-4bae-8e25-90a4dc1226c5
description: 'Última modificación: 3 de marzo de 2013'
ms.openlocfilehash: c881691e7c1ba83a396e659f6aac0328625e49a5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457014"
---
# <a name="cchksgfileserrinit-function"></a>Función función cchksgfiles. ErrInit
  
**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Inicializa el objeto **función cchksgfiles** especificando las bases de datos que se van a comprobar y la ruta de acceso y el nombre base de los archivos de registro de transacciones que se van a comprobar. Las aplicaciones deben llamar a esta función inmediatamente después de llamar correctamente a la **nueva** función. 
  
```cs
Vitual ERRErrInit  
(
    Const WCHAR  * const rgwszDb[],
    Const ULONGcDB,
    __in_z const WCHAR  * const wszLogPath,
    __in_z const WCHAR  * const wszBaseName,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>Parámetros

### <a name="rgwszdb"></a>rgwszDb[]
  
Parámetro de entrada. Matriz que especifica las bases de datos que se van a comprobar. Cada elemento de matriz es una cadena Unicode terminada en null que contiene la ruta de acceso y el nombre de archivo de la base de datos que se va a comprobar.
    
### <a name="cdb"></a>cDB
  
Parámetro de entrada. El número de elementos de ruta de acceso de base de datos válidos en la matriz **rgwszDb** . 
    
#### <a name="wszlogpath"></a>wszLogPath
  
Parámetro de entrada. Ruta de acceso completa de los archivos de registro de transacciones que se van a comprobar, en forma de una cadena Unicode terminada en NULL.
    
### <a name="wszbasename"></a>wszBaseName
  
Parámetro de entrada. Nombre base de tres letras de los archivos de registro de transacciones de Exchange, en forma de una cadena Unicode terminada en NULL.
    
### <a name="ulflags"></a>ulFlags
  
Parámetro de entrada opcional. Este valor se reserva para uso futuro. El valor que pasa este parámetro debe ser 0 (cero).
    
## <a name="return-value"></a>Valor devuelto

Un código de error de la enumeración [Err](cchksgfiles-err-enumeration.md) . 
  
## <a name="remarks"></a>Comentarios

La función **ErrInit** registra las bases de datos y los archivos de registro que se van a comprobar. Se debe llamar a esta función después de llamar a la función **New** pero antes de llamar a cualquier otra función **ChkSGFiles** . 
  
Debe proporcionar todos los nombres de bases de datos, la ruta de acceso al archivo de registro y el nombre base como cadenas Unicode terminadas en NULL.
  
Puede comprobar sólo los archivos de base de datos, sólo los archivos de registro o los archivos de registro y de base de datos. Sin embargo, al llamar a esta función, la aplicación debe especificar al menos una entidad que se va a comprobar. Si se pasa 0 (cero) para **cDB** y null para **wszLogPath** , se devolverá un error. 
  
Si el valor de **cDB** es distinto de 0 (cero) y se pasa null para **rgwszDb** , se producirá un error. Para comprobar los archivos de base de datos, la aplicación debe proporcionar los nombres de las bases de datos. 
  
Si se pasa NULL para **wszBaseName** pero **WSZLOGPATH** no es null, se devolverá un error. El nombre base de un archivo de registro siempre es necesario cuando se comprueban los archivos de registro. 
  
Si está usando CHKSGFILES en una aplicación multiproceso, debe llamar a la función **ErrInit** en la parte de subproceso único de la aplicación y puede llamarla solo una vez para cada objeto **CCheckSGFiles** . 
  
## <a name="requirements"></a>Requirements

Exchange 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de base de datos y de registro que se van a comprobar.
  

