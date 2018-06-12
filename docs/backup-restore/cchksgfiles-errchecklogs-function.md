---
title: CChkSGFiles.ErrCheckLogs (función)
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
ms.openlocfilehash: 5b1070de73bc23ae09ddb7835bd72c8e8a71a95f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19762980"
---
# <a name="cchksgfileserrchecklogs-function"></a>CChkSGFiles.ErrCheckLogs (función)

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Valida los archivos de registro de todos los archivos de base de datos que se especificaron en la función **ErrInit** . Los registros de validado son aquellos que existen en la ruta de acceso, y que tienen el nombre de archivo de registro de base de tres letras que se pasan a **ErrInit**.
  
```cs
Vitual ERRErrCheckLogs 
(
        BOOL  * const pfOnlyUnnecessaryLogsCorrup,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>Sintaxis

### <a name="pfonlyunnecessarylogscorrupt"></a>pfOnlyUnnecessaryLogsCorrupt 
  
Parámetro de salida. Cuando **true**, este parámetro indica que se encontraron errores en los archivos de registro de transacciones, pero esos errores se han poner todos los que se encuentran en los archivos de registro que no son necesarios para la base de datos en un estado de cierre limpio sin pérdida de datos. Un valor **true** devuelto en este parámetro sólo es válido cuando **ErrCheckLogs** devuelve **errSuccess**. 
    
### <a name="ulflags"></a>ulFlags
  
Parámetro de entrada opcional. Este valor está reservado para uso futuro. El valor pasado por este parámetro debe ser 0 (cero).
    
## <a name="return-value"></a>Valor devuelto

Un código de error de la enumeración [ERR](cchksgfiles-err-enumeration.md) . 
  
Es importante recordar que esta función puede devolver **errSuccess** incluso cuando se encuentran errores en los archivos de registro. Por lo tanto, cuando **ErrCheckLogs** devuelve **errSuccess**, la aplicación debe comprobar también el parámetro de devolución de **pfOnlyUnnecessaryLogsCorrupt** . Si **pfOnlyUnnecessaryLogsCorrupts** es **true** cuando **ErrCheckLogs** devuelve **errSuccess**, esto indica que se han encontrado uno o más errores, pero sólo en los archivos de registro que no sea necesarios para actualizar la base de datos.
  
## <a name="remarks"></a>Notas

Para poder llamar a la función **ErrCheckLogs** , se debe llamar a la función **ErrCheckDbHeaders** . 
  
Cuando se están comprobando los archivos de registro de transacciones de base de datos de Exchange, algunos de los archivos de registro será necesario para incorporar las bases de datos en el grupo de almacenamiento a un estado de cierre limpio sin pérdida de datos, mientras que otros archivos de registro que no sean necesarios. La función **ErrCheckLogs** determina el más antiguo y los archivos de registro más recientes que se necesitan para incorporar las bases de datos actualizados. 
  
La función **ErrCheckLogs** comprueba todos los archivos de registro de las rutas de acceso especificadas que también tienen el nombre de archivo de base de tres letras, tal y como se pasan a la función **ErrInit** . 
  
Si no se encontraron errores en los archivos de registro, **ErrCheckLogs** devuelve **errSuccess**. 
  
Si encuentra alguno de los archivos de registro necesarios que está dañado, **ErrCheckLogs** devuelve un error. 
  
Si se encuentran errores sólo en los archivos de registro que son anteriores a los que se necesitan más antigua, la función devuelve **errSuccess** y establece el parámetro de devolución **pfOnlyUnnecessaryLogCorrupt** en **true**. La aplicación debe reconocer que hay errores en algunos de los archivos de registro anterior y, si es así, posiblemente avisará al usuario. En cualquier caso, esos errores no deberían afectar a la integridad de la base de datos general o afecta a si reproducir los registros hacia delante se realizará correctamente.
  
Si se encuentran errores en cualquier archivo de registro creado después de la fecha más temprana registro que determina **ErrCheckLogs** es necesario, la función devuelve un error. Incluso si se encontró el error del archivo de registro en un archivo de registro que se generó más adelante a lo que es necesario para incorporar la base de datos actualizado se devolverá el error. Si bien sería posible incorporar las bases de datos a un estado de cierre limpio mediante el uso de los archivos de registro identificada, no se aplicaría transacciones especificadas en los archivos de registro dañado más adelante, lo que resulta en pérdida de datos cuando se restaura la base de datos. 
  
El objeto **CChkSGFiles** determina si realmente se han comprobado todos los archivos de registro registrados con la función **ErrInit** . Si no todos los registros de no correctamente comprobados, la función **ErrTerm** devuelve un error. 
  
Si está utilizando CHKSGFILES en una aplicación multiproceso, puede llamar a la función **ErrCheckLogs** en la parte de la aplicación multiproceso, pero se le puede llamar sólo una vez para cada objeto **CCheckSGFiles** . 
  
## <a name="requirements"></a>Requisitos

Exchange 2013 sólo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de registro y base de datos que se va a revisar.
  

