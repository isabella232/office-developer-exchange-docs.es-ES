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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455236"
---
# <a name="cchksgfilesnew-function"></a><span data-ttu-id="f8a5b-103">Función función cchksgfiles. New</span><span class="sxs-lookup"><span data-stu-id="f8a5b-103">CChkSGFiles.New function</span></span>

<span data-ttu-id="f8a5b-104">**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="f8a5b-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="f8a5b-105">Crea una nueva instancia de la clase **función cchksgfiles** .</span><span class="sxs-lookup"><span data-stu-id="f8a5b-105">Creates a new instance of the **CChkSGFiles** class.</span></span> <span data-ttu-id="f8a5b-106">Debe llamar a esta función para poder especificar el grupo de almacenamiento y las bases de datos que se van a comprobar.</span><span class="sxs-lookup"><span data-stu-id="f8a5b-106">You must call this function before you can specify the storage group and databases to be checked.</span></span> 
  
```cs
Static CCheckSGFiles  * __stdcall New  ();

```

## <a name="parameters"></a><span data-ttu-id="f8a5b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8a5b-107">Parameters</span></span>

<span data-ttu-id="f8a5b-108">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f8a5b-108">None.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="f8a5b-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8a5b-109">Return value</span></span>

<span data-ttu-id="f8a5b-110">Una referencia (puntero) al objeto que se acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="f8a5b-110">A reference (pointer) to the newly created object.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f8a5b-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f8a5b-111">Remarks</span></span>

<span data-ttu-id="f8a5b-112">La **nueva** función crea un objeto **CCheckSGFiles** y devuelve al autor de la llamada una referencia (puntero) a ese objeto.</span><span class="sxs-lookup"><span data-stu-id="f8a5b-112">The **New** function creates a **CCheckSGFiles** object and returns to the caller a reference (pointer) to that object.</span></span> <span data-ttu-id="f8a5b-113">Debe llamar a esta función antes de llamar a cualquiera de las demás funciones de la clase **CCheckSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="f8a5b-113">You must call this function before it calls any of the other functions in the **CCheckSGFiles** class.</span></span> 
  
<span data-ttu-id="f8a5b-114">Si está usando CHKSGFILES en una aplicación multiproceso, debe llamar a la **nueva** función en la parte de subproceso único de la aplicación, y puede llamarla solo una vez para cada objeto **CCheckSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="f8a5b-114">If you're using CHKSGFILES in a multithreaded application, you must call the **New** function in the single-threaded portion of the application, and you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="f8a5b-115">Requirements</span><span class="sxs-lookup"><span data-stu-id="f8a5b-115">Requirements</span></span>

<span data-ttu-id="f8a5b-116">Exchange 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.</span><span class="sxs-lookup"><span data-stu-id="f8a5b-116">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="f8a5b-117">La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de base de datos y de registro que se van a comprobar.</span><span class="sxs-lookup"><span data-stu-id="f8a5b-117">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

