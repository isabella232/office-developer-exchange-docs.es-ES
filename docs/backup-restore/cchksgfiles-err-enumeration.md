---
title: Enumeración CChkSGFiles.ERR
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ERR
api_type:
- dllExport
ms.assetid: f0efe195-91c3-4f3a-8c7d-e5dba336465a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 12cfff44a6dacbb07ee5518d0008092fbfb644d1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510466"
---
# <a name="cchksgfileserr-enumeration"></a>Enumeración CChkSGFiles.ERR 
  
**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Indica los resultados de la función llamada. Muchas funciones de la **clase CCheckSGFiles** devuelven esta enumeración. 
  
```cs
Enum ERR  
{
        errSuccess = 0,
        errTaskDropped = -106,
        errRequiredLogFilesMissing = -543,
        errInvalidParameter = -1003,
        errOutOfMemory = -1011,
        errReadVerifyFailure = -1018,
        errTooManyActiveUsers = -1059,
        errDatabaseCorrupted = -1206
}

```

## <a name="values"></a>Valores

|**Nombre del miembro**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|errSuccess  <br/> |0  <br/> |La función se completó sin errores.  <br/> |
|errTaskDropped  <br/> |-106  <br/> |Devuelto por la **función ErrTerm** para indicar que no se comprobaron todas las páginas de base de datos y los archivos de registro de transacciones, o que se encontraron errores durante la comprobación.  <br/> |
|errRequiredLogFilesMissing  <br/> |-543  <br/> |Uno o varios archivos de registro que son necesarios para llevar la base de datos a un estado de apagado limpio no se encontró en la ruta de acceso del archivo de registro o no tenía el nombre base de tres letras especificado.  <br/> |
|errInvalidParameter  <br/> |-1003  <br/> |Uno o varios parámetros que se pasaron a la función no eran válidos.  <br/> |
|errOutOfMemory  <br/> |-1011  <br/> |No había suficiente memoria disponible para completar la operación solicitada.  <br/> |
|errReadVerifyFailure  <br/> |-1018  <br/> |La suma de comprobación almacenada en una página de base de datos no coincide con la suma de comprobación esperada.  <br/> |
|errTooManyActiveUsers  <br/> |-1059  <br/> |Se **llamó a la** función ErrTerm mientras se seguía utilizando el objeto. Esto puede ocurrir si **se llama a ErrTerm** antes de que **ErrCheckDbPages** o **ErrCheckLogFiles** haya devuelto.  <br/> |
   
## <a name="requirements"></a>Requisitos

Exchange Server 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a la base de datos y a los archivos de registro que se van a comprobar.
  

