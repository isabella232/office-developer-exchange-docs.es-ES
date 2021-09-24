---
title: Estructura CChkSGFiles.PAGE_INFO
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PAGE_INFO
api_type:
- dllExport
ms.assetid: 408335e1-6977-441f-bfad-ede791d1630c
description: 'Last modified: February 22, 2013'
ms.openlocfilehash: f324ec9aca6f94911041c227ce039139292a10aa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516261"
---
# <a name="cchksgfilespage_info-struct"></a>Estructura CChkSGFiles.PAGE_INFO

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Contiene información para una página Exchange base de datos. Esta estructura se usa con la **función ErrCheckDbPages.** 
  
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
  
Long sin signo. Número de página lógica de la página de base de datos que se va a comprobar. Este valor debe establecerse antes de llamar a **ErrCheckDbPages**. Si la aplicación está leyendo el archivo en función de los desplazamientos de archivo y, por lo tanto, debe asignar esos desplazamientos de archivo a números de página lógicos, encontrará el método **PgnoFromFileOffset** útil para determinar el valor de este campo. **ErrCheckDbPages** no modifica este valor. 
    
### <a name="fpageisinitialized"></a>fPageIsInitialized 
  
Boolean. Un valor de TRUE indica que la página de base de datos contiene datos. Un valor de FALSE indica que la página solo contiene ceros. **ErrCheckDbPages** establece este valor. 
    
### <a name="fcorrectableerror"></a>fCorrectableError
  
Boolean. Un valor de TRUE indica que se detectó un error de coincidencia de suma de comprobación en la página de la base de datos, pero que es un error que se puede corregir. **ErrCheckDbPages** establece este valor. 
    
### <a name="checksumactual"></a>checksumActual
  
Entero de 64 bits sin signo. Indica el valor de suma de comprobación almacenado en la base de datos para esta página lógica. **ErrCheckDbPages** establece este valor. 
    
### <a name="checksumexpected"></a>checksumExpected
  
Entero de 64 bits sin signo. Este es el valor de suma de comprobación esperado que se calcula para la página de base de datos; se establece mediante **ErrCheckDbPages**. Si este valor es diferente del almacenado en la página de la base de datos (es decir, el valor devuelto en **checksumActual),** **ErrCheckDbPages** indicará que se encontró un error en esta página de base de datos. 
    
### <a name="dbtime"></a>dbTime
  
Entero de 64 bits sin signo. **ErrCheckDbPages** establece este miembro en la marca de tiempo de la página de base de datos. 
    
### <a name="checksumpagestructure"></a>checksumPageStructure 
  
Entero de 64 bt sin signo. **ErrCheckDbPages** establece este miembro en el valor calculado de suma de comprobación del contenido de la página excluyendo los datos que son innecesarios al determinar la equivalencia lógica de la página. Por ejemplo, no es necesario tener en cuenta los valores de datos en el espacio de páginas de la base de datos sin usar. Este miembro solo es válido si los valores **checksumActual**  y  **checksumExpected**  son iguales entre sí. 
    
### <a name="ulflags"></a>ulFlags
  
Entero de 64 bits sin signo. Reservado para uso futuro. El valor de este campo debe establecerse en 0 (cero) antes de llamar a **ErrCheckDbPages**.
    
## <a name="remarks"></a>Comentarios

Al llamar a **la función ErrCheckDbPages,** el parámetro **rgPageInfo** es una matriz de estructuras **PAGE \_ INFO.** Debe haber una estructura **PAGE \_ INFO** para cada página de base de datos que se va a comprobar. 
  
La aplicación debe establecer el **miembro ulPgno**  en el valor correcto y también debe establecer el miembro  **ulFlags**  en 0 (cero) antes de llamar a **ErrCheckDbPages**. 
  
## <a name="requirements"></a>Requisitos

Exchange Server 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a la base de datos y a los archivos de registro que se van a comprobar.
  

