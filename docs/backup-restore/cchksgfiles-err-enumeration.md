---
title: CChkSGFiles.ERR (enumeración)
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 20f10c43e3b92604bb51e1aa5f896a8bd7c4b335
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763923"
---
# <a name="cchksgfileserr-enumeration"></a>CChkSGFiles.ERR (enumeración) 
  
**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Indica el resultado de la función llamada. Esta enumeración es devuelto por muchas funciones de la clase **CCheckSGFiles** . 
  
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
|errSuccess  <br/> |0  <br/> |La función que se completó sin errores.  <br/> |
|errTaskDropped  <br/> |-106  <br/> |Devuelto por la función **ErrTerm** para indicar que no todas las páginas de la base de datos y los archivos de registro de transacciones se protegieron o que se produjeron errores durante la comprobación.  <br/> |
|errRequiredLogFilesMissing  <br/> |-543  <br/> |Uno o varios archivos de registro que se requieren para poner la base de datos a un estado de cierre limpio no se encontró en la ruta de acceso del archivo de registro o no tiene el nombre de base de tres letras especificado.  <br/> |
|errInvalidParameter  <br/> |-1003  <br/> |Uno o más parámetros que se han pasado a la función no son válidos.  <br/> |
|errOutOfMemory  <br/> |-1011  <br/> |Memoria insuficiente estaba disponible para completar la operación solicitada.  <br/> |
|errReadVerifyFailure  <br/> |-1018  <br/> |La suma de comprobación que se almacena en una página de base de datos no coincide con su suma de comprobación esperada.  <br/> |
|errTooManyActiveUsers  <br/> |-1059  <br/> |La función **ErrTerm** se ha llamado mientras estaba utilizando el objeto. Esto puede ocurrir si se llama a **ErrTerm** antes de **ErrCheckDbPages** o **ErrCheckLogFiles** ha devuelto.  <br/> |
   
## <a name="requirements"></a>Requisitos

Exchange Server 2013 sólo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de registro y base de datos que se va a revisar.
  

