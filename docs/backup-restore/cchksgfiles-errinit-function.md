---
title: Función CChkSGFiles.ErrInit
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ErrInit
api_type:
- dllExport
ms.assetid: 61bb3af1-8b51-4bae-8e25-90a4dc1226c5
description: 'Last modified: March 03, 2013'
ms.openlocfilehash: ccb5293e35f20328181c4cf1cb5f0eddbb42e03f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516296"
---
# <a name="cchksgfileserrinit-function"></a>Función CChkSGFiles.ErrInit
  
**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Inicializa el **objeto CChkSGFiles** especificando las bases de datos que se deben comprobar y la ruta de acceso y el nombre base de los archivos de registro de transacciones que se deben comprobar. Las aplicaciones deben llamar a esta función inmediatamente después de llamar correctamente a **la función New.** 
  
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
  
Parámetro Input. Matriz que especifica las bases de datos que se deben comprobar. Cada elemento de matriz es una cadena Unicode terminada en null que contiene la ruta de acceso y el nombre de archivo de una base de datos que se va a comprobar.
    
### <a name="cdb"></a>cDB
  
Parámetro Input. Número de elementos de ruta de acceso de base de datos válidos en la **matriz rgwszDb.** 
    
#### <a name="wszlogpath"></a>wszLogPath
  
Parámetro Input. La ruta de acceso completa de los archivos de registro de transacciones que se va a comprobar, en forma de una cadena Unicode terminada en null.
    
### <a name="wszbasename"></a>wszBaseName
  
Parámetro Input. El nombre base de tres letras de los Exchange de registro de transacciones, en forma de una cadena Unicode terminada en null.
    
### <a name="ulflags"></a>ulFlags
  
Parámetro de entrada opcional. Este valor está reservado para uso futuro. El valor pasado por este parámetro debe ser 0 (cero).
    
## <a name="return-value"></a>Valor devuelto

Código de error de la [enumeración ERR.](cchksgfiles-err-enumeration.md) 
  
## <a name="remarks"></a>Comentarios

La **función ErrInit** registra las bases de datos y los archivos de registro que se van a comprobar. Se debe llamar a esta función después de llamar a **la función New,** pero antes de llamar a cualquier otra función **ChkSGFiles.** 
  
Debe proporcionar todos los nombres de base de datos, la ruta de acceso del archivo de registro y el nombre base como cadenas Unicode terminadas en null.
  
Solo puede comprobar los archivos de base de datos, solo los archivos de registro o los archivos de base de datos y registro. Sin embargo, al llamar a esta función, la aplicación debe especificar al menos una entidad que se va a comprobar. Si se pasa 0 (cero) para  **cDB**  y NULL para  **wszLogPath,**  se devolverá un error. 
  
Si el valor de  **cDB**  es distinto de 0 (cero), si se pasa NULL para  **rgwszDb,**  se producirá un error. Para comprobar los archivos de base de datos, la aplicación debe proporcionar los nombres de la base de datos. 
  
Si se pasa NULL para  **wszBaseName pero**  **wszLogPath**  no es NULL, se devolverá un error. Siempre es necesario un nombre base de archivo de registro al comprobar los archivos de registro. 
  
Si usa CHKSGFILES en una aplicación multiproceso, debe llamar a la **función ErrInit** en la parte de subproceso único de la aplicación y puede llamarla solo una vez para cada objeto **CCheckSGFiles.** 
  
## <a name="requirements"></a>Requisitos

Exchange 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a la base de datos y a los archivos de registro que se van a comprobar.
  

