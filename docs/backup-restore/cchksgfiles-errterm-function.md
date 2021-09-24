---
title: Función CChkSGFiles.ErrTerm
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ErrTerm
api_type:
- dllExport
ms.assetid: eea20a55-4a2a-4209-ae79-dc1ee1cd631b
description: 'Last modified: February 25, 2013'
ms.openlocfilehash: 152fd613ef461d8c1ef69401237cfea09cd32b08
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516289"
---
# <a name="cchksgfileserrterm-function"></a>Función CChkSGFiles.ErrTerm
  
**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Proporciona un estado general de la base de datos y la comprobación del registro, que indica si todas las páginas y registros de la base de datos se comprobaron correctamente.
  
> [!IMPORTANT]
> Storage no están disponibles en Exchange 2013. Para la compatibilidad con versiones anteriores con bases de datos y grupos de almacenamiento en versiones de Exchange anteriores a Exchange Server 2010, la API chksgfiles permite especificar grupos de almacenamiento. Al ejecutar CHKSGFILES en Exchange bases de datos de 2013, debe establecer parámetros que especifiquen un identificador de grupo de almacenamiento en una cadena vacía. 
  
```cs
Vitual ERRErrTerm 
(
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>Parámetros

### <a name="ulflags"></a>ulFlags
  
Parámetro de entrada opcional. Este valor está reservado para uso futuro. El valor pasado por este parámetro debe ser 0 (cero).
    
## <a name="return-value"></a>Valor devuelto

Código de error de la [enumeración ERR.](cchksgfiles-err-enumeration.md) 
  
## <a name="remarks"></a>Comentarios

El **objeto CChkSGFiles** determina si todas las bases de datos registradas con la **función ErrInit** se comprobaron realmente. Este objeto usa la **función ErrCheckDbPages** para comprobar que el mismo número de páginas de base de datos identificadas por la **función ErrCheckDbHeaders** se han comprobado realmente. Si no se comprueba correctamente el número correcto de páginas de cada base de datos, la **función ErrTerm** devuelve un error. 
  
Si el número de páginas de base de datos marcadas con **ErrCheckDbPages** es menor que la indicada por **ErrCheckDbHeaders,** esta función crea un error en el registro de eventos de Windows y **ErrTerm** devuelve un error. 
  
Si el número de páginas de base de datos marcadas con **ErrCheckDbPages** es mayor que la indicada por **ErrCheckDbHeaders,** esta función crea una advertencia en el registro de eventos de Windows para indicar que la aplicación podría comprobar innecesariamente algunas páginas de base de datos más de una vez. Sin embargo, en este caso, la **función ErrTerm** se realiza correctamente. 
  
El **objeto CChkSGFiles** también determina si los archivos de registro registrados con **ErrInit** se comprobaron realmente. Si no todos los registros se comprobaron correctamente, la **función ErrTerm** devuelve un error. 
  
Cuando **ErrTerm** devuelve un error, será el primer error que encuentre, aunque comprueba el estado de comprobación de todas las bases de datos registradas con **ErrInit**.
  
Si usa CHKSGFILES en una aplicación multiproceso, debe llamar a la función **ErrTerm** en la parte de subproceso único de la aplicación y no puede llamarla más de una vez para cada objeto **CCheckSGFiles.** 
  
## <a name="requirements"></a>Requisitos

Exchange 2013 solo incluye una versión de 64 bits de CHKSGFILES.
  
La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a la base de datos y a los archivos de registro que se van a comprobar.
  

