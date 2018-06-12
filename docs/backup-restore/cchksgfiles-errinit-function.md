---
title: CChkSGFiles.ErrInit (función)
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
description: 'Última modificación: 03 de marzo de 2013'
ms.openlocfilehash: d4b76933a747fe4bf084061cf080bc68264132ed
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19762976"
---
# <a name="cchksgfileserrinit-function"></a>CChkSGFiles.ErrInit (función)
  
**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Inicializa el objeto **CChkSGFiles** mediante la especificación de las bases de datos que se va a comprobar y la ruta de acceso y el nombre de base de los archivos de registro de transacciones que se va a comprobar. Las aplicaciones deben llamar a esta función inmediatamente después de llamar correctamente a la función de **nuevo** . 
  
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

## <a name="parameters"></a>Sintaxis

### <a name="rgwszdb"></a>[] rgwszDb
  
Parámetro de entrada. Una matriz que especifica las bases de datos que se va a comprobar. Cada elemento de la matriz es una cadena Unicode terminada en null que contiene la ruta de acceso y el nombre de una base de datos que se va a comprobar.
    
### <a name="cdb"></a>cDB
  
Parámetro de entrada. El número de elementos de la ruta de acceso de base de datos válido en la matriz **rgwszDb** . 
    
#### <a name="wszlogpath"></a>wszLogPath
  
Parámetro de entrada. La ruta de acceso completa de los archivos de registro de transacciones a comprobarse, con el formato de una cadena Unicode terminada en null.
    
### <a name="wszbasename"></a>wszBaseName
  
Parámetro de entrada. El nombre de base de tres letras de los archivos de registro de transacciones de Exchange, en el formulario de una cadena Unicode terminada en null.
    
### <a name="ulflags"></a>ulFlags
  
Parámetro de entrada opcional. Este valor está reservado para uso futuro. El valor pasado por este parámetro debe ser 0 (cero).
    
## <a name="return-value"></a>Valor devuelto

Un código de error de la enumeración [ERR](cchksgfiles-err-enumeration.md) . 
  
## <a name="remarks"></a>Notas

La función **ErrInit** registra las bases de datos y los archivos de registro que se va a revisar. Después de llamar a la función de **nuevo** , pero antes de cualquier otro **ChkSGFiles** se denomina función, se debe llamar a esta función. 
  
Debe proporcionar todos los nombres de base de datos, la ruta de acceso del archivo de registro y el nombre base como cadenas de Unicode terminada en null.
  
Puede comprobar los archivos de base de datos, sólo los archivos de registro o los archivos de registro y base de datos. Sin embargo, cuando se llama a esta función, la aplicación debe especificar al menos una entidad que se va a comprobar. Pasar un valor 0 (cero) para **cDB** y NULL para **wszLogPath** devolverá un error. 
  
Si el valor de **cDB** es distinto de 0 (cero), pasando NULL para **rgwszDb** dará como resultado un error. Para comprobar los archivos de base de datos, la aplicación debe proporcionar los nombres de base de datos. 
  
Si se pasa NULL para **wszBaseName** , pero **wszLogPath** no es NULL, se devolverá un error. Siempre se requiere un nombre base del archivo de registro durante la comprobación de los archivos de registro. 
  
Si utiliza en una aplicación multiproceso CHKSGFILES, debe llamar a la función **ErrInit** en la parte de un único subproceso de la aplicación y se le puede llamar sólo una vez para cada objeto **CCheckSGFiles** . 
  
## <a name="requirements"></a>Requisitos

Exchange 2013 sólo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de registro y base de datos que se va a revisar.
  

