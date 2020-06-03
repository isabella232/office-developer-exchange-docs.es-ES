---
title: Función función cchksgfiles. ErrCheckLogs
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrCheckLogs
api_type:
- dllExport
ms.assetid: cec0df4b-4679-4682-bacf-69b4f4aef343
description: 'Última modificación: 22 de febrero de 2013'
ms.openlocfilehash: 71e21bb3a748a532f9e3167e0b36898acde71b02
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526721"
---
# <a name="cchksgfileserrchecklogs-function"></a>Función función cchksgfiles. ErrCheckLogs

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Valida los archivos de registro de todos los archivos de base de datos especificados en la función **ErrInit** . Los registros validados son los que existen en la ruta de acceso y que tienen el nombre del archivo de registro base de tres letras pasado a **ErrInit**.
  
```cs
Vitual ERRErrCheckLogs 
(
        BOOL  * const pfOnlyUnnecessaryLogsCorrup,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>Parámetros

### <a name="pfonlyunnecessarylogscorrupt"></a>pfOnlyUnnecessaryLogsCorrupt 
  
Parámetro de salida. Cuando **es true**, este parámetro indica que se encontraron errores en los archivos de registro de transacciones, pero estos errores se encontraron en los archivos de registro que no son necesarios para poner la base de datos en un estado de cierre limpio sin pérdida de datos. Un valor **true** devuelto en este parámetro es válido sólo cuando **ErrCheckLogs** devuelve **errSuccess**. 
    
### <a name="ulflags"></a>ulFlags
  
Parámetro de entrada opcional. Este valor se reserva para uso futuro. El valor que pasa este parámetro debe ser 0 (cero).
    
## <a name="return-value"></a>Valor devuelto

Un código de error de la enumeración [Err](cchksgfiles-err-enumeration.md) . 
  
Es importante recordar que esta función puede devolver **errSuccess** incluso cuando se encuentran errores en los archivos de registro. Por lo tanto, cuando **ErrCheckLogs** devuelve **errSuccess**, la aplicación también debe comprobar el parámetro **pfOnlyUnnecessaryLogsCorrupt** Return. Si **pfOnlyUnnecessaryLogsCorrupts** es **true** cuando **ErrCheckLogs** devuelve **errSuccess**, esto indica que se encontraron uno o varios errores, pero solo en los archivos de registro no se necesitan para actualizar la base de datos.
  
## <a name="remarks"></a>Comentarios

Se debe llamar a la función **ErrCheckDbHeaders** antes de que se pueda llamar a la función **ErrCheckLogs** . 
  
Cuando se comprueban los archivos de registro de transacciones de base de datos de Exchange, algunos de los archivos de registro serán necesarios para traer las bases de datos del grupo de almacenamiento a un estado de cierre limpio sin pérdida de datos, mientras que otros archivos de registro podrían no ser necesarios. La función **ErrCheckLogs** determina los archivos de registro más antiguos y los más recientes que se necesitan para actualizar las bases de datos. 
  
La función **ErrCheckLogs** comprueba todos los archivos de registro en las rutas de acceso especificadas que también tienen el nombre de archivo base de tres letras especificado, como se pasan a la función **ErrInit** . 
  
Si no se encuentran errores en los archivos de registro, **ErrCheckLogs** devuelve **errSuccess**. 
  
Si alguno de los archivos de registro necesarios se encuentra dañado, **ErrCheckLogs** devuelve un error. 
  
Si se encuentran errores sólo en los archivos de registro más antiguos que los que se necesitan antes, la función devuelve **errSuccess** y establece el parámetro de devolución **pfOnlyUnnecessaryLogCorrupt** en **true**. La aplicación debe reconocer que hay errores en algunos de los archivos de registro antiguos y, si es así, se alerta al usuario. En cualquier caso, estos errores no deberían afectar a la integridad general de la base de datos ni influir en que la reproducción de los registros reenvío se realice correctamente.
  
Si se encuentran errores en cualquier archivo de registro que se crea después del registro más antiguo que **ErrCheckLogs** determina que es necesario, la función devuelve un error. El error se devolverá incluso si se encuentra el error del archivo de registro en un archivo de registro que se generó después de lo necesario para poner la base de datos actualizada. Si bien sería posible traer las bases de datos a un estado de cierre limpio mediante el uso de los archivos de registro identificados, las transacciones especificadas en los archivos de registro dañados más adelante no se aplicarían, lo que daría como resultado una pérdida de datos cuando se restaure la base de datos. 
  
El objeto **función cchksgfiles** determina si todos los archivos de registro registrados con la función **ErrInit** se han comprobado realmente. Si no todos los registros no se comprobaron correctamente, la función **ErrTerm** devuelve un error. 
  
Si está usando CHKSGFILES en una aplicación multiproceso, puede llamar a la función **ErrCheckLogs** en la parte multiproceso de la aplicación, pero sólo puede llamar una vez por cada objeto **CCheckSGFiles** . 
  
## <a name="requirements"></a>Requirements

Exchange 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de base de datos y de registro que se van a comprobar.
  

