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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19762972"
---
# <a name="cchksgfilesnew-function"></a><span data-ttu-id="af037-103">CChkSGFiles.New (función)</span><span class="sxs-lookup"><span data-stu-id="af037-103">CChkSGFiles.New function</span></span>

<span data-ttu-id="af037-104">**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="af037-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="af037-105">Crea una nueva instancia de la clase **CChkSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="af037-105">Creates a new instance of the **CChkSGFiles** class.</span></span> <span data-ttu-id="af037-106">Debe llamar a esta función antes de que puede especificar el grupo de almacenamiento y bases de datos que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="af037-106">You must call this function before you can specify the storage group and databases to be checked.</span></span> 
  
```cs
Static CCheckSGFiles  * __stdcall New  ();

```

## <a name="parameters"></a><span data-ttu-id="af037-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af037-107">Parameters</span></span>

<span data-ttu-id="af037-108">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="af037-108">None.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="af037-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af037-109">Return value</span></span>

<span data-ttu-id="af037-110">Referencia (puntero) al objeto recién creado.</span><span class="sxs-lookup"><span data-stu-id="af037-110">A reference (pointer) to the newly created object.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="af037-111">Notas</span><span class="sxs-lookup"><span data-stu-id="af037-111">Remarks</span></span>

<span data-ttu-id="af037-112">La función **New** crea un objeto **CCheckSGFiles** y devuelve al llamador una referencia (puntero) a ese objeto.</span><span class="sxs-lookup"><span data-stu-id="af037-112">The **New** function creates a **CCheckSGFiles** object and returns to the caller a reference (pointer) to that object.</span></span> <span data-ttu-id="af037-113">Debe llamar a esta función antes de llamar a cualquiera de las demás funciones en la clase **CCheckSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="af037-113">You must call this function before it calls any of the other functions in the **CCheckSGFiles** class.</span></span> 
  
<span data-ttu-id="af037-114">Si utiliza en una aplicación multiproceso CHKSGFILES, debe llamar a la función de **nuevo** en la parte de un único subproceso de la aplicación y se le puede llamar sólo una vez para cada objeto **CCheckSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="af037-114">If you're using CHKSGFILES in a multithreaded application, you must call the **New** function in the single-threaded portion of the application, and you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="af037-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af037-115">Requirements</span></span>

<span data-ttu-id="af037-116">Exchange 2013 sólo incluye una versión de 64 bits de la API CHKSGFILES.</span><span class="sxs-lookup"><span data-stu-id="af037-116">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="af037-117">La cuenta que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de registro y base de datos que se va a revisar.</span><span class="sxs-lookup"><span data-stu-id="af037-117">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

