---
title: CChkSGFiles.Delete (función)
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
ms.openlocfilehash: 5c41007a797e5a256692b2c4bdcb3cfae82c12ab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19762978"
---
# <a name="cchksgfilesdelete-function"></a>CChkSGFiles.Delete (función)

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Destruye una instancia existente de la clase **CChkSGFiles** . Debe llamar a esta función después de la aplicación ha terminado de trabajar con el objeto especificado. 
  
```cs
Static VOID __stdcall Delete 
(
        CCheckSGFiles  * pcchecksgfiles
);

```

## <a name="parameters"></a>Sintaxis

### <a name="pcchecksgfiles"></a>pcchecksgfiles 
  
Parámetro de entrada. Un puntero a un objeto **CCheckSGFiles** existente. A continuación, se liberará la memoria asociada con el objeto. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Observaciones

La función **Eliminar** libera la memoria asociada con el objeto **CCheckSGFiles** . Después de llamar a **Eliminar**, el puntero que se pasa en el parámetro *pcchecksgfiles* no será válido y no se puede realizar ninguna otra operación en ese objeto. 
  
Si la aplicación usa la función **ErrCheckDbPages** , la aplicación debe liberar el búfer de memoria manualmente; la función **Eliminar** no liberará lo. 
  
Si utiliza en una aplicación multiproceso CHKSGFILES, debe llamar a la función **Eliminar** en la parte de un único subproceso de la aplicación y se le puede llamar sólo una vez para cada objeto **CCheckSGFiles** . 
  
## <a name="requirements"></a>Requisitos

Exchange 2013 sólo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de registro y base de datos que se va a revisar.
  

