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
# <a name="cchksgfilesdelete-function"></a><span data-ttu-id="6912d-103">Función función cchksgfiles. Delete</span><span class="sxs-lookup"><span data-stu-id="6912d-103">CChkSGFiles.Delete function</span></span>

<span data-ttu-id="6912d-104">**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="6912d-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="6912d-105">Destruye una instancia existente de la clase **función cchksgfiles** .</span><span class="sxs-lookup"><span data-stu-id="6912d-105">Destroys an existing instance of the **CChkSGFiles** class.</span></span> <span data-ttu-id="6912d-106">Debe llamar a esta función después de que la aplicación haya terminado de trabajar con el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="6912d-106">You must call this function after the application has finished working with the specified object.</span></span> 
  
```cs
Static VOID __stdcall Delete 
(
        CCheckSGFiles  * pcchecksgfiles
);

```

## <a name="parameters"></a><span data-ttu-id="6912d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6912d-107">Parameters</span></span>

### <a name="pcchecksgfiles"></a><span data-ttu-id="6912d-108">pcchecksgfiles</span><span class="sxs-lookup"><span data-stu-id="6912d-108">pcchecksgfiles</span></span> 
  
<span data-ttu-id="6912d-109">Parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="6912d-109">Input parameter.</span></span> <span data-ttu-id="6912d-110">Un puntero a un objeto **CCheckSGFiles** existente.</span><span class="sxs-lookup"><span data-stu-id="6912d-110">A pointer to an existing **CCheckSGFiles** object.</span></span> <span data-ttu-id="6912d-111">A continuación, se liberará la memoria asociada con el objeto.</span><span class="sxs-lookup"><span data-stu-id="6912d-111">The memory associated with the object will then be freed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6912d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6912d-112">Return value</span></span>

<span data-ttu-id="6912d-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6912d-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6912d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6912d-114">Remarks</span></span>

<span data-ttu-id="6912d-115">La función **Delete** libera la memoria asociada con el objeto **CCheckSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="6912d-115">The **Delete** function frees the memory associated with the **CCheckSGFiles** object.</span></span> <span data-ttu-id="6912d-116">Después de llamar a **Delete**, el puntero que se pasa en el parámetro *pcchecksgfiles* no será válido y no se podrá realizar ninguna otra operación en ese objeto.</span><span class="sxs-lookup"><span data-stu-id="6912d-116">After you call **Delete**, the pointer passed in the  *pcchecksgfiles*  parameter will be invalid and no other operations can be performed on that object.</span></span> 
  
<span data-ttu-id="6912d-117">Si la aplicación usa la función **ErrCheckDbPages** , la aplicación debe liberar manualmente el búfer de memoria; la función **Delete** no lo liberará.</span><span class="sxs-lookup"><span data-stu-id="6912d-117">If the application uses the **ErrCheckDbPages** function, the application must free the memory buffer manually; the **Delete** function will not free it.</span></span> 
  
<span data-ttu-id="6912d-118">Si está usando CHKSGFILES en una aplicación multiproceso, debe llamar a la función **Delete** en la parte de subproceso único de la aplicación y puede llamarla solo una vez para cada objeto **CCheckSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="6912d-118">If you're using CHKSGFILES in a multithreaded application, you must call the **Delete** function in the single-threaded portion of the application, and you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="6912d-119">Requirements</span><span class="sxs-lookup"><span data-stu-id="6912d-119">Requirements</span></span>

<span data-ttu-id="6912d-120">Exchange 2013 solo incluye una versión de 64 bits de la API CHKSGFILES.</span><span class="sxs-lookup"><span data-stu-id="6912d-120">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="6912d-121">La cuenta en la que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de base de datos y de registro que se van a comprobar.</span><span class="sxs-lookup"><span data-stu-id="6912d-121">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

