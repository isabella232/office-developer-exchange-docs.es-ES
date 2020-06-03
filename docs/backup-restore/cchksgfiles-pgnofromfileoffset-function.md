---
title: Función función cchksgfiles. PgnoFromFileOffset
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PgnoFromFileOffset
api_type:
- dllExport
ms.assetid: 3d69ca6d-5ed1-4038-859e-106e776eeec1
description: 'Última modificación: 22 de febrero de 2013'
ms.openlocfilehash: 3c8f749a03b4aa251bf9312eba5d7e2d46c91fae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452898"
---
# <a name="cchksgfilespgnofromfileoffset-function"></a>Función función cchksgfiles. PgnoFromFileOffset

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Devuelve el número de página de la base de datos lógica que corresponde al índice de bytes especificado en el archivo de base de datos físico. Si el desplazamiento de archivo no es válido o si no se ha llamado a la función **ErrCheckDbHeaders** para las bases de datos, esta función devuelve 0 (cero). 
  
```cs
Vitual ULONGPgnoFromFileOffset  
(
    Const ULONGLONGibFileOffset
);

```

## <a name="parameters"></a>Parámetros

### <a name="ibfileoffset"></a>ibFileOffset
  
Parámetro de entrada. El desplazamiento en un archivo de base de datos, en bytes.
    
## <a name="return-value"></a>Valor devuelto

Número de página lógica del archivo de base de datos que incluye el desplazamiento especificado.
  
## <a name="remarks"></a>Comentarios

Si el parámetro **ibFileOffset** no es válido, la función **PgnoFromFileOffset** devuelve 0 (cero). 
  
**PgnoFromFileOffset** también devuelve 0 (cero) si no ha llamado a la función **ErrCheckDbHeaders** en la instancia de **CCheckSGFiles** . Debe llamar a **ErrCheckDbHeaders** para inicializar el tamaño de página de la base de datos y el número de páginas asignadas a los encabezados de la base de datos. 
  
Debe usar **PgnoFromFileOffset** para rellenar los elementos de la estructura de ** \_ información de página** en preparación para llamar a **ErrCheckDbPages**. El parámetro **rgPageInfo** para **ErrCheckDbPages** requiere que cada elemento de la matriz sea una estructura **PAGE_INFO** , con los valores de los miembros **ulPgno** inicializados correctamente. 
  
Si está usando CHKSGFILES en una aplicación multiproceso, puede llamar a la función **PgnoFromFileOffset** en la parte multiproceso de la aplicación. Tenga en cuenta que normalmente llamaría esta función varias veces para cada base de datos que se está comprobando. 
  
## <a name="requirements"></a>Requirements

Exchange Server 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta con la que se ejecuta la aplicación debe tener permiso de lectura en los archivos de base de datos y de registro que se van a comprobar.
  

