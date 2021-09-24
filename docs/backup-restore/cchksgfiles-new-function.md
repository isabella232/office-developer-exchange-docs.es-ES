---
title: Función CChkSGFiles.New
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- New
api_type:
- dllExport
ms.assetid: 588d8c74-c9ce-4d5e-8a79-a2a68676e858
description: 'Last modified: February 22, 2013'
ms.openlocfilehash: e50b41e761b8e46d778011b6bac3db4dbb624809
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516275"
---
# <a name="cchksgfilesnew-function"></a>Función CChkSGFiles.New

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Crea una nueva instancia de la **clase CChkSGFiles.** Debe llamar a esta función para poder especificar el grupo de almacenamiento y las bases de datos que se deben comprobar. 
  
```cs
Static CCheckSGFiles  * __stdcall New  ();

```

## <a name="parameters"></a>Parámetros

Ninguno.
  
## <a name="return-value"></a>Valor devuelto

Referencia (puntero) al objeto recién creado.
  
## <a name="remarks"></a>Comentarios

La **función New** crea un objeto **CCheckSGFiles** y devuelve al autor de la llamada una referencia (puntero) a ese objeto. Debe llamar a esta función antes de llamar a cualquiera de las otras funciones de la **clase CCheckSGFiles.** 
  
Si usa CHKSGFILES en una aplicación multiproceso, debe llamar a la función **New** en la parte de subproceso único de la aplicación y puede llamarla solo una vez para cada objeto **CCheckSGFiles.** 
  
## <a name="requirements"></a>Requisitos

Exchange 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a la base de datos y a los archivos de registro que se van a comprobar.
  

