---
title: Función CChkSGFiles.Delete
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Delete
api_type:
- dllExport
ms.assetid: 869e927f-7df2-4247-88ef-b8b05b29a700
description: 'Last modified: February 22, 2013'
ms.openlocfilehash: cf1c23dd75442d73dfea49e0831d0859da321a40
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510543"
---
# <a name="cchksgfilesdelete-function"></a>Función CChkSGFiles.Delete

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Destruye una instancia existente de la **clase CChkSGFiles.** Debe llamar a esta función después de que la aplicación haya terminado de trabajar con el objeto especificado. 
  
```cs
Static VOID __stdcall Delete 
(
        CCheckSGFiles  * pcchecksgfiles
);

```

## <a name="parameters"></a>Parámetros

### <a name="pcchecksgfiles"></a>pcchecksgfiles 
  
Parámetro Input. Puntero a un objeto **CCheckSGFiles** existente. A continuación, se liberará la memoria asociada al objeto. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

La **función Delete** libera la memoria asociada al objeto **CCheckSGFiles.** Después de llamar **a Delete**, el puntero pasado en el  *parámetro pcchecksgfiles*  no será válido y no se puede realizar ninguna otra operación en ese objeto. 
  
Si la aplicación usa la **función ErrCheckDbPages,** la aplicación debe liberar el búfer de memoria manualmente; la **función Delete** no la liberará. 
  
Si usa CHKSGFILES en una aplicación multiproceso, debe llamar a la función **Delete** en la parte de subproceso único de la aplicación y puede llamarla solo una vez para cada objeto **CCheckSGFiles.** 
  
## <a name="requirements"></a>Requisitos

Exchange 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a la base de datos y a los archivos de registro que se van a comprobar.
  

