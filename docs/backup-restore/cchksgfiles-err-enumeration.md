---
title: Enumeración función cchksgfiles. ERR
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ERR
api_type:
- dllExport
ms.assetid: f0efe195-91c3-4f3a-8c7d-e5dba336465a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dbc76601a808f79ce3ed5b5dc9fbe4cf92efb015
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455257"
---
# <a name="cchksgfileserr-enumeration"></a>Enumeración función cchksgfiles. ERR 
  
**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Indica los resultados de la función llamada. Esta enumeración es devuelta por muchas funciones de la clase **CCheckSGFiles** . 
  
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
|errSuccess  <br/> |comprendi  <br/> |La función se completó sin errores.  <br/> |
|errTaskDropped  <br/> |-106  <br/> |Devuelto por la función **ErrTerm** para indicar que no se comprobaron todas las páginas de base de datos y los archivos de registro de transacciones, o que se detectaron errores durante la comprobación.  <br/> |
|errRequiredLogFilesMissing  <br/> |-543  <br/> |No se encontró en la ruta del archivo de registro uno o varios archivos de registro que son necesarios para poner la base de datos en un estado de cierre limpio, o bien no tenían el nombre base de tres letras especificado.  <br/> |
|errInvalidParameter  <br/> |-1003  <br/> |Uno o más parámetros que se pasaron a la función no son válidos.  <br/> |
|errOutOfMemory  <br/> |-1011  <br/> |Memoria insuficiente para completar la operación solicitada.  <br/> |
|errReadVerifyFailure  <br/> |-1018  <br/> |La suma de comprobación que se almacena en una página de base de datos no coincide con la suma de comprobación esperada.  <br/> |
|errTooManyActiveUsers  <br/> |-1059  <br/> |Se llamó a la función **ErrTerm** mientras el objeto se usaba todavía. Esto puede ocurrir si se llama a **ErrTerm** antes de que se devuelva **ErrCheckDbPages** o **ErrCheckLogFiles** .  <br/> |
   
## <a name="requirements"></a>Requirements

Exchange Server 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de base de datos y de registro que se van a comprobar.
  

