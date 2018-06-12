---
title: CChkSGFiles.ErrTerm (función)
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrTerm
api_type:
- dllExport
ms.assetid: eea20a55-4a2a-4209-ae79-dc1ee1cd631b
description: 'Última modificación: 25 de febrero de 2013'
ms.openlocfilehash: 099ec33663baa2414a0c28b90364523b6191c697
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19762982"
---
# <a name="cchksgfileserrterm-function"></a>CChkSGFiles.ErrTerm (función)
  
**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Proporciona un estado general de la comprobación de la base de datos y registro, que indica si se ha comprobado correctamente todas las páginas de la base de datos y los registros.
  
> [!IMPORTANT]
> Grupos de almacenamiento no están disponibles en Exchange 2013. Para la compatibilidad con versiones anteriores con las bases de datos y grupos de almacenamiento en versiones de Exchange anteriores a Exchange Server 2010, la API de CHKSGFILES permite especificar grupos de almacenamiento. Cuando ejecuta CHKSGFILES frente a las bases de datos de Exchange 2013, debe establecer los parámetros que especifican un identificador de grupo de almacenamiento de información en una cadena vacía. 
  
```cs
Vitual ERRErrTerm 
(
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>Sintaxis

### <a name="ulflags"></a>ulFlags
  
Parámetro de entrada opcional. Este valor está reservado para uso futuro. El valor pasado por este parámetro debe ser 0 (cero).
    
## <a name="return-value"></a>Valor devuelto

Un código de error de la enumeración [ERR](cchksgfiles-err-enumeration.md) . 
  
## <a name="remarks"></a>Notas

El objeto **CChkSGFiles** determina si todas las bases de datos registrados con la función **ErrInit** realmente se han activado. Este objeto usa la función **ErrCheckDbPages** para comprobar que el mismo número de páginas identificado mediante la función **ErrCheckDbHeaders** se han comprobado realmente de la base de datos. Si el número correcto de las páginas de cada base de datos no se comprueba correctamente, la función **ErrTerm** devuelve un error. 
  
Si el número de páginas de base de datos que se debe comprobado con **ErrCheckDbPages** es menor que el se indican mediante **ErrCheckDbHeaders**, esta función crea un error en el registro de eventos de Windows y **ErrTerm** devuelve un error. 
  
Si el número de páginas de base de datos que se debe comprobado con **ErrCheckDbPages** es mayor que el indicado por **ErrCheckDbHeaders**, esta función crea una advertencia en el registro de eventos de Windows para indicar que la aplicación podría estar innecesariamente comprobando algunas páginas de base de datos más de una vez. En este caso, sin embargo, la función **ErrTerm** se realiza correctamente. 
  
El objeto **CChkSGFiles** también determina si los archivos de registro registrados con **ErrInit** realmente se han activado. Si no se han comprobado correctamente todos los registros, la función **ErrTerm** devuelve un error. 
  
Cuando **ErrTerm** devuelve un error, será el primer error que encuentre, incluso aunque comprueba el estado de comprobación para todas las bases de datos registrados con **ErrInit**.
  
Si utiliza en una aplicación multiproceso CHKSGFILES, debe llamar a la función **ErrTerm** en la parte de un único subproceso de la aplicación y se le no puede llamar más de una vez para cada objeto **CCheckSGFiles** . 
  
## <a name="requirements"></a>Requisitos

Exchange 2013 sólo incluye una versión de 64 bits de CHKSGFILES.
  
La cuenta que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de registro y base de datos que se va a revisar.
  

