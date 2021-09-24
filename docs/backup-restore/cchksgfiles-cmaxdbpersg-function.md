---
title: Función CChkSGFiles.CMaxDbPerSG
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CMaxDbPerSG
api_type:
- dllExport
ms.assetid: 5871988b-a5d7-42cc-9b83-8fededb5072f
description: 'Last modified: February 22, 2013'
ms.openlocfilehash: 1a82e71afde4766734d0875f68d7932a9fd9f26a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510530"
---
# <a name="cchksgfilescmaxdbpersg-function"></a>Función CChkSGFiles.CMaxDbPerSG

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Devuelve el número máximo de bases de datos permitidas en un único Exchange de almacenamiento de servidores.
  
```cs
Static ULONG  __stdcall CMaxDbPerSG  ();

```

## <a name="parameters"></a>Parámetros

Ninguno.
  
## <a name="return-value"></a>Valor devuelto

Número máximo de bases de datos que el servidor Exchange por grupo de almacenamiento. Dado que los grupos de almacenamiento no forman parte Exchange 2013, esta función devuelve 1.
  
## <a name="remarks"></a>Comentarios

Puede usar el objeto **CCheckSGFiles** para validar bases de datos (y archivos de registro de transacciones) en un solo grupo de almacenamiento, por lo que el valor devuelto por la función **CMaxDbPerSG** también representa el número máximo de bases de datos que puede comprobar mediante una instancia de la clase **CCheckSGFiles.** 
  
Tenga en cuenta que, Exchange Server 2003 y Exchange Server 2007 permiten un máximo de cinco bases de datos por grupo de almacenamiento.
  
## <a name="requirements"></a>Requisitos

Exchange 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a la base de datos y a los archivos de registro que se van a comprobar.
  

