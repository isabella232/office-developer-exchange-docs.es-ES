---
title: Función función cchksgfiles. New
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- New
api_type:
- dllExport
ms.assetid: 588d8c74-c9ce-4d5e-8a79-a2a68676e858
description: 'Última modificación: 22 de febrero de 2013'
ms.openlocfilehash: d18d3ef20890012a1d8c193ec87bdca10a1ed451
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455236"
---
# <a name="cchksgfilesnew-function"></a>Función función cchksgfiles. New

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Crea una nueva instancia de la clase **función cchksgfiles** . Debe llamar a esta función para poder especificar el grupo de almacenamiento y las bases de datos que se van a comprobar. 
  
```cs
Static CCheckSGFiles  * __stdcall New  ();

```

## <a name="parameters"></a>Parámetros

Ninguno.
  
## <a name="return-value"></a>Valor devuelto

Una referencia (puntero) al objeto que se acaba de crear.
  
## <a name="remarks"></a>Comentarios

La **nueva** función crea un objeto **CCheckSGFiles** y devuelve al autor de la llamada una referencia (puntero) a ese objeto. Debe llamar a esta función antes de llamar a cualquiera de las demás funciones de la clase **CCheckSGFiles** . 
  
Si está usando CHKSGFILES en una aplicación multiproceso, debe llamar a la **nueva** función en la parte de subproceso único de la aplicación, y puede llamarla solo una vez para cada objeto **CCheckSGFiles** . 
  
## <a name="requirements"></a>Requirements

Exchange 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de base de datos y de registro que se van a comprobar.
  

