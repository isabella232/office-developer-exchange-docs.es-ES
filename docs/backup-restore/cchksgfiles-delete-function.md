---
title: Función función cchksgfiles. Delete
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Delete
api_type:
- dllExport
ms.assetid: 869e927f-7df2-4247-88ef-b8b05b29a700
description: 'Última modificación: 22 de febrero de 2013'
ms.openlocfilehash: 38cb72b42727855f652de607bb2a02ecdeaae16e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44447053"
---
# <a name="cchksgfilesdelete-function"></a>Función función cchksgfiles. Delete

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Destruye una instancia existente de la clase **función cchksgfiles** . Debe llamar a esta función después de que la aplicación haya terminado de trabajar con el objeto especificado. 
  
```cs
Static VOID __stdcall Delete 
(
        CCheckSGFiles  * pcchecksgfiles
);

```

## <a name="parameters"></a>Parámetros

### <a name="pcchecksgfiles"></a>pcchecksgfiles 
  
Parámetro de entrada. Un puntero a un objeto **CCheckSGFiles** existente. A continuación, se liberará la memoria asociada con el objeto. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

La función **Delete** libera la memoria asociada con el objeto **CCheckSGFiles** . Después de llamar a **Delete**, el puntero que se pasa en el parámetro *pcchecksgfiles* no será válido y no se podrá realizar ninguna otra operación en ese objeto. 
  
Si la aplicación usa la función **ErrCheckDbPages** , la aplicación debe liberar manualmente el búfer de memoria; la función **Delete** no lo liberará. 
  
Si está usando CHKSGFILES en una aplicación multiproceso, debe llamar a la función **Delete** en la parte de subproceso único de la aplicación y puede llamarla solo una vez para cada objeto **CCheckSGFiles** . 
  
## <a name="requirements"></a>Requirements

Exchange 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de base de datos y de registro que se van a comprobar.
  

