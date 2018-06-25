---
title: CChkSGFiles.New (función)
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
ms.openlocfilehash: b40f8b1a95477715b29defb4addabfb333e92d04
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19762972"
---
# <a name="cchksgfilesnew-function"></a>CChkSGFiles.New (función)

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Crea una nueva instancia de la clase **CChkSGFiles** . Debe llamar a esta función antes de que puede especificar el grupo de almacenamiento y bases de datos que se va a comprobar. 
  
```cs
Static CCheckSGFiles  * __stdcall New  ();

```

## <a name="parameters"></a>Parámetros

Ninguno.
  
## <a name="return-value"></a>Valor devuelto

Referencia (puntero) al objeto recién creado.
  
## <a name="remarks"></a>Comentarios

La función **New** crea un objeto **CCheckSGFiles** y devuelve al llamador una referencia (puntero) a ese objeto. Debe llamar a esta función antes de llamar a cualquiera de las demás funciones en la clase **CCheckSGFiles** . 
  
Si utiliza en una aplicación multiproceso CHKSGFILES, debe llamar a la función de **nuevo** en la parte de un único subproceso de la aplicación y se le puede llamar sólo una vez para cada objeto **CCheckSGFiles** . 
  
## <a name="requirements"></a>Requisitos

Exchange 2013 sólo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de registro y base de datos que se va a revisar.
  

