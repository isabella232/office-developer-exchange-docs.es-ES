---
title: Función función cchksgfiles. CMaxDbPerSG
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
ms.openlocfilehash: b7c3517779eb07ef053c1dd4fa25544310fb3343
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455264"
---
# <a name="cchksgfilescmaxdbpersg-function"></a>Función función cchksgfiles. CMaxDbPerSG

**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Devuelve el número máximo de bases de datos permitidas en un único grupo de almacenamiento de Exchange Server.
  
```cs
Static ULONG  __stdcall CMaxDbPerSG  ();

```

## <a name="parameters"></a>Parámetros

Ninguno.
  
## <a name="return-value"></a>Valor devuelto

El número máximo de bases de datos que el servidor de Exchange especificado permite por grupo de almacenamiento. Como los grupos de almacenamiento no forman parte de Exchange 2013, esta función devuelve 1.
  
## <a name="remarks"></a>Comentarios

Puede usar el objeto **CCheckSGFiles** para validar las bases de datos (y los archivos de registro de transacciones) en un solo grupo de almacenamiento, por lo que el valor devuelto por la función **CMaxDbPerSG** también representa el número máximo de bases de datos que puede comprobar mediante una instancia de la clase **CCheckSGFiles** . 
  
Tenga en cuenta que, de forma predeterminada, Exchange Server 2003 y Exchange Server 2007 permiten un máximo de cinco bases de datos por grupo de almacenamiento.
  
## <a name="requirements"></a>Requirements

Exchange 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.
  
La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de base de datos y de registro que se van a comprobar.
  

