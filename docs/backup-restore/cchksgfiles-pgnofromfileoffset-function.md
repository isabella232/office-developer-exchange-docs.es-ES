---
title: CChkSGFiles.PgnoFromFileOffset (función)
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
ms.openlocfilehash: d42ba7c8178c6fccdddec0b5da88a972f51184c6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19762985"
---
# <a name="cchksgfilespgnofromfileoffset-function"></a>CChkSGFiles.PgnoFromFileOffset (función)

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Devuelve el número de página de base de datos lógica que corresponde al índice especificado de bytes en el archivo de base de datos físico. Si el desplazamiento de archivo no es válido, o si no se ha llamado a la función **ErrCheckDbHeaders** para las bases de datos, esta función devuelve 0 (cero). 
  
```cs
Vitual ULONGPgnoFromFileOffset  
(
    Const ULONGLONGibFileOffset
);

```

## <a name="parameters"></a>Sintaxis

### <a name="ibfileoffset"></a>ibFileOffset
  
Parámetro de entrada. Especifica el desplazamiento en un archivo de base de datos, en bytes.
    
## <a name="return-value"></a>Valor devuelto

Número de página lógica del archivo de base de datos que incluye el desplazamiento especificado.
  
## <a name="remarks"></a>Comentarios

Si el parámetro **ibFileOffset** no es válido, la función **PgnoFromFileOffset** devuelve 0 (cero). 
  
**PgnoFromFileOffset** también devuelve 0 (cero) si no ha llamado a la función **ErrCheckDbHeaders** en la instancia de **CCheckSGFiles** . Se debe llamar a **ErrCheckDbHeaders** para inicializar el tamaño de página de la base de datos y el número de páginas asignadas a los encabezados de la base de datos. 
  
Debe usar **PgnoFromFileOffset** para rellenar la **página\_INFO** elementos en la preparación para llamar a **ErrCheckDbPages**de estructura. El parámetro **rgPageInfo** para **ErrCheckDbPages** requiere que cada elemento de la matriz sea una estructura **PAGE_INFO** , con los valores de miembro **ulPgno** inicializado correctamente. 
  
Si está utilizando CHKSGFILES en una aplicación multiproceso, puede llamar a la función **PgnoFromFileOffset** en la parte de la aplicación multiproceso. Tenga en cuenta que se haría normalmente llamar a esta función varias veces para cada base de datos está activado. 
  
## <a name="requirements"></a>Requisitos

Exchange Server 2013 sólo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta que se ejecuta la aplicación debe tener permiso para los archivos de registro y base de datos que se va a revisar de lectura.
  

