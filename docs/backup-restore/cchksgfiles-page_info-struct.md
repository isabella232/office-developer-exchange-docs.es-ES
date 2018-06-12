---
title: Estructura de CChkSGFiles.PAGE_INFO
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PAGE_INFO
api_type:
- dllExport
ms.assetid: 408335e1-6977-441f-bfad-ede791d1630c
description: 'Última modificación: 22 de febrero de 2013'
ms.openlocfilehash: fa66d253b4fc6bd5c29a39c5323f59bf323a906f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763917"
---
# <a name="cchksgfilespageinfo-struct"></a>Estructura de CChkSGFiles.PAGE_INFO

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Contiene la información de una página de base de datos de Exchange. Esta estructura se utiliza con la función **ErrCheckDbPages** . 
  
```cs
Struct PAGE_INFO  
{
        ULONGulPgno;
        BOOLfPageIsInitialized : 1;
        BOOLfCorrectableError : 1;
        ULONGLONGchecksumActual;
        ULONGLONGchecksumExpected;
        ULONGLONGdbTime;
        ULONGLONGchecksumPageStructure;
        ULONGLONGulFlags;
}

```

## <a name="members"></a>Miembros

### <a name="ulpgno"></a>ulPgNo
  
Unsigned Long. Número de página lógica de la página de la base de datos que se va a comprobar. Este valor debe establecerse antes de llamar a **ErrCheckDbPages**. Si la aplicación está leyendo el archivo en función de los desplazamientos de archivo y, por lo tanto, debe asignar los desplazamientos de archivo a los números de página lógica, encontrará el método **PgnoFromFileOffset** útil para determinar el valor para este campo. **ErrCheckDbPages** no modifique este valor. 
    
### <a name="fpageisinitialized"></a>fPageIsInitialized 
  
Valor booleano. Un valor de TRUE indica que la página de la base de datos contiene datos. Un valor de FALSE indica que la página contiene sólo ceros. **ErrCheckDbPages** establece este valor. 
    
### <a name="fcorrectableerror"></a>fCorrectableError
  
Valor booleano. Un valor de TRUE indica que se ha producido un error de coincidencia de suma de comprobación detectado en la página de la base de datos, pero que es un error puede corregir. **ErrCheckDbPages** establece este valor. 
    
### <a name="checksumactual"></a>checksumActual
  
Entero sin signo de 64 bits. Indica el valor de suma de comprobación almacenado en la base de datos para esta página lógica. **ErrCheckDbPages** establece este valor. 
    
### <a name="checksumexpected"></a>checksumExpected
  
Entero sin signo de 64 bits. Éste es el valor de suma de comprobación esperada que se calcula para la página de la base de datos; se establece mediante **ErrCheckDbPages**. Si este valor es diferente de la que se almacenan en la página de la base de datos (es decir, el valor devuelto en **checksumActual**), **ErrCheckDbPages** que le indicará que se ha encontrado un error en esta página de la base de datos. 
    
### <a name="dbtime"></a>dbTime
  
Entero sin signo de 64 bits. **ErrCheckDbPages** establece a este miembro en la marca de tiempo en la página de la base de datos. 
    
### <a name="checksumpagestructure"></a>checksumPageStructure 
  
Entero sin signo de 64-bt. **ErrCheckDbPages** establece a este miembro en el valor calculado de la suma de comprobación del contenido de la página excluidos los datos que no es necesarios cuando la determinación de la equivalencia de página lógica. Por ejemplo, es necesario tener en cuenta los valores de datos en el espacio de página de base de datos no usados. Este miembro sólo es válida si los valores de **checksumActual** y **checksumExpected** son iguales a los otros. 
    
### <a name="ulflags"></a>ulFlags
  
Entero sin signo de 64 bits. Reservado para uso posterior. El valor de este campo debe establecerse en 0 (cero) antes de llamar a **ErrCheckDbPages**.
    
## <a name="remarks"></a>Notas

Cuando se llama a la función **ErrCheckDbPages** , el parámetro **rgPageInfo** es una matriz de **página\_INFO** estructuras. Debe ser uno **página\_INFO** estructura para cada página de la base de datos que se va a comprobar. 
  
La aplicación debe establecer al miembro **ulPgno** en el valor correcto y también debe establecer la del miembro **ulFlags** en 0 (cero) antes de llamar a **ErrCheckDbPages**. 
  
## <a name="requirements"></a>Requisitos

Exchange Server 2013 sólo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de registro y base de datos que se va a revisar.
  

