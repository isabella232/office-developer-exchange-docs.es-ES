---
title: Función función cchksgfiles. ErrTerm
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
ms.openlocfilehash: 12b07fba69054d327c7250bbf83e4c77016e8b3f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466202"
---
# <a name="cchksgfileserrterm-function"></a>Función función cchksgfiles. ErrTerm
  
**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Proporciona un estado general de la comprobación de registro y base de datos, que indica si se han comprobado correctamente todas las páginas de base de datos y los registros.
  
> [!IMPORTANT]
> Los grupos de almacenamiento no están disponibles en Exchange 2013. Para la compatibilidad con bases de datos y grupos de almacenamiento en versiones de Exchange anteriores a Exchange Server 2010, la API CHKSGFILES permite especificar grupos de almacenamiento. Cuando ejecuta CHKSGFILES en bases de datos de Exchange 2013, debe establecer los parámetros que especifican un identificador de grupo de almacenamiento en una cadena vacía. 
  
```cs
Vitual ERRErrTerm 
(
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>Parámetros

### <a name="ulflags"></a>ulFlags
  
Parámetro de entrada opcional. Este valor se reserva para uso futuro. El valor que pasa este parámetro debe ser 0 (cero).
    
## <a name="return-value"></a>Valor devuelto

Un código de error de la enumeración [Err](cchksgfiles-err-enumeration.md) . 
  
## <a name="remarks"></a>Comentarios

El objeto **función cchksgfiles** determina si se han comprobado realmente todas las bases de datos registradas con la función **ErrInit** . Este objeto usa la función **ErrCheckDbPages** para comprobar que se ha comprobado realmente el mismo número de páginas de base de datos identificadas por la función **ErrCheckDbHeaders** . Si el número correcto de páginas de cada base de datos no se comprueba correctamente, la función **ErrTerm** devuelve un error. 
  
Si el número de páginas de base de datos que se comprueba con **ErrCheckDbPages** es menor que el indicado por **ErrCheckDbHeaders**, esta función genera un error en el registro de eventos de Windows y **ErrTerm** devuelve un error. 
  
Si el número de páginas de base de datos que se comprueba con **ErrCheckDbPages** es superior al indicado por **ErrCheckDbHeaders**, esta función crea una advertencia en el registro de eventos de Windows para indicar que es posible que la aplicación no Compruebe innecesariamente algunas páginas de base de datos más de una vez. En este caso, sin embargo, la función **ErrTerm** se realiza correctamente. 
  
El objeto **función cchksgfiles** también determina si se han comprobado realmente los archivos de registro registrados con **ErrInit** . Si no todos los registros se comprobó correctamente, la función **ErrTerm** devuelve un error. 
  
Cuando **ErrTerm** devuelve un error, será el primer error que encuentre, aunque comprueba el estado de comprobación de todas las bases de datos registradas con **ErrInit**.
  
Si está usando CHKSGFILES en una aplicación multiproceso, debe llamar a la función **ErrTerm** en la parte de subproceso único de la aplicación y puede llamarla no más de una vez para cada objeto **CCheckSGFiles** . 
  
## <a name="requirements"></a>Requirements

Exchange 2013 solo incluye una versión de 64 bits de CHKSGFILES.
  
La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de base de datos y de registro que se van a comprobar.
  

