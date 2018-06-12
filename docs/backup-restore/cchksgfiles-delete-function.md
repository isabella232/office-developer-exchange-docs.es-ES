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
# <a name="cchksgfilesdelete-function"></a><span data-ttu-id="d7069-103">CChkSGFiles.Delete (función)</span><span class="sxs-lookup"><span data-stu-id="d7069-103">CChkSGFiles.Delete function</span></span>

<span data-ttu-id="d7069-104">**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="d7069-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="d7069-105">Destruye una instancia existente de la clase **CChkSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="d7069-105">Destroys an existing instance of the **CChkSGFiles** class.</span></span> <span data-ttu-id="d7069-106">Debe llamar a esta función después de la aplicación ha terminado de trabajar con el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="d7069-106">You must call this function after the application has finished working with the specified object.</span></span> 
  
```cs
Static VOID __stdcall Delete 
(
        CCheckSGFiles  * pcchecksgfiles
);

```

## <a name="parameters"></a><span data-ttu-id="d7069-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7069-107">Parameters</span></span>

### <a name="pcchecksgfiles"></a><span data-ttu-id="d7069-108">pcchecksgfiles</span><span class="sxs-lookup"><span data-stu-id="d7069-108">pcchecksgfiles</span></span> 
  
<span data-ttu-id="d7069-109">Parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="d7069-109">Input parameter.</span></span> <span data-ttu-id="d7069-110">Un puntero a un objeto **CCheckSGFiles** existente.</span><span class="sxs-lookup"><span data-stu-id="d7069-110">A pointer to an existing **CCheckSGFiles** object.</span></span> <span data-ttu-id="d7069-111">A continuación, se liberará la memoria asociada con el objeto.</span><span class="sxs-lookup"><span data-stu-id="d7069-111">The memory associated with the object will then be freed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d7069-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7069-112">Return value</span></span>

<span data-ttu-id="d7069-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d7069-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d7069-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7069-114">Remarks</span></span>

<span data-ttu-id="d7069-115">La función **Eliminar** libera la memoria asociada con el objeto **CCheckSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="d7069-115">The **Delete** function frees the memory associated with the **CCheckSGFiles** object.</span></span> <span data-ttu-id="d7069-116">Después de llamar a **Eliminar**, el puntero que se pasa en el parámetro *pcchecksgfiles* no será válido y no se puede realizar ninguna otra operación en ese objeto.</span><span class="sxs-lookup"><span data-stu-id="d7069-116">After you call **Delete**, the pointer passed in the  *pcchecksgfiles*  parameter will be invalid and no other operations can be performed on that object.</span></span> 
  
<span data-ttu-id="d7069-117">Si la aplicación usa la función **ErrCheckDbPages** , la aplicación debe liberar el búfer de memoria manualmente; la función **Eliminar** no liberará lo.</span><span class="sxs-lookup"><span data-stu-id="d7069-117">If the application uses the **ErrCheckDbPages** function, the application must free the memory buffer manually; the **Delete** function will not free it.</span></span> 
  
<span data-ttu-id="d7069-118">Si utiliza en una aplicación multiproceso CHKSGFILES, debe llamar a la función **Eliminar** en la parte de un único subproceso de la aplicación y se le puede llamar sólo una vez para cada objeto **CCheckSGFiles** .</span><span class="sxs-lookup"><span data-stu-id="d7069-118">If you're using CHKSGFILES in a multithreaded application, you must call the **Delete** function in the single-threaded portion of the application, and you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="d7069-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7069-119">Requirements</span></span>

<span data-ttu-id="d7069-120">Exchange 2013 sólo incluye una versión de 64 bits de la API CHKSGFILES.</span><span class="sxs-lookup"><span data-stu-id="d7069-120">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="d7069-121">La cuenta que se ejecuta la aplicación debe tener permisos de acceso de lectura a los archivos de registro y base de datos que se va a revisar.</span><span class="sxs-lookup"><span data-stu-id="d7069-121">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

