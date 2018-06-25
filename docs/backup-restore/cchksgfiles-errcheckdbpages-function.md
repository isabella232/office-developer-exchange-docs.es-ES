---
title: CChkSGFiles.ErrCheckDbPages (función)
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrCheckDbPages
api_type:
- dllExport
ms.assetid: 5e981a7c-28cd-470c-b7eb-606463e9dd05
description: 'Última modificación: 22 de febrero de 2013'
ms.openlocfilehash: f1588b1dbc4bd7e83683fa4432a175405ad17903
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19762977"
---
# <a name="cchksgfileserrcheckdbpages-function"></a><span data-ttu-id="c8022-103">CChkSGFiles.ErrCheckDbPages (función)</span><span class="sxs-lookup"><span data-stu-id="c8022-103">CChkSGFiles.ErrCheckDbPages function</span></span>

<span data-ttu-id="c8022-104">**Se aplica a:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="c8022-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="c8022-105">Valida un intervalo de páginas en una base de datos especificado.</span><span class="sxs-lookup"><span data-stu-id="c8022-105">Validates a range of pages in a specified database.</span></span> 
  
```cs
Vitual ERRErrCheckDbPages  
(
    Const ULONGiDb,
    Const VOID  * const pvPageBuffer,
    Const ULONGcbPageBuffer,
    PAGE_INFOrgPageInfo[],
    Const ULONGcPageInfo,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a><span data-ttu-id="c8022-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8022-106">Parameters</span></span>

### <a name="idb"></a><span data-ttu-id="c8022-107">iDb</span><span class="sxs-lookup"><span data-stu-id="c8022-107">iDb</span></span>
  
<span data-ttu-id="c8022-108">Parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="c8022-108">Input parameter.</span></span> <span data-ttu-id="c8022-109">Un índice en la matriz de las bases de datos especificado en el parámetro **[] rgwszDb** a la función **ErrInit** .</span><span class="sxs-lookup"><span data-stu-id="c8022-109">An index into the array of databases specified in the **rgwszDb[]** parameter to the **ErrInit** function.</span></span> <span data-ttu-id="c8022-110">Se comprobará la base de datos indizada por este parámetro.</span><span class="sxs-lookup"><span data-stu-id="c8022-110">The database indexed by this parameter will be checked.</span></span> 
    
### <a name="pvpagebuffer"></a><span data-ttu-id="c8022-111">pvPageBuffer</span><span class="sxs-lookup"><span data-stu-id="c8022-111">pvPageBuffer</span></span> 
  
<span data-ttu-id="c8022-112">Parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="c8022-112">Input parameter.</span></span> <span data-ttu-id="c8022-113">Un puntero a un búfer que contiene una o más páginas de base de datos que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="c8022-113">A pointer to a buffer containing one or more database pages to be checked.</span></span> <span data-ttu-id="c8022-114">El tamaño del búfer debe ser un múltiplo del tamaño de página de base de datos, tal como lo devuelve en el parámetro **pcbDbPageSize** por la función **ErrCheckDbHeaders** .</span><span class="sxs-lookup"><span data-stu-id="c8022-114">The size of the buffer must be a multiple of the database page size, as returned in the **pcbDbPageSize** parameter by the **ErrCheckDbHeaders** function.</span></span> <span data-ttu-id="c8022-115">La aplicación de llamada debe llene el búfer con el contenido de página de la base de datos antes de llamar a **ErrCheckDbPages**.</span><span class="sxs-lookup"><span data-stu-id="c8022-115">The calling application must fill the buffer with the database page contents before calling **ErrCheckDbPages**.</span></span>
    
### <a name="cbpagebuffer"></a><span data-ttu-id="c8022-116">cbPageBuffer</span><span class="sxs-lookup"><span data-stu-id="c8022-116">cbPageBuffer</span></span>
  
<span data-ttu-id="c8022-117">Parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="c8022-117">Input parameter.</span></span> <span data-ttu-id="c8022-118">El tamaño del parámetro **pvPageBuffer** , en bytes.</span><span class="sxs-lookup"><span data-stu-id="c8022-118">The size of the **pvPageBuffer** parameter, in bytes.</span></span> <span data-ttu-id="c8022-119">Este valor debe ser un múltiplo del tamaño de página de base de datos, tal como lo devuelve en el parámetro **pcbDbPageSize** por la función **ErrCheckDbHeaders** .</span><span class="sxs-lookup"><span data-stu-id="c8022-119">This value must be a multiple of the database page size, as returned in the **pcbDbPageSize** parameter by the **ErrCheckDbHeaders** function.</span></span> 
    
### <a name="rgpageinfo"></a><span data-ttu-id="c8022-120">[] rgPageInfo</span><span class="sxs-lookup"><span data-stu-id="c8022-120">rgPageInfo[]</span></span> 
  
<span data-ttu-id="c8022-121">Parámetro de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="c8022-121">Input/output parameter.</span></span> <span data-ttu-id="c8022-122">Una matriz de **página\_INFO** detallan de estructuras que **ErrCheckDbPages** se rellena con los resultados de cada página de la base de datos que está protegido.</span><span class="sxs-lookup"><span data-stu-id="c8022-122">An array of **PAGE\_INFO** structures that **ErrCheckDbPages** fills with detailed results of each database page that is checked.</span></span> <span data-ttu-id="c8022-123">La matriz debe tener un elemento para cada página de base de datos que se pasa en el parámetro **pvPageBuffer** y el campo **ulPgno** de cada **página\_INFO** estructura debe establecerse en el número de página lógica que corresponde a la página de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="c8022-123">The array must have one element for each database page passed in the **pvPageBuffer** parameter, and the **ulPgno** field in each **PAGE\_INFO** structure must be set to the logical page number that corresponds to the database page.</span></span> <span data-ttu-id="c8022-124">Para obtener más información, vea "Comentarios" más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="c8022-124">For more information, see "Remarks" later in this topic.</span></span> 
    
### <a name="cpageinfo"></a><span data-ttu-id="c8022-125">cPageInfo</span><span class="sxs-lookup"><span data-stu-id="c8022-125">cPageInfo</span></span>
  
<span data-ttu-id="c8022-126">Parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="c8022-126">Input parameter.</span></span> <span data-ttu-id="c8022-127">El número de entradas en la matriz **[] rgPageInfo** .</span><span class="sxs-lookup"><span data-stu-id="c8022-127">The number of entries in the **rgPageInfo[]** array.</span></span> <span data-ttu-id="c8022-128">Este valor debe ser igual que el número de páginas de base de datos que se pasa en el parámetro **pvPageBuffer** .</span><span class="sxs-lookup"><span data-stu-id="c8022-128">This value must be equal to the number of database pages passed in the **pvPageBuffer** parameter.</span></span> 
    
### <a name="ulflags"></a><span data-ttu-id="c8022-129">ulFlags</span><span class="sxs-lookup"><span data-stu-id="c8022-129">ulFlags</span></span> 
  
<span data-ttu-id="c8022-130">Parámetro de entrada opcional.</span><span class="sxs-lookup"><span data-stu-id="c8022-130">Optional input parameter.</span></span> <span data-ttu-id="c8022-131">Este valor está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="c8022-131">This value is reserved for future use.</span></span> <span data-ttu-id="c8022-132">El valor que se pasa en este parámetro debe ser 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="c8022-132">The value passed in this parameter should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c8022-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8022-133">Return value</span></span>

<span data-ttu-id="c8022-134">Un código de error de la enumeración [ERR](cchksgfiles-err-enumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="c8022-134">An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c8022-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c8022-135">Remarks</span></span>

<span data-ttu-id="c8022-136">Tenga en cuenta que tiene que ha especificado la base de datos en la matriz de las bases de datos que se pasan a la función **ErrInit** .</span><span class="sxs-lookup"><span data-stu-id="c8022-136">Note that you need to have specified the database in the array of databases passed to the **ErrInit** function.</span></span> <span data-ttu-id="c8022-137">Además, se debe llamar a **ErrCheckDbHeaders** antes de **ErrCheckDbPages**.</span><span class="sxs-lookup"><span data-stu-id="c8022-137">Also, **ErrCheckDbHeaders** must be called before **ErrCheckDbPages**.</span></span>
  
<span data-ttu-id="c8022-138">La aplicación de llamada debe asignar un búfer de memoria que es lo suficientemente grande como para contener las páginas de la base de datos que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="c8022-138">The calling application must allocate a memory buffer that is large enough to hold the database pages to be checked.</span></span> <span data-ttu-id="c8022-139">La aplicación es responsable de rellenar el búfer con el contenido de una o varias de estas páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="c8022-139">The application is responsible for filling the buffer with the contents of one or more such database pages.</span></span> 
  
<span data-ttu-id="c8022-140">La aplicación de llamada debe llamar a **ErrCheckDbHeaders** antes de llamar a **ErrCheckDbPages**.</span><span class="sxs-lookup"><span data-stu-id="c8022-140">The calling application must call **ErrCheckDbHeaders** before calling **ErrCheckDbPages**.</span></span> <span data-ttu-id="c8022-141">Esta función se puede llamar tantas veces como sea necesario para cubrir todas las páginas de todos los archivos de base de datos que se va a revisar.</span><span class="sxs-lookup"><span data-stu-id="c8022-141">This function can be called as many times as necessary to cover all the pages in all database files that are to be checked.</span></span>
  
<span data-ttu-id="c8022-142">En el parámetro **[] rgPageInfo** , cada elemento devuelto contiene información acerca de la página de la base de datos en un **página\_INFO** estructura.</span><span class="sxs-lookup"><span data-stu-id="c8022-142">In the **rgPageInfo[]** parameter, each element returned contains information about the database page in a **PAGE\_INFO** structure.</span></span> <span data-ttu-id="c8022-143">Si la función **ErrCheckDbPages** devuelve un error, la aplicación debe comprobar cada uno de ellos **página\_INFO** estructura para determinar en qué página se ha encontrado el error.</span><span class="sxs-lookup"><span data-stu-id="c8022-143">If the **ErrCheckDbPages** function returns an error, the application should check each **PAGE\_INFO** structure to determine on which page the error was found.</span></span> <span data-ttu-id="c8022-144">Por ejemplo, comparación de los valores **checksumActual** y **checksumExpected** indicará si se detectó un error de suma de comprobación en esa página de base de datos.</span><span class="sxs-lookup"><span data-stu-id="c8022-144">For example, comparing the **checksumActual** and **checksumExpected** values will indicate whether a checksum error was detected on that database page.</span></span> 
  
<span data-ttu-id="c8022-145">Si **ErrCheckDbPages** detecta los errores en el contenido de la base de datos, creará una entrada de registro de eventos de Error de Windows.</span><span class="sxs-lookup"><span data-stu-id="c8022-145">If **ErrCheckDbPages** detects any errors in the database content, it will create a Windows Error event log entry.</span></span> 
  
<span data-ttu-id="c8022-146">El objeto **CChkSGFiles** determina si todas las bases de datos registrados con la función **ErrInit** realmente se han activado.</span><span class="sxs-lookup"><span data-stu-id="c8022-146">The **CChkSGFiles** object determines whether all the databases registered with the **ErrInit** function were actually checked.</span></span> <span data-ttu-id="c8022-147">Específicamente, **CChkSGFiles** usa la función **ErrCheckDbPages** para determinar si realmente se ha comprobado el mismo número de páginas de base de datos indicada por **ErrCheckDbHeaders** .</span><span class="sxs-lookup"><span data-stu-id="c8022-147">Specifically, **CChkSGFiles** uses the **ErrCheckDbPages** function to determine whether the same number of database pages indicated by **ErrCheckDbHeaders** were actually verified.</span></span> <span data-ttu-id="c8022-148">Si el número correcto de las páginas de cada base de datos no se protegieron correctamente, la función **ErrTerm** devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="c8022-148">If the correct number of pages in each database were not successfully checked, the **ErrTerm** function returns an error.</span></span> 
  
<span data-ttu-id="c8022-149">Si está utilizando CHKSGFILES en una aplicación multiproceso, puede llamar a la función **ErrCheckDbPages** en la parte de la aplicación multiproceso.</span><span class="sxs-lookup"><span data-stu-id="c8022-149">If you're using CHKSGFILES in a multithreaded application, you can call the **ErrCheckDbPages** function in the multithreaded portion of the application.</span></span> <span data-ttu-id="c8022-150">Tenga en cuenta que **ErrCheckDbPages** normalmente se llama varias veces para cada base de datos que está protegido.</span><span class="sxs-lookup"><span data-stu-id="c8022-150">Note that **ErrCheckDbPages** is typically called multiple times for each database that is checked.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="c8022-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8022-151">Requirements</span></span>

<span data-ttu-id="c8022-152">Exchange 2013 sólo incluye una versión de 64 bits de la API CHKSGFILES.</span><span class="sxs-lookup"><span data-stu-id="c8022-152">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="c8022-153">La cuenta que se ejecuta la aplicación debe tener permisos para los archivos de registro y base de datos que se va a revisar de lectura.</span><span class="sxs-lookup"><span data-stu-id="c8022-153">The account that the application is running under must have read permissions to the database and log files that are to be checked.</span></span>
  

