---
title: Función CChkSGFiles.ErrCheckLogs
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ErrCheckLogs
api_type:
- dllExport
ms.assetid: cec0df4b-4679-4682-bacf-69b4f4aef343
description: 'Last modified: February 22, 2013'
ms.openlocfilehash: 64484b32fdc566d6fee8631f80d078aca82b11d1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516393"
---
# <a name="cchksgfileserrchecklogs-function"></a>Función CChkSGFiles.ErrCheckLogs

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Valida los archivos de registro de todos los archivos de base de datos especificados en la **función ErrInit.** Los registros validados son los que existen en la ruta de acceso y que tienen el nombre de archivo de registro base de tres letras pasado a **ErrInit**.
  
```cs
Vitual ERRErrCheckLogs 
(
        BOOL  * const pfOnlyUnnecessaryLogsCorrup,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>Parámetros

### <a name="pfonlyunnecessarylogscorrupt"></a>pfOnlyUnnecessaryLogsCorrupt 
  
Parámetro de salida. Cuando **true**, este parámetro indica que se encontraron errores en los archivos de registro de transacciones, pero todos estos errores se encontraron en archivos de registro que no son necesarios para llevar la base de datos a un estado de apagado limpio sin pérdida de datos. Un **valor** true devuelto en este parámetro solo es válido cuando **ErrCheckLogs** devuelve **errSuccess**. 
    
### <a name="ulflags"></a>ulFlags
  
Parámetro de entrada opcional. Este valor está reservado para uso futuro. El valor pasado por este parámetro debe ser 0 (cero).
    
## <a name="return-value"></a>Valor devuelto

Código de error de la [enumeración ERR.](cchksgfiles-err-enumeration.md) 
  
Es importante recordar que esta función puede devolver **errSuccess** incluso cuando se encuentran errores en los archivos de registro. Por lo tanto, cuando **ErrCheckLogs** devuelve **errSuccess**, la aplicación también debe comprobar el parámetro devuelto **pfOnlyUnnecessaryLogsCorrupt.** Si **pfOnlyUnnecessaryLogsCorrupts** es **true** cuando **ErrCheckLogs** devuelve **errSuccess**, esto indica que se encontraron uno o más errores, pero solo en archivos de registro no necesarios para poner la base de datos actualizada.
  
## <a name="remarks"></a>Comentarios

Se debe llamar a la función **ErrCheckDbHeaders** para poder llamar a la **función ErrCheckLogs.** 
  
Cuando Exchange de registro de transacciones de base de datos se comprueban, algunos de los archivos de registro serán necesarios para que las bases de datos del grupo de almacenamiento estén en un estado de apagado limpio sin pérdida de datos, mientras que es posible que no se necesiten otros archivos de registro. La **función ErrCheckLogs** determina los archivos de registro más antiguos y los más nuevos necesarios para poner las bases de datos actualizadas. 
  
La **función ErrCheckLogs** comprueba todos los archivos de registro de las rutas de acceso especificadas que también tienen el nombre de archivo base de tres letras especificado, tal como se pasa a la **función ErrInit.** 
  
Si no se encuentra ningún error en los archivos de registro, **ErrCheckLogs** devuelve **errSuccess**. 
  
Si se encuentra que alguno de los archivos de registro necesarios está dañado, **ErrCheckLogs** devuelve un error. 
  
Si solo se encuentran errores en archivos de registro anteriores a los primeros necesarios, la función devuelve **errSuccess** y establece el parámetro de devolución **pfOnlyUnnecessaryLogCorrupt** en **true**. La aplicación debe reconocer que hay errores en algunos de esos archivos de registro antiguos y, si es así, posiblemente avisará al usuario. En cualquier caso, estos errores no deben afectar a la integridad general de la base de datos ni afectar a si la reproducción de los registros hacia delante se realizará correctamente.
  
Si se encuentran errores en cualquier archivo de registro creado después del registro más antiguo que **ErrCheckLogs** determine que es necesario, la función devuelve un error. El error se devolverá incluso si el error del archivo de registro se encontró en un archivo de registro que se generó más tarde de lo necesario para poner la base de datos actualizada. Aunque sería posible llevar las bases de datos a un estado de apagado limpio mediante los archivos de registro identificados, las transacciones especificadas en los archivos de registro dañados posteriormente no se aplicarían, lo que provocaría la pérdida de datos cuando se restaure la base de datos. 
  
El **objeto CChkSGFiles** determina si todos los archivos de registro registrados con la **función ErrInit** se comprobaron realmente. Si no todos los registros no se comprobaron correctamente, la **función ErrTerm** devuelve un error. 
  
Si usa CHKSGFILES en una aplicación multiproceso, puede llamar a la función **ErrCheckLogs** en la parte multiproceso de la aplicación, pero solo puede llamarla una vez para cada objeto **CCheckSGFiles.** 
  
## <a name="requirements"></a>Requisitos

Exchange 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a la base de datos y a los archivos de registro que se van a comprobar.
  

