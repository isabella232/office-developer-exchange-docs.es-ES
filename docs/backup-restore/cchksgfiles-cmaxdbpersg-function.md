---
title: CChkSGFiles.CMaxDbPerSG (función)
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CMaxDbPerSG
api_type:
- dllExport
ms.assetid: 5871988b-a5d7-42cc-9b83-8fededb5072f
description: 'Última modificación: 22 de febrero de 2013'
ms.openlocfilehash: bf09074bab6dee13e97e8a59a22ae1b19522a5e5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763940"
---
# <a name="cchksgfilescmaxdbpersg-function"></a>CChkSGFiles.CMaxDbPerSG (función)

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Devuelve el número máximo de bases de datos permitidos en un único grupo de almacenamiento de Exchange server.
  
```cs
Static ULONG  __stdcall CMaxDbPerSG  ();

```

## <a name="parameters"></a>Parámetros

Ninguno.
  
## <a name="return-value"></a>Valor devuelto

El número máximo de bases de datos que permite que el servidor de Exchange especificado por grupo de almacenamiento. Dado que los grupos de almacenamiento no forman parte de Exchange 2013, esta función devuelve 1.
  
## <a name="remarks"></a>Notas

Puede usar el objeto **CCheckSGFiles** para validar las bases de datos (y los archivos de registro de transacciones) en un solo grupo de almacenamiento, por lo que el valor devuelto por la función **CMaxDbPerSG** también representa el número máximo de bases de datos que se pueden proteger mediante un instancia de la clase **CCheckSGFiles** . 
  
Tenga en cuenta que de forma predeterminada, Exchange Server 2003 y Exchange Server 2007 permiten un máximo de cinco bases de datos por grupo de almacenamiento.
  
## <a name="requirements"></a>Requisitos

Exchange 2013 sólo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de registro y base de datos que se va a revisar.
  

