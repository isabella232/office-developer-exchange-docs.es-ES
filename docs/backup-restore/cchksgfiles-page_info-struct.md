---
title: Struct función cchksgfiles. PAGE_INFO
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
ms.openlocfilehash: 5ec9f4303b26ea95b125adac6943945ae1276439
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456342"
---
# <a name="cchksgfilespage_info-struct"></a>Struct función cchksgfiles. PAGE_INFO

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Contiene información para una página de base de datos de Exchange. Esta estructura se usa con la función **ErrCheckDbPages** . 
  
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

## <a name="members"></a>Members

### <a name="ulpgno"></a>ulPgNo
  
Unsigned Long. Número de página lógica de la página de base de datos que se va a comprobar. Este valor debe establecerse antes de llamar a **ErrCheckDbPages**. Si la aplicación está leyendo el archivo en función de los desplazamientos de los archivos y, por tanto, debe asignar los desplazamientos de estos archivos a los números de página lógica, el método **PgnoFromFileOffset** le resultará útil para determinar el valor de este campo. **ErrCheckDbPages** no modifica este valor. 
    
### <a name="fpageisinitialized"></a>fPageIsInitialized 
  
Tipo. Un valor de TRUE indica que la página de base de datos contiene datos. Un valor de FALSE indica que la página contiene solo ceros. **ErrCheckDbPages** establece este valor. 
    
### <a name="fcorrectableerror"></a>fCorrectableError
  
Tipo. Un valor de TRUE indica que se detectó un error de coincidencia de suma de comprobación en la página de la base de datos, pero es un error corregible. **ErrCheckDbPages** establece este valor. 
    
### <a name="checksumactual"></a>checksumActual
  
Entero de bit de bit 64 sin signo. Indica el valor de la suma de comprobación que se almacena en la base de datos para esta página lógica. **ErrCheckDbPages** establece este valor. 
    
### <a name="checksumexpected"></a>checksumExpected
  
Entero de bit de bit 64 sin signo. Se trata del valor de suma de comprobación esperado que se calcula para la página de la base de datos; se establece en **ErrCheckDbPages**. Si este valor es distinto del que se almacena en la página de la base de datos (es decir, el valor devuelto en **checksumActual**), **ErrCheckDbPages** indicará que se encontró un error en esta página de base de datos. 
    
### <a name="dbtime"></a>dbTime
  
Entero de bit de bit 64 sin signo. **ErrCheckDbPages** establece este miembro en la marca de hora de la página de la base de datos. 
    
### <a name="checksumpagestructure"></a>checksumPageStructure 
  
Entero de 64-BT sin signo. **ErrCheckDbPages** establece este miembro en el valor de suma de comprobación calculado del contenido de la página, excepto los datos que no son necesarios para determinar la equivalencia de página lógica. Por ejemplo, no es necesario tener en cuenta los valores de datos en un espacio de páginas de base de datos sin usar. Este miembro sólo es válido si los valores **checksumActual** y **checksumExpected** son iguales entre sí. 
    
### <a name="ulflags"></a>ulFlags
  
Entero de bit de bit 64 sin signo. Reservado para uso futuro. El valor de este campo debe establecerse en 0 (cero) antes de llamar a **ErrCheckDbPages**.
    
## <a name="remarks"></a>Comentarios

Cuando se llama a la función **ErrCheckDbPages** , el parámetro **rgPageInfo** es una matriz de las estructuras de ** \_ información de página** . Debe haber una estructura **de \_ información de página** por cada página de base de datos que se va a comprobar. 
  
La aplicación debe establecer el miembro **ulPgno** en el valor correcto y también debe establecer el miembro **ulFlags** en 0 (cero) antes de llamar a **ErrCheckDbPages**. 
  
## <a name="requirements"></a>Requirements

Exchange Server 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de base de datos y de registro que se van a comprobar.
  

