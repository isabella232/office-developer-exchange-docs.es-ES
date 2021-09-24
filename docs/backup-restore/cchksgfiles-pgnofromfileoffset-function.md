---
title: Función CChkSGFiles.PgnoFromFileOffset
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PgnoFromFileOffset
api_type:
- dllExport
ms.assetid: 3d69ca6d-5ed1-4038-859e-106e776eeec1
description: 'Last modified: February 22, 2013'
ms.openlocfilehash: 3e2845cc326520ad875dc8bda52bac3d7c2e2cfa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516247"
---
# <a name="cchksgfilespgnofromfileoffset-function"></a>Función CChkSGFiles.PgnoFromFileOffset

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Devuelve el número de página de base de datos lógica que corresponde al índice de bytes especificado en el archivo de base de datos física. Si el desplazamiento del archivo no es válido o si no se ha llamado a la función **ErrCheckDbHeaders** para las bases de datos, esta función devuelve 0 (cero). 
  
```cs
Vitual ULONGPgnoFromFileOffset  
(
    Const ULONGLONGibFileOffset
);

```

## <a name="parameters"></a>Parámetros

### <a name="ibfileoffset"></a>ibFileOffset
  
Parámetro Input. Desplazamiento en un archivo de base de datos, en bytes.
    
## <a name="return-value"></a>Valor devuelto

Número de página lógica del archivo de base de datos que incluye el desplazamiento especificado.
  
## <a name="remarks"></a>Comentarios

Si el **parámetro ibFileOffset** no es válido, la función **PgnoFromFileOffset** devuelve 0 (cero). 
  
**PgnoFromFileOffset** también devuelve 0 (cero) si no ha llamado a la **función ErrCheckDbHeaders** en la instancia **CCheckSGFiles.** Debe llamar a **ErrCheckDbHeaders para** inicializar el tamaño de página de la base de datos y el número de páginas asignadas a los encabezados de la base de datos. 
  
Debe usar **PgnoFromFileOffset para** rellenar los elementos de la estructura **PAGE \_ INFO** en preparación para llamar a **ErrCheckDbPages**. El **parámetro rgPageInfo** de **ErrCheckDbPages** requiere que cada elemento de la matriz sea una estructura **PAGE_INFO,** con los valores de miembro **ulPgno** inicializados correctamente. 
  
Si usa CHKSGFILES en una aplicación multiproceso, puede llamar a la función **PgnoFromFileOffset** en la parte multiproceso de la aplicación. Tenga en cuenta que normalmente llamaría a esta función varias veces para cada base de datos que se está revisando. 
  
## <a name="requirements"></a>Requisitos

Exchange Server 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta en la que se ejecuta la aplicación debe tener permiso de lectura para la base de datos y los archivos de registro que se van a comprobar.
  

